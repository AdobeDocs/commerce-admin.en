---
title: Enable Inventory Management
description: Learn how to enable [!DNL Inventory Management] at the global store or product level.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
---
# Enable Inventory Management

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

## Enable or Disable Inventory Management

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
