---
title: Dynamic Blocks
description: Use dynamic blocks to create rich, interactive content that is driven by logic from price rules and customer segments.
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
---
# Dynamic Blocks

{{ee-feature}}

Create rich, interactive content that is driven by logic from [price rules](../merchandising-promotions/introduction.md#price-rules) and [customer segments](../customers/customer-segments.md). Existing [dynamic blocks](../page-builder/dynamic-block.md) can be added directly to the [!DNL Page Builder] [stage](../page-builder/workspace.md). For a detailed, step-by-step example for using dynamic blocks, see [Tutorial 2: Blocks](../page-builder/2-blocks.md).

>[!NOTE]
>
>The _[!UICONTROL Banner]_ option in the [[!UICONTROL Content] menu](content-menu.md) was deprecated in 2.3.1 and removed in 2.4.0. Its functionality is replaced by Dynamic Blocks.

![[!DNL Page Builder] - dynamic block with price rule and customer segment](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png)<!-- zoom -->

## Step 1: Create a dynamic block

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Elements]_ > **[!UICONTROL Dynamic Blocks]**.

   ![Dynamic blocks list](../page-builder/assets/pb-tutorial2-block-dynamic-add.png)<!-- zoom -->

1. In the upper-right corner, click **[!UICONTROL Add Dynamic Block]**.

   ![New dynamic block](../page-builder/assets/pb-tutorial2-block-dynamic-new.png)<!-- zoom -->

1. If applicable, set **[!UICONTROL Store View]** to a specific store view where the dynamic block is to appear.

1. To activate the dynamic block, set **[!UICONTROL Enable Dynamic Block]** to `Yes`.

1. For internal reference, enter a descriptive **[!UICONTROL Dynamic Block Name]**.

1. Set **[!UICONTROL Dynamic Block Type]** to the area of the page where you want the dynamic block to appear and click **[!UICONTROL Done]**.

   ![Setting the dynamic block type](../page-builder/assets/pb-dynamic-block-type.png)<!-- zoom -->

1. In the **[!UICONTROL Customer Segment]** list, select the checkbox of each segment that you want to see the dynamic block and click **[!UICONTROL Done]** to save the setting.

   ![Choosing a customer segment](../page-builder/assets/pb-dynamic-block-customer-segment.png)<!-- zoom -->

   >[!NOTE]
   >
   >- If no Segment is created, the dynamic block is visible to everyone.
   >- If the customer does not belong to any segments and the dynamic block is created for all segments, the contents of dynamic block is still displayed.
   >- If all customer segments assigned to a Dynamic Block are deleted, its contents are then visible to everyone.

## Step 2: Complete the content

Use the [!DNL Page Builder] [workspace](../page-builder/workspace.md) to complete the content.

![[!DNL Page Builder] - dynamic block workspace](../page-builder/assets/pb-dynamic-block-workspace.png)<!-- zoom -->

## Step 3: Choose a related promotion

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. Click the type of promotion that you want to associate with the dynamic block:

   - **[!UICONTROL Add Cart Price Rules]** (see [Cart Price Rules](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** (see [Catalog Price Rules](../merchandising-promotions/price-rules-catalog.md))

1. In the list of available rules, select the checkbox of each rule that you want to use and click **[!UICONTROL Add Selected]**.

1. When the dynamic block is complete, click **[!UICONTROL Save]**.

## Step 4: Add the dynamic block to a page

1. Open the page where you want the dynamic block to appear.

1. Use the [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) content type to add the dynamic block to the stage.

## Field and tool descriptions

|Field|Description|
|--- |--- |
|[!UICONTROL Store View]|Specifies the store views where the dynamic block is to be available.|
|[!UICONTROL Enable Dynamic Block]|Activates or deactivates the dynamic block. Options: Yes / No|
|[!UICONTROL Dynamic Block Name]|A descriptive name that identifies the dynamic block in the Admin.|
|[!UICONTROL Dynamic Block Type]|Identifies the place in the [standard page layout](layout-updates.md) where the dynamic block is placed. Options: <br/>**[!UICONTROL Content Area]** - Places the dynamic block in the main [content area](layout-updates.md) of the page. <br/>**[!UICONTROL Footer]** - Places the dynamic block in the page [footer](page-setup.md#footer). <br/>**[!UICONTROL Header]** - Places the dynamic block in the page [header](page-setup.md#header). <br/>**[!UICONTROL Left Column]** - Places the dynamic block in the [left sidebar](page-layout.md#standard-page-layouts) of a two-or three-column layout. <br/>**[!UICONTROL Right Column]** - Places the dynamic block in the [right sidebar](page-layout.md#standard-page-layouts) of a two- or three-column layout.|
|Customer Segment|Associates a customer segment with the dynamic block to determine which customers can see it.|

{style="table-layout:auto"}

### Contents

|Field|Description|
|--- |--- |
|[!UICONTROL Layout]|Add rows, columns, or tabs to the stage.|
|[!UICONTROL Elements]|Add text, headings, buttons, dividers, and HTML code to any layout container on the stage.|
|[!UICONTROL Media]|Add images, video, banners, sliders, and Google Maps to any existing layout container on the stage.|
|[!UICONTROL Add Content]|Add existing blocks, dynamic blocks, and products to the stage.|

{style="table-layout:auto"}

### Related Promotions

|Field|Description|
|--- |--- |
|[!UICONTROL Related Cart Price Rule]|**[!UICONTROL Add Cart Price Rules]** - Associate an existing [cart price rule](../merchandising-promotions/price-rules-cart.md) with the dynamic block as a promotion.|
|[!UICONTROL Related Catalog Price Rule]|**[!UICONTROL Add Catalog Price Rules]** - Associate an existing [catalog price rule](../merchandising-promotions/price-rules-catalog.md) with the dynamic block as a promotion.|

{style="table-layout:auto"}
