---
title: "Create the User Pool"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 5.3.1. </b> "
---

#### Step 1: Open Amazon Cognito

1. Sign in to the AWS Management Console.
2. Change the Region to **Asia Pacific (Singapore) – ap-southeast-1**.
3. Open **Amazon Cognito** and choose **User pools**.
4. Choose **Create user pool**.

#### Step 2: Define the application

1. Select the application type for a mobile or Single Page Application.
2. Name the application `trustbite-mobile-dev`.
3. Select **Email** as the sign-in identifier.
4. Do not create a client secret for a mobile/SPA public client because it cannot protect the secret.

#### Step 3: Configure sign-up and confirmation

1. Enable self-service sign-up because TrustBite allows public user registration.
2. Make email a required attribute.
3. Enable Cognito-assisted verification so Cognito sends email confirmation codes.
4. Use a strong password policy: at least 8 characters with uppercase, lowercase, number, and special characters.
5. Set MFA to **Optional** for the lab; production should prefer TOTP or passkeys according to security requirements.

#### Step 4: Create the resources

1. Review the configuration.
2. Choose **Create application** or **Create user pool**, depending on the console experience.
3. Open the new User Pool overview.
4. Record the **User Pool ID**, for example `ap-southeast-1_AbCdEf123`.

#### Step 5: Verify the configuration

Confirm that:

- Email is the sign-in identifier.
- Self-service sign-up is enabled.
- Email verification is enabled.
- The App Client exists.
- Password and MFA policies match the lab environment.

{{% notice warning %}}
Enable public self-sign-up only when anyone on the Internet should be able to register. For internal applications, disable it and use an administrative provisioning workflow.
{{% /notice %}}
