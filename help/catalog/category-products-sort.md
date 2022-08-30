---
title: Sort category products
description: Learn how to define the positioning of products in a category manually or by applying a predefined sort order.
---
# Sort category products

{{ee-feature}}

The position of products in a category can be specified manually by dragging and dropping products into position or by applying a predefined sort order. By default, products can be sorted by stock level, age, color, name, SKU, and price. Automatic sort overrides the current sort order and resets any drag-and-drop positions that were set manually. The sort order of colors and the minimum stock level that can be required for products to be included in the list are set in the [Visual Merchandiser](https://docs.magento.com/user-guide/configuration/catalog/visual-merchandiser.html) configuration.

You can set up the category options separately for each [store](https://docs.magento.com/user-guide/stores/stores-all-create-store.html) to determine the selection of products, their relative position in the list, and the attributes that are available for category rules. However, only one sort order can be assigned to the [store view](https://docs.magento.com/user-guide/stores/stores-all-create-view.html) level of any store.

## Step 1: Set the scope of the configuration

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. If necessary, choose the **[!UICONTROL Store View]** where the settings apply.

   For a multi-store installation, the _[!UICONTROL Store View]_ setting applies the sort order to all available views within the store.

1. In the category tree on the left, choose the category that you want to edit.

   ![Category tree](./assets/category-selected.png)<!-- zoom -->

## Step 2: Sort the products

In the _[!UICONTROL Products in Category]_ section, click the tiles ( ![View tiles](../assets/icon-view-tiles.png) ) icon to show the product tiles in a grid. Use either the manual or automatic method to sort the products.

![Product tiles](./assets/category-products-tiles.png)<!-- zoom -->

### Method 1: Manual sort

1. Set **[!UICONTROL Sort Order]** to your preference.

1. Click **[!UICONTROL Sort]** to apply the new sort order.

   ![Sort order](./assets/category-edit-sort-order.png)<!-- zoom -->

1. To save the sort order, click **[!UICONTROL Save Category]**.

1. When prompted, update any invalid indexers.

### Method 2: Automatic sort

1. Set **[!UICONTROL Match products by rule]** (![Toggle yes](../assets/toggle-yes.png)) to `Yes`.

   ![Match Products by Rule](./assets/category-edit-automatic-sorting.png)<!-- zoom -->

1. Set **[!UICONTROL Automatic Sorting]** to your preference.

1. Follow the instructions in the next step to create a category rule.

## Step 3: Create a category rule

1. Set **[!UICONTROL Match products by rule]** (![Toggle yes](../assets/toggle-yes.png)) to `Yes`.

1. Click **[!UICONTROL Add Condition]** and do the following:

   ![Category condition](./assets/category-edit-condition.png)<!-- zoom -->

   - Choose the **[!UICONTROL Attribute]** that is the basis of the condition.

   - Set **[!UICONTROL Operator]** to one of the following:

      - `Equal`
      - `Not equal`
      - `Greater than`
      - `Greater than or equal to`
      - `Less than`
      - `Less than or equal to`
      - `Contains`

   - Enter the appropriate **[!UICONTROL Value]**.

1. To add another condition, click **[!UICONTROL Add Condition]** and repeat the process.

## Step 4: Save, refresh, and verify

1. When complete, click **[!UICONTROL Save Category]**.

1. When prompted to refresh the cache, click **[!UICONTROL Cache Management]** and refresh each invalid cache.

1. In the storefront, verify that the product selection, sorting, and category rules work correctly.

   If you need to make adjustments, change the settings and try again.
