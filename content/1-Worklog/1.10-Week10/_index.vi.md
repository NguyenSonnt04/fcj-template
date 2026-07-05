---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Thiết lập môi trường phát triển với Docker Compose và xây dựng cơ sở dữ liệu PostgreSQL.
* Xây dựng bộ khung backend theo kiến trúc phân tầng và triển khai Repository Harness.
* Thiết kế cơ chế soft delete, mô hình phân quyền và làm quen quy trình phát triển của nhóm.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | Thiết lập môi trường với Docker Compose: khởi chạy đồng thời PostgreSQL, Redis, LocalStack, pgAdmin; kiểm tra trạng thái container và xác nhận kết nối cơ sở dữ liệu qua pgAdmin | 29/06/2026 | 29/06/2026 | |
| 3 | Thiết kế cơ sở dữ liệu PostgreSQL qua migration 001_init_schema.sql; xây dựng bảng dữ liệu cốt lõi; kích hoạt extension pgcrypto và PostGIS; thiết lập migration tự động và bảng schema_migrations | 30/06/2026 | 30/06/2026 | |
| 4 | Xây dựng bộ khung backend theo kiến trúc phân tầng với Express và Native ESModules; tổ chức mã nguồn thành config, routes, controllers, services, models và middlewares; thiết lập quy ước snake_case/camelCase | 01/07/2026 | 01/07/2026 | |
| 5 | Nghiên cứu và triển khai Repository Harness; cài đặt Harness CLI trên Windows, khởi tạo cơ sở dữ liệu cục bộ; thực hiện truy vấn ma trận kiểm thử và hoàn thành story TB-HARNESS với trạng thái implemented | 02/07/2026 | 02/07/2026 | |
| 6 | Nghiên cứu soft delete cho bảng nhà hàng; thiết kế bảng roles, user_roles và rank_definitions; tìm hiểu quy trình tiếp nhận tính năng mới, coding convention và cấu trúc story packet | 03/07/2026 | 03/07/2026 | |

### Kết quả đạt được tuần 10:

* Thiết lập môi trường phát triển cho dự án; cài đặt và cấu hình Docker Compose để khởi chạy đồng thời PostgreSQL, Redis, LocalStack và pgAdmin; kiểm tra trạng thái hoạt động của toàn bộ container và xác nhận kết nối cơ sở dữ liệu qua pgAdmin.
* Thiết kế cơ sở dữ liệu PostgreSQL ban đầu thông qua migration 001_init_schema.sql; xây dựng các bảng dữ liệu cốt lõi; kích hoạt các extension pgcrypto và PostGIS; thiết lập cơ chế migration tự động cùng bảng schema_migrations để quản lý phiên bản cơ sở dữ liệu.
* Xây dựng bộ khung backend theo kiến trúc phân tầng với Express và Native ESModules; tổ chức mã nguồn thành các thư mục config, routes, controllers, services, models và middlewares; thiết lập quy ước thống nhất sử dụng snake_case cho request và camelCase cho response.
* Nghiên cứu và triển khai hệ thống Repository Harness; cài đặt Harness CLI trên Windows và khởi tạo cơ sở dữ liệu Harness cục bộ; thực hiện truy vấn ma trận kiểm thử và hoàn thành story TB-HARNESS với trạng thái implemented.
* Nghiên cứu cơ chế soft delete cho bảng nhà hàng; thực hiện migration bổ sung các trường is_deleted và deleted_at cho bảng restaurants.
* Tìm hiểu mô hình phân quyền và quản lý vai trò người dùng; nghiên cứu thiết kế các bảng roles, user_roles và rank_definitions.
* Nghiên cứu quy trình quản lý công việc và coding convention của nhóm; tìm hiểu quy trình tiếp nhận tính năng mới và cấu trúc của một story packet.
