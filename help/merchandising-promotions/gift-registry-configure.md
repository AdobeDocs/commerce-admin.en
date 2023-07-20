---
title: Configure gift registries
description: Lean how to enable gift registries and configure the related email notifications.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
---
# Configure gift registries

{{ee-feature}}

Before you can offer gift registries to your customers, you must enable gift registries and configure the related email notifications. Adobe Commerce sends the following email notifications in response to events in the gift registry workflow.

- When a new gift registry is created, an email is sent to the owner with a link to registry that can be shared.
- Optionally, the store can send notification with a link to the gift registry to friends and family of the gift registry owner.
- The owner is notified when items are purchased from the gift registry, but does not indicate the purchaser.

Adobe Commerce has predefined templates for each of these email messages that can be customized for your brand.

## Step 1. Enable Gift Registries

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Customers]** and choose **[!UICONTROL Gift Registry]**

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL General Options]** section and do the following:

   ![Customers configuration - gift registry general](../configuration-reference/customers/assets/gift-registry-general-options.png)<!-- zoom -->

   - The Gift Registry is enabled by default. If necessary, set **[!UICONTROL Enable Gift Registry]** to `Yes`.

   - For **[!UICONTROL Maximum Registrants]**, enter the maximum number of people that can be invited to participate in a gift registry event.

## Step 2. Configure Email Notifications

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Owner Notification]** section and do the following:

   ![Customers configuration - gift registry owner notification](../configuration-reference/customers/assets/gift-registry-owner-notification.png)<!-- zoom -->

   - Choose the **[!UICONTROL Email Template]** that notifies gift registry owners when their registries are created.

   - Choose the [store contact](../getting-started/store-details.md#store-email-addresses) that appears as the **[!UICONTROL Email Sender]** of the message.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Gift Registry Sharing]** section and do the following:

   ![Customers configuration - gift registry sharing](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

   - Choose the **[!UICONTROL Email Template]** that notifies gift registry recipients when a registry is shared with them.

   - Choose the store identify that appears as the **[!UICONTROL Email Sender]** of the message.

   - For **[!UICONTROL Maximum Sent Emails Threshold]**, enter the maximum number of emails that can be sent at one time.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Gift Registry Update]** section and do the following:

   ![Customers configuration - gift registry update](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png)<!-- zoom -->

   - Choose the **[!UICONTROL Email Template]** that notifies gift registry owners of changes to the registry.

   - Choose the store identify that appears as the **[!UICONTROL Email Sender]** of the message.

1. When complete, click **[!UICONTROL Save Config]**.

1. When prompted, update the cache.

   After the cache is refreshed, Gift Registry appears in the Stores menu under Other Settings and becomes available in customer accounts.
