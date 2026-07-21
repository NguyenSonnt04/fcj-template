---
title: "Worklog Tuần 12"
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12

- Hoàn thiện các module hóa đơn, review và tìm kiếm nhà hàng của TrustBite.
- Phát triển, tích hợp và hoàn thiện các màn hình chính trên ứng dụng mobile.
- Kiểm thử, khắc phục lỗi và triển khai sản phẩm hoàn chỉnh lên server.
- Hoàn thiện báo cáo thực tập cuối kỳ và quay video demo phục vụ buổi đánh giá dự án.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **Module hóa đơn và OCR**<br>- Tham gia phát triển module xử lý hóa đơn ở backend.<br>- Hỗ trợ xây dựng service tải ảnh hóa đơn lên Amazon S3 và tích hợp với hàng đợi OCR.<br>- Viết test cho các trường hợp upload thành công, upload thất bại và lỗi trong quá trình xác minh.<br>- Kiểm tra việc xử lý exception và phản hồi lỗi từ service lưu trữ hoặc hàng đợi. | 13/07/2026 | 13/07/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |
| 3 | **Review API và luồng xác minh**<br>- Hỗ trợ phát triển các API liên quan đến chức năng tạo và xử lý review.<br>- Xây dựng integration test cho toàn bộ luồng từ khi người dùng tạo review đến khi hệ thống xác minh và trả kết quả.<br>- Kiểm tra trạng thái dữ liệu, mã phản hồi và cách hệ thống xử lý các tình huống xác minh thất bại. | 14/07/2026 | 14/07/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |
| 4 | **Tìm kiếm và lọc nhà hàng**<br>- Tham gia phát triển tính năng tìm kiếm và lọc nhà hàng trong Phase 3.<br>- Viết integration test cho các chức năng xem danh sách, xem chi tiết và tìm kiếm nhà hàng trên môi trường local.<br>- Kiểm tra dữ liệu đầu vào, kết quả phân trang, bộ lọc và các trường hợp không tìm thấy dữ liệu. | 15/07/2026 | 15/07/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |
| 5 | **Authentication và giao diện mobile**<br>- Hỗ trợ xây dựng màn hình đăng nhập mobile tích hợp Amazon Cognito.<br>- Xử lý lỗi đăng nhập, trạng thái loading và điều hướng sau khi xác thực thành công.<br>- Tham gia phát triển màn hình Home, tab Thông báo và màn hình nhập thông tin dành cho người dùng mới.<br>- Phối hợp với thành viên backend để cập nhật luồng lưu hồ sơ theo quy trình đăng ký mới. | 16/07/2026 | 16/07/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |
| 6 | **Triển khai cuối kỳ, báo cáo và video demo**<br>- Chỉnh sửa giao diện Favorites, Splash Screen và cập nhật icon ứng dụng theo thiết kế chung.<br>- Rà soát tính thống nhất của giao diện, điều hướng, trạng thái hiển thị và các lỗi cuối trên mobile.<br>- Refactor và dọn dẹp mã nguồn trước khi bàn giao.<br>- Triển khai sản phẩm hoàn chỉnh lên server và kiểm tra các chức năng chính trên môi trường đã deploy.<br>- Hoàn thiện báo cáo thực tập cuối kỳ và tài liệu workshop liên quan.<br>- Xây dựng kịch bản demo và quay video giới thiệu hệ thống TrustBite cùng các chức năng chính. | 17/07/2026 | 17/07/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |

### Kết quả đạt được

- Hoàn thiện thêm các module hóa đơn, OCR, review và tìm kiếm nhà hàng ở backend.
- Bổ sung integration test cho các luồng nghiệp vụ chính và tình huống lỗi.
- Phát triển, tích hợp các màn hình đăng nhập, Home, Thông báo, thông tin người dùng mới, Favorites và Splash Screen trên mobile.
- Rà soát chức năng, sửa lỗi và dọn dẹp mã nguồn trước khi bàn giao.
- Triển khai sản phẩm hoàn chỉnh lên server và xác minh hoạt động của hệ thống sau khi deploy.
- Hoàn thiện báo cáo thực tập cuối kỳ và quay video demo dự án.
