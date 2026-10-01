---
title: Sort category products
description: Learn how to define the positioning of products in a category manually or by applying a predefined sort order.
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
TQID: https://experienceleague.adobe.com/Co2sHVc4YaLqjVrc-Varq9-ssecBB-C2mL3MTAPuQbU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
    internal-label: Categories
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
# Sort category products

{{ee-feature}}

The position of products in a category can be specified manually by dragging and dropping products into position or by applying a predefined sort order. By default, products can be sorted by stock level, age, color, name, SKU, and price. Automatic sort overrides the current sort order and resets any drag-and-drop positions that were set manually. The sort order of colors and the minimum stock level that can be required for products to be included in the list are set in the [Visual Merchandiser](../configuration-reference/catalog/visual-merchandiser.md) configuration.

You can set up the category options separately for each [store view](../stores-purchase/stores.md#add-stores) to determine the selection of products, their relative position in the list, and the attributes that are available for category rules. However, there is a single, **_global_** sort order and product position in the catalog and they are shared across all [store views](../stores-purchase/store-views.md), stores, and websites.

## Step 1: Set the scope of the configuration

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. If necessary, choose the **[!UICONTROL Store View]** where the settings apply.

   For a multi-store installation, the _[!UICONTROL Store View]_ setting applies the sort order to all available views within the store.

1. In the category tree on the left, choose the category that you want to edit.

   ![Category tree](./assets/category-selected.png){width="700" zoomable="yes"}

## Step 2: Sort the products

>[!NOTE]
>
>When sorting a category by a product attribute, products with the same attribute values are also sorted by their _[!UICONTROL Product ID]_ in the ascending order.

In the _[!UICONTROL Products in Category]_ section, click the tiles ( ![View tiles](../assets/icon-view-tiles.png) ) icon to show the product tiles in a grid. Use either the manual or automatic method to sort the products.

![Product tiles](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### Method 1: Manual sort

1. Set **[!UICONTROL Sort Order]** to your preference.

   ![Sort order](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. To apply the new sort order, click **[!UICONTROL Sort]**.

1. To save the sort order, click **[!UICONTROL Save Category]**.

1. When prompted, update any invalid indexers.

### Method 2: Automatic sort

1. Set **[!UICONTROL Match products by rule]** (![Toggle yes](../assets/toggle-yes.png)) to `Yes`.


1. Set **[!UICONTROL Automatic Sorting]** to your preference.

1. To create a category rule, follow the instructions in the next step.

## Step 3: Create a category rule

1. Set **[!UICONTROL Match products by rule]** (![Toggle yes](../assets/toggle-yes.png)) to `Yes`.

1. Click **[!UICONTROL Add Condition]**.

1. Choose the **[!UICONTROL Attribute]** that is the basis of the condition.

1. Set **[!UICONTROL Operator]** to one of the following:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Enter the appropriate **[!UICONTROL Value]**.

   ![Category condition](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. To add another condition, click **[!UICONTROL Add Condition]** and repeat the process.

## Step 4: Save, refresh, and verify

1. When complete, click **[!UICONTROL Save Category]**.

1. When prompted to refresh the cache, click **[!UICONTROL Cache Management]** and refresh each invalid cache.

1. In the storefront, verify that the product selection, sorting, and category rules work correctly.

   If you must make adjustments, change the settings and try again.
