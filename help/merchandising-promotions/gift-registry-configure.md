---
title: Configure gift registries
description: Lean how to enable gift registries and configure the related email notifications.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
TQID: https://experienceleague.adobe.com/a7DRiAPSkWhBIPdXPXnH3HB1uw9d4WY4vXOtfgg9kRY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
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

   ![Customers configuration - gift registry general](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - The Gift Registry is enabled by default. If necessary, set **[!UICONTROL Enable Gift Registry]** to `Yes`.

   - For **[!UICONTROL Maximum Registrants]**, enter the maximum number of people that can be invited to participate in a gift registry event.

## Step 2. Configure Email Notifications

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Owner Notification]** section and do the following:

   ![Customers configuration - gift registry owner notification](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Choose the **[!UICONTROL Email Template]** that notifies gift registry owners when their registries are created.

   - Choose the [store contact](../getting-started/store-details.md#store-email-addresses) that appears as the **[!UICONTROL Email Sender]** of the message.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Gift Registry Sharing]** section and do the following:

   ![Customers configuration - gift registry sharing](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Choose the **[!UICONTROL Email Template]** that notifies gift registry recipients when a registry is shared with them.

   - Choose the store identify that appears as the **[!UICONTROL Email Sender]** of the message.

   - For **[!UICONTROL Maximum Sent Emails Threshold]**, enter the maximum number of emails that can be sent at one time.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Gift Registry Update]** section and do the following:

   ![Customers configuration - gift registry update](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Choose the **[!UICONTROL Email Template]** that notifies gift registry owners of changes to the registry.

   - Choose the store identify that appears as the **[!UICONTROL Email Sender]** of the message.

1. When complete, click **[!UICONTROL Save Config]**.

1. When prompted, update the cache.

   After the cache is refreshed, Gift Registry appears in the Stores menu under Other Settings and becomes available in customer accounts.
