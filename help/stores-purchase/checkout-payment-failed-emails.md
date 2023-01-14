---
title: Payment failure notification
description: Learn how to configure email communications for a payment method that fails to complete a transaction.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
---
# Payment failure notification

A notification is sent to the store contact or a designated Admin user if the payment method selected during checkout fails to complete the transaction.

![Payment Failed Emails](../configuration-reference/sales/assets/checkout-payment-failed-emails.png)<!-- zoom -->

## Step 1: Update the email template

Make sure that you have updated the needed email template to reflect your brand. For a complete list of templates, see [Email Template List](../systems/email-templates.md#email-template-list).

## Step 2: Configure the payment failed emails

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. On the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Checkout]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Payment Failed Emails]** section.

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
