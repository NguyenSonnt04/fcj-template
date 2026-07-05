---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Chuyển đổi ứng dụng Java Spring Boot từ Monolithic sang kiến trúc Microservices.
* Xây dựng giao tiếp bất đồng bộ với SQS/SNS và triển khai ứng dụng Serverless với Lambda.
* Thiết lập CI/CD và giám sát hệ thống phân tán với CloudWatch và X-Ray.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | Thực hiện chuyển đổi ứng dụng Java Spring Boot từ kiến trúc Monolithic sang mô hình Microservices; phân tách các thành phần chức năng và xây dựng các service độc lập | 25/05/2026 | 25/05/2026 | |
| 3 | Xây dựng và triển khai các API giao tiếp giữa các Microservice; kiểm tra luồng xử lý dữ liệu và khả năng hoạt động độc lập của từng dịch vụ | 26/05/2026 | 26/05/2026 | |
| 4 | Cấu hình giao tiếp bất đồng bộ bằng Amazon SQS và Amazon SNS; triển khai ứng dụng Serverless sử dụng AWS Lambda kết hợp API Gateway, S3 và DynamoDB | 27/05/2026 | 27/05/2026 | |
| 5 | Thiết lập xác thực và phân quyền người dùng bằng Amazon Cognito cho ứng dụng SPA; xây dựng quy trình CI/CD bằng AWS CodePipeline | 28/05/2026 | 28/05/2026 | |
| 6 | Cấu hình giám sát với Amazon CloudWatch và AWS X-Ray; thực hành Step Functions và tích hợp AWS AppSync theo mô hình GraphQL | 29/05/2026 | 30/05/2026 | |

### Kết quả đạt được tuần 5:

* Thực hiện chuyển đổi ứng dụng Java Spring Boot từ kiến trúc Monolithic sang mô hình Microservices; phân tách các thành phần chức năng và xây dựng các service độc lập phục vụ từng nghiệp vụ.
* Xây dựng và triển khai các API phục vụ giao tiếp giữa các Microservice; kiểm tra luồng xử lý dữ liệu và khả năng hoạt động độc lập của từng dịch vụ.
* Cấu hình cơ chế giao tiếp bất đồng bộ giữa các thành phần hệ thống bằng Amazon SQS và Amazon SNS; thực hiện kiểm thử luồng xử lý sự kiện trong môi trường phân tán.
* Triển khai ứng dụng Serverless sử dụng AWS Lambda kết hợp Amazon API Gateway, Amazon S3 và DynamoDB; xây dựng các hàm xử lý dữ liệu và kết nối với cơ sở dữ liệu.
* Thiết lập xác thực và phân quyền người dùng bằng Amazon Cognito cho ứng dụng Single Page Application (SPA); kiểm tra quy trình đăng nhập và quản lý phiên làm việc.
* Xây dựng quy trình CI/CD bằng AWS CodePipeline để tự động hóa việc build, kiểm thử và triển khai ứng dụng lên môi trường AWS.
* Cấu hình giám sát và theo dõi hoạt động hệ thống bằng Amazon CloudWatch và AWS X-Ray; phân tích log, theo dõi hiệu năng và xử lý các lỗi phát sinh.
* Thực hành xây dựng workflow xử lý nghiệp vụ bằng AWS Step Functions và tích hợp AWS AppSync để cung cấp API theo mô hình GraphQL.
