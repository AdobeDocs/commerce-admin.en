---
title: Categories - Content settings
description: Learn about using the [!UICONTROL Content] settings to define any additional content that appears on the category page.
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/PKCKw4i-EDB10X3AU-daMiyVMT96naqRLF8vrVBp24s
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
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
# Categories - Content settings

The _[!UICONTROL Content]_ settings determine any additional content appears on the category page. In addition to the list of category products, the page can include an image, description, and CMS block. You can use the [[!DNL Page Builder]](../page-builder/introduction.md) content tools to define the category description.

## Add the category description in [!DNL Page Builder]

1. Open the category in edit mode.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Content]** section.

   ![Category content](./assets/category-content.png){width="600" zoomable="yes"}

1. At the top right of the **[!UICONTROL Description]** area, click **[!UICONTROL Edit with Page Builder]**.

1. Use the [[!DNL Page Builder]](../page-builder/introduction.md) content tools to [edit any existing text](../page-builder/text.md) and add other content (if needed).

## [!DNL Page Builder] preview

When you expand the _Content_ section for an existing category where there is content created with [!DNL Page Builder], it displays a preview of the **[!UICONTROL Description]** content as it would appear in the category page. Clicking the content area opens the [!DNL Page Builder] workspace, where you can make any needed updates.

![Description preview](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

This content preview is enabled for the product and category forms by default. If performance suffers due to loading the preview, you can disable the preview in the [Content Management configuration](../configuration-reference/general/content-management.md#advanced-content-tools) settings.

## Add the category description in the editor

Enter only plain ASCII characters into the text box. If pasting text from a word processor, save it first as a plain .TXT file to remove any invisible control characters.

For more information, see [WYSIWYG editor](../content-design/editor.md).

1. Open the category in edit mode.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Content]** section.

   ![Category content](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. Enter the category **[!UICONTROL Description]** and use the [editor toolbar](../content-design/editor.md) to format as needed.

   You can drag the lower-right corner to change the height of the text box.

## Add a CMS block to the category page

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. In the category tree, select the category that you want to edit.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Content]** section.

1. For **[!UICONTROL Add the CMS block]**, select a block you want to add.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Display Settings]** section.

1. Set the **[!UICONTROL Display Mode]** to one of the following:

   - `Static block only`
   - `Static block and products`

1. When complete, click **[!UICONTROL Save]** and review the block display on the storefront (requires cache refresh).

## Content settings reference

|Setting|[Scope](../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Category Image]|Store View|Specifies an image for the top of the category page. Methods: <br/><br/>**[!UICONTROL Upload]** - Uploads an image file from your local computer to the gallery and uses it as the category image. <br/><br/>**[!UICONTROL Select from Gallery]** - Prompts you to choose an existing image from the gallery. <br/><br/>![Page Builder camera icon](../assets/icon-camera.png) - Either drag an image file to the camera tile or browse to the image and select it from your local file system.|
|[!UICONTROL Description]|Store View|Specifies a description that appears on the category page. <br/><br/>**[!UICONTROL Edit with Page Builder]** - Opens the [[!DNL Page Builder] workspace](../page-builder/workspace.md), where you can edit the description. <br/><br/>**[!UICONTROL Show / Hide Editor]** - Toggles the display between WYSIWYG editor and HTML modes.|
|[!UICONTROL Add CMS Block]|Store View|Adds an existing [CMS block](../content-design/blocks.md) to the category page.|

{style="table-layout:auto"}
