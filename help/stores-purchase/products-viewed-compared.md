---
title: Recently viewed or compared products
description: Learn how to configure the storefront content blocks for recently viewed and compared products.
exl-id: a4580835-68c2-4eb0-825e-0939eeab921b
feature: Products, Storefront
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/YeayJ1RkE6Muq0wNnd6KAQmmZcyjTQrSZOqEltlj8T8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
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
# Recently viewed or compared products

The _Recently Viewed and Recently Compared_ blocks usually appear in the right sidebar of a catalog page. The number of products listed in each can be configured for each website, store, or store view.

**_To configure recently viewed and compared products:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Recently Viewed/Compared Products]** section.

   ![Catalog configuration - recently viewed/compared products](../configuration-reference/catalog/assets/catalog-recently-viewed-and-compared-products.png){width="600" zoomable="yes"}

   For a detailed description of each of these configuration settings, see [Recently Viewed/Compared Products](../configuration-reference/catalog/catalog.md#recently-viewedcompared-products) in the _Configuration Reference Guide_.

1. Set **[!UICONTROL Synchronize widget products with backend storage]** to synchronize product widget information, such as product ID, with your current product storage availability in the database and reuse this information on different devices.

1. Set **[!UICONTROL Show for Current]** to the website, store, or store view where the configuration applies.

1. For **[!UICONTROL Default Recently Viewed Products Count]**, enter the number of recently viewed products to appear in the list.

1. For **[!UICONTROL Default Recently Compared Products Count]**, enter the number of recently compared products to appear in the list.

1. For **[!UICONTROL Lifetime of products in Recently Viewed Widget]**, enter any time range in seconds, greater than zero.

   This setting determines how long the viewed products are shown in the recently viewed list.

1. For **[!UICONTROL Lifetime of products in Recently Compared Widget]**, enter any time range in seconds, greater than zero.

   This setting determines how long the compared products are shown in the recently compared list.

1. When complete, click **[!UICONTROL Save Config]**.
