---
title: "Worklog Tuần 11"
date: 2024-01-01
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11

- Hoàn thiện kiểm thử cơ chế xác thực JWT và các API liên quan đến người dùng.
- Xây dựng service xác minh khoảng cách GPS cho cơ chế chống gian lận của TrustBite.
- Nâng cấp quy trình CI để tự động chạy migration và toàn bộ test suite.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **Unit test cho Cognito JWT**<br>- Nghiên cứu cách CognitoIdentityProvider xác thực và giải mã JWT do Amazon Cognito phát hành.<br>- Viết unit test cho các trường hợp token hợp lệ, token hết hạn và JWT bị cắt xén.<br>- Tạo helper sinh JWT bằng cặp khóa RSA trong bộ nhớ để bộ test có thể chạy độc lập mà không cần kết nối Cognito thật. | 06/07/2026 | 06/07/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |
| 3 | **Kiểm thử các trường hợp JWT không hợp lệ**<br>- Bổ sung test cho token sai issuer, sai client_id và token có chữ ký không hợp lệ.<br>- Kiểm tra mã lỗi và hành vi của provider khi nhận các loại token không đáng tin cậy.<br>- Refactor helper tạo token để dễ dàng thay đổi payload, thời hạn, issuer, client và khóa ký cho từng test case. | 07/07/2026 | 07/07/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |
| 4 | **Integration test đăng nhập và user profile**<br>- Viết integration test cho luồng đăng nhập và đọc hồ sơ người dùng qua Express.<br>- Kiểm tra ba trường hợp chính: người dùng hợp lệ, người dùng có trạng thái SUSPENDED và request không có token.<br>- Sử dụng trusted-local header để giả lập identity trong môi trường test thay vì phụ thuộc vào Cognito thật. | 08/07/2026 | 08/07/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |
| 5 | **GPS Proximity Service**<br>- Xây dựng server/src/services/verification/gpsProximityService.js để tính khoảng cách giữa người dùng và nhà hàng bằng công thức Haversine.<br>- Trả về khoảng cách theo mét và kết quả đạt/không đạt so với ngưỡng được cấu hình.<br>- Bổ sung validation cho latitude, longitude và threshold; xử lý các giá trị vượt phạm vi hoặc không hợp lệ.<br>- Tạo server/src/config/antiFraud.js với ngưỡng GPS mặc định 200 mét và hỗ trợ ghi đè bằng biến môi trường GPS_PROXIMITY_THRESHOLD_METERS. | 09/07/2026 | 09/07/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |
| 6 | **Kiểm thử GPS và cập nhật CI**<br>- Viết 13 unit test cho GPS service, bao gồm khoảng cách bằng 0, trong ngưỡng, ngoài ngưỡng, đúng ranh giới và dữ liệu đầu vào không hợp lệ.<br>- Chạy npm run test:unit --prefix server và xác nhận toàn bộ 80 test vượt qua.<br>- Hỗ trợ cập nhật GitHub Actions để tự động chạy database migration và toàn bộ Vitest test suite thay vì chỉ kiểm tra syntax.<br>- Cập nhật test factory helper để tạo dữ liệu kiểm thử linh hoạt hơn. | 10/07/2026 | 10/07/2026 | [Mã nguồn](https://github.com/trustbite-team-tcc/trustbite-review-system) <br> [Tài liệu](https://github.com/NguyenSonnt04/docs_trustbite) |

### Kết quả đạt được

- Hoàn thiện unit test cho CognitoIdentityProvider và integration test cho luồng đăng nhập, user profile.
- Xây dựng GPS Proximity Service với cấu hình ngưỡng linh hoạt và validation đầy đủ.
- Hoàn thành 13 test case GPS, nâng tổng số unit test vượt qua lên 80.
- Nâng cấp CI workflow để tự động kiểm tra migration và test suite trên GitHub Actions.
