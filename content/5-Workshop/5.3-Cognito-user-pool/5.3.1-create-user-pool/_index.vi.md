---
title: "Tạo User Pool"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.3.1. </b> "
---

#### Bước 1: Mở Amazon Cognito

1. Đăng nhập AWS Management Console.
2. Chuyển Region sang **Asia Pacific (Singapore) – ap-southeast-1**.
3. Tìm **Amazon Cognito** và chọn **User pools**.
4. Chọn **Create user pool**.

#### Bước 2: Định nghĩa ứng dụng

1. Chọn application type phù hợp với mobile hoặc Single Page Application.
2. Đặt tên ứng dụng `trustbite-mobile-dev`.
3. Chọn **Email** làm sign-in identifier.
4. Không tạo client secret cho mobile/SPA vì public client không thể bảo vệ secret.

#### Bước 3: Cấu hình đăng ký và xác nhận

1. Bật self-service sign-up vì TrustBite cho phép người dùng tự đăng ký.
2. Chọn email là thuộc tính bắt buộc.
3. Bật Cognito-assisted verification để Cognito gửi mã xác nhận email.
4. Giữ chính sách password đủ mạnh: tối thiểu 8 ký tự, có chữ hoa, chữ thường, số và ký tự đặc biệt.
5. Trong môi trường lab có thể đặt MFA là **Optional**; production nên ưu tiên TOTP hoặc passkey theo yêu cầu bảo mật.

#### Bước 4: Tạo tài nguyên

1. Kiểm tra lại cấu hình.
2. Chọn **Create application** hoặc **Create user pool** tùy giao diện Console.
3. Mở phần overview của User Pool vừa tạo.
4. Ghi lại **User Pool ID**, ví dụ `ap-southeast-1_AbCdEf123`.

#### Bước 5: Kiểm tra cấu hình

Trong User Pool, xác nhận:

- Sign-in identifier là email.
- Self-service sign-up đang bật.
- Email verification đang bật.
- App Client đã được tạo.
- Password policy và MFA đúng với môi trường lab.

{{% notice warning %}}
Chỉ bật public self-sign-up khi ứng dụng thực sự cho phép bất kỳ người dùng Internet nào đăng ký. Với ứng dụng nội bộ, hãy tắt self-sign-up và tạo người dùng bằng quy trình quản trị.
{{% /notice %}}
