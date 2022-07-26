---
title: Grouped product
description: <placeholder>
---
# Grouped product

A grouped product consists of simple standalone products that are presented as a group. You can offer variations of a single product or group them by season or theme. Presenting a grouped product can create an incentive for customers to purchase additional items. A grouped product provides an easy way to offer variations of a product and list them all on the same page.

For example, you might sell open stock flatware and list every type of utensil that is used in a formal place setting. Some might order multiple salad forks, fish forks, dinner forks, dinner knives, fish knives, butter knives, soup spoons, and dessert spoons. Other customers might order a simple fork, knife, and spoon. Customers can order as many of each item as they want.

Although they are presented as a group, each product in the group is purchased as a separate item. In the shopping cart, each item and the quantity purchased appears a separate line item.

The following instructions demonstrate the process of creating a grouped product using a [product template](attribute-sets.md), required fields, and basic settings. Each required field is marked with a red asterisk (`*`). When you finish the basics, you can complete the other product settings as needed.

![Grouped Product](./assets/product-grouped.png)<!-- zoom -->

## Step 1: Choose the product type

1. On the _Admin_ sidebar, go to **Catalog** > **Products**.

1. On the _Add Product_ ( ![Menu arrow](../assets/icon-menu-down-arrow-red.png)<!-- {: width="25px"} --> ) menu at the upper-right corner, choose **Grouped Product**.

   ![Add Grouped Product](./assets/product-add-grouped.png)<!-- zoom -->

## Step 2: Choose the attribute set

To choose the [attribute set](attribute-sets.md) that is used as a template for the product, do one of the following:

- To search, enter the name of the **Attribute Set**.
- In the list, choose the **Attribute Set** that you want to use.

The form is updated to reflect the change.

![Choose Template](./assets/product-grouped-create-choose-attribute-set.png)<!-- zoom -->

If the needed attributes do not exist, you can add new attributes while creating a product:

- In the upper-right corner, click **Add Attribute**.
- Define a new attribute (see [Adding an Attribute to a Product](product-attributes-add.md)).

   ![New Attribute](./assets/product-attribute-add-select.png)<!-- zoom -->

To add an existing attribute to the product, use the [filter controls](https://docs.magento.com/user-guide/stores/admin-grid-controls.html) to find the attribute in the grid and do the following:

- Select the checkbox in the first column of each attribute to be added.
- Click **Add Selected**.

## Step 3: Complete the required settings

1. Enter the **Product Name**.

1. Accept the default **SKU** that is based on the product name or enter another.

   Take note that the **Quantity** field is not available because the value is derived from the individual products that make up the group.

1. Because the product is not yet ready to publish, set **Enable Product** to `No` ( ![Toggle no](../assets/toggle-no.png) ).

1. Click **Save** and continue.

   When the product is saved, the product name appears at the top of the page, and the [Store View](introduction.md#product-scope) chooser appears in the upper-left corner.

1. Choose the **Store View** where the product is to be available.

   ![Choose Store View](./assets/product-grouped-create-store-view-choose.png)<!-- zoom -->

## Step 4: Complete the basic settings

1. Accept the **Stock Status** setting of `In Stock`.

1. To assign **Categories** to the product, click the **Select…** box and do either of the following:

   **Choose an existing category:**

   - Start typing in the box to find a match.

   - Select the checkbox of the category that is to be assigned.

   **Create a new category:**

   - Click **New Category**.

   - Enter the **Category Name** and choose the **Parent Category** to determine its position in the menu structure.

   - Click **Create Category**.

1. Accept the **Visibility** settings of `Catalog, Search`.

1. To feature the product in the [list of new products](../content-design/widget-new-products-list.md), choose the **Set Product as New** **From** and **To** dates on the calendar.

1. Choose the **Country of Manufacture**.

   There might be additional individual attributes that describe the product. The selection varies attribute set, and you can complete them later.

   ![Grouped Product Details](./assets/product-grouped-details.png)<!-- zoom -->

## Step 5: Add products to the group

1. Scroll down to the **Grouped Products** section and click **Add Products to Group**.

   ![Grouped Products](./assets/product-grouped-products.png)<!-- zoom -->

1. If necessary, use the [filters](https://docs.magento.com/user-guide/stores/admin-grid-controls.html) to find the products that you want to include in the group.

1. In the list, select the checkbox of each item that you want to include in the group.

   >[!NOTE]
   >
   >Only simple, downloadable, and virtual products with no configurable options can be grouped child products. Other product types do not appear in the selection list.

   ![Add Selected Products](./assets/product-grouped-add-products.png)<!-- zoom -->

1. Click **Add Selected Products** to add them to the group.

   The selected products appear in the _Grouped Products_ section.

   For Multi Source merchants with Inventory Management, the grid includes a **Quantity per Source** column with each assigned source and inventory stock amount.

   ![Products in Group](./assets/product-grouped-grouped-products-section.png)<!-- zoom -->

1. Enter a **Default Quantity** for any of the items.

1. To change the order of the products, grab the **Change Order** icon ( ![Position controller](../assets/icon-sort-order.png) ) in the first column and drag the product to the new position in the list.

1. To remove a product from the group, click **Remove**.

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

## Step 6: Publish the product

1. If you are ready to publish the product in the catalog, set **Enable Product** to `Yes`.

1. Do one of the following:

   **Method 1:**: Save and Preview

   - In the upper-right corner, click **Save**.

   - To view the product in your store, choose **Customer View** on the _Admin_ ( ![Menu arrow](../assets/icon-menu-down-arrow-black.png) ) menu.

      The store opens in a new browser tab.

      ![Customer View](./assets/product-admin-customer-view.png)<!-- zoom -->

   **Method 2:** Save and Close

   - On the _Save_ (![Menu arrow](../assets/icon-menu-down-arrow-red.png)<!-- {: width="25px"} --> ) menu, choose **Save & Close**.

   ![Save & Close](./assets/product-edit-save-close.png)<!-- zoom -->

## Step 7: Configure the cart thumbnails (optional)

If you have a different image for each product in the group, you can set the configuration to use the correct image for the shopping cart thumbnail.

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Sales** and choose **Checkout**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Shopping Cart**.

1. Set **Grouped Product Image** to `Product Thumbnail Itself`.

   If necessary, deselect the **Use system value** checkbox to set this option.

1. Click **Save Config**.

   ![Shopping Cart](./assets/cart-grouped-product.png)<!-- zoom -->
   
   See also [Shopping Cart](https://docs.magento.com/user-guide/configuration/sales/checkout.html)

## Things to remember

- A grouped product is essentially a collection of simple associated products.

- Grouped child products can be simple, downloadable, or virtual products **without custom options**.

- Each item purchased appears individually in the shopping cart, rather than as part of the group.

- The thumbnail image in the shopping cart can be set to display the image from the grouped parent product or associated product.
