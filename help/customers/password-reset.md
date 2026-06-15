---
title: Reset customer passwords
description: Customers usually reset their passwords from the storefront but a store administrator can initiate either a password reset or a forced sign-in from the Admin.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
TQID: https://experienceleague.adobe.com/yzGC0T8unOSE-sZkE4PRHM6xMVX68qD6fARb-OSUB0U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Reset customer passwords

Customers usually reset their passwords from the storefront by clicking _[!UICONTROL Forgot Your Password?]_. However, the store administrator can initiate either a password reset or a forced sign-in from the Admin.

|Function|Description|
| --- | --- |
|Reset Password | A password reset email is sent directly to the customer's email account. The store administrator cannot gain access to the customer's password.|
|Force Sign In | Revokes the OAuth access tokens that are associated with the customer account. This can be used only with customer accounts that have been assigned OAuth tokens, as part of a Web API [integration](../systems/integrations.md). To learn more, see [OAuth-based authentication](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in the developer documentation. <br/><br/>Standard customer accounts created from the storefront or from the Admin do not have OAuth tokens.|

{style="table-layout:auto"}

## Reset a password from the storefront

1. On the login page, the customer clicks **[!UICONTROL Forgot Your Password?]**.

1. When prompted, enters the **[!UICONTROL Email Address]** that is associated with their account and clicks **[!UICONTROL Reset My Password]**.

   ![Forgot Your Password](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >If the entered email address matches the one that is associated with the account, the customer receives a Password Reset Confirmation email with a link to reset their password.

1. When the email arrives, the customer clicks the _reset password_ link and enters their **[!UICONTROL New Password]** when prompted.

1. Enters it again to confirm and clicks **[!UICONTROL Reset Password]**.
   
   >[!IMPORTANT]
   >
   >The new password must be six or more characters in length without spaces. When they receive confirmation that the password is updated, they can use the new password to sign in to their account. By default, the _reset password_ link is valid for 24 hours.

## Reset a password from the Admin

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Find the customer account in the grid and click **[!UICONTROL Edit]** in the _Action_ column.

1. In the set of options across the top of the page, click **[!UICONTROL Reset Password]**.

   The number of password reset requests that are allowed within an hour is set in the [configuration](../configuration-reference/customers/customer-configuration.md) topic.

## Revoke a customer's OAuth tokens

>[!IMPORTANT]
>
>Do not proceed unless you have a full understanding of API Authentication.

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Find the customer account in the grid and click **[!UICONTROL Edit]** in the _Action_ column.

1. In the set of options across the top of the page, click **[!UICONTROL Force Sign In]**.

1. When prompted to confirm, click **OK**.
