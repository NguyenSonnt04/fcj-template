---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2

- Sử dụng IAM Role để cấp quyền an toàn giữa các dịch vụ AWS.
- Triển khai website tĩnh, cơ sở dữ liệu và làm quen với công cụ phát triển trên AWS.
- Tìm hiểu mô hình web có tính sẵn sàng cao và các dịch vụ hỗ trợ vận hành.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **IAM Role và AWS Cloud9**<br>- Phân biệt IAM user, IAM policy và IAM role.<br>- Tạo IAM role và gắn role cho EC2 để truy cập dịch vụ AWS mà không lưu Access Key trực tiếp trên máy chủ.<br>- Làm quen với môi trường AWS Cloud9 và thực hiện các thao tác phát triển cơ bản. | 04/05/2026 | 04/05/2026 |  |
| 3 | **Website tĩnh trên Amazon S3**<br>- Tạo S3 bucket, cấu hình quyền truy cập và tổ chức object trong bucket.<br>- Bật tính năng Static Website Hosting và triển khai các tệp HTML/CSS mẫu.<br>- Kiểm tra website endpoint và tìm hiểu các lưu ý về Block Public Access. | 05/05/2026 | 05/05/2026 |  |
| 4 | **Cơ sở dữ liệu Amazon RDS**<br>- Tìm hiểu các thành phần của Amazon RDS: database engine, instance class, storage và backup.<br>- Khởi tạo cơ sở dữ liệu RDS và cấu hình security group cho phép kết nối từ EC2.<br>- Kiểm tra kết nối và thực hiện một số thao tác dữ liệu cơ bản. | 06/05/2026 | 06/05/2026 |  |
| 5 | **Giám sát và khả năng mở rộng**<br>- Tìm hiểu Auto Scaling Group và cơ chế điều chỉnh số lượng EC2 theo nhu cầu.<br>- Sử dụng Amazon CloudWatch để theo dõi metric, log và alarm.<br>- Tìm hiểu cách Route 53 phân giải tên miền và điều hướng lưu lượng đến ứng dụng. | 07/05/2026 | 07/05/2026 |  |
| 6 | **AWS CLI và mô hình High Availability**<br>- Cài đặt, cấu hình và sử dụng AWS CLI trên EC2 thông qua IAM Role.<br>- Thực hành truy vấn thông tin tài nguyên bằng các lệnh CLI cơ bản.<br>- Tổng hợp mô hình website có tính sẵn sàng cao kết hợp nhiều Availability Zone, Load Balancer, Auto Scaling và RDS. | 08/05/2026 | 08/05/2026 |  |

### Kết quả đạt được

- Cấp quyền giữa EC2 và các dịch vụ AWS bằng IAM Role an toàn hơn so với Access Key tĩnh.
- Triển khai được website tĩnh trên S3 và kết nối ứng dụng với Amazon RDS.
- Hiểu vai trò của Auto Scaling, CloudWatch, Route 53 và AWS CLI trong vận hành hệ thống có tính sẵn sàng cao.
