---
title: Price scope
description: Learn about the scope used for product prices, which can be configured to apply at either the global or website level.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/4tNRviXPzBubIpyAn9vgUs8BaILjJ6BEdV4yj5ngz6Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Price scope

The scope of the [base currency](../stores-purchase/currency-configuration.md) that is used for product prices can be configured to apply at either the global or website level. If applied to  the global level, the same price is used throughout the store hierarchy. If applied to the website level, the same product can be available at different prices from stores that are associated with different websites. By default, the scope of product pricing is global.

Different factors can affect the price of the same product in one location and not another. For example, there might be additional distribution costs for the product, and other considerations that impact the price of products sold in a specific store. The following diagram shows a multisite installation with the base currency set to the website level. The stores and store views associated with each website reflect the product pricing that is set at the website level.

![Adobe Commerce B2B](../assets/b2b.svg) If you are using shared catalogs, also refer to [Set shared catalog pricing and structure](../b2b/catalog-shared-pricing-structure.md) in the _Adobe Commerce B2B Guide_.

![Price scope diagram](./assets/catalog-price-scope.svg){width="550"}

## Configure price scope

1. On the _Admin_ menu, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. Scroll down to the **[!UICONTROL Price]** section and set **[!UICONTROL Catalog Price Scope]** to one of the following:

   - `Global`
   - `Website`

   The scope setting that you choose appears below price fields in your catalog.

   ![Catalog price scope](./assets/catalog-price.png){width="600" zoomable="yes"}

1. When complete, click **[!UICONTROL Save Config]**.

## Use scope to set up product prices

Commerce does not allow setting a product price for each store. But you can change the price per website:

1. On the _Admin_ menu, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. In the **[!UICONTROL Price]** tab, set price scope to `Website` instead of `Global`.

1. Set the price by opening the product edit page, selecting the scope on the upper left, and then entering a new price per website.

In rare cases when price scope is set to `Global`, the Commerce database can still have different prices on the website level. This can happen as a result of synchronization issues outside of Commerce. In these cases, the Merchant must perform a price cleanup on the store level and run a Catalog Sync with Commerce Services.