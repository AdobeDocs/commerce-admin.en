---
title: Allow cancel order
description: Learn how to provide cancel capabilities for your customers.
feature: Orders, Storefront 
---
# Allow cancel order

When enabled, you can cancel an order directly from the customer's account. Cancel is disabled by default.

## Criteria for cancellation to be enabled for an order

- The _Allow Cancel Order_ configuration option must be enabled.

- If order is in `Hold`, `Canceled`, `Complete` or `Closed` status, the cancel option is disabled on the storefront.

- If any of the items in the order have shipped, the cancel option is disabled on the storefront.

- If there is some item paid, the cancel option is enabled and the refund is created for that item.

- If order is in `Pending` or `Processing` status, the cancel option is enabled on the storefront.

## Configure to allow customer cancellation and customize the cancellation reasons

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Sales]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Order cancellation]** section.

   ![Order Cancellation options](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Order cancellation through GraphQL]** to `Yes`. 

   This setting enables cancel functionality from the customer account on the storefront.

1. In the **[!UICONTROL Order Order cancellation reasons]** it is possible to add, delete or modify any cancellation reason.

   This setting allows to set the cancellation reasons that are going to be displayed when the customer try to cancel from the storefront.
   This should have almost one reason set.

1. Click **[!UICONTROL Save Config]**.

## Cancel from the storefront

A customer can initiate the cancel functionality for a specific order from three pages:

- _My Orders_ page

- _Order View_ page

- _My Account_ page

### My Orders

The _Cancel Order_ button is displayed in the list with Orders if the order can be canceled.

![Example storefront - My Orders page](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Order view page

The _Cancel Order_ button is displayed in the View Order page if the order can be canceled.

![Order details page](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### My Account

The _Cancel Order_ button is displayed in the My Account page, in the Recent Orders section if the order can be canceled.

![My Account page](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}


