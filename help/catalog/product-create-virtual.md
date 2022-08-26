---
title: Virtual product
description: <placeholder>
---
# Virtual product

Virtual products, or digital goods, represent non-tangible items such as memberships, services, warranties, or subscriptions and digital downloads of books, music, videos, or other products. Virtual products can be sold individually or included as part of the [Grouped Product](product-create-grouped.md), [Configurable Product](product-create-configurable.md) or [Bundle Product](product-create-bundle.md) product types.

Aside from the absence of the Weight field, the process of creating a virtual product and a simple product is the same. The following instructions demonstrate the process of creating a virtual product using a [product template](attribute-sets.md), required fields, and basic settings. When you finish the basics, you can complete the other product settings as needed.

>[!NOTE]
>
>PayPal has deprecated support for the sale of digital goods through PayPal Express Checkout and recommends that you use either [PayPal Payments Standard](https://docs.magento.com/user-guide/payment/paypal-payments-standard.html) or any other PayPal payment gateway to process any order that includes virtual products.

![Virtual Product](./assets/product-virtual-membership.png)<!-- zoom -->

## Step 1: Choose the product type

1. On the _Admin_ sidebar, go to **Catalog** > **Products**.

1. On the _Add Product_ ( ![Menu arrow](../assets/icon-menu-down-arrow-red.png)<!-- {: width="25px"} --> ) menu at the upper-right corner, choose **Virtual Product**.

   ![Add Virtual Product](./assets/product-add-virtual.png)<!-- zoom -->

## Step 2: Choose the attribute set

To choose the [attribute set](attribute-sets.md) that is used as a template for the product, do one of the following:

- For **Search**, enter the name of the attribute set.

- In the list, choose the attribute set that you want to use.

The form is updated to reflect the change.

![Choose Attribute Set](./assets/product-create-choose-attribute-set.png)<!-- zoom -->

## Step 3: Complete the required settings

1. Enter the **Product Name**.

1. Accept the default **SKU** that is based on the product name or enter another.

1. Enter the product **Price**.

1. Because the product is not yet ready to publish, set **Enable Product** to `No`.

1. Click **Save** and continue.

   When the product is saved, the [Store View](introduction.md#product-scope) chooser appears in the upper-left corner.

1. Choose the **Store View** where the product is to be available.

   ![Choose Store View](./assets/product-create-store-view-choose.png)<!-- zoom -->

## Step 4: Complete the basic settings

1. Set **Tax Class** to one of the following:

   - `None`
   - `Taxable Goods`

1. Enter the **Quantity** of the product that is currently in stock and do the following:

   - Accept the default **Stock Status** setting of `In Stock`.

      Because a virtual product is not shipped, the **Weight** field is not used.

   - Accept the default **Visibility** setting of `Catalog, Search`.

   >[!NOTE]
   >
   >**Inventory Management:** If you enable [Inventory Management](../inventory-management/introduction.md), Single Source merchants set the quantity in this section. Multi Source merchants add sources and quantities in the Sources section. See the following _Assign Sources and Quantities (Inventory Management)_ section.

1. To assign **Categories** to the product, click the **Select…** box and do either of the following:

   - Choose an existing category:

      - Start typing in the box to find a match.

      - Select the checkbox of the category that is to be assigned.

   - Create a new category:

      - Click **New Category**.

      - Enter the **Category Name** and choose the **Parent Category** to determine its position in the menu structure.

      - Click **Create Category**.

      There might be additional individual attributes that describe the product. The selection varies by attribute set and you can complete them later.

{{$include /help/_includes/inventory-assign-sources.md}}

## Step 5: Complete the product information

Complete the information in the following sections as needed:

- [Content](product-content.md)
- [Images and Videos](product-images-and-video.md)
- [Search Engine Optimization](product-search-engine-optimization.md)
- [Related Products, Up-Sells, and Cross-Sells](related-products-up-sells-cross-sells.md)
- [Customizable Options](settings-advanced-custom-options.md)
- [Products in Websites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Gift Options](product-gift-options.md)

>[!NOTE]
>
>The _Is this downloadable product_ option is disabled by default. Enabling this feature for a virtual product makes the product [Downloadable](product-create-downloadable.md#downloadable-product).

## Step 6: Publish the product

1. If you are ready to publish the product in the catalog, set **Enable Product** to `Yes`.

1. Do one of the following:

   - **Method 1:** Save and Preview

      - At the upper-right corner, click **Save**.

      - To view the product in your store, choose **Customer View** on the _Admin_ ( ![Menu arrow](../assets/icon-menu-down-arrow-black.png) ) menu.

      The store opens in a new browser tab.

      ![Customer View](./assets/product-admin-customer-view.png)<!-- zoom -->

   - **Method 2:** Save and Close

      On the _Save_ (![Menu arrow](../assets/icon-menu-down-arrow-red.png)<!-- {: width="25px"} --> ) menu, choose **Save & Close**.

      ![Save & Close](./assets/product-edit-save-close.png)<!-- zoom -->

## Things to remember

- Virtual products are used for non-tangible products such as services, subscriptions, and warranties.

- Virtual products are much like simple products, but without weight.

- Shipping options do not appear during checkout unless there is a tangible product in the cart.
