---
title: Manage a shopping cart
description: Learn how to assist a customer with their shopping cart directly from the Admin.
exl-id: beb41dfa-ef87-4065-96fd-0649a5c4c21c
feature: Customer Service, Shopping Cart
---
# Manage a shopping cart

{{ee-feature}}

To begin an assisted shopping session, the customer must be logged into their account from the storefront to make the information available. If the customer does not have an account, you can [create one](../customers/account-create.md).

![Shopping Cart in in the customer account](./assets/customer-account-manage-cart-items.png){width="600" zoomable="yes"}

## Actions control

|Option|Description|
|--- |--- |
|[!UICONTROL Remove]|Removes items from the current shopping cart|
|[!UICONTROL Move to Wish List]|Moves items to the selected customer wishlist|

{style="table-layout:auto"}

## Control buttons

|Button|Description|
|--- |--- |
|[!UICONTROL Clear my shopping cart]|Removes all items from the cart.|
|[!UICONTROL Update Items and Quantities|]Enter the required quantity in the **[!UICONTROL Qty]** field and update the number of items in the cart.|
|[!UICONTROL Add selections to my cart]|Adds products from all sections to the cart.|

{style="table-layout:auto"}

## Verify that the customer is logged in

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Now Online]**.

   All visitors to the store and logged in customers appear in the list.

   ![Customers Now Online](./assets/customers-now-online.png){width="700" zoomable="yes"}

## Offer assisted shopping

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. In the list, open the customer record in edit mode.

   >[!TIP]
   >
   >To find the customer record in a hurry, use the [Filters](../getting-started/admin-grid-controls.md) control.

   In the customer profile under _[!UICONTROL Personal Information]_, the _[!UICONTROL Last Logged In]_ date and time shows that the customer is online.

   ![Customer profile of an online customer](./assets/customer-account-manage-cart.png){width="600" zoomable="yes"}

1. To enter assisted shopping mode, click **[!UICONTROL Manage Shopping Cart]** in the top button bar.

   ![Assisted shopping mode](./assets/customer-manage-shopping-cart.png){width="600" zoomable="yes"}

## Add products to cart by attribute

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Products]** section.

1. Find a product using any of the filters at the top of each column.

1. Click **[!UICONTROL Search]**.

1. Use one of the following series of steps according to the product type:

### Add a simple product

1. Click the product that you want to order.

   This action selects the record and sets **[!UICONTROL Quantity]** to the default value of `1`.

1. If necessary, update the quantity ordered.

1. On the left above the grid, click **[!UICONTROL Add selections to my cart]**.

   ![Add Product to Cart](./assets/customer-account-manage-cart-order-products.png){width="600" zoomable="yes"}

   The line item is added to the shopping cart at the top of the page.

   ![Cart Updated](./assets/customer-account-manage-cart-update-cart.png){width="600" zoomable="yes"}

### Add a product with configuration

There are three types of products that must be configured before adding to the cart: `Bundle Product`, `Configurable Product`, and `Grouped Product`.

1. In the grid, click **[!UICONTROL Configure]** next to the product name.

   ![Configure the product](./assets/customer-account-manage-cart-order-configurable-product.png){width="600" zoomable="yes"}

1. In the _Associated Products_ dialog, choose each product option to describe the item to be ordered, enter the **[!UICONTROL Quantity]**, and click **[!UICONTROL OK]**.

   The product is selected with a checkmark and the quantity ordered appears in the grid.

1. To add the product to the cart, click **[!UICONTROL Add selections to my cart]**.

   ![Configurable product in the cart](./assets/customer-account-manage-cart-order-configurable-product-cart.png){width="600" zoomable="yes"}

1. Update product options in the cart if needed:

   - Click **[!UICONTROL Configure]**.

   - Update the options and then click **[!UICONTROL OK]**.

## Add product by SKU

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Add to Shopping Cart by SKU]** section.

1. Add products individually by **[!UICONTROL SKU]** or add products by uploading a CSV file.

### Add items individually by SKU

1. Enter the **[!UICONTROL SKU]** and **[!UICONTROL Qty]** of the item to be ordered.

1. To order another product, click **[!UICONTROL Add another]**.

   ![Add Products by SKU](./assets/customer-account-manage-cart-order-product-by-sku.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Add selections to my cart]**.

1. If the item is a configurable product, choose the product options when prompted, and then click **[!UICONTROL Add to Shopping Cart]**.

### Add products by uploading a CSV file

1. Prepare a [csv file](../systems/data-csv.md) with the items to be added to the cart.

   The file must contain only two columns, with `sku` and `qty` in the header.

1. Upload the prepared file:

   - Click **[!UICONTROL Choose File]**.

   - Select the file to be uploaded from your directory.

## Transfer an item

You can transfer items to the cart from a customer's wish list, and recently viewed, compared, or ordered items. The number of items in each section appears in parentheses after the section header.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) one of the following sections:

   - [!UICONTROL Wish List]
   - [!UICONTROL Products in the Comparison List]
   - [!UICONTROL Recently Compared Products]
   - [!UICONTROL Recently Viewed Products]
   - [!UICONTROL Last Ordered Items]

1. In the grid, select each product to be ordered and enter the **[!UICONTROL Quantity]**.

1. To enter the options for a configurable product, click **[!UICONTROL Configure]** and set the product options as needed.

1. Click **[!UICONTROL Add selections to my cart]**.

1. Apply one or more coupon codes if available:

   - For **[!UICONTROL Apply Coupon Code]**, enter a valid coupon code.

   - Click the _Apply_ ( ![Arrow icon](../assets/icon-apply-arrow.png) ) arrow.

1. Adjust the quantity ordered as needed:

   - In the **[!UICONTROL Qty]** column of the product to be adjusted, enter the correct amount.

   - Click **[!UICONTROL Update Items and Quantities]**.

## Create the order

1. Click **[!UICONTROL Create Order]**.

   The _[!UICONTROL Create New Order]_ page shows the items in the cart, followed by the shipping and payment information.

1. Complete the shipping and payment information.

1. Click **[!UICONTROL Submit Order]**.

To learn more, see [Create an order](customer-account-create-order.md).

## Remove all items from a cart

Removing all items from a customer's cart in assisted shopping mode is useful if the customer wants to start over, has added incorrect items, or needs to clear their cart before placing a new order. This helps ensure the cart only contains the products the customer actually wants to purchase.

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. In the list, open the customer record in edit mode.

1. Click **[!UICONTROL Manage Shopping Cart]** in the top button bar.

1. Click **[!UICONTROL Clear my shopping cart]**.

   ![Clear my shopping cart](./assets/customer-manage-shopping-cart-clear.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL OK]** when prompted to confirm the action.
