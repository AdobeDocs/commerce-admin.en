---
title: Customer password options
description: The customer password options determine the level of security for various customer-facing functions of your store.
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
TQID: https://experienceleague.adobe.com/ttWsiKhuvquDE2oQRWLF9rTDTZ64BHkKD0Lbv-EDnHs
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
# Customer password options

The customer password options determine the level of security that is used for password reset requests, the email templates that are used for customer notification, and the lifetime of the password recovery link. You can allow customers to change their own passwords or require that only store administrators can do so.

## Configure customer password options

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Customers]** and choose **[!UICONTROL Customer Configuration]**.

1. Expand the **[!UICONTROL Password Options]** section.

   ![Password Options](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. Set the **[!UICONTROL Password Reset Protection Type]** to the method that you want to use for checking password reset requests:

   - `By IP and Email` - Check for previous attempts to reset password for specific email or from specific IP.
   - `By IP` - Check for previous attempts to reset password from specific IP.
   - `By Email` - Check for previous attempts to reset password for specific email.
   - `None` - Protection disabled (no limits for resetting password).

   The **[!UICONTROL Max Number of Password Reset Requests]** and **[!UICONTROL Min Time Between Password Reset Requests]** are calculated based on this configuration.

1. To limit the number of password reset requests sent per hour, do the following:

   - For **[!UICONTROL Max Number of Password Reset Requests]**, enter the maximum number of password reset requests that can be sent per hour.

   - For **[!UICONTROL Min Time Between Password Reset Requests]**, enter the minimum number of minutes that must elapse between requests.

1. To configure the password reset email notification, do the following:

   - Set **[!UICONTROL Forgot Email Template]** to the template that is used for the email sent to customers who have forgotten their passwords.

   - Set **[!UICONTROL Remind Email Template]** to the template that is used when a customer password is reset by an Admin user.

   - Set **[!UICONTROL Reset Password Template]** to the template that is used when customers change their passwords.

   - Set **[!UICONTROL Password Template Email Sender]** to the [store contact](../getting-started/store-details.md) that appears as the sender of password-related notifications.

1. Complete the following password reset security options:

   - For **[!UICONTROL Recovery Link Expiration Period (hours)]**, enter the number of hours before the password recovery link expires.

   - If you want the fields in the customer login and forgot password forms to be filled automatically from previous entries, set **[!UICONTROL Enable Autocomplete on login/forgot password forms]** to `Yes`.

   - For **[!UICONTROL Number of Required Character Classes]**, enter the number of different character types that must be included in a password based on the following character classes:

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - For **[!UICONTROL Maximum Login Failures to Lockout Account]**, enter the number of failed login attempts until the customer account is locked. For unlimited attempts, enter zero (`0`).

   - For **[!UICONTROL Minimum Password Length]**, enter the minimum number of characters that can be used in a password. The number must be greater than zero.

   - For **[!UICONTROL Lockout Time (minutes)]**, enter the number of minutes a customer account is locked after too many failed attempts to log in.

1. When complete, click **[!UICONTROL Save Config]**.
