---
title: "Triển khai hệ thống lên AWS"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 5.10. </b> "
---

### 1. Tổng quan kiến trúc triển khai thực tế trên AWS
Để chạy thử nghiệm và vận hành hệ thống **TrustBite** một cách bảo mật, sẵn sàng cao (High Availability) và có khả năng mở rộng, chúng ta thiết kế mô hình kiến trúc hạ tầng sử dụng các dịch vụ đám mây AWS.

Luồng tổng thể hạ tầng triển khai thực tế:
```text
Người dùng ──> CloudFront ──> Application Load Balancer (ALB)
                                     │
                   ┌─────────────────┴─────────────────┐
                   ▼                                   ▼
       ECS Fargate (API Service)           ECS Fargate (OCR Worker)
                   │                                   │
     ┌─────────────┼─────────────┬─────────────┐       │
     ▼             ▼             ▼             ▼       ▼
Cognito IDP   RDS Postgres  Redis (Queue)   S3 (Receipts) + Textract
```

---

### 2. Bước 1: Khởi tạo Cơ sở dữ liệu trên Amazon RDS
Dự án sử dụng cơ sở dữ liệu quan hệ PostgreSQL. Trong môi trường thực tế, chúng ta tự động hóa sao lưu và mở rộng thông qua **Amazon RDS PostgreSQL**:

1.  Tại giao diện AWS Console, tìm kiếm dịch vụ **RDS** và nhấn nút **Create database**.
2.  **Engine options**: Chọn **PostgreSQL** (chọn phiên bản v15 hoặc v16 phù hợp với môi trường phát triển).
3.  **Templates**: Chọn **Dev/Test** (hoặc **Free Tier** để thử nghiệm tiết kiệm).
4.  **Settings**:
    *   **DB instance identifier**: Nhập **trustbite-db-prod**.
    *   **Master username**: Nhập **trustbite_admin**.
    *   **Master password**: Thiết lập mật khẩu bảo mật cao.
5.  **Connectivity**:
    *   Chọn đúng mạng **VPC** của hệ thống.
    *   **Public access**: Chọn **No** (chỉ cho phép truy cập nội bộ từ cụm container ECS Fargate, không mở cổng ra Internet).
    *   Cấu hình Security Group cho phép cổng **5432** chỉ nhận kết nối từ Security Group của cụm Backend API ECS Service.
6.  Nhấn nút **Create database**.

> [!IMPORTANT]
> **Hướng dẫn chụp ảnh minh chứng:**
> * **Ảnh chụp màn hình 12:** Danh sách cơ sở dữ liệu trong trang quản trị AWS RDS hiển thị database **trustbite-db-prod** hoạt động ở trạng thái **Available** màu xanh.

---

### 3. Bước 2: Tạo phân vùng lưu trữ ảnh hóa đơn trên Amazon S3
Toàn bộ ảnh hóa đơn do người dùng tải lên sẽ được lưu trữ riêng tư trên dịch vụ lưu trữ đối tượng **Amazon S3**:

1.  Truy cập trang quản trị **Amazon S3** và nhấn nút **Create bucket**.
2.  **Bucket name**: Đặt tên duy nhất, ví dụ: **trustbite-invoices-production**.
3.  **AWS Region**: Chọn **ap-southeast-1** (Singapore).
4.  **Object Ownership**: Chọn **ACLs disabled (recommended)**.
5.  **Block Public Access settings for this bucket**: Tích chọn **Block all public access** để bảo vệ hoàn toàn quyền riêng tư của ảnh hóa đơn người dùng, không cho phép truy cập công khai.
6.  Nhấn **Create bucket**.
7.  Cấu hình **CORS** trong tab **Permissions** của bucket để cho phép ứng dụng upload trực tiếp:
    ```json
    [
      {
        "AllowedHeaders": ["*"],
        "AllowedMethods": ["PUT", "POST"],
        "AllowedOrigins": ["https://trustbite.example.com"],
        "ExposeHeaders": []
      }
    ]
    ```

> [!IMPORTANT]
> **Hướng dẫn chụp ảnh minh chứng:**
> * **Ảnh chụp màn hình 13:** AWS S3 Console hiển thị bucket **trustbite-invoices-production** đã được tạo thành công với cấu hình **Bucket status: Bucket and objects not public**.

---

### 4. Bước 3: Đóng gói và đẩy Container Image lên Amazon ECR
Ứng dụng Express backend được đóng gói dưới dạng Docker image. Chúng ta lưu trữ Docker image trên dịch vụ **Amazon Elastic Container Registry (ECR)** trước khi triển khai lên máy chủ container:

1.  Trong **Amazon ECR**, nhấn **Create repository**.
2.  **Repository name**: Nhập **trustbite-api-prod**.
3.  Chạy các lệnh Docker tại local để đóng gói và đẩy image lên đám mây:
    ```bash
    # 1. Đăng nhập AWS CLI vào ECR registry
    aws ecr get-login-password --region ap-southeast-1 | docker login --username AWS --password-stdin <aws_account_id>.dkr.ecr.ap-southeast-1.amazonaws.com

    # 2. Build Docker image từ thư mục /server
    docker build -t trustbite-api-prod ./server

    # 3. Gắn tag image tương thích với địa chỉ ECR repository
    docker tag trustbite-api-prod:latest <aws_account_id>.dkr.ecr.ap-southeast-1.amazonaws.com/trustbite-api-prod:latest

    # 4. Đẩy image lên kho lưu trữ AWS ECR
    docker push <aws_account_id>.dkr.ecr.ap-southeast-1.amazonaws.com/trustbite-api-prod:latest
    ```

> [!IMPORTANT]
> **Hướng dẫn chụp ảnh minh chứng:**
> * **Ảnh chụp màn hình 14:** Giao diện AWS ECR Repositories hiển thị kho lưu trữ **trustbite-api-prod** đã nhận được image tải lên thành công với tag **latest**.

---

### 5. Bước 4: Chạy Dịch vụ máy chủ container trên Amazon ECS Fargate
Chúng ta sử dụng cụm máy chủ serverless container **Amazon ECS Fargate** để chạy backend API ổn định, tự động scale mà không cần quản trị hạ tầng máy chủ ảo EC2:

1.  **Tạo ECS Cluster**: Tại trang **Amazon ECS**, nhấn **Create cluster**, đặt tên cụm là **trustbite-cluster** và nhấn tạo.
2.  **Tạo Task Definition (Định nghĩa tác vụ)**:
    *   Chọn kiểu khởi chạy **Fargate**.
    *   Cấu hình thông số CPU: **0.5 vCPU**, RAM: **1 GB**.
    *   Thêm container: Đặt tên **api-container**, trỏ liên kết ảnh Image tới địa chỉ URI của ECR repository đã đẩy lên ở Bước 3.
    *   Khai báo các biến môi trường cấu hình production:
        *   **DATABASE_HOST** = địa chỉ endpoint của RDS database đã tạo ở Bước 1.
        *   **DATABASE_NAME** = **trustbite_db**.
        *   **AWS_COGNITO_USER_POOL_ID** = mã ID của Cognito User Pool thực tế.
        *   **AWS_COGNITO_CLIENT_ID** = mã ID của Cognito App Client thực tế.
        *   **AWS_S3_BUCKET_NAME** = **trustbite-invoices-production**.
3.  **Khởi tạo ECS Service**:
    *   Bên trong cụm **trustbite-cluster**, tạo mới một Service với kiểu Fargate.
    *   Chọn Task Definition vừa định nghĩa.
    *   **Number of tasks**: Đặt số lượng là **2** (chạy song song 2 container chạy luân phiên để tránh downtime).
    *   **Load balancing**: Gắn kèm một **Application Load Balancer (ALB)** để điều phối lưu lượng mạng cổng 80/443 ngoài Internet đi vào các container.
    *   Nhấn nút tạo Service.

> [!IMPORTANT]
> **Hướng dẫn chụp ảnh minh chứng:**
> * **Ảnh chụp màn hình 15:** Trang quản trị dịch vụ AWS ECS Services hiển thị trạng thái service **trustbite-api-service** ở trạng thái **Active** và chỉ số chạy Fargate task hiển thị **2 / 2 running**.

---

### 6. Bước 5: Kiểm thử khói (Smoke Test) và kiểm tra hoạt động
Sau khi dịch vụ Application Load Balancer cấp địa chỉ DNS công khai, chúng ta tiến hành kiểm tra nhanh kết nối sức khỏe (Health Check) để xác minh backend API đã kết nối thông suốt tới RDS và các tài nguyên bảo mật AWS:

Gửi lệnh kiểm tra API:
```bash
curl -i http://trustbite-alb-prod-123456789.ap-southeast-1.elb.amazonaws.com/health
```

Kết quả phản hồi mong đợi (HTTP **200 OK**):
```json
{
  "status": "OK",
  "database": "connected",
  "aws": "verified"
}
```

> [!IMPORTANT]
> **Hướng dẫn chụp ảnh minh chứng:**
> * **Ảnh chụp màn hình 16:** Kết quả gửi API bằng Postman tới URL của Application Load Balancer (ALB) nhận về mã trạng thái **200 OK** cùng dữ liệu JSON thông báo hệ thống hoạt động ổn định.
