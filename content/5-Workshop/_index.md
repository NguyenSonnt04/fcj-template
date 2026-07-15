---
title: "Workshop"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# TrustBite User Authentication with Amazon Cognito

#### Overview

In this workshop, you will build user registration, email confirmation, sign-in, and REST API protection for **TrustBite Review System** with Amazon Cognito User Pools.

The mobile or web client redirects users to Cognito Managed Login using the **Authorization Code flow with PKCE**. After sign-in, the client receives tokens and sends the **access token** to the Express backend in `Authorization: Bearer <token>`. The backend uses `aws-jwt-verify` to validate the signature, expiration, user pool, app client, and `token_use` before processing the request.

{{% notice info %}}
This workshop uses **Asia Pacific (Singapore) – ap-southeast-1**. You can choose another Region, but must update the Region, User Pool ID, and App Client ID throughout the configuration.
{{% /notice %}}

#### Content

1. [Architecture overview](5.1-Workshop-overview/)
2. [Prerequisites](5.2-Prerequisites/)
3. [Create and configure a Cognito User Pool](5.3-Cognito-user-pool/)
4. [Integrate Cognito with the application](5.4-Application-integration/)
5. [Security and testing](5.5-Security/)
6. [Clean up](5.6-Cleanup/)

#### Expected results

- Users can register and confirm their accounts by email.
- The application signs users in through Cognito and receives ID, access, and refresh tokens.
- The backend allows protected API access only with a valid access token.
- Expired tokens and tokens with invalid signatures, issuers, or app client IDs return HTTP `401`.
