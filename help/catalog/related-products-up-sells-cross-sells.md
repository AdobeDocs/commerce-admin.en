---
title: Product settings - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]
description: For a product, the [!UICONTROL Related Products, Up-Sells, and Cross-Sells] settings define simple promotional blocks on the product page that highlight a selection of additional products.
exl-id: 5bd65fad-4e55-40db-8702-10c366261565
feature: Catalogs, Products, Page Content
---
# Product settings - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]

Use the _[!UICONTROL Related Products, Up-Sells, and Cross-Sells]_ section to set up simple promotional blocks that present a selection of additional products that might be of interest to the customer. For more information, see [Product Relationships](../merchandising-promotions/product-relationships.md).

![Related Products, Up-Sells, and Cross-Sells](./assets/product-related-up-sell-cross-sell.png){width="600" zoomable="yes"}

Every block consists of a list of products which belong to a specific option.

|Field|Description|    
|--- |--- |
|[!UICONTROL ID]|A unique numeric identifier that is assigned to product entity.|
|[!UICONTROL Thumbnail]|Product thumbnail image.|
|[!UICONTROL Name]|The name of the product.|
|[!UICONTROL Status]|Indicates the product status. Options: `Enabled` / `Disabled`. Disabled products are not displayed in the blocks on the frontend.|
|[!UICONTROL Attribute Set]|The name of the attribute set that is used as a template for the product.|
|[!UICONTROL SKU]|The unique Stock Keeping Unit that is assigned to the product.|
|[!UICONTROL Price]|The unit price of the product.|
|[!UICONTROL Action]|Options: `Remove`. Removes a product from the block.|

{style="table-layout:auto"}

>[!TIP]
>
>![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) **Product Recommendations powered by Adobe Sensei** simplifies the process of defining product relationships by using artificial intelligence and machine-learning algorithms to perform a deep analysis of aggregated visitor data. This data, when combined with your Adobe Commerce catalog, results in highly engaging, relevant, and personalized experiences for the shopper.
><br/>
>For more information about using this Adobe-developed extension as an alternative to manually configured product recommendations and up-sells, see the _[Product Recommendations Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)_.

## Related Products

Related products are meant to be purchased in addition to the item the customer is viewing. The customer can place the item in the shopping cart by simply clicking the checkbox. The placement of the _Related Products_ block varies according to defined theme and page layout. In the example below, the _Related Products_ block appears at the bottom of the _Product View_ page. With a two-column layout, the _Related Products_ block often appears in the right sidebar.

![Related Products](./assets/storefront-product-related-products.png){width="600" zoomable="yes"}

To set up related products:

1. Open the product in edit mode.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** section.

1. Click **[!UICONTROL Add Related Products]**.

1. Use the [filter controls](../getting-started/admin-grid-controls.md) to find the products that you want.

1. In the list, select the checkbox of any product you want to feature as a related product.

   ![Related Products](./assets/products-related-add.png){width="600" zoomable="yes"}

1. When complete, click **[!UICONTROL Add Selected Products]**.

## Up-sells

Up-sell products are items that your customer might prefer instead of the product currently considered. An item offered as an up sell might be of a higher quality, more popular, or have better profit margin. Up-sell products appear on the product page under a heading such as _You may also be interested in the following products_.

![Up-Sell](./assets/storefront-product-upsell.png){width="600" zoomable="yes"}

To select up-sell products:

1. Open the product in edit mode.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** section.

1. Click **[!UICONTROL Add Up-Sell Products]**.  

1. Use the [filter controls](../getting-started/admin-grid-controls.md) to find the products that you want.

1. In the list, select the checkbox of any product you want to feature as an up-sell product.

   ![Up-Sell Products](./assets/product-up-sell-add.png){width="600" zoomable="yes"}

1. When complete, click **[!UICONTROL Add Selected Products]**.

## Cross-sells

Cross-sell items are similar to impulse purchases positioned next to the cash register in the checkout line. Products offered as a cross-sell appear on the shopping cart page, just before the customer begins the checkout process.

>[!NOTE]
>
>To show or hide cross-sell items per store view, see the [Checkout > Shopping Cart](../configuration-reference/sales/checkout.md) option called _[!UICONTROL Show Cross-sell Items]_ in the Shopping Cart. You may want to hide cross-sells during specific sales or for A/B testing in a store view.

![Cross-sells in shopping cart](./assets/storefront-cart-cross-sells.png){width="600" zoomable="yes"}

**_To select cross-sell products:_**

1. Open the product in edit mode.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** section.

1. Click **[!UICONTROL Add Cross-Sell Products]**.

1. Use the [filter controls](../getting-started/admin-grid-controls.md) to find the products that you want.

1. In the list, select the checkbox of any product you want to feature as a cross-sell product.

   ![Cross-sell Products](./assets/product-cross-sell-add.png){width="600" zoomable="yes"}

1. When complete, click **[!UICONTROL Add Selected Products]**.
