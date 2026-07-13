---
title: Allow reorders
description: Learn how to provide reorder capabilities for your customers.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
TQID: https://experienceleague.adobe.com/comSKludWZnDkDjdZyhi4-9WNAE9scH3dgSce08IyJo
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
# Allow reorders

When enabled, reorders can be made directly from the customer account or from the original order in the _Admin_. Reorders are enabled by default.

![Customer reorder link in the Admin](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Criteria for reorder to be enabled for an order

- The _Allow Reorder_ configuration option must be enabled.

- If order is in `Hold` or in `Payment Review` status, the reorder option is disabled.

- If any of the items in the order is unavailable, out of stock, or disabled, the reorder option is disabled on the storefront.

- An _Admin_ can reorder even if any of the items are out of stock or disabled.

## Configure to allow customer reorders

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Sales]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Reorder]** section.

   ![Reorder options](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Allow Reorder]** to `Yes`. 

   This setting enables reorder functionality from the customer account on the storefront or orders list in the Admin.

1. Click **[!UICONTROL Save Config]**.

## Reorder from the storefront

A customer can initiate the reorder functionality for a specific order from two pages:

- _My Orders_ page

- _Order View_ page

### My Orders

The _Reorder_ button is always displayed in the list with Orders (even if all products from the order are not available for reorder).

![Example storefront - My Orders page](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Case 1.** All products from the order are **available** for reorder

User is redirected to the cart, and all products are added to the cart

![Shopping cart](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Case 2.** Some/all products from the order are **not available** for reorder

>[!NOTE]
>
>It is possible to reorder `Not Visible Individually` products.

The _Reorder_ button does not appear on the _My Orders_ and _View Order_ pages.

![My Orders page 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Order view page

**Case 1.** All products from the order are available for reorder

User is redirected to the cart, and all products are added to the cart

**Case 2.** Some/all products from the order are **not available** for reorder

>[!NOTE]
>
>It is possible to reorder `Not Visible Individually` products.

The _Reorder_ button does not appear on the _My Orders_ and _View Order_ pages.

![Order details page](./assets/order-view-page.png){width="700" zoomable="yes"}

### Cart is not empty

If the cart is not empty and the user clicks **[!UICONTROL Reorder]** (from the _My Orders_  or _Order View_ page), the existing products remain in the cart with the added reorder products.

![Reorder items](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Reorder from the Admin

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Locate the order and open in **[!UICONTROL View]** mode.

1. Click **[!UICONTROL Reorder]** which is displayed in the top button bar.

   ![Order details in the Admin](./assets/order-view-admin.png){width="600" zoomable="yes"}

   After you click **[!UICONTROL Reorder]**, the _Create New Order_ page opens with reorder products.

   ![Create reorder](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Complete all required fields as needed.

1. To submit the order, click **[!UICONTROL Submit Order]**.
