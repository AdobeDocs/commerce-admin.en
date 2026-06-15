---
title: Allow cancel order
description: Learn how to provide cancel capabilities for your customers.
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
TQID: https://experienceleague.adobe.com/a0jMKgF4a0qXUe15oT2syai6-kGSegU1BX56PO9SSKs
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Allow cancel order

When enabled, you can cancel an order directly from the customer's account. Cancel is disabled by default.

## Criteria for cancellation to be enabled for an order

- The _Allow Cancel Order_ configuration option must be enabled.

- If order is in `Hold`, `Canceled`, `Complete`, or `Closed` status, the cancel option is disabled on the storefront.

- If any of the items in the order have shipped, the cancel option is disabled on the storefront.

- If there is some item paid, the cancel option is enabled and the refund is created for that item.

- If order is in `Pending` or `Processing` status, the cancel option is enabled on the storefront.

## Configure to allow customer cancellation and customize the cancellation reasons

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and select **[!UICONTROL Sales]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Order cancellation]** section.

   ![Order Cancellation options](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Order cancellation through GraphQL]** to `Yes`. 

   This setting enables cancel functionality from the customer account on the storefront.

1. In the **[!UICONTROL Order Order cancellation reasons]** you can add, delete, or modify any cancellation reason.

   With this setting, cancellation reasons are displayed on the storefront to the customer when they cancel an order.
   Make sure you have specified at least one reason.

1. Click **[!UICONTROL Save Config]**.

## Cancel from the storefront

A customer can initiate the cancel functionality for a specific order from three pages:

- _My Orders_ page

- _Order View_ page

- _My Account_ page

### My Orders

The _Cancel Order_ button is displayed in the My Orders page if the order can be canceled.

![Example storefront - My Orders page](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Order view page

The _Cancel Order_ button is displayed in the View Order page if the order can be canceled.

![Order details page](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### My Account

The _Cancel Order_ button is displayed in the Recent Orders section of the My Account page, if the order can be canceled.

![My Account page](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}
