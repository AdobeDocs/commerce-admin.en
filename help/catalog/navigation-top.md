---
title: Top navigation
description: Learn how to define the main menu of a store, which functions like a directory to the different departments.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
TQID: https://experienceleague.adobe.com/REad4AtBdJeK2eVNRo1XiTrrjJqmTs6oJfum260IfOk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
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
# Top navigation

The main menu of your store is like a directory to the different departments in your store. Each option represents a different category of products. The position and presentation of the top navigation might vary by theme, but the way it works is essentially the same.

![Top Navigation](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

The category structure of your catalog can influence how well your site is indexed by search engines. The more deeply nested a category, the less likely it is to be thoroughly indexed. Generally, using between one and three visible levels is the most effective. The [root category](category-root.md) counts as the first level, although it doesn't appear in the menu. The maximum number of levels that are available in the top navigation is determined by the configuration. In addition, there might be a limit to the number of menu levels that are supported by your store theme. For example, the sample Luma theme supports up to five levels, including the root.

## Counting menu levels

|Item |Description |
|--- |--- |
|Level 1|The first level is the root category, which in the sample data  is named "Default Category." The root is a container for the menu, and its name does not appear as an option in the menu.|
|Level 2|On a desktop display, the top navigation is the main menu that appears across the top of the page. On a mobile device, the main menu typically appears as a fly-out menu of options. The second-level options in the Luma  store are _What's New_, _Women_, _Men_, _Gear_, _Training_, and _Sale_.|
|Level 3|The third level appears below each  main menu option. For example, under _Women_, the third-level options are _Tops_ and _Bottoms_.|
|Level 4|The fourth-level options are subcategories that fly out from a third-level option. For example, under _Tops_, the fourth level menu options are _Jackets_, _Hoodies & Sweatshirts_, _Tees_, and _Bras & Tanks_.|

{style="table-layout:auto"}

## Set the top navigation

For a category to appear in the top navigation of a store, complete the following steps:

### Step 1: Create a category

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Set a **[!UICONTROL Store View]** to determine where the new category is to be available.

1. In the category tree, select the parent category of the new category.

   If you're starting from the beginning without any data, there might be only two categories in the list: _Default Category_, which is the root, and an _Example category_.

1. Click **[!UICONTROL Add Subcategory]**.

1. Complete the basic information with following settings:

   - **[!UICONTROL Enable Category]** set to `Yes`
   - **[!UICONTROL Include in Menu]** set to `Yes`

1. In Display Setting set **[!UICONTROL Anchor]** to `Yes`.

1. Complete any other required [category settings](category-create.md).

1. When complete, click **[!UICONTROL Save]**.

For a multistore installation, a different main menu can be assigned as the [root category](category-root.md) for each [store](../stores-purchase/stores.md#add-stores).

### Step 2: Set the depth of the top navigation

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. Expand the **[!UICONTROL Category Top Navigation]** section.

   ![Category Top Navigation](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   Because the depth of the top navigation has a global [configuration scope](../getting-started/websites-stores-views.md#scope-settings), the setting applies to all websites, stores, and store views in the Commerce installation. The _[!UICONTROL Category Top Navigation]_ configuration section is available only when _[!UICONTROL Store View]_ in the upper-left corner is set to `Default Config`.

   For a detailed list of these options, see [Category Top Navigation](../configuration-reference/catalog/catalog.md#layered-navigation) in the _Configuration Reference_.
      
1. To limit the number of subcategories that appear in the top navigation, enter the number for **[!UICONTROL Maximal Depth]**.

   The default value is `0`, which does not place a limit on the number of subcategory levels.

1. When complete, click **[!UICONTROL Save Config]**.
