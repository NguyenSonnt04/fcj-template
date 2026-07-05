---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Nghiên cứu tổng quan dự án TrustBite Review System và cấu trúc mã nguồn monorepo.
* Thiết lập môi trường phát triển và tìm hiểu các dịch vụ AWS được sử dụng trong dự án.
* Nghiên cứu cơ sở dữ liệu PostgreSQL, cơ chế xác thực và quy trình phát triển của nhóm.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | Tổng quan về dự án TrustBite Review System: nghiên cứu mục tiêu, phạm vi và các chức năng chính của hệ thống nhằm nắm bắt định hướng phát triển sản phẩm | 22/06/2026 | 22/06/2026 | |
| 3 | Đọc tài liệu và tìm hiểu cấu trúc mã nguồn monorepo với 3 thành phần: backend (Node.js + Express), web client (Next.js, React) và mobile (Flutter); tìm hiểu cách các thành phần giao tiếp qua REST API | 23/06/2026 | 23/06/2026 | |
| 4 | Thiết lập môi trường phát triển theo tài liệu hướng dẫn; cài đặt Node.js, npm, Flutter, Docker và các dependency; build và chạy thử các thành phần trên môi trường cục bộ | 24/06/2026 | 24/06/2026 | |
| 5 | Tìm hiểu các dịch vụ AWS trong dự án (S3, Cognito, Textract, Bedrock, SES); nghiên cứu cơ chế Anti-Fraud Verification và thiết kế cơ sở dữ liệu PostgreSQL (users, restaurants, reviews, badges, price_history) | 25/06/2026 | 25/06/2026 | |
| 6 | Nghiên cứu quy trình xác thực JWT qua AWS Cognito và bảo vệ API; làm quen với coding convention, quy trình tạo Pull Request và kiểm thử của nhóm | 26/06/2026 | 27/06/2026 | |

### Kết quả đạt được tuần 9:

* Tổng quan về dự án TrustBite Review System, nghiên cứu mục tiêu, phạm vi và các chức năng chính của hệ thống nhằm nắm bắt định hướng phát triển sản phẩm.
* Đọc tài liệu và tìm hiểu cấu trúc mã nguồn của dự án theo mô hình monorepo; làm quen với ba thành phần chính gồm backend (Node.js + Express), web client (Next.js, React) và mobile (Flutter), đồng thời tìm hiểu cách các thành phần giao tiếp thông qua REST API.
* Thực hiện cài đặt môi trường phát triển theo tài liệu hướng dẫn của dự án; cài đặt các công cụ và thư viện cần thiết như Node.js, npm, Flutter, Docker và các dependency liên quan, sau đó build và chạy thử các thành phần của hệ thống trên môi trường cục bộ.
* Tìm hiểu các dịch vụ AWS được sử dụng trong dự án như Amazon S3, Amazon Cognito, Amazon Textract, Amazon Bedrock và Amazon SES; nghiên cứu vai trò của từng dịch vụ trong hệ thống và cách sử dụng LocalStack để mô phỏng các dịch vụ AWS trong quá trình phát triển.
* Đọc tài liệu về cơ chế xác minh đánh giá (Anti-Fraud Verification) của hệ thống; tìm hiểu quy trình xử lý từ việc tiếp nhận hóa đơn, trích xuất thông tin bằng OCR, kiểm tra tính hợp lệ của dữ liệu và xác minh vị trí người dùng.
* Tìm hiểu thiết kế cơ sở dữ liệu PostgreSQL của dự án; đọc các file migration và schema để nắm được mối quan hệ giữa các bảng chính như users, restaurants, reviews, badges và price_history.
* Nghiên cứu quy trình xác thực và phân quyền của hệ thống thông qua AWS Cognito; tìm hiểu cách backend xác thực JWT và bảo vệ các API trước khi xử lý nghiệp vụ.
* Làm quen với quy trình phát triển phần mềm của nhóm; đọc tài liệu hướng dẫn coding convention, quy trình quản lý công việc, cách tạo Pull Request, quy trình kiểm thử và chuẩn bị môi trường để tham gia phát triển.
