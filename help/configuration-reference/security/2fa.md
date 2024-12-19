---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Review the configurations settings on the [!UICONTROL Security] &gt; [!UICONTROL 2FA] page of the Commerce Admin.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
---
# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Stores that have enabled Adobe Identity Management Services (IMS) authentication have native Adobe Commerce and Magento Open Source two-factor authentication (2FA) disabled. Admin users who are logged into their Adobe Commerce instance with their Adobe credentials do not need to reauthenticate for many Admin tasks. Authentication is handled by Adobe IMS when the Admin user logs into their current session. See [Integrating Adobe Commerce with Adobe IMS overview](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

For more information about changing these settings, see [Two-factor authentication (2FA)](../../systems/security-two-factor-authentication.md) in the _Admin Systems Guide_.

## [!UICONTROL General]

![General](./assets/2fa-general.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Providers to use]|Global|Indicates the two-factor authentication methods that you require. If you select more than one provider, each user is required to configure each 2FA method the next time they log in.|
|[!UICONTROL Configuration Email URL for Web API]|Global |For custom implementations, the URL for an alternate email configuration link that is sent to _Admin_ users at first login. In the email template, use the placeholder `:tfat` to indicate where the token is injected.|
|[!UICONTROL Retry attempt limit for Two-Factor Authentication]|Global| Determines how many times an administrator can enter a [!DNL one-time password (OTP)] before their account is temporarily disabled. Default: `10`|
|[!UICONTROL Two-Factor Authentication lockout time (seconds)]|Global| Determines how long (in seconds) that an administrator can wait to enter a [!DNL one-time password (OTP)] before their account is temporarily disabled. Default: `300`|

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL OTP Window]|Global|Determines how long (in seconds) that the system accepts an administrator's [!DNL one-time-password (OTP)] after it has expired. Cannot be higher than the lifetime of a single OTP (usually 30 seconds). Default: `29`|

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Duo Security](./assets/2fa-duo-security.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Client Id]|Global|The Client ID from your [!DNL Duo Security] account.|
|[!UICONTROL Client Secret]|Global|The Client Secret from your [!DNL Duo Security] account.|
|[!UICONTROL Duo Failmode]|Global|The Failmode settings for your [!DNL Duo Security] account.|
|[!UICONTROL Integration Key]|Global|The integration key from your [!DNL Duo Security] API account.|
|[!UICONTROL Secret Key]|Global|The secret key from your [!DNL Duo Security] API account.|
|[!UICONTROL API Hostname]|Global|The API hostname from your [!DNL Duo Security] account.|

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Authy](./assets/2fa-authy.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL API Key]|Global|The API key from your [!DNL Authy] account.|
|[!UICONTROL OneTouch Message]|Global|The message that appears in the [!DNL Authy] authenticator at login. Default: `Login request to your Magento Admin`|

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![U2F Key](./assets/2fa-u2f-key.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL WebApi Challenge Domain]|Global|The domain that is used to issue and process [!DNL WebAuthn] challenges for custom WebAPI implementations.|

{style="table-layout:auto"}
