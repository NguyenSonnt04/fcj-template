---
title: "Architecture overview"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

#### Authentication architecture

```text
User
  │
  ▼
Mobile / Web Application
  │  1. Authorization Code + PKCE
  ▼
Amazon Cognito User Pool
  │  2. Sign-up, email confirmation, sign-in
  │  3. Return ID, access, and refresh tokens
  ▼
Mobile / Web Application
  │  4. Authorization: Bearer <access_token>
  ▼
TrustBite Express API
  │  5. Verify JWT with Cognito JWKS
  ▼
Protected API / PostgreSQL
```

#### Component roles

| Component | Role |
| --- | --- |
| **Cognito User Pool** | User directory and OpenID Connect identity provider |
| **App Client** | Defines how the mobile/web application communicates with the user pool |
| **Managed Login** | Cognito-provided sign-up, sign-in, MFA, and password recovery pages |
| **Authorization Code + PKCE** | Secure authentication flow for public clients that cannot keep a client secret |
| **Access token** | Token the backend uses to authorize API access |
| **ID token** | Contains user identity and profile attributes |
| **Refresh token** | Obtains new tokens without requiring another sign-in |
| **JWKS** | Public keys used to verify JWT signatures issued by Cognito |

#### Authentication and authorization

- **Authentication** establishes who the user is. Cognito handles registration, sign-in, and token issuance.
- **Authorization** determines what the user can do. TrustBite checks scopes, groups, roles, and account status before allowing business operations.

{{% notice warning %}}
Do not use the ID token to protect REST APIs. This workshop accepts only access tokens with `token_use` set to `access`.
{{% /notice %}}
