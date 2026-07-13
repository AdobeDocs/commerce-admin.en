---
title: Two-factor authentication (2FA)
description: Learn about two-factor authentication support to ensure the security of your system and data.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/-201IPkmoP1dmQL3kk4zb3XdTgrYtiUovj4-hkaNrnc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
    internal-label: 2FA
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Two-factor authentication (2FA)

The Commerce _Admin_ for your Adobe Commerce or Magento Open Source installation provides access to your store, orders, and customer data. To prevent unauthorized access to your data, all users who attempt to sign in to the _Admin_ must complete an authentication process to verify their identity.

>[!NOTE]
>
>This implementation of two-factor authentication (2FA) applies to the _Admin_ only, and is not available for customer accounts. The two-factor authentication that protects your Commerce account has a separate setup. To learn more, go to [Secure your Commerce account](../getting-started/commerce-account-secure.md).

Two-factor authentication is widely used, and it is common to generate access codes for different websites on the same app. This additional authentication ensures that only you are able to log in to your user account. If you lose your password or a bot guesses it, two-factor authentication adds a layer of protection. For example, you might use Google Authenticator to generate codes for the Admin of your store, your Commerce account, and Google account.

![Security configuration iphone - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce supports 2FA methods from multiple providers. Some require the installation of an app that generates a one-time password (OTP) that users enter at sign-in to verify their identity. Universal second factor (U2F) devices resemble a key fob and generate a unique key to verify identity. Other devices verify identity when they are inserted into a USB port. As the store administrator, you can require one or more of the available 2FA methods to verify user identity. Your 2FA configuration applies to all websites and stores that are associated with the Adobe Commerce installation.

The first time a user signs in to the _Admin_, they must set up each [2FA](../configuration-reference/security/2fa.md) method that you require, and verify their identity using the associated app or device. After this initial setup, the user must authenticate with one of the configured methods each time they sign in. Each user's 2FA information is recorded in their _Admin_ account and can be [reset](security-two-factor-authentication-manage.md) if necessary. To learn more about the sign-in process, go to [_Admin_ Sign In](../getting-started/admin-signin.md).

>[!NOTE]
>
>Stores that have enabled Adobe Identity Management Services (IMS) authentication have native Adobe Commerce and Magento Open Source 2FA disabled. Admin users who are logged into their Commerce instance with their Adobe credentials do not need to reauthenticate for many Admin tasks. Authentication is handled by Adobe IMS when the Admin user logs into their current session. See [Adobe Identity Management Service (IMS) Integration Overview](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

You can watch this [video demo](https://video.tv.adobe.com/v/339104?quality=12&learn=on) for an overview of two-factor authentication in the Admin.

## Configure your required 2FA providers

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Security]** and choose **[!UICONTROL 2FA]**.

1. In the _[!UICONTROL General]_ section, select the providers to use.

   |Provider|Function|
   |--- |--- |
   |[!UICONTROL Google Authenticator]|Generates a one-time password in the application for user authentication.|
   |[!UICONTROL Duo Security]|Provides SMS and push notification.|
   |[!UICONTROL Authy]|Generates a time-dependent six-digit code and delivers SMS or Voice Call 2FA protection or token.|
   |[!UICONTROL U2F Devices (Yubikey and others)]| Uses a physical device to authenticate, such as [[!DNL YubiKey]](https://www.yubico.com/).|

   To select multiple methods, hold down the Ctrl key (PC) or the Command key (Mac) and click each item.

1. Complete the [settings](../configuration-reference/security/2fa.md) for each required 2FA method.

   ![Security configuration - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. When complete, click **[!UICONTROL Save Config]**.

   The first time users sign in to the _Admin_, they must set up each required 2FA method. After this initial setup, they must authenticate with one of the configured methods each time they sign in.

## 2FA Provider Settings

Complete the settings for each 2FA method that you require.

### Google

To change how long the one-time password (OTP) is available during sign-in, clear the **[!UICONTROL Use system value]** checkbox. Then, enter the number of seconds that you want the **[!UICONTROL OTP Window]** to be valid.

![Security configuration - Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

>[!NOTE]
>
>In Adobe Commerce 2.4.7 and later, the OTP window configuration setting controls how long (in seconds) the system accepts an administrator's one-time-password (OTP) after it has expired. This value must be less than 30 seconds. The system default setting is `29`.<br><br> In version 2.4.6, the OTP window setting determines the number of past and future OTP codes that remain valid. A value of `1` indicates that the current OTP code plus one code in the past and one code in the future remain valid at any given point in time. 

### [!DNL Duo Security]

Enter the following credentials from your Duo Security account:

- Client ID
- Client Secret
- Integration key
- Secret key
- API hostname

![Security configuration - Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Enter the API key from your [!DNL Authy] account.

1. To change the default message that appears during authentication, clear the **[!UICONTROL Use system value]** checkbox. Then, enter the **[!UICONTROL OneTouch Message]** that you want to appear.

   ![Security configuration - Authy](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### U2F Devices ([!DNL Yubikey] and others)

The store domain is used by default during the authentication process. To use a custom domain for authentication challenges, clear the **[!UICONTROL Use system value]** checkbox. Then, enter the **[!UICONTROL WebAPi Challenge Domain]**.

![Security configuration - U2F Devices](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
