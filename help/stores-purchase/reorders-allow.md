---
title: Allow reorders
description: <Add description here>
---
# Allow reorders

When enabled, reorders can be made directly from the customer account or from the original order in the _Admin_. Reorders are enabled by default.

![Customer reorder link in the Admin](./assets/customer-reorder.png)<!-- zoom -->

## Criteria for reorder to be enabled for an order

- The _Allow Reorder_ configuration option must be enabled.

- If order is in Hold or in Payment Review status, the reorder option is disabled.

- If any of the items in the order is unavailable, out of stock, or disabled, the reorder option is disabled on the _Storefront_.

- An _Admin_ can reorder even if any of the items are out of stock or disabled.

## Configure to allow customer reorders

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Sales** and choose **Sales** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Reorder** section.

   ![Reorder options](../configuration-reference/sales/assets/sales-reorder.png)<!-- zoom -->

1. Set **Allow Reorder** to `Yes`. 

   This setting enables reorder functionality from the customer account on the storefront or orders list in the Admin.

1. Click **Save Config**.

## Reorder from the storefront

A customer can initiate the reorder functionality for a specific order from two pages:

- _My Orders_ page

- _Order View_ page

### My Orders

The _Reorder_ button is always displayed in the list with Orders (even if all products from the order are not available for reorder).

![Example storefront - My Orders page](./assets/my-order-page-view.png)<!-- zoom -->

**Case 1.** All products from the order are **available** for reorder

User is redirected to the cart, and all products are added to the cart

![Shopping cart](./assets/shopping-cart-page.png)<!-- zoom -->

**Case 2.** Some/all products from the order are **not available** for reorder

>[!NOTE]
>
>It is possible to reorder `Not Visible Individually` products.

The _Reorder_ button does not appear on the _My Orders_ and _View Order_ pages.

![My Orders page 1](./assets/my-orders-view-page1.png)<!-- zoom -->

### Order view page

**Case 1.** All products from the order are available for reorder

User is redirected to the cart, and all products are added to the cart

**Case 2.** Some/all products from the order are **not available** for reorder

>[!NOTE]
>
>It is possible to reorder `Not Visible Individually` products.

The _Reorder_ button does not appear on the _My Orders_ and _View Order_ pages.

![Order details page](./assets/order-view-page.png)<!-- zoom -->

### Cart is not empty

If the cart is not empty and the user clicks **Reorder** (from the _My Orders_  or _Order View_ page), the existing products remain in the cart with the added reorder products.

![Reorder items](./assets/shopping-cart-view1.png)<!-- zoom -->

## Reorder from the Admin

1. On the _Admin_ sidebar, go to **Sales** > **Orders**.

1. Locate the order and open in **View** mode.

1. Click **Reorder** which is displayed in the top button bar.

   ![Order details in the Admin](./assets/order-view-admin.png)<!-- zoom -->

   After you click **Reorder**, the _Create New Order_ page opens with reorder products.

   ![Create reorder](./assets/create-reorder-page.png)<!-- zoom -->

1. Fill in all required fields as needed.

1. To submit the order, click **Submit Order**.
