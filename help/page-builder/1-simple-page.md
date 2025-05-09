---
title: '[!DNL Page Builder] Walkthrough part 1: simple page'
description: Use the sample files and follow the steps to create a simple page in the [!DNL Page Builder] interface.
exl-id: 2c146241-675f-4d23-9513-1722d5dd3357
feature: Page Builder, Page Content
---
# [!DNL Page Builder] Walkthrough part 1: simple page

Follow this three-part exercise to become familiar with the [!DNL Page Builder] workspace by creating a simple page that illustrates how easy it is to create content-rich pages of your own design.

![Simple Page example](./assets/pb-tutorial1-simple-layout.png){width="700" zoomable="yes"}

>[!NOTE]
>
>These walkthrough exercises are updated to reflect recent changes to the [!DNL Page Builder] workspace in the 2.4.1 release.

## Before you begin

Before starting this exercise, it is recommended that you increase the [Admin Session Lifetime](../systems/security-admin.md) to prevent the session from timing out while you work.

Verify the required Content Management configuration settings:

- WYSIWYG Editor is enabled in the [WYSIWYG Options](../content-design/editor.md#configure-the-editor) configuration.

- [!DNL Page Builder] is enabled in the [Advanced Content Tools](setup.md) configuration.

### Download the walkthrough image assets

1. Download the [`simple-page-assets`](./assets/simple-page-assets.zip) file and save the file to your local system.

1. Navigate to the downloaded file and extract the zipped files.

   On a Windows system, right-click and choose **[!UICONTROL Extract All]** files. Then, choose the destination folder and click **[!UICONTROL Extract]**.

   On a Mac system, you can simply double-click the zip file and the move the extracted files to the destination folder.

   The folder contains the following image files:

   ![[!DNL Page Builder] walkthrough files - simple page assets](./assets/pb-tutorial-simple-page-assets.png){width="500"}

Follow the three parts of this walkthrough in order.

## Part 1: Full-Bleed Row with Banner

In this part of the Simple Page exercise, you create a page that has a full-bleed row and banner. The row has different background images for desktop and mobile devices.

![[!DNL Page Builder] full bleed row with banner](./assets/pb-tutorial1-full-bleed-with-banner.png){width="700" zoomable="yes"}

### Step 1: Create a page

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Elements]_ > **[!UICONTROL Pages]**.

1. In the upper-right corner, click **[!UICONTROL Add New Page]** and do the following:

   - To prevent this page from being published in your store, set **[!UICONTROL Enable Page]** to `No`.

   - For **[!UICONTROL Page Title]**, enter `Simple Page`.

   ![Basic page settings](./assets/pb-tutorial1-currently-active.png){width="600" zoomable="yes"}

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Design]** section.

   Notice that **[!UICONTROL Layout]** is set to `Page -- Full Width` by default. In addition to the five standard [layout](../content-design/page-layout.md) options, [!DNL Page Builder] adds full-width layouts for pages, categories, and products.

1. If the sample data is available, set **[!UICONTROL New Theme]** to `Magento Luma`. Otherwise, you can choose another available theme or leave it blank to use the default theme.

   The _[!UICONTROL New Theme]_ setting can be used to override the default theme and to apply a different theme to the page.

   >[!NOTE]
   >
   >The Full Width layout can be used only with a compatible [theme](../content-design/themes.md).

   ![Page design settings](./assets/pb-tutorial1-design-section.png){width="600" zoomable="yes"}

1. In the upper-right corner, click **[!UICONTROL Save]**.

   When the page is saved, the name _Simple Page_ appears in the upper-left corner of the page.

### Step 2: Format the row

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Content]** section.

   This action displays the [!DNL Page Builder] preview with an empty row.

   >[!NOTE]
   >
   >The [Content Heading](workspace.md) field is optional. It is by default, formatted as a heading level 1 (H1) according to the theme. For this exercise, the _Content Heading_ is left blank.

   ![Page content preview with empty row](./assets/pb-content-preview-empty.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Edit with Page Builder]** or inside the content preview area.

   In the expanded [!DNL Page Builder] [workspace](workspace.md), the panel on the left provides the content tools you can use to build your content in the stage.

1. Hover over the empty row to display the toolbox.

   Each content container has a toolbox with a similar set of options.

   ![[!DNL Page Builder] row toolbox](./assets/pb-layout-page-add-content-row-tools.png){width="600" zoomable="yes"}

1. In the Row toolbox, choose the _Settings_ (![Settings icon](./assets/pb-icon-settings.png){width="20"} icon.

1. Under _[!UICONTROL Appearance]_, choose **Full Bleed**.

   The Full Bleed appearance setting extends the left and right borders of the content area of the row and background to the full width of the page.

   ![Row settings - full bleed](./assets/pb-tutorial1-row-settings-appearance-full-bleed.png){width="600" zoomable="yes"}

1. Scroll down to the _[!UICONTROL Advanced]_ section and set all **[!UICONTROL Margins and Padding]** settings to `0`.

   This setting ensures that the banner extends the full width of the row.

   ![Row settings - margins and padding](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

1. To save the settings and return to the [!DNL Page Builder] workspace, scroll up to the top of the page and click **[!UICONTROL Save]** in the upper-right corner.

### Step 3: Add a banner

>[!NOTE]
>
>[!DNL Page Builder] has a new content type called _Banner_, which is featured in this step. What was previously the _Banner_ option in the Content menu, is now a _Dynamic Block_.

1. In the [!DNL Page Builder] panel, expand **[!UICONTROL Media]** and drag a **Banner** placeholder to the stage.

   ![Dragging a banner content type to the stage](./assets/pb-tutorial1-banner-drag-to-stage.png){width="600" zoomable="yes"}
1. Hover over the banner container to display the toolbox.

   >[!NOTE]
   >
   >The stage now has two content containers, each with a separate toolbox. Because the banner is nested inside the row, make sure that you are working in the correct toolbox.

   In addition to the toolbox, the _Upload Image_ and _Select from Gallery_ buttons are included so you can make quick changes to the banner directly from the stage.

   ![Banner toolbox](./assets/pb-tutorial1-banner-toolbox.png){width="600" zoomable="yes"}

1. In the Banner toolbox, choose the _Settings_ ( ![Settings icon](./assets/pb-icon-settings.png){width="20"} ) icon.

1. Under _[!UICONTROL Appearance]_, choose **[!UICONTROL Collage Right]**.

   The Collage Right setting positions content on the right side of the banner.

   ![Banner appearance - collage right](./assets/pb-tutorial1-row-banner-settings-appearance-collage-right.png){width="600" zoomable="yes"}

1. Scroll down to the _[!UICONTROL Background]_ section and set the background image for the banner:

   - For **[!UICONTROL Background Image]**, click **Upload**.

      ![Banner background - upload image](./assets/pb-tutorial1-row-background-image-upload.png){width="600" zoomable="yes"}

      Navigate to the directory where you saved the extracted simple page assets and choose the `wide-banner-background.jpg` file.

      The image is uploaded and a thumbnail of the uploaded image appears. The file name, image dimensions, and file size are noted below.

      ![Uploaded background image in the media gallery](./assets/pb-tutorial1-row-settings-background-image-selected.png){width="600" zoomable="yes"}

   - For **[!UICONTROL Background Mobile Image]**, click **Upload**.

      In the same file directory, choose the `wide-banner-background-mobile.jpg` file.

      The mobile background image is used for mobile devices, and also whenever a desktop browser window is resized to the width of a mobile device.

      ![Selecting the sample banner image file for mobile](./assets/pb-tutorial1-row-settings-background-mobile-image-selected.png){width="600" zoomable="yes"}

   - Scroll back to the top of the page and click **[!UICONTROL Save]** to save the settings and return to the [!DNL Page Builder] workspace.

      The background appears on the stage and extends the full width of the row.

      ![Banner with background image](./assets/pb-tutorial1-banner-background.png){width="600" zoomable="yes"}

   Notice the placeholder text that appears on the right side of the row. The position of this text reflects the _Collage Right_ appearance setting.

1. Click the placeholder text, and enter the following message as two lines:

      `Get fit and look fab in new seasonal styles.`

      `New LUMA yoga collection`

   The editor toolbar appears above the text box. Text can be entered and formatted either directly from the stage, or by choosing _Settings_ in the banner toolbox.

   ![Editing banner content from the stage](./assets/pb-tutorial1-banner-stage-text.png){width="600" zoomable="yes"}

1. Apply formatting to the text:

   - Select the first line of text. Then, on the editor toolbar under **Formats**, choose `Heading 2`.

      ![Applying the Heading 2 format](./assets/pb-tutorial1-banner-stage-text-format-line1.png){width="600" zoomable="yes"}

   - Select the second line of text. Then, on the editor toolbar under **Formats**, choose `Paragraph`.

   The format settings apply the styles from the style sheet that is associated with the current theme.

   ![Banner in the content stage with formatted text](./assets/pb-tutorial1-banner-stage-text-format-line2.png){width="600" zoomable="yes"}
   __

1. Hover to display the Banner toolbox, choose the _Settings_ ( ![Settings icon](./assets/pb-icon-settings.png){width="20"} ) icon again, then scroll to the _[!UICONTROL Content]_ section.

   Notice that your text is displayed in the _Message Text_ box. Text can be entered and edited either from the stage or from the _[!UICONTROL Content]_ section of the banner settings.

   ![Banner settings - message text](./assets/pb-tutorial1-banner-settings-content-message-text.png){width="600" zoomable="yes"}

1. Continuing in the _[!UICONTROL Content]_ section, set the banner link and button:

   - Set **Link** to `Category`, and then click **[!UICONTROL Select]** to show the category tree.

   - Choose `What's New` as the linked category.

      ![Banner content - link to category](./assets/pb-tutorial1-banner-settings-link-category-tree.png){width="600" zoomable="yes"}

   - Set **[!UICONTROL Show Button]** to `Always`.

   - For **[!UICONTROL Button Text]**, enter `Shop Now` as the text that appears on the button.

   - For **[!UICONTROL Button Type]**, accept the `Primary` default.

      The button style from the current theme determines the button format.

1. Set the banner overlay:

   You can use an overlay to apply a background color to the active content area that is defined by the Appearance setting. The banner background image remains visible for the full width of the banner.

   - Set **[!UICONTROL Show Overlay]** to `Always`.

   - For **[!UICONTROL Overlay Color]**, do one of the following:

      - Click the color square and choose the white swatch.
      - Click in the _No Color_ text box and enter `White` or the hexadecimal value `#ffffff`.

      Then, click **[!UICONTROL Apply]**.

      ![Banner settings - button overlay color](./assets/pb-tutorial1-banner-settings-overlay-color.png){width="600" zoomable="yes"}

   - Scroll back to the top of the page and click **[!UICONTROL Save]** to save the settings and return to the [!DNL Page Builder] workspace.

      The button appears below the banner message on the stage.

      ![Banner in the content stage with text message and button](./assets/pb-tutorial1-banner-stage-background-color.png){width="600" zoomable="yes"}

1. In the upper-right corner of the stage, click the _Close Full Screen_ (![Close full screen icon](./assets/pb-icon-reduce.png)) icon.

   Clicking this icon returns you to the _[!UICONTROL Content]_ section for the page with the preview displayed.

   You can toggle between the two workspace modes at any time you want.

1. In the upper-right corner, click the **[!UICONTROL Save]** arrow and choose **[!UICONTROL Save & Close]**.

1. If prompted, click the [Cache Management](../systems/cache-management.md) link in the message at the top of the page and refresh any invalid cache.

## Part 2: Contained row with two equal columns

In this part of the exercise, you add a row to the page, and divide the row into two equal columns. Then, you add a linked image to each column. In the instructions, each new row is added before the first row to make the [!DNL Page Builder] panel line up with the stage. At the end of the exercise, you rearrange the rows so they match the Simple Page example.

![Example page using contained row with two equal columns](./assets/pb-tutorial1-contained-row-with-two-equal-columns.png){width="600" zoomable="yes"}

### Step 1: Add a row

1. In the Pages grid, find the _Simple Page_ that you created in the first part of this exercise and select **[!UICONTROL Edit]** in the _[!UICONTROL Action]_ column.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Content]** section.

1. Click **[!UICONTROL Edit with Page Builder]** or inside the content preview area.

1. In the [!DNL Page Builder] panel under _[!UICONTROL Layout]_, drag a **[!UICONTROL Row]** placeholder to the stage and place it above the banner.

   The red guideline marks the boundary between the two rows.

   ![Adding a new row above the banner](./assets/pb-tutorial1-row-drag-to-stage.png){width="600" zoomable="yes"}

1. Hover over the new row to display the toolbox and choose the _Settings_ ( ![Settings icon](./assets/pb-icon-settings.png){width="20"} ) icon.

   ![Row toolbox](./assets/pb-tutorial1-row-settings.png){width="600" zoomable="yes"}

1. Under _[!UICONTROL Appearance]_, accept the **Contained** default setting.

   This setting limits the content area of the row to the width of the page as defined by the theme.

   ![Keeping the default Contained appearance setting](./assets/pb-tutorial1-row-settings-appearance.png){width="600" zoomable="yes"}

1. In the upper-right corner, click **[!UICONTROL Save]** to save the settings and return to the [!DNL Page Builder] workspace.

### Step 2: Add a column

1. In the [!DNL Page Builder] panel under _[!UICONTROL Layout]_, drag a **[!UICONTROL Column]** placeholder to the new row.

   ![Dragging a column content type to the stage](./assets/pb-tutorial1-column-drag-to-stage.png){width="600" zoomable="yes"}

   The row is now divided into two columns of equal width. Each column is a separate container for content with its own dedicated toolbox of options.

   ![Row with two columns of equal width](./assets/pb-tutorial1-columns-equal-width.png){width="600" zoomable="yes"}

1. In the upper-left corner of the first column, click the circular _Grid_ control (![Grid control](./assets/pb-icon-grid-control.png)) to show the grid guidelines.

   The grid ensures that content is aligned consistently, and that it renders correctly on both desktop and mobile devices. For information about configuring the grid size, see the [Configure [!DNL Page Builder]](setup.md#configure-page-builder) section in the [!DNL Page Builder] Setup topic.

   The numbers in parentheses (6/12) in the top border of each column container indicate the number of grid divisions in each column, and the total number of divisions in the row.

   ![Displaying grid size details for the column](./assets/pb-tutorial1-columns-grid-size.png){width="600" zoomable="yes"}

### Step 3: Add images with links

In this step, you learn how to upload an image to the banner.

1. In the [!DNL Page Builder] panel, expand the **[!UICONTROL Media]** section and drag an **[!UICONTROL Image]** placeholder to the first column.

   ![Dragging the image content type to first column](./assets/pb-tutorial1-column1-media-image-drag.png){width="600" zoomable="yes"}

1. Insert the sample image into the placeholder.

   ![Image placeholder](./assets/pb-tutorial1-column-image-upload.png){width="600" zoomable="yes"}

   For am image that is located on your system, you can choose either of these methods:

   - **Upload the image file**: In the first column, click **[!UICONTROL Upload Image]**. Then, navigate to the directory where you saved the extracted simple page assets and choose the `small-banner-1.jpg` file.

      ![Uploaded image added to the first column](./assets/pb-tutorial1-column1-image.png){width="600" zoomable="yes"}

      Repeat this action to add the `small-banner-2.jpg` file to the second column.

   - **Drag the image file**: On your desktop, open the simple page assets folder and position it alongside the Admin browser window where you are working with the [!DNL Page Builder] stage. Then, drag the file `small-banner-1.jpg` from the simple page assets folder, and drop it in the first column.

      ![Dragging the image onto the second column](./assets/pb-tutorial1-column-image-drag.png){width="600" zoomable="yes"}

      Repeat this action to add the `small-banner-2.jpg` file to the second column.

1. Determine which page from your catalog that you want to link to each image.

1. Hover over the image in the first column to display the toolbox and choose the _Settings_ ( ![Settings icon](./assets/pb-icon-settings.png){width="20"} ) icon.

   ![Image toolbox](./assets/pb-tutorial1-column1-image-settings.png){width="600" zoomable="yes"}

1. Link the image to a category:

   - Scroll down and set **Link** to `Category`.

   - In the category tree, drill down and choose the `Men's Hoodies & Sweatshirt` category.

   - In the upper-right corner, **[!UICONTROL Save]** the settings and return to the [!DNL Page Builder] workspace.

1. Repeat the previous step to link the image in the second column to the _Gear_ category.

1. In the upper-right corner of the stage, click the _Close Full Screen_ (![Close full screen icon](./assets/pb-icon-reduce.png)) icon.

   Clicking this icon returns you to the _[!UICONTROL Content]_ section for the page with the preview displayed.

1. In the upper-right corner, click the **[!UICONTROL Save]** arrow and choose **[!UICONTROL Save & Close]**.

1. When prompted, click the [Cache Management](../systems/cache-management.md) link in the message at the top of the page and refresh any invalid cache.

## Part 3: Full-width row with unequal columns

The final row on this page features content from a product review. You add a full-width row and divide it into two columns of different widths. A background image is added to the first column, with a matching background color that is applied to the row for a unified effect.

![Example full width row with columns of different widths](./assets/pb-tutorial1-full-width-row-two-unequal-columns.png){width="500"}

### Step 1: Add a row

1. In the Pages grid, find the _Simple Page_ that you created in the first part of this exercise and select **[!UICONTROL Edit]** in the _[!UICONTROL Action]_ column.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Content]** section.

1. Click **[!UICONTROL Edit with Page Builder]** or inside the content preview area.

1. In the [!DNL Page Builder] panel under _[!UICONTROL Layout]_, drag a **[!UICONTROL Row]** placeholder to the stage and place it above the row that was created in the second part of this exercise.

   A red guideline marks the boundary between the two rows.

   ![Adding a new row](./assets/pb-tutorial1-add-new-row.png){width="600" zoomable="yes"}

1. Hover over the new row to display the toolbox and choose the _Settings_ (![Settings icon](./assets/pb-icon-settings.png){width="20"} ) icon.

   ![Row toolbox](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

1. On the Edit Row page Under _[!UICONTROL Appearance]_, choose **[!UICONTROL Full Width]**.

   This setting limits the content area to the maximum page width that is defined by the theme. The background color and/or image are not limited, and extend the full width of the row.

   ![Selecting the Full Width appearance](./assets/pb-tutorial1-row-settings-appearance-full-width.png){width="600" zoomable="yes"}

1. In the _[!UICONTROL Background]_ section, enter `#f1f1f1` as the **[!UICONTROL Background Color]**.

   ![Setting the background color](./assets/pb-tutorial1-row-settings-background-color.png){width="600" zoomable="yes"}

1. Scroll down to the _[!UICONTROL Advanced]_ section and set all **Margins & Padding** values to `0`.

   ![Setting the margins and padding](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

1. Scroll back to the top of the page and click **[!UICONTROL Save]** to save the settings and return to the [!DNL Page Builder] workspace.

   The background color of the row is now a pale beige.

   ![Row with the background color in the stage](./assets/pb-tutorial1-row-background-beige.png){width="600" zoomable="yes"}

### Step 2: Add columns of different widths

1. In the [!DNL Page Builder] panel under _[!UICONTROL Layout]_, drag a **[!UICONTROL Column]** placeholder to the top row on the stage.

   ![Dragging a column to the stage](./assets/pb-tutorial1-column-drag.png){width="600" zoomable="yes"}

1. Drag the right border of the first column to the four of 12 (`4/12`) position on the grid.

   The size of the second column adjusts to eight of 12 (`8/12`).

   ![Resizing the first column](./assets/pb-tutorial1-column-first-4.png){width="600" zoomable="yes"}

1. Hover over the first column container to display the toolbox and choose the _Settings_ ( ![Settings icon](./assets/pb-icon-settings.png){width="20"} ) icon.

1. Scroll down to the _[!UICONTROL Advanced]_ section and set all **Margins & Padding** values to `0`.

   ![Setting the margins and padding](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

1. Scroll back to the top of the page and click **[!UICONTROL Save]** to save the settings and return to the [!DNL Page Builder] workspace.

### Step 3: Add an image to the first column

1. In the [!DNL Page Builder] panel, expand **[!UICONTROL Media]** and drag an **[!UICONTROL Image]** content type to the first column.

   ![Dragging an image content type to the first column](./assets/pb-tutorial1-column1-image-drag.png){width="600" zoomable="yes"}

1. In the image placeholder, click **[!UICONTROL Upload Image]**.

   ![Upload Image](./assets/pb-tutorial1-column1-image-upload.png){width="600" zoomable="yes"}

1. Navigate to the directory where you saved the extracted simple page assets and choose the `review-image.jpg` file.

   The uploaded image appears in the first column, and blends seamlessly with the background color of the row.

   ![Uploaded image added to the column](./assets/pb-tutorial1-column1-image-uploaded.png){width="600" zoomable="yes"}

### Step 4: Add review content to the second column

The second column of the row should contain content from a customer review, including the five-star rating image and formatted text message.

1. In the [!DNL Page Builder] panel, expand the **[!UICONTROL Elements]** section and drag the **[!UICONTROL Text]** content type to the second column.

   ![Dragging the text content type to the stage](./assets/pb-tutorial1-column2-text-drag.png){width="600" zoomable="yes"}

1. Click in the text element to display the editor toolbar.

1. In the toolbar, click the _Insert Image_ (![Insert image icon](./assets/editor-btn-insert-edit-image.png)) icon and do the following:

   ![Inserting an image in the text](./assets/pb-tutorial1-column2-editor-toolbar-insert-image.png){width="600" zoomable="yes"}

   - In the _[!UICONTROL Insert/edit image]_ dialog, click the _Find_ ( ![Find icon](./assets/editor-btn-find-source.png) ) icon next to the _[!UICONTROL Source]_ field.

      ![Insert/edit image dialog](./assets/pb-tutorial1-column2-text-insert-edit-image.png){width="600" zoomable="yes"}

   - On the _[!UICONTROL Select Images]_ page, click **[!UICONTROL Choose Files]**.

   - In the folder where you saved the simple page assets, choose `rating.png`.

   - Back on the page, double-click the image tile to select it and insert its URL into the Source field.

      ![Choosing the image on the page](./assets/pb-tutorial1-column2-editor-gallery-select-image.png){width="600" zoomable="yes"}

   - For **[!UICONTROL Image Description]**, enter `5-Star Rating` and click **[!UICONTROL OK]** to insert the image into the column.

   - In the editor toolbar, click **Align Center** (![Align center button](./assets/editor-btn-align-center.png)) to center the image in the column.

      ![Centered rating image](./assets/pb-tutorial1-column2-5stars-centered.png){width="600" zoomable="yes"}

1. Position the insertion point just after the five-star image, press the Enter/Return key to start a new line, and enter the following text:

   `Awesome Tank!`

   `I'm a long distance runner and it keeps me pretty comfortable, although these companies always act like their shirts are magical and really it's just pretty basic stuff. Still it's a great shirt, and I would recommend it.`

   `Antonia Racer Tank – Reviewed by Allyson`

   The text is centered as you type.

   ![Review text centered in the column](./assets/pb-tutorial1-column2-text-unformatted.png){width="600" zoomable="yes"}

1. Format the text:

   - Click anywhere in the first line of text and on the editor toolbar under **Formats**, choose `Heading 2`.

   - Select the remaining text and on the editor toolbar under **Formats**, choose `Paragraph`.

   The text is formatted according to the style sheet that is associated with the theme.

1. Get the dimensions of the image so that you can center the content vertically in the column:

   - Hover over the image in the first column to display the toolbox and choose the _Settings_ (![Settings icon](./assets/pb-icon-settings.png){width="20"} ) icon.

   - Below the thumbnail of the image, take note of the dimensions of the image.

      ![Image dimensions displayed below the thumbnail](./assets/pb-tutorial1-column1-image-dimensions.png){width="600" zoomable="yes"}

   - In the upper-right corner, click **Close**.

1. Center the content vertically in the second column:

   - Hover over the second column to display the toolbox and choose the _Settings_ (![Settings icon](./assets/pb-icon-settings.png){width="20"} ) icon.

   >[!NOTE]
   >
   >Make sure to select the column container rather than the Text container to display the correct toolbox.

   - For **[!UICONTROL Minimum Height]**, enter `450` as the height in pixels for the image in the first column.

   - Set **[!UICONTROL Vertical Alignment]** to `Center`.

   ![Setting the minimum height and vertical alignment](./assets/pb-tutorial1-column2-layout-vertical-alignment.png){width="600" zoomable="yes"}

1. Scroll down to the _[!UICONTROL Advanced]_ section and set all **[!UICONTROL Margins and Padding]** values to zero ( `0` ).

   ![Setting the margins and padding](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

1. Scroll back to the top of the page and in the upper-right corner, click **[!UICONTROL Save]** to save the settings and return to the [!DNL Page Builder] workspace.

   ![Row with review content on the stage](./assets/pb-tutorial1-row-reviw-content.png){width="600" zoomable="yes"}

### Step 5: Insert a catalog product link

1. Select the `Antonia Racer Tank` text and click the _Insert Link_ (![Insert link icon](./assets/editor-btn-insert-edit-link.png)) icon in the editor toolbar.

1. In the _Insert link_ dialog, specify the link to the catalog product:

   - Enter the product **[!UICONTROL URL]**.

      You can enter either a relative or fully qualified URL. The following relative link is entered for this example:

      `../antonia-racer-tank.html`

   - (Optional) For **Title**, enter the product name.

      The Title link attribute is used by some browsers as a tooltip.

      ![Inserting a link in the text](./assets/pb-tutorial1-text-link-insert.png){width="600" zoomable="yes"}

   - When complete, click **[!UICONTROL OK]** to save the link.

      The linked text is now highlighted in the banner.

      ![Banner with linked text](./assets/pb-tutorial1-text-link-highlight.png){width="600" zoomable="yes"}

1. In the upper-right corner of the stage, click the _Close Full Screen_ (![Close full screen icon](./assets/pb-icon-reduce.png)) icon.

   Clicking this icon returns you to the _[!UICONTROL Content]_ section for the page with the preview displayed.

1. In the upper-right corner, click **[!UICONTROL Save]**.

### Step 6: Rearrange the rows

With all three rows complete, the final step is to rearrange the rows to match the original _Simple Page_ example. To match the original example, the first row must be moved to the bottom, and the last row must be moved to the top.

1. If necessary, expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Content]** section.

1. Click **[!UICONTROL Edit with Page Builder]** or inside the content preview area.

1. Hover over the first row on the stage to display the toolbox and choose the _Move_ ( ![Move icon](./assets/pb-icon-move.png)) icon.

   ![Move](./assets/pb-tutorial1-row-toolbox-move.png){width="600" zoomable="yes"}

1. Hold down the mouse button as you verify that all content in the row is selected and drag the row into position below the red guideline at the bottom of the page.

   >[!NOTE]
   >
   >If you accidentally move only part of the content — such as the image — simply move the content back where it belongs, and try again.

   ![Moving a row on the stage](./assets/pb-tutorial1-row-toolbox-move-to-position.png){width="600" zoomable="yes"}

1. Repeat this process to move the first row to the second position.

   The order of the rows on your page now matches the Simple Page example.

1. In the upper-right corner of the stage, click the _Close Full Screen_ (![Close full screen icon](./assets/pb-icon-reduce.png)) icon.

   Clicking this icon returns you to the _[!UICONTROL Content]_ section for the page with the preview displayed.

1. In the upper-right corner, click the **[!UICONTROL Save]** arrow and choose **[!UICONTROL Save & Close]**.

1. If prompted, click the [Cache Management](../systems/cache-management.md) link in the message at the top of the page and refresh any invalid cache.

You have completed the Simple Page exercise. Keep the work that you created, so you can refer to it later.

When you are ready, proceed to [Part 2: Blocks](2-blocks.md).
