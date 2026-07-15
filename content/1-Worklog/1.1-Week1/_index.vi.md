---
title: "Worklog Tuần 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1

- Làm quen với môi trường AWS và các nhóm dịch vụ cơ bản.
- Hiểu cách quản lý tài khoản, chi phí và quyền truy cập bằng IAM.
- Bước đầu triển khai hạ tầng mạng và ứng dụng trên Amazon EC2.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **Tổng quan về AWS**<br>- Tìm hiểu mô hình điện toán đám mây và các nhóm dịch vụ chính của AWS như Compute, Storage, Networking và Database.<br>- Làm quen với AWS Management Console, cách tìm kiếm dịch vụ và lựa chọn Region phù hợp.<br>- Tìm hiểu quy trình tạo, quản lý tài khoản AWS và các lưu ý khi sử dụng Free Tier. | 27/04/2026 | 27/04/2026 | <https://cloudjourney.awsstudygroup.com/1-explore/> |
| 3 | **Quản lý chi phí và quyền truy cập**<br>- Tìm hiểu AWS Billing, Cost Explorer và Budget để theo dõi chi phí sử dụng.<br>- Nghiên cứu cơ chế hỗ trợ của AWS và Shared Responsibility Model.<br>- Thực hành tạo IAM user, group và policy; phân biệt tài khoản root với IAM user. | 28/04/2026 | 28/04/2026 | <https://cloudjourney.awsstudygroup.com/1-explore/> |
| 4 | **Xây dựng hạ tầng mạng VPC**<br>- Tìm hiểu các thành phần của Amazon VPC: CIDR, subnet, route table, Internet Gateway và security group.<br>- Thiết kế hạ tầng mạng cơ bản gồm public subnet và tuyến kết nối Internet.<br>- Kiểm tra quy tắc inbound và outbound để chuẩn bị kết nối đến EC2. | 29/04/2026 | 29/04/2026 | <https://cloudjourney.awsstudygroup.com/1-explore/> |
| 5 | **Khởi tạo Amazon EC2**<br>- Tìm hiểu AMI, instance type, key pair và EBS volume.<br>- Thực hành khởi tạo một EC2 instance trong VPC đã cấu hình.<br>- Gán security group và kiểm tra thông tin public IPv4 của instance. | 30/04/2026 | 30/04/2026 | <https://cloudjourney.awsstudygroup.com/1-explore/> |
| 6 | **Triển khai và kiểm tra ứng dụng**<br>- Kết nối đến EC2 bằng SSH và kiểm tra trạng thái hệ điều hành.<br>- Cài đặt các thành phần cần thiết, triển khai ứng dụng mẫu và mở cổng dịch vụ phù hợp.<br>- Kiểm tra khả năng truy cập ứng dụng, rà soát kết nối mạng và ghi nhận kết quả thực hành. | 01/05/2026 | 02/05/2026 | <https://cloudjourney.awsstudygroup.com/1-explore/> |

### Kết quả đạt được

- Nắm được cách sử dụng AWS Management Console, quản lý tài khoản và theo dõi chi phí cơ bản.
- Biết tạo và phân quyền IAM theo nguyên tắc cấp quyền tối thiểu.
- Hoàn thành hạ tầng VPC cơ bản, khởi tạo EC2 và triển khai thử nghiệm ứng dụng.
