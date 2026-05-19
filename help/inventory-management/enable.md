---
title: Enable [!DNL Inventory Management]
description: Learn how to enable [!DNL Inventory Management] at the global store or product level.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/evCX34nY-m7WQnZt3xw7ng6-It7Xlf5DTanjKbP1fCk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
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
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Enable [!DNL Inventory Management]

To manage your product inventory, enable [!DNL Inventory Management] at the global store or product level. When the _Manage Stock_ option is enabled, [!DNL Inventory Management] automatically tracks product quantities available for the site through configured stocks and sources. Every feature and option begins tracking and reporting when enabled, without additional configuration.

Your business runs and inventory updates at the speed of sales. As customers shop, you receive exact, updated information for available stock per sales channel and source. Available Salable Quantities update per stock when customers add products to cart and complete purchases and when and you manage orders, create shipments, and issue refunds. Arrivals of new or transferred stock update to your sources, immediately available for online sales. Backorders complete up to specified thresholds without infinite orders or additional configurations. And you enter and complete partial or full shipments across one or more sources with recommendations, giving you complete control over order fulfillment and on-hand inventory.

>[!NOTE]
>
>By default, [!DNL Inventory Management] is enabled when installing or upgrading [!DNL Commerce]. Depending on your business needs, you may want to enable or disable the tracked [!DNL Inventory Management] within [!DNL Commerce].

How this setting works in single- and multi-source inventories:

- To use [!DNL Inventory Management], enable _[!UICONTROL Manage Stock]_.

- [!UICONTROL Manage Stock] settings at the product level configuration override the store configuration.

- To use Order Management or third-party services (such as ERP), disable [!UICONTROL Manage Stock].

- If the product level configuration uses the system default, the store configuration overrides.

With [!DNL Inventory Management] enabled, see the following to configure all settings:

- [Configuring Global Options](global-options.md) - Settings that affect your entire catalog, considered the system default settings.

- [Configuring Product Options](product-options.md) - Settings for a specific product that override global options.

## Enable or disable [!DNL Inventory Management]

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Inventory]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) _Product Stock Options_ and configure:

   ![Product Stock Options](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - To manage inventory and use all [!DNL Commerce] features, set **[!UICONTROL Manage Stock]** to `Yes` (default).

   - To disable [!DNL Inventory Management], deselect the **[!UICONTROL Use system value]** checkbox and set **[!UICONTROL Manage Stock]** to `No`.

1. When complete, click **[!UICONTROL Save Config]**.

## Manage stock for a store

See [Configure Global Options](global-options.md).

## Manage stock for a product

See [Configuring Product Options](product-options.md).
