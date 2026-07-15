---
title: "Cấu hình App Client"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.4.2. </b> "
---

#### Bước 1: Kiểm tra App Client

1. Trong User Pool, chọn **App clients**.
2. Mở `trustbite-mobile-dev`.
3. Xác nhận App Client không có client secret.
4. Ghi lại **Client ID**.

#### Bước 2: Tạo Cognito domain

1. Mở menu **Domain** hoặc **Managed login**.
2. Chọn Cognito domain prefix duy nhất, ví dụ `trustbite-dev-<mã-của-bạn>`.
3. Lưu domain đầy đủ:

```text
https://trustbite-dev-<mã-của-bạn>.auth.ap-southeast-1.amazoncognito.com
```

#### Bước 3: Cấu hình OAuth 2.0

Trong App Client, cấu hình:

| Thuộc tính | Giá trị |
| --- | --- |
| Allowed callback URL | `http://localhost:3000/auth/callback` |
| Allowed sign-out URL | `http://localhost:3000/logout` |
| OAuth grant | Authorization code grant |
| OpenID Connect scopes | `openid`, `email`, `profile` |
| Identity provider | Cognito user pool |

Managed Login dùng Authorization Code. Ứng dụng phải sinh `code_verifier` và `code_challenge` mới cho mỗi request PKCE.

#### Bước 4: Tạo URL đăng nhập thử nghiệm

```text
https://<domain>/oauth2/authorize
  ?response_type=code
  &client_id=<app_client_id>
  &redirect_uri=http%3A%2F%2Flocalhost%3A3000%2Fauth%2Fcallback
  &scope=openid+email+profile
  &code_challenge=<base64url_sha256_of_verifier>
  &code_challenge_method=S256
```

Sau khi đăng nhập thành công, Cognito chuyển trình duyệt về callback URL cùng tham số `code`. Client đổi code và `code_verifier` tại `/oauth2/token` để nhận token.

#### Bước 5: Lưu cấu hình

Cập nhật `.env` của backend:

```dotenv
COGNITO_REGION=ap-southeast-1
COGNITO_USER_POOL_ID=<user_pool_id>
COGNITO_APP_CLIENT_ID=<app_client_id>
```

{{% notice warning %}}
Callback URL phải khớp chính xác với URL đã đăng ký, bao gồm protocol, port, path và dấu `/` cuối nếu có.
{{% /notice %}}
