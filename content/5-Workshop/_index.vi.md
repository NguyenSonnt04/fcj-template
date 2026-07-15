---
title: "Workshop"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Xác thực người dùng TrustBite bằng Amazon Cognito

#### Tổng quan

Trong workshop này, chúng ta sẽ xây dựng luồng đăng ký, xác nhận email, đăng nhập và bảo vệ REST API cho **TrustBite Review System** bằng Amazon Cognito User Pools.

Ứng dụng mobile hoặc web chuyển người dùng đến Cognito Managed Login bằng luồng **Authorization Code với PKCE**. Sau khi đăng nhập, client nhận token và gửi **access token** trong header `Authorization: Bearer <token>` đến backend Express. Backend sử dụng `aws-jwt-verify` để kiểm tra chữ ký, thời hạn, User Pool, App Client và `token_use` trước khi xử lý request.

{{% notice info %}}
Workshop sử dụng Region **Asia Pacific (Singapore) – ap-southeast-1**. Bạn có thể chọn Region khác nhưng phải thay giá trị Region, User Pool ID và App Client ID trong toàn bộ cấu hình.
{{% /notice %}}

#### Nội dung

1. [Tổng quan kiến trúc](5.1-Workshop-overview/)
2. [Chuẩn bị môi trường](5.2-Prerequisites/)
3. [Tạo và cấu hình Cognito User Pool](5.3-Cognito-user-pool/)
4. [Tích hợp Cognito vào ứng dụng](5.4-Application-integration/)
5. [Bảo mật và kiểm thử](5.5-Security/)
6. [Dọn dẹp tài nguyên](5.6-Cleanup/)

#### Kết quả mong đợi

- Người dùng có thể đăng ký và xác nhận tài khoản bằng email.
- Ứng dụng đăng nhập qua Cognito và nhận ID, access, refresh token.
- Backend chỉ cho phép request có access token hợp lệ truy cập API được bảo vệ.
- Token hết hạn, sai chữ ký, sai issuer hoặc sai App Client ID đều bị từ chối với HTTP `401`.
