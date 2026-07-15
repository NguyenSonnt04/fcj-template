---
title: "Tổng quan kiến trúc"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

#### Kiến trúc xác thực

```text
Người dùng
    │
    ▼
Ứng dụng Mobile / Web
    │  1. Authorization Code + PKCE
    ▼
Amazon Cognito User Pool
    │  2. Đăng ký, xác nhận email, đăng nhập
    │  3. Trả về ID token, access token, refresh token
    ▼
Ứng dụng Mobile / Web
    │  4. Authorization: Bearer <access_token>
    ▼
TrustBite Express API
    │  5. Xác minh JWT bằng Cognito JWKS
    ▼
Protected API / PostgreSQL
```

#### Vai trò của các thành phần

| Thành phần | Vai trò |
| --- | --- |
| **Cognito User Pool** | Thư mục người dùng và OpenID Connect Identity Provider |
| **App Client** | Cấu hình cách mobile/web giao tiếp với User Pool |
| **Managed Login** | Giao diện đăng ký, đăng nhập, MFA và quên mật khẩu do Cognito cung cấp |
| **Authorization Code + PKCE** | Luồng đăng nhập an toàn cho public client không thể giữ client secret |
| **Access token** | Token được backend dùng để cấp quyền truy cập API |
| **ID token** | Chứa thông tin định danh và thuộc tính hồ sơ người dùng |
| **Refresh token** | Dùng để nhận token mới mà không yêu cầu đăng nhập lại |
| **JWKS** | Bộ public key dùng để xác minh chữ ký JWT do Cognito phát hành |

#### Phân biệt xác thực và phân quyền

- **Authentication** xác định người dùng là ai. Cognito User Pool chịu trách nhiệm đăng ký, đăng nhập và phát hành token.
- **Authorization** xác định người dùng được phép làm gì. Backend TrustBite kiểm tra scope, group, role và trạng thái tài khoản trước khi cho phép thực hiện nghiệp vụ.

{{% notice warning %}}
Không dùng ID token để bảo vệ REST API. API của workshop chỉ chấp nhận access token có `token_use` bằng `access`.
{{% /notice %}}
