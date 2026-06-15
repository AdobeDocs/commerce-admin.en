---
title: Payment failure notification
description: Learn how to configure email communications for a payment method that fails to complete a transaction.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
TQID: https://experienceleague.adobe.com/ZnVr9N90qZ58fJARyOw4rAecOhQF6KLmJZSBJflgMKc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
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
# Payment failure notification

A notification is sent to the store contact or a designated Admin user if the payment method selected during checkout fails to complete the transaction.

## Step 1: Update the email template

Make sure that you have updated the needed email template to reflect your brand. For a complete list of templates, see [Email Template List](../systems/email-templates.md#email-template-list).

## Step 2: Configure the payment failed emails

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. On the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Checkout]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Payment Failed Emails]** section.

   ![Payment Failed Emails](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Set the options for payment failed emails:

   - Set **[!UICONTROL Payment Failed Email Sender]** to the store contact that appears as the sender of the message.
   - Set **[!UICONTROL Payment Failed Email Receiver]** to the store contact that is to receive notification of failed email transmissions.
   - Set **[!UICONTROL Payment Failed Template]** to the template that is used for the email that is sent when the payment method fails during checkout.

1. For **[!UICONTROL Send Payment Failed Email Copy To]**, enter the email address of anyone who is to receive a copy of the payment failed notification.

   If sending a copy to multiple recipients, separate each address with a comma.

1. Set **[!UICONTROL Payment Failed Copy Method]** to one of the following:

   - `Bcc` - Sends a _blind courtesy copy_ by including the recipient in the header of the same email that is sent to the customer. The BCC recipient is not visible to the customer.
   - `Separate Email` - Sends the copy as a separate email.

1. Click **[!UICONTROL Save Config]**.
