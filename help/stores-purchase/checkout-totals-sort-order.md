---
title: Sort order for checkout totals
description: Learn about the displayed checkout total and how to configure the checkout totals sort order on the order summary.
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
TQID: https://experienceleague.adobe.com/cXt3dbS5Jd8baKFk8K8HP1Cypk1oMS85iCq-WZ8cIgg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
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
# Sort order for checkout totals

During order review, the total appears at the bottom of the order, with any adjustments for discounts, shipping charges, store credit, and tax. The order of each item determines the sequence of the calculations, and is set in the configuration by a number that is assigned to each item. For example, the Subtotal is the first item in the section, and is assigned a value of 10. The Grand Total appears last, and is assigned a value of 100. All other items in the totals section are assigned a value between those values.

![Order Summary displays the checkout total](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_To configure the checkout totals sort order:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In left panel, expand the **[!UICONTROL Sales]** section and choose **[!UICONTROL Sales]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Checkout Totals Sort Order]** section.

   ![Checkout totals options numbered to determine the sort order](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   For a detailed description of each of these configuration settings, see [Checkout Totals Sort Order](../configuration-reference/sales/sales.md#checkout-totals-sort-order) in the _Configuration Reference Guide_.

1. If the setting is for a specific store view, [choose the store view](../configuration-reference/scope-change.md#set-the-scope) where the configuration applies.

   When prompted, click **[!UICONTROL OK]** to continue.

1. To determine the order in the _Totals_ section, change the number assigned to each item.

   The lower the value, the earlier its placement in the list. In the default configuration, the Subtotal (`10`) is the first and Grand total (`100`) is the last.

   If necessary, clear the **[!UICONTROL Use system value]** checkbox to complete these changes.

1. Click **[!UICONTROL Save Config]**.
