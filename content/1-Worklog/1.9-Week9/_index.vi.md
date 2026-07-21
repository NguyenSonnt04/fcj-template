---
title: "Worklog Tuần 9"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9

- Nắm được mục tiêu, phạm vi và kiến trúc của TrustBite Review System.
- Thiết lập môi trường phát triển và tìm hiểu các dịch vụ AWS trong dự án.
- Hiểu cơ chế chống gian lận, cơ sở dữ liệu, xác thực và quy trình làm việc của nhóm.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **Tổng quan dự án TrustBite**<br>- Tìm hiểu vấn đề đánh giá giả và mục tiêu xây dựng nền tảng đánh giá có xác minh.<br>- Nghiên cứu phạm vi, nhóm người dùng và các chức năng chính của hệ thống.<br>- Đọc tài liệu tổng quan để nắm định hướng phát triển sản phẩm. | 22/06/2026 | 22/06/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |
| 3 | **Cấu trúc monorepo**<br>- Khảo sát ba thành phần: backend Node.js/Express, web client Next.js/React và mobile Flutter.<br>- Tìm hiểu cấu trúc thư mục, dependency và cách tổ chức mã nguồn của từng thành phần.<br>- Nghiên cứu cách các client giao tiếp với backend thông qua REST API. | 23/06/2026 | 23/06/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |
| 4 | **Thiết lập môi trường phát triển**<br>- Cài đặt Node.js, npm, Flutter, Docker và các dependency theo tài liệu dự án.<br>- Cấu hình biến môi trường, build và chạy thử từng thành phần trên máy cục bộ.<br>- Ghi nhận lỗi thiết lập, kiểm tra kết nối và xác nhận môi trường sẵn sàng phát triển. | 24/06/2026 | 24/06/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |
| 5 | **AWS và cơ chế Anti-Fraud**<br>- Tìm hiểu vai trò của S3, Cognito, Textract, Bedrock và SES trong TrustBite.<br>- Nghiên cứu cách LocalStack mô phỏng dịch vụ AWS trong môi trường phát triển.<br>- Đọc luồng xác minh hóa đơn: tiếp nhận ảnh, OCR, kiểm tra dữ liệu, phát hiện trùng lặp và xác minh vị trí. | 25/06/2026 | 25/06/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |
| 6 | **Database, authentication và quy trình nhóm**<br>- Đọc migration và schema PostgreSQL; tìm hiểu quan hệ giữa users, restaurants, reviews, badges và price_history.<br>- Nghiên cứu cách backend xác thực JWT từ Amazon Cognito và bảo vệ API.<br>- Làm quen coding convention, quản lý công việc, Pull Request và quy trình kiểm thử của nhóm. | 26/06/2026 | 26/06/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |

### Kết quả đạt được

- Nắm được kiến trúc monorepo và luồng giao tiếp chính của TrustBite.
- Thiết lập thành công môi trường phát triển cục bộ và hiểu vai trò của các dịch vụ AWS liên quan.
- Hiểu cơ chế Anti-Fraud, mô hình dữ liệu, xác thực Cognito và quy trình cộng tác của nhóm.
