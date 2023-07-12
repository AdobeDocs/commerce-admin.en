---
title: '[!DNL Page Builder] Walkthrough Part 3: Catalog Content'
description: Learn how to add a product list to a page in [!DNL Page Builder].
exl-id: f2a0dc29-6d8f-4b97-a947-72659c01d0cb
feature: Page Builder, Page Content
---
# Walkthrough Part 3: Catalog Content

This exercise demonstrates how easy it is to add a product list to a page, customize product pages, and create a custom attribute that adds the [!DNL Page Builder] workspace to a product attribute set.

![Product list](./assets/pb-add-content-products-list.png)<!-- zoom -->

This exercise assumes that you have completed [Part 1: Simple Page](1-simple-page.md) and [Part 2: Blocks](2-blocks.md), including the prerequisites and downloaded sample files. Follow the three parts of this exercise in order.

## Part 1: Add a product list

[!DNL Page Builder] makes it easy to add a product list to the stage. In this example, the product list is added directly to a page.

### Step 1: Add a product list to the stage

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Elements]_ > **[!UICONTROL Pages]**.

1. Find the _Simple Page_ that you created in the first exercise and modified in the second, and select **[!UICONTROL Edit]** in the _[!UICONTROL Action]_ column.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Content]** section and click **[!UICONTROL Edit with Page Builder]** or inside the content preview area.

1. In the [!DNL Page Builder] panel under _[!UICONTROL Layout]_, drag a **[!UICONTROL Row]** to the top of the stage.

1. In the [!DNL Page Builder] panel, expand **[!UICONTROL Add Content]** and drag a **[!UICONTROL Products]** placeholder to the new row.

   ![Dragging a products placeholder onto the row](./assets/pb-add-content-products-drag.png)<!-- zoom -->

### Step 2: Compose the condition

1. Hover over the empty products container to display the toolbox and choose the _Settings_ (![Settings icon](./assets/pb-icon-settings.png)<!-- width="20px" --> ) icon.

   ![Products toolbox](./assets/pb-add-content-products-toolbox.png)<!-- zoom -->

1. For **[!UICONTROL Select Products By]**, choose `Condition`.

1. Add a condition:

   - Click the _Add_ (![Add icon](../assets/icon-add-green-circle.png)) icon.

   - Under _[!UICONTROL Product Attribute]_, choose **[!UICONTROL Category]**.

      ![Choosing the category attribute for the condition](./assets/pb-add-content-products-settings-condition.png)<!-- zoom -->

   - Complete the _[!UICONTROL Category is] ..._ part of the condition by clicking the More (...) icon and then click the _Chooser_ (![Chooser icon](../assets/icon-list-chooser.png)) icon.

      ![Defining the condition](./assets/pb-add-content-products-settings-condition-category-is.png)<!-- zoom -->

   - In the category tree, drill down to the **Women > Tops** category and select the **Tees** checkbox.

      ![Choosing the category in the tree](./assets/pb-add-content-products-settings-condition-category-tree.png)<!-- zoom -->

   - Click the Checkmark (![Checkmark icon](../assets/icon-checkmark-green-circle.png)) icon.

      The corresponding category ID appears in the field to complete the condition.

### Step 3: Complete the settings

1. Enter the **[!UICONTROL Number of Products to Display]**.

   By default, the list displays five products.

1. Complete the remaining settings as needed.

   If needed, use the field descriptions at the end of the [Add Products](products.md) topic for reference.

1. When complete, click **[!UICONTROL Save]** to save the settings and return to the [!DNL Page Builder] workspace.

   ![Products list in the stage](./assets/pb-add-content-products-list-stage.png)<!-- zoom -->

1. In the upper-right corner of the stage, click the _Close Full Screen_ (![Close full screen icon](./assets/pb-icon-reduce.png)) icon.

   Clicking this icon returns you to the _[!UICONTROL Content]_ section for the page with the preview displayed.

1. In the upper-right corner, click the **[!UICONTROL Save]** arrow and choose **[!UICONTROL Save & Close]**.

## Part 2: Customize the product page

>[!NOTE]
>
>An Admin user must have [!UICONTROL Content] permissions for their [role scope](../systems/permissions-user-roles.md) to see [!UICONTROL Edit with Page Builder] buttons and be able to use Page Builder.

In this part of the exercise, you learn how easy it is to customize a product page by placing a video below the set of tabs on the product page. The process to update [category page](../catalog/categories-content-settings.md) content is basically the same.

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Find a simple product that you can use for this example and open it in edit mode.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Content]** section.

1. Next to _[!UICONTROL Description]_, click **[!UICONTROL Edit with Page Builder]**.

   ![Product description content](./assets/pb-catalog-product-content.png)<!-- zoom -->

   If the product description was entered previously without [!DNL Page Builder], the current description appears as HTML in an [HTML Code](html-code.md) container. With the Luma theme, the product description appears on the Detail tab.

1. In the [!DNL Page Builder] panel under _[!UICONTROL Layout]_, drag a **[!UICONTROL Row]** to the stage, placing it below the HTML code container.

   Look for the red guideline to appear when the row is in the correct position.

   ![Dragging a row to the stage](./assets/catalog-product-content-stage-row-drag.png)<!-- zoom -->

1. In the [!DNL Page Builder] panel, expand **[!UICONTROL Media]** and drag a **[!UICONTROL Video]** placeholder to the new row.

   ![Video placeholder in the row](./assets/tutorial3-product-drag-video.png)<!-- zoom -->

1. Hover over the empty video container to display the toolbox and choose the _Settings_ (![Settings icon](./assets/pb-icon-settings.png)<!-- width="20px" --> ) icon.

   ![Video toolbox](./assets/pb-tutorial3-product-video-toolbox.png)<!-- zoom -->

1. Enter the **[!UICONTROL Video URL]**.

   The video can be hosted on either [YouTube][1] or [Vimeo][2]. The video in this example can be found on YouTube at the following URL:

      `https://www.youtube.com/watch?v=ZpFrNyD4100`

   ![Editing the video](./assets/pb-tutorial3-product-edit-video.png)<!-- zoom -->

1. Enter the **[!UICONTROL Maximum Width]** in pixels for the video display.

   If you leave this option blank, the video fills the available space.

1. Click **[!UICONTROL Save]** to save the settings and return to the [!DNL Page Builder] workspace.

   ![Video in the content stage](./assets/pb-tutorial3-product-video.png)<!-- zoom -->

1. In the upper-right corner of the stage, click the _Close Full Screen_ (![Close full screen icon](./assets/pb-icon-reduce.png)) icon.

   Clicking this icon returns you to the _[!UICONTROL Content]_ section for the page with the preview displayed.

1. In the upper-right corner, click the **[!UICONTROL Save]** arrow and choose **[!UICONTROL Save & Close]**.

In the storefront, the video appears below the set of tabs. To see how the page looks on a mobile device, you can resize the window.

![Video displayed on the product page](./assets/pb-tutorial3-product-video-storefront.png)<!-- zoom -->

**Congratulations!** You have completed the second part of the Catalog Content tutorial. Keep the work that you created, so you can refer to it later.

## Part 3: Add custom attributes

Use the [!DNL Page Builder] custom attribute to add a fully functioning [!DNL Page Builder] workspace to a product page, which you can use to create engaging content. In this part of the exercise, you learn how to create a custom attribute using the [!DNL Page Builder] input type and apply it to product pages in your catalog. For more information about these attributes, see [Product Attributes](../catalog/product-attributes.md).

![[!DNL Page Builder] and text editor attributes in the storefront](./assets/pb-storefront-product-attribute.png)<!-- zoom -->

### Step 1: Create a product

To avoid changes to your live store, create a product using the described properties.

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. In the upper-right corner, click **[!UICONTROL Add Product]**.

1. Create the product with the following properties:

   - [!UICONTROL Attribute Set]: Default
   - [!UICONTROL Product Name]: My Product
   - [!UICONTROL SKU]: Tutorial
   - [!UICONTROL Price]: 75.00 
   - [!UICONTROL Quantity]: 100
   - [!UICONTROL Stock Status]: In Stock
   - [!UICONTROL Weight]: 1
   - [!UICONTROL Categories]: Women > Tops > Tees

1. In the upper-right corner, click the **[!UICONTROL Save]** arrow and choose **[!UICONTROL Save & Close]**.

### Step 2: Create custom attributes

In this step, you create two new custom attributes to show how the [!DNL Page Builder] and Text Editor input types can be used.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_ > **[!UICONTROL Product]**.

1. In the upper-right corner, click **[!UICONTROL Add New Attribute]**.

1. Enter a **[!UICONTROL Default Label]** for the attribute.

   For this example, use `My Page Builder Attribute` for the label.

1. Set **[!UICONTROL Catalog Input Type for Store Owner]** to `Page Builder`.

   When creating a custom attribute, you can specify the editor that is most suitable to the application as either `Page Builder` or the standard, WYSIWYG `Text Editor`.

   ![[!DNL Page Builder] Input Type](./assets/pb-attribute-page-builder.png)<!-- zoom -->

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Advanced Attribute Properties]** section and make the following settings:

   - [!UICONTROL Attribute Code]: Enter an attribute code in lowercase characters, using hyphens instead of spaces. For this example, use `my_page_builder_attribute`.
   - [!UICONTROL Scope]: Accept the default value, `Store View`.
   - [!UICONTROL Default Value]: Enter a default value for the attribute.
   - [!UICONTROL Unique Value]: `No`
   - [!UICONTROL Add to Column Options]: `No`
   - [!UICONTROL Use in Filter Options]: `Yes`

1. In the _[!UICONTROL Attribute Information]_ panel on the left, choose **[!UICONTROL Storefront Properties]** and make the following settings:

   - [!UICONTROL Use for Promo Rule Conditions]: `Yes`
   - [!UICONTROL Visible on Catalog Pages on Storefront]: `Yes`
   - [!UICONTROL Used in Product Listing]: `Yes`

1. When complete, click **[!UICONTROL Save Attribute]**.

1. Repeat the previous steps to create a second attribute with the same basic properties, but with the Text Editor input type as follows:

   - [!UICONTROL Default Label]: My Text Editor Attribute
   - [!UICONTROL Catalog Input Type for Store Owner]: Text Editor
   - [!UICONTROL Attribute Code]: `my_text_editor_attribute` 

### Step 3: Update the product attribute set

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_ > **[!UICONTROL Attribute Set]**.

   For this example, you temporarily add the new attributes to the `default` attribute set. At the end of this exercise, remove the attributes from the attribute set, so don't impact your catalog.

   >[!NOTE]
   >
   >If you don't want to change your live store, you can follow along without updating the attribute set.

1. Find the _[!UICONTROL Default]_ attribute set in the list and double-click it to open it in edit mode.

1. In the _Unassigned Attributes_ list, find the new attributes you created and drag each one to the _[!UICONTROL Groups]_ column, under **[!UICONTROL Content]**.

   The location of the attribute in the [!UICONTROL Groups] column determines where it appears on the page.

   ![New attributes added to the Content group](./assets/pb-product-attribute-set.png)<!-- zoom -->

1. Click **[!UICONTROL Save]** to return to the Attribute Sets list.

1. When prompted, click the **[!UICONTROL Cache Management]** link at the top of the page and refresh any invalid cache.

### Step 4: Update the product

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. In the Products grid, find _My Product_ and open it in edit mode.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Content]** section.

   At the top of the section, there are two standard attributes for product content:

   - _Short Description_, which uses the standard WYSIWYG [editor](../content-design/editor.md).
   - _Description_, which displays the [!DNL Page Builder] preview.

   ![Product content](./assets/pb-product-content-edit-with-page-builder.png)<!-- zoom -->

   As you scroll to the lower half of the section, there are the two attributes you created and assigned:

   - _My [!DNL Page Builder] Attribute_, which displays the [!DNL Page Builder] preview.
   - _My Text Editor Attribute_, which uses the standard WYSIWYG editor.

   ![Product content editing](./assets/pb-product-content-my-attributes.png)<!-- zoom -->

1. In the **My Text Editor Attribute** editor, enter `Text Editor Attribute placeholder text`.

   - In the upper-right corner, click the **[!UICONTROL Save]** arrow and choose **[!UICONTROL Save & Close]**.

1. For **My Page Builder Attribute**, click **[!UICONTROL Edit with Page Builder]** and add the description text:

   - In the [!DNL Page Builder] panel, expand **[!UICONTROL Elements]** and drag a **[!UICONTROL Text object]** to the stage.

   - Enter `Page Builder attribute placeholder text`.

   - In the upper-right corner of the stage, click the _Close Full Screen_ (![Close full screen icon](./assets/pb-icon-reduce.png)) icon.

      ![Custom attributes with placeholder text](./assets/pb-product-content-attributes.png)<!-- zoom -->

1. Scroll up to **[!UICONTROL Description]**, click **[!UICONTROL Edit with Page Builder]**, and add any text that you like using the same method as the previous step.

1. In the upper-right corner of the product page, click the **[!UICONTROL Save]** arrow and choose **[!UICONTROL Save & Close]**.

1. If prompted, click the **[!UICONTROL Cache Management]** link in the message at the top of the page and refresh any invalid cache.

### Step 5: Check it out

1. Navigate to your sample product page in the storefront.

   In this example, the product can be found in the top navigation under Women > Tops > Tees.

1. Scroll down to the _My Page Builder Attribute_ information.

   The position of the attributes on the product page is determined by the theme. In the Luma theme, the new attributes are located just after the product description.

   ![[!DNL Page Builder] and Text Editor attributes in the storefront](./assets/pb-storefront-product-attribute.png)<!-- zoom -->

**Congratulations!** You have completed the [!DNL Page Builder] Catalog Content exercise. Keep the work that you created, so you can refer to it later.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
