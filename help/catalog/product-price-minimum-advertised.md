---
title: Minimum advertised price
description: Learn how to use the minimum advertised price (MAP) feature to remain in compliance with the manufacturer's requirements with special pricing.
exl-id: ccd44cfe-3967-4d82-b5b2-3f92701d152e
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/DRNm0PPX81W4jzLnu7ALhJ1lQZYUpTcO6ojp1E50vto
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
    internal-label: Compliance
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
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
# Minimum advertised price

Merchants are sometimes prohibited from displaying a price that is lower than the manufacturer's suggested retail price (MSRP). Minimum Advertised Price (MAP) gives you the ability to remain in compliance with the manufacturer's requirements while offering your customers a better price. Because requirements differ from one manufacturer to another, you can configure your store to prevent the display of your actual price on pages where it is not allowed.

The MAP feature adds a dedicated _Click for Price_ link instead of the regular product price. If the price in your store is below the minimum set price for that product, there are two ways that the pricing information can be handled on the storefront. The first way is that the price is not displayed. If the buyer clicks the _Click for Price_ button, only then does the actual price at which you are selling the product become visible. The second way is that the list/market price is displayed with a strikethrough to emphasize that your price is lower. 

Also, the MAP feature allows you to suggest some improvements. For example, when a customer adds such a product to their cart, they are not redirected to the cart, and instead there are offers displayed that allow the buyer to:

- Remove an item from the cart (can be done if the buyer just wants to clarify the price and has not yet made a purchase decision)

- Leave it in their shopping cart and keep shopping

- Proceed to checkout

## MAP logic

Some products have prices that depend on a selected option, such as custom options or simple products with their own SKUs and stock management). For these products, the following logic is applied, according to the product type and price setting. The actual price is used by order management, customer management tools, and reports.

## Using MAP with product types

|Product type|Description|
|--- |--- |
|[Simple](product-create-simple.md), [Virtual](product-create-virtual.md)|The actual price does not automatically appear on catalog list and product pages, but is included only according to the [!UICONTROL Display Actual Price] setting. Custom option prices appear normally.|
|[Grouped](product-create-grouped.md)|The prices of associated simple products do not automatically appear on catalog list and product pages, but are included only according to the [!UICONTROL Display Actual Price] setting.|
|[Configurable](product-create-configurable.md)|The actual price does not automatically appear on catalog list and product pages, but is included only according to the [!UICONTROL Display Actual Price] setting. Option prices appear normally.|
|[Bundle](product-create-bundle.md) (with fixed price)|The actual price does not automatically appear on catalog pages, but is included only according to the [!UICONTROL Display Actual Price] setting. The prices of bundle items appear normally. MAP is not available for bundle products with dynamic pricing.|
|[Downloadable](product-create-downloadable.md)|The actual price does not automatically appear on  catalog list and product pages, but is included only according to the [!UICONTROL Display Actual Price] setting. The price associated with each download link appears normally.|

{style="table-layout:auto"}

## Using MAP with price settings

| Price setting | Description |
|--- |--- |
| Main Price | When MAP is applied to the main price, the prices of options, bundle items, and associated products (which add or subtract from the main price) appear normally. |
| Associated Product Price | If a product does not have a main price, and its price is derived from the associated product prices (such as in a grouped product), the MAP settings of the associated products are applied. |
| [MSRP](product-price-minimum-advertised.md) | If a product in the cart has the Manufacturer's Suggested Retail Price (MSRP) specified, the price is not crossed-out. |
| [Tier Price](product-price-tier.md) | If tier pricing is set, the tier pricing message is not displayed in the catalog. On the product page, a notification is displayed that indicates that the price can be lower when ordering more than a certain quantity, but the discount is displayed in percentages only. For associated products of a grouped product, the discounts are not displayed on the product page. The tier price appears according to the Display Actual Price setting. |
| [Special Price](product-price-special.md) | If the Special price is specified, the special price is displayed according to the Display Actual Price setting. |

## MAP configuration

The Minimum Advertised Price (MAP) feature is not enabled by default. If you want to add this capability to your store, you must enable it and configure the MAP settings for your products. The MAP settings can be applied to all products in your catalog or configured for specific products. When MAP is enabled globally, all product prices in the storefront are hidden from view. There are various configuration options that you can use to remain in compliance with the terms of your agreement with the manufacturer, while still offering your customers a better price.

![Actual Price Appears "On Gesture"](./assets/storefront-msrp-on-gesture.png){width="700" zoomable="yes"}

On the global level, you can enable or disable MAP, apply it to all products, define how the actual price is displayed. You can also edit the text of the related messages and information tips that appear in the store.

When MAP is enabled, the product-level MAP settings become available. You can apply MAP to an individual product by entering the MSRP and choosing how you want the actual price to appear in the store. Product-level MAP settings override the global MAP settings.

![Click for Price](./assets/storefront-price-map.png){width="700" zoomable="yes"}

### Step 1: Enable MAP for the store view

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. If applicable, set **[!UICONTROL Store View]** at the upper-right corner to the view where the configuration applies.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Sales]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the _[!UICONTROL Minimum Advertised Price]_ section.

1. If necessary, set **Enable MAP** to `Yes`.

   ![MAP configuration](./assets/sales-minimum-advertised-price.png){width="600" zoomable="yes"}
   
   For a detailed list of these configuration options, see [_Minimum Advertised Price_](../configuration-reference/sales/sales.md#minimum-advertised-price) in the _Configuration Reference_.

### Step 2: Configure the MAP settings

Use one of the following methods to configure the MAP settings:

#### Method 1: Configure MAP for all products

1. To determine when and where you want the actual price to be visible to customers, do the following:

   - To change the default value, deselect the **[!UICONTROL Use system value]** checkbox.

   - Set **Display Actual Price** to one of the following:
      - `In Cart`
      - `Before Order Confirmation`
      - `On Gesture (on click)`

1. Enter the text that you want to appear in the **[!UICONTROL Default Popup Text Message]**.

1. Enter any additional explanation that you want to appear in the **[!UICONTROL Default "What's This" Text Message]**.

1. When complete, click **[!UICONTROL Save Config]**.

#### Method 2: Configure MAP for a single product

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Inventory]** > **[!UICONTROL Products]**.

1. Open the product in **[!UICONTROL Edit]** mode.

1. In the left panel, expand **[!UICONTROL Advanced Settings]** and choose **[!UICONTROL Advanced Pricing]**.

   >[!NOTE]
   >
   >The [!UICONTROL Manufacturer's Suggested Retail Price] and [!UICONTROL Display Actual Price] fields appear only when [Minimum Advertised Price](../configuration-reference/sales/sales.md#minimum-advertised-price) is enabled in the configuration.

1. Enter the **[!UICONTROL Manufacturer's Suggested Retail Price]** (MSRP).

   In this example, the product price is $54.00, and the MSRP is 59.95.

   ![Manufacturer's Suggested Retail Price](./assets/product-price-msrp.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Display Actual Price]** to one of the following:

   - `Use config` - (Default) Applies the display settings as [configured](../configuration-reference/sales/sales.md#minimum-advertised-price) for the store. |
   - `On Gesture` - Displays the actual product price in a popup when the customer clicks the _Click for price_ or _What's this?_ link.
   - `In Cart` - Displays the actual product price in the shopping cart.
   - `Before Order Confirmation` - Displays the actual product price at the end of the checkout process, just before the order is confirmed.

1. When complete, click **[!UICONTROL Done]** and then **[!UICONTROL Save]**.
