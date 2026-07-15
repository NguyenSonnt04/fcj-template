---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10

- Hoàn thiện môi trường phát triển và cơ sở dữ liệu PostgreSQL cho TrustBite.
- Xây dựng bộ khung backend và triển khai Repository Harness.
- Nghiên cứu soft delete, mô hình phân quyền và quy trình phát triển theo story của nhóm.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **Docker Compose và dịch vụ cục bộ**<br>- Cấu hình Docker Compose để khởi chạy PostgreSQL, Redis, LocalStack và pgAdmin.<br>- Chạy npm run docker:up, kiểm tra trạng thái và log của toàn bộ container.<br>- Kết nối PostgreSQL qua pgAdmin và xác nhận các dịch vụ có thể giao tiếp trong môi trường local. | 29/06/2026 | 29/06/2026 |  |
| 3 | **Database schema và migration**<br>- Xây dựng migration 001_init_schema.sql cho các bảng dữ liệu cốt lõi và bảng hỗ trợ nghiệp vụ.<br>- Kích hoạt extension pgcrypto và PostGIS phục vụ UUID và dữ liệu địa lý.<br>- Thiết lập migration tự động cùng bảng schema_migrations để quản lý phiên bản cơ sở dữ liệu. | 30/06/2026 | 30/06/2026 |  |
| 4 | **Bộ khung backend phân tầng**<br>- Xây dựng backend bằng Express và Native ES Modules.<br>- Tổ chức mã nguồn thành config, routes, controllers, services, models và middlewares.<br>- Thống nhất quy ước sử dụng snake_case cho request và camelCase cho response. | 01/07/2026 | 01/07/2026 |  |
| 5 | **Repository Harness**<br>- Đọc tài liệu về Repository Harness và quy trình phân loại công việc.<br>- Cài đặt Harness CLI trên Windows và khởi tạo cơ sở dữ liệu Harness cục bộ.<br>- Thực hiện truy vấn ma trận kiểm thử và hoàn thành story TB-HARNESS với trạng thái implemented. | 02/07/2026 | 02/07/2026 |  |
| 6 | **Soft delete, phân quyền và story workflow**<br>- Xây dựng decision record cho cơ chế soft delete của nhà hàng; bổ sung is_deleted và deleted_at vào bảng restaurants.<br>- Nghiên cứu thiết kế các bảng roles, user_roles, rank_definitions và vòng đời trạng thái tài khoản.<br>- Tìm hiểu feature intake, coding convention, quy tắc theo domain và cấu trúc story packet; thực hành phân tích một story mẫu. | 03/07/2026 | 03/07/2026 |  |

### Kết quả đạt được

- Hoàn thiện môi trường local gồm PostgreSQL, Redis, LocalStack và pgAdmin.
- Xây dựng database migration, backend skeleton và Repository Harness cho dự án.
- Hiểu và triển khai bước đầu cơ chế soft delete, mô hình phân quyền và quy trình phát triển theo story.
