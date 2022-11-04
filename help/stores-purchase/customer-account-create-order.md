---
title: Create an order
description: Learn how to create an order for a customer in the Commerce Admin.
---
# Create an order

For registered customers who need assistance, you can create an entire order directly from the Admin. The Create New Order form includes all the information that is needed to complete the normal checkout process, with activity summaries from the customer's account dashboard.

![Create an order for a customer](./assets/create-new-order.png)<!-- zoom -->

## Step 1: Create an order

1. On the _Admin_ sidebar, click **[!UICONTROL Customers]**.

1. Find the customer in the grid.

1. In the _Action_ column, click **[!UICONTROL Edit]**.

1. In the workspace header, click **[!UICONTROL Create Order]**.

   ![Workspace header](./assets/order-create-buttons.png)<!-- zoom -->

   You can also create an order in the [Order workspace](orders.md#orders-workspace) by clicking **[!UICONTROL Create New Order]**.

## Step 2: Add products

If your store has multiple views, choose the store view where the order is to be placed.

### Add products from the Customer's Activities sidebar

You can transfer items to the cart from a customer's wish list, and recently viewed, compared, or ordered items.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) one of the following sections:

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. Select the checkbox of each product in the left panel.

1. Scroll down and click **[!UICONTROL Update Changes]**.

   The item appears in the order form.

   ![Add to Cart](./assets/create-order-add-wishlist.png)<!-- zoom -->

### Add products from the catalog

1. Click **[!UICONTROL Add Products]**.

   ![Add Products](./assets/account-add-wishlist-product.png)<!-- zoom -->

1. In the grid, select the checkbox of each product to be added to the cart and enter the **[!UICONTROL Qty]** to be purchased.

   ![Select Products](./assets/create-order-from-catalog.png)<!-- zoom -->

   >[!NOTE]
   >
   >Product selection grid always shows regular base prices for products, without discounts and any cart or group price rules applied. Final product price is calculated only when product is added to an order/cart.

1. Configure available product options:

   - Click **[!UICONTROL Configure]**.

   - Complete the options as needed.

   - Click **[!UICONTROL OK]**.

   - Click **[!UICONTROL Add Selected Product(s) to Order]** to update the cart.

1. If a product is configured for [gift options](../catalog/product-gift-options.md), set the options as needed.

1. Override the price of an item if necessary:

   - Select the **[!UICONTROL Custom Price]** checkbox and enter the new price in the box below.

   - To update the cart totals, click **[!UICONTROL Update Items and Quantities]**.

   ![Custom Price](./assets/create-order-custom-price.png)<!-- zoom -->

1. Complete the following sections as needed for the order:

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]

>[!NOTE]
>
>See the [Payment Services Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/create-order.html) for more information about payment methods to support this functionality when the Payment Services extension is installed and configured.

## Step 3: Submit the order

Click **[!UICONTROL Submit Order]**.

A confirmation is sent to the customer and the customer can view the order details from their account.

![Order Created](./assets/create-order-submitted.png)<!-- zoom -->
