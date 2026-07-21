---
title: "Worklog Tuần 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3

- Hiểu quy trình và các chiến lược Migration to AWS.
- Thực hành di chuyển máy chủ và cơ sở dữ liệu lên AWS.
- Đánh giá, kiểm thử và tối ưu hệ thống sau migration.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **Tổng quan Migration to AWS**<br>- Tìm hiểu các động lực chuyển hệ thống lên cloud và AWS Migration Acceleration Program.<br>- Nghiên cứu chiến lược 7Rs: Retire, Retain, Relocate, Rehost, Replatform, Repurchase và Refactor.<br>- Phân loại workload để lựa chọn phương án migration phù hợp. | 11/05/2026 | 11/05/2026 | <https://cloudjourney.awsstudygroup.com/2-migrate/> |
| 3 | **Đánh giá và lập kế hoạch migration**<br>- Khảo sát ứng dụng, cơ sở dữ liệu, phụ thuộc hệ thống và yêu cầu về mạng.<br>- Xác định thứ tự di chuyển, thời gian bảo trì và phương án rollback.<br>- Tìm hiểu các biện pháp giảm downtime và rủi ro trong quá trình triển khai. | 12/05/2026 | 12/05/2026 | <https://cloudjourney.awsstudygroup.com/2-migrate/> |
| 4 | **Di chuyển máy chủ ảo**<br>- Tìm hiểu yêu cầu và quy trình sử dụng AWS VM Import/Export.<br>- Chuẩn bị image máy ảo, import lên AWS và tạo AMI từ image đã nhập.<br>- Khởi tạo EC2 từ AMI, sau đó kiểm tra trạng thái hệ điều hành và ứng dụng. | 13/05/2026 | 13/05/2026 | <https://cloudjourney.awsstudygroup.com/2-migrate/> |
| 5 | **Migration cơ sở dữ liệu**<br>- Tìm hiểu AWS Database Migration Service (DMS) và AWS Schema Conversion Tool (SCT).<br>- Đánh giá khả năng tương thích schema giữa cơ sở dữ liệu nguồn và đích.<br>- Nghiên cứu Full Load, Change Data Capture và cách duy trì đồng bộ dữ liệu trong thời gian chuyển đổi. | 14/05/2026 | 14/05/2026 | <https://cloudjourney.awsstudygroup.com/2-migrate/> |
| 6 | **Kiểm thử và tối ưu sau migration**<br>- Kiểm tra kết nối mạng, security group, DNS và quyền truy cập của workload sau migration.<br>- Đối chiếu dữ liệu và kiểm tra chức năng của ứng dụng trên môi trường AWS.<br>- Rà soát hiệu năng, tính ổn định, khả năng giám sát và lập kế hoạch tối ưu sau chuyển đổi. | 15/05/2026 | 15/05/2026 | <https://cloudjourney.awsstudygroup.com/2-migrate/> |

### Kết quả đạt được

- Hiểu quy trình đánh giá, lập kế hoạch, thực hiện và kiểm thử migration lên AWS.
- Thực hành quy trình di chuyển máy chủ ảo bằng VM Import/Export.
- Nắm được vai trò của DMS và SCT trong migration cơ sở dữ liệu và giảm downtime.
