---
title: Manage two-factor authentication
description: Learn how to manage two-factor authentication and reset the authenticators for Admin users.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/aE-36667-f0E4GSXDjZZmFUkS3wa-xTLUMbVtjwS6qk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
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
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Manage two-factor authentication

Users who are unable to sign in to the _Admin_ with two-factor authentication (2FA) can try to sync or troubleshoot the problem. You can also reset the authenticators associated with the account. When reset, the user must sign in again and reconfigure the required authenticators.

If you have trouble signing in with 2FA, consider the following:

- Some mobile apps include synchronization options. This option reconnects the app and server, and synchronizes the time settings on the device and server.
- Revoking a device or resetting an authenticator can help users connect.
- Clearing web cache and cookies for the Adobe Commerce or Magento Open Source installation can also help. Authenticators, like Google, use generated cookies to save access and duration. Clear the cookies for your specific browser and store domain.
- Blocking cookies prevents some authenticators, such as [!DNL Google Authenticator], from completing the verification process. Add a rule to your browser that allows cookies for your Adobe Commerce installation.

To reset authenticators from the command line and more advanced troubleshooting information, see [Two-Factor Authentication](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) in the developer documentation.

**_To reset authenticators for a user account:_**

>[!NOTE]
>
>To reset 2FA providers for other users, you must be an _administrator_ with `All` permissions, or have `Custom` permissions for your role with [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] and [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] selected. To learn more, see [User Roles](permissions-user-roles.md).

1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Permissions]_ > **[!UICONTROL All Users]**.

1. Select the user and open the account in edit mode.

1. Scroll down to the _[!UICONTROL Current User Identity Verification]_ section and enter your password.

1. In the left panel, click **[!UICONTROL 2FA]**.

1. In the _[!UICONTROL Configuration reset]_ section, click **[!UICONTROL Reset]** and **[!UICONTROL OK]** to confirm.

   ![User account - enable 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   If the user wants to restore the required 2FA methods to their account, they must reconfigure each from the _Sign On_ page.

1. When complete, click **[!UICONTROL Save User]**.
