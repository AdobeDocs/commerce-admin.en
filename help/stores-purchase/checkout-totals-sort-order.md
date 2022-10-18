---
title: Sort order for checkout totals
description: Learn about the displayed checkout total and how to configure the checkout totals sort order on the order summary.
---
# Sort order for checkout totals

During Order Review, the total appears at the bottom of the order, with any adjustments for discounts, shipping charges, store credit, and tax. The order of each item determines the sequence of the calculations, and is set in the configuration by a number that is assigned to each item. For example, the Subtotal is the first item in the section, and is assigned a value of 10. The Grand Total appears last, and is assigned a value of 100. All other items in the totals section are assigned a value between those values.

![Order Summary displays the checkout total](./assets/storefront-checkout-totals.png)<!-- zoom -->

## Configure the checkout totals sort order

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In left panel, expand the **Sales** section and choose **Sales** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Checkout Totals Sort Order** section.

   ![Checkout totals options numbered to determine the sort order](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png)<!-- zoom -->

   For a detailed description of each of these configuration settings, see [Checkout Totals Sort Order](https://docs.magento.com/user-guide/configuration/sales/sales.html#checkout-totals-sort-order) in the _Configuration Reference Guide_.

1. If the setting is for a specific store view, [choose the store view](https://docs.magento.com/user-guide/configuration/scope-change.html) where the configuration applies.

   When prompted, click **OK** to continue.

1. Change the number assigned to each item to determine its order in the _Totals_ section.

   The lower the value, the earlier its placement in the list. In the default configuration, the Subtotal (`10`) is the first and Grand total (`100`) is the last.

   If necessary, clear the **Use system value** checkbox to complete these changes.

1. Click **Save Config**.
