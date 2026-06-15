---
title: Assign inventory quantities per product
description: Learn how to update the inventory quantities for your product and track the on-hand, available stock amounts.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/0OBXyHUbsWVXmEnWEWd0CGcBNhci57w8HGtDCGCWuOk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Assign quantities per product

After adding [sources](sources-assign-per-product.md), update the inventory quantities for your product. These values track the on-hand, available stock amounts.

To hide a source's inventory from shipments without removing the source, set _[!UICONTROL Source Item Status]_ to `Out of Stock`. The SSA and shipment options only access sources listed as `In Stock` with available inventory quantity.

All updated quantities and sources display in the product grid.

## Update quantities

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Locate and open a product in edit mode.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Sources]** section.

1. Set **[!UICONTROL Source Item Status]** to `In Stock`.

1. to update the quantity for on-hand stock, enter an amount for **[!UICONTROL Qty]**.

1. To set a notification for inventory quantities, do one of the following:

   - Custom Notify Quantity - Deselect the **[!UICONTROL Use Default]** checkbox and enter an amount in **[!UICONTROL Notify Qty]**.
   - Default Notify Quantity - Select the **[!UICONTROL Use Default]** checkbox. [!DNL Commerce] checks and uses the setting in _[!UICONTROL Advanced Inventory]_ or global store configuration.

   ![Update Product Quantities per Source](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Do one of the following to save:

   - Click **[!UICONTROL Save]**.

   - On the **[!UICONTROL Save]** (![Menu arrow](../assets/icon-menu-down-arrow-red.png)) menu, choose **[!UICONTROL Save & Close]**.


The Product Grid updates with a list of all sources and related quantities. For products with more than five assigned sources, hover over the _[!UICONTROL Quantity per Source]_ column to see the full list.

![Product quantities per source](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
