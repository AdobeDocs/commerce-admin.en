---
title: Visual Merchandiser overview
description: Learn about the Visual Merchandiser tools that allow you to position products and determine which products appear in the category listing.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/MbeCfIBdepAr5U2B1I-lfFGNm1b5DiKGevM5365brpo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
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
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Visual Merchandiser

{{ee-feature}}

The _Visual Merchandiser_ is a set of advanced tools that allows you to position products and apply conditions that determine which products appear in the category listing. The result can be a dynamic selection of products that adjusts to changes in the catalog. You can work in _visual mode_, which shows each product as a tile on a grid, or to work from a list of products in the category. The same tools are available in each mode and you can use the buttons in the upper-right corner to toggle between each type of display.

![Category products in tile view](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Access the Visual Merchandiser

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Drill down through the category tree and click the category that you want to edit.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Products in Category]** section.

1. Click the _View as Tiles_ ( ![View as tiles](../assets/icon-view-tiles.png) ) button to display the products as a grid.

1. When complete, click **[!UICONTROL Save Category]**.

## Change the position of a product

1. Use the [sort order](../catalog/navigation-product-listings.md) to view the product that you want to move.

   - **Method 1: Drag and Drop**

      Grab the _Drag_ (![Drag icon](../assets/icon-move.png)) control in the upper-right corner of the product tile and drop the product into position. The number of each product adjusts to reflect the new position.

   - **Method 2: Set Position Value**

      In the _Position_ controller (![Position field](../assets/control-position.png)) on the product tile, enter the number where you want the product to appear. Enter `0` to place the product at the top of the list.

1. When complete, click **[!UICONTROL Save Category]**.

>[!NOTE]
>
>In a clean installation, Adobe Commerce reserves the category ID `2` for the root catalog of the default store. Visual Merchandiser can use only categories with an ID number of `3` or greater.

## Workspace controls

|Control|Description|
|--- |--- |
|![View list icon](../assets/icon-view-list.png)|View as list|
|![View as tiles icon](../assets/icon-view-tiles.png)|View as tiles|
|![Match by rule toggle - no](../assets/toggle-no.png)|Match by rule - no|
|![Match by rule toggle - yes](../assets/toggle-yes.png)|Match by rule - yes|
|![Move icon](../assets/icon-move.png)|Drag|
|![Position controller](../assets/control-position.png)|Position|
|![Remove from category icon](../assets/icon-delete-x.png)|Remove from category|
|![Items per page control](../assets/control-items-per-page.png)|View per page|
|![Change page display](../assets/control-page-display.png)|Go to next / previous|

{style="table-layout:auto"}
