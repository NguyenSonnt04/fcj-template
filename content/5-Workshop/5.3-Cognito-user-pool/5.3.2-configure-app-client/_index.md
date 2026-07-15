---
title: "Configure the App Client"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 5.3.2. </b> "
---

#### Step 1: Verify the App Client

1. In the User Pool, choose **App clients**.
2. Open `trustbite-mobile-dev`.
3. Confirm that it has no client secret.
4. Record the **Client ID**.

#### Step 2: Create a Cognito domain

1. Open **Domain** or **Managed login**.
2. Choose a unique domain prefix such as `trustbite-dev-<your-id>`.
3. Save the complete domain:

```text
https://trustbite-dev-<your-id>.auth.ap-southeast-1.amazoncognito.com
```

#### Step 3: Configure OAuth 2.0

Configure the App Client:

| Setting | Value |
| --- | --- |
| Allowed callback URL | `http://localhost:3000/auth/callback` |
| Allowed sign-out URL | `http://localhost:3000/logout` |
| OAuth grant | Authorization code grant |
| OpenID Connect scopes | `openid`, `email`, `profile` |
| Identity provider | Cognito user pool |

Managed Login uses the Authorization Code flow. The application must generate a new `code_verifier` and `code_challenge` for every PKCE request.

#### Step 4: Build a test authorization URL

```text
https://<domain>/oauth2/authorize
  ?response_type=code
  &client_id=<app_client_id>
  &redirect_uri=http%3A%2F%2Flocalhost%3A3000%2Fauth%2Fcallback
  &scope=openid+email+profile
  &code_challenge=<base64url_sha256_of_verifier>
  &code_challenge_method=S256
```

After sign-in, Cognito redirects to the callback URL with a `code`. The client exchanges the code and `code_verifier` at `/oauth2/token` for tokens.

#### Step 5: Save the configuration

Update the backend `.env`:

```dotenv
COGNITO_REGION=ap-southeast-1
COGNITO_USER_POOL_ID=<user_pool_id>
COGNITO_APP_CLIENT_ID=<app_client_id>
```

{{% notice warning %}}
The callback URL must exactly match the registered URL, including protocol, port, path, and any trailing slash.
{{% /notice %}}
