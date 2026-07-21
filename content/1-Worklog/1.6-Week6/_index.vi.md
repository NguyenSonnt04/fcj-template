---
title: "Worklog Tuần 6"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6

- Đóng gói và quản lý ứng dụng container bằng Docker.
- Triển khai container trên Lightsail Containers, EKS và AWS Fargate.
- Tự động hóa triển khai, giám sát và bảo mật môi trường container.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **Docker và quản lý image**<br>- Viết Dockerfile, xây dựng Docker image và chạy thử ứng dụng bằng container.<br>- Tìm hiểu layer, tag, registry và các phương pháp tối ưu kích thước image.<br>- Kiểm tra log, biến môi trường, network và volume của container. | 01/06/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/5-container/> |
| 3 | **Amazon Lightsail Containers và EKS**<br>- Triển khai ứng dụng mẫu trên Amazon Lightsail Containers và kiểm tra endpoint dịch vụ.<br>- Tìm hiểu kiến trúc Kubernetes và các thành phần chính của Amazon EKS.<br>- Cấu hình workload, tài nguyên và kiểm tra trạng thái pod/service trên môi trường thử nghiệm. | 02/06/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/5-container/> |
| 4 | **Microservices trên AWS Fargate**<br>- Phân tách ứng dụng Monolithic thành các service container độc lập.<br>- Tạo task definition và triển khai các service bằng AWS Fargate.<br>- Kiểm tra giao tiếp giữa các service và đánh giá khả năng mở rộng của hệ thống. | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/5-container/> |
| 5 | **CI/CD cho ứng dụng container**<br>- Kết nối GitHub với AWS CodePipeline để nhận thay đổi mã nguồn.<br>- Cấu hình quy trình build, kiểm thử và tạo Docker image tự động.<br>- Thực hiện triển khai image mới và kiểm tra kết quả sau mỗi lần cập nhật. | 04/06/2026 | 04/06/2026 | <https://cloudjourney.awsstudygroup.com/5-container/> |
| 6 | **Giám sát và bảo mật container**<br>- Theo dõi log, metric và mức sử dụng tài nguyên của ứng dụng container.<br>- Rà soát IAM role, security group, secret và quyền truy cập registry.<br>- Kiểm tra khả năng phục hồi, ổn định và các phương án mở rộng workload. | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/5-container/> |

### Kết quả đạt được

- Xây dựng và quản lý được Docker image phục vụ triển khai ứng dụng.
- Thực hành triển khai container trên Lightsail Containers, EKS và Fargate.
- Hoàn thành quy trình CI/CD cơ bản và áp dụng giám sát, quản lý tài nguyên, bảo mật cho môi trường container.
