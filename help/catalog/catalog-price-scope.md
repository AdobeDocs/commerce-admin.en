---
title: Price Scope
description: Learn about the scope used for product prices, which can be configured to apply at either the global or website level.
---
# Price Scope

The scope of the [base currency](../stores-purchase/currency-configuration.md) that is used for product prices can be configured to apply at either the global or website level. If applied to  the global level, the same price is used throughout the store hierarchy. If applied to the website level, the same product can be available at different prices from stores that are associated with different websites. By default, the scope of product pricing is global.

Different factors can affect the price of the same product in one location and not another. For example, there might be additional distribution costs for the product, and other considerations that impact the price of products sold in a specific store. The following diagram shows a multisite installation with the base currency set to the website level. The stores and store views associated with each website reflect the product pricing that is set at the website level.

![B2B for Adobe Commerce](../assets/b2b.svg) If you are using shared catalogs, also refer to [Set Pricing and Structure](../b2b/catalog-shared-pricing-structure.md) in the _B2B for Adobe Commerce Guide_.

![Price scope diagram](./assets/catalog-price-scope.svg)<!-- {: "width=550px"} -->

## Configure price scope

1. On the _Admin_ menu, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. Scroll down to the **[!UICONTROL Price]** section and set **[!UICONTROL Catalog Price Scope]** to one of the following:

   - `Global`
   - `Website`

   The scope setting that you choose appears below price fields in your catalog.

   ![Catalog price scope](./assets/catalog-price.png)<!-- zoom -->

1. When complete, click **[!UICONTROL Save Config]**.

## Use scope to set up product prices

Commerce does not allow setting a product price for each store. But you can change the price per website:

1. On the _Admin_ menu, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. In the **[!UICONTROL Price]** tab, set price scope to `Website` instead of global.

1. Set the price by opening the product edit page, selecting the scope on the upper left, and then entering a new price per website.
