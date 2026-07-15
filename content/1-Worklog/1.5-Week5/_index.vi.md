---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5

- Chuyển đổi ứng dụng Spring Boot từ Monolithic sang Microservices.
- Xây dựng giao tiếp đồng bộ, bất đồng bộ và workflow serverless trên AWS.
- Thiết lập xác thực, CI/CD và giám sát cho hệ thống phân tán.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **Phân tích Monolithic và Microservices**<br>- Phân tích các module nghiệp vụ trong ứng dụng Java Spring Boot hiện tại.<br>- Xác định ranh giới service và tách các thành phần chức năng thành service độc lập.<br>- Chuẩn hóa cấu hình và dữ liệu cần thiết để từng service có thể hoạt động riêng biệt. | 25/05/2026 | 25/05/2026 |  |
| 3 | **API và giao tiếp giữa các service**<br>- Xây dựng REST API phục vụ giao tiếp giữa các microservice.<br>- Kiểm tra luồng xử lý dữ liệu, mã lỗi và khả năng hoạt động độc lập của từng service.<br>- Cấu hình Amazon SQS và Amazon SNS cho giao tiếp bất đồng bộ, sau đó kiểm thử luồng sự kiện. | 26/05/2026 | 26/05/2026 |  |
| 4 | **Xây dựng ứng dụng Serverless**<br>- Phát triển các hàm AWS Lambda để xử lý nghiệp vụ và dữ liệu.<br>- Kết hợp API Gateway, Amazon S3 và DynamoDB để xây dựng luồng serverless hoàn chỉnh.<br>- Kiểm tra request, response, quyền IAM và khả năng truy cập dữ liệu. | 27/05/2026 | 27/05/2026 |  |
| 5 | **Xác thực và tự động triển khai**<br>- Thiết lập Amazon Cognito cho ứng dụng Single Page Application.<br>- Kiểm tra quy trình đăng ký, đăng nhập, cấp token và quản lý phiên người dùng.<br>- Xây dựng AWS CodePipeline để tự động build, kiểm thử và triển khai ứng dụng. | 28/05/2026 | 28/05/2026 |  |
| 6 | **Workflow và giám sát hệ thống**<br>- Xây dựng workflow nghiệp vụ bằng AWS Step Functions và theo dõi trạng thái từng bước.<br>- Tìm hiểu AWS AppSync và tích hợp GraphQL API cho ứng dụng.<br>- Cấu hình CloudWatch và AWS X-Ray để phân tích log, trace request và xử lý lỗi hiệu năng. | 29/05/2026 | 29/05/2026 |  |

### Kết quả đạt được

- Hiểu và thực hành quá trình phân rã ứng dụng Monolithic thành các microservice độc lập.
- Triển khai giao tiếp REST, SQS/SNS và một luồng serverless với Lambda, API Gateway, S3 và DynamoDB.
- Thiết lập Cognito, CodePipeline, Step Functions, AppSync, CloudWatch và X-Ray cho hệ thống.
