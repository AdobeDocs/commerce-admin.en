---
title: Email a friend
description: Learn how to provide an email link that makes it easy for your customers to share links to products with their friends.
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
TQID: https://experienceleague.adobe.com/a75E4X5mTDXeCQKysvIecdU3OhsICiWTtwh7k-oK9cw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Email a friend

The Email link makes it easy for your customers to share links to products with their friends. In the demo Luma store, the Email link appears as an envelope icon. The message template can be customized for your voice and brand. To prevent spamming, you can limit the number of recipients for each email, and the number of products that can be shared over a one-hour period.

![Example storefront - email a friend](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## Configure email-a-friend

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Email to a Friend]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Email Templates]** section and set the options:

    ![Catalog configuration - email templates](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

    For a detailed description of each of these configuration settings, see [Email Templates](../configuration-reference/catalog/email-to-a-friend.md) in the _Configuration Reference Guide_.

    To change the default setting of any field, clear the **[!UICONTROL Use system value]** checkbox to make the field editable.

    - Set **[!UICONTROL Enabled]** to `Yes`.

    - Set **[!UICONTROL Select Email Template]** to the template that you want to use as the basis of the messages.

    - If you want to require that only registered customers can send email to friends, set **[!UICONTROL Allow for Guests]** to `No`.

    - For **[!UICONTROL Max Recipients]**, enter the maximum number of friends who can be on the distribution list for a single message.

    - For **[!UICONTROL Max Products Sent in 1 Hour]**, enter the maximum number of products that can be shared by a single user with friends over a one-hour time period.

    - Set **[!UICONTROL Limit Sending By]** to one of the following methods to identify the sender of emails:

      `IP Address`  - (Recommended) Identifies the sender by the IP address of the computer that is used to send the emails.

      `Cookie (unsafe)` - Identifies the sender by browser cookie. This method is less effective because the sender can delete the cookie to bypass the limit.

1. When complete, click **[!UICONTROL Save Config]**.

## Send email to a friend on the storefront

When this feature is configured, store customers follow these steps to share product information with friends.

1. On a catalog page, the customer clicks the **[!UICONTROL Email]** link.

1. If the feature is configured only for registered users, does one of the following:

   - Logs in to your customer account.
   - Signs up for a new account.

1. Completes the **[!UICONTROL Message]** and enters the recipient **[!UICONTROL Name]** and **[!UICONTROL Email Address]**.
   
   If needed, the customer can add more recipients:

    - Clicks **[!UICONTROL Add Invitee]**.

    - Enters the **[!UICONTROL Name]** and **[!UICONTROL Email Address]** of the additional person.

      They can send the message to as many additional people as the configuration allows. They can remove the added invitee by clicking the **[!DNL Remove]** link.

1. When ready to send the message, clicks **[!UICONTROL Send Email]**.

    ![Example storefront - email to a friend](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
