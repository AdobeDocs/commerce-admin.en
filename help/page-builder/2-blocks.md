---
title: 'Walkthrough Part 2: Blocks'
description: Learn the difference between simple blocks and dynamic blocks when using Page Builder.
---
# Walkthrough Part 2: Blocks

The following exercise illustrates the difference between [simple blocks](https://docs.magento.com/user-guide/cms/blocks.html) and [dynamic blocks](dynamic-block.md), and how to use Page Builder to create each type of block.

>[!NOTE]
>
>Page Builder has a new content type called _Banner_, which is featured in the first walkthrough exercise and is unrelated to the previous banner functionality. What was previously the Banner option in the [Content menu](https://docs.magento.com/user-guide/cms/content-menu.html), is now _Dynamic Block_.

![Dynamic block in the storefront](./assets/pb-tutorial2-dynamic-block-storefront.png)<!-- zoom -->

This exercise assumes that you have completed [Part 1: Simple Page](1-simple-page.md), including the prerequisites and downloaded sample files. Follow the parts of this walkthrough exercise in order.

>[!NOTE]
>
>These walkthrough exercises are updated to reflect recent changes to the Page Builder workspace in the 2.4.1 release. If you are using an earlier Adobe Commerce release, use the Page Builder exercises included in the [Commerce 2.3 User Guide](https://docs.magento.com/user-guide/v2.3/cms/page-builder-learn.html).

## Part 1: Create a simple block

In this walkthrough exercise, you create a simple block with content from Google Maps. Simple blocks are sometimes called _CMS blocks_ or _static blocks_, because the content does not change. A simple block is ideal for content that you might want to reuse.

### Step 1: Create a block

1. On the _Admin_ sidebar, go to **Content** > _Elements_ > **Blocks**.

1. In the upper-right corner, click **Add New Block**.

1. For **Block Title**, enter `Google Map`.

1. For **Identifier**, enter `google-map`.

1. Choose the **Store View** where the block is to be available.

   ![Block Information](./assets/pb-tutorial2-block-new-google-map.png)<!-- zoom -->

1. In the upper-right corner, click **Save**.

### Step 2: Add a [!DNL Google Map]

1. Scroll down to the Page Builder content preview (currently empty) and click **Edit with Page Builder**.

1. In the Page Builder panel, expand **Media** and drag a **Map** placeholder to the stage.

   ![Dragging a map to the stage](./assets/pb-media-map-drag.png)<!-- zoom -->

   A map to your store location appears if [!DNL Google Maps] is configured for your store.

   ![Configured Google Map for your store](./assets/pb-tutorial2-google-map.png)<!-- zoom -->

   A placeholder map appears if Google Maps isn’t yet configured for your store.

   ![Google Maps placeholder](./assets/pb-tutorial2-media-map-not-configured.png)<!-- zoom -->

1. In the upper-right corner of the stage, click the _Close Full Screen_ (![Close full screen icon](./assets/pb-icon-reduce.png)) icon.

   Clicking this icon returns you to the _Content_ section for the block with the preview displayed.

1. In the upper-right corner, click the **Save** arrow and choose **Save & Close**.

### Step 3: Configure Google Maps

If Google Maps is already configured for your store, you can skip this step and proceed to the next.

1. Go to the [Google Cloud Platform Console](https://console.cloud.google.com/google/maps-apis/overview).

1. Click the project drop-down and select or create the project for which you want to add an API key.

1. To configure your API credentials, follow the [instructions][1] in the [!DNL Google Maps] documentation.

1. Copy your API Key to the clipboard.

1. Return to the Commerce Admin and go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel under _General_, choose **Content Management**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) **Advanced Content Tools**.

   ![Advanced Content Tools](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

   For more information about the Content Management Advanced Tools configuration options, see the [Configuration Reference Guide](https://docs.magento.com/user-guide/configuration/general/content-management.html).

1. For **Google Maps API Key**, paste the key you copied.

1. Click **Test Key**.

   If there is a problem with your key, return to the Google Maps Platform site to resolve the problem. Then, try again.

1. After your key is verified, click **Save Config**.

### Step 4: Add the block to a page

1. On the _Admin_ sidebar, go to **Content** > _Elements_ > **Pages**.

1. In the grid, find the _Simple Page_ that you created in the first tutorial and select **Edit** in the _Action_ column.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Content** section and click **Edit with Page Builder** or inside the content preview area.

1. In the Page Builder panel under _Layout_, drag a **Row** placeholder to the top of the stage.

   ![Adding the row to the top of the stage](./assets/pb-tutorial2-elements-row-drag-top.png)<!-- zoom -->

1. In the Page Builder panel, expand **Add Content** and drag a **Block** placeholder to the new row.

1. Hover over the empty block container to display the toolbox and choose the _Settings_ (![Settings icon](./assets/pb-icon-settings.png)<!-- width="20px" --> ) icon.

   ![Block toolbox](./assets/pb-add-content-block-toolbox.png)<!-- zoom -->

1. On the Edit Block page, click **Select Block**.

   ![Select Block](./assets/pb-add-content-block-settings-block-select.png)<!-- zoom -->

1. In the search box, enter `map` and press the Enter/Return key to find the block that you created.

   ![Find Block in List](./assets/pb-add-content-block-settings-block-find.png)<!-- zoom -->

1. In the grid, click **Select** to choose the Google Maps block.

1. In the upper-right corner, click **Save** to save the settings and return to the Page Builder workspace.

1. In the upper-right corner of the stage, click the _Close Full Screen_ (![Close full screen icon](./assets/pb-icon-reduce.png)) icon.

   Clicking this icon returns you to the _Content_ section for the page with the preview displayed.

1. In the upper-right corner, click the **Save** arrow and choose **Save & Close**.

   ![Choosing the Save & Close option](./assets/pb-tutorial1-save-and-close.png)<!-- zoom -->

**Congratulations!** You have completed the first part of the Block exercise. Make sure to keep your work for reference.

## Part 2: Create a dynamic block

A dynamic block includes logic that determines where, when, and to whom it appears. In this walkthrough exercise, you create a dynamic block for a promotion that is triggered when price rule conditions are met, and that appears only to a specific customer segment. The result of this example is similar to the banner that was created in the first exercise, but with logic that controls when it appears in the storefront.

![Sample Luma tee promotion](./assets/pb-tutorial2-dynamic-block-row-page.png)<!-- zoom -->

### Step 1: Create a new dynamic block

1. On the _Admin_ sidebar, go to **Content** > _Elements_ > **Dynamic Blocks**.

   ![Dynamic Blocks list](./assets/pb-tutorial2-block-dynamic-add.png)<!-- zoom -->

1. In the upper-right corner, click **Add Dynamic Block**.

   ![New Dynamic Block page](./assets/pb-tutorial2-block-dynamic-new.png)<!-- zoom -->

1. Complete the basic settings for the new dynamic block:

   - Set **Enable Dynamic Block** to `Yes`.

   - For **Dynamic Block Name**, enter `Tee Shirt Promo`.

   - Set **Dynamic Block Type** to `Content Area` and click **Done**.

      The Dynamic Block Type determines where in the [page layout](https://docs.magento.com/user-guide/design/page-layout-standard.html) that the block is placed. When setting up a dynamic block for your store, consider both the [page layout](https://docs.magento.com/user-guide/design/page-layout.html) and the [theme](https://docs.magento.com/user-guide/design/themes.html), so you can put the available space to good use. Some stores have an active content area that is limited to a fixed width, while others extend the full width of the screen.

      ![Dynamic Block Type setting](./assets/pb-dynamic-block-type.png)<!-- zoom -->

   - For **Customer Segment**, select the checkbox of each segment that you want to apply to the dynamic block and click **Done** to save the list of segments.

      For the following example, there are two [customer segments](https://docs.magento.com/user-guide/marketing/customer-segments.html) that identify registered customers by gender. This dynamic block appears only to registered female customers who are logged in to their accounts while they shop in your store.

      ![Choosing the customer segments](./assets/pb-dynamic-block-customer-segment.png)<!-- zoom -->

### Step 2: Complete the settings

Scroll down to the _Content_ section, which displays an empty Page Builder content preview, and click **Edit with Page Builder**. Then, complete the following tasks:

**Task 1:** Add a background image

1. Hover over the row container to display the toolbox and choose the _Settings_ (![Settings icon](./assets/pb-icon-settings.png)<!-- width="20px" --> ) icon.

1. Under _Appearance_, choose **Full Bleed**.

1. For **Minimum Height**, enter `400px`.

1. Scroll to the _Background_ section and set the **Background Image** by clicking **Select from Gallery** and choosing the `wide-banner-background.png` image uploaded in the first tutorial.

1. In the upper-right corner, click **Save** to apply the settings and return to the Page Builder workspace.

   ![Row with the image](./assets/pb-tutorial2-row-image.png)<!-- zoom -->

**Task 2:** Add columns

In the Page Builder panel under _Layout_, drag a **Column** placeholder onto the row.

![Dragging the column type into the row](./assets/pb-tutorial2-column-drag.png)<!-- zoom -->

The row is now divided into two columns of equal width.

**Task 3:** Add text

1. In the Page Builder panel, expand **Elements** and drag a **Text** placeholder to the second column.

   ![Dragging a text box to the second column](./assets/pb-tutorial2-column-text-drag.png)<!-- zoom -->

1. Enter the following three lines of text into the editor:

   `Even more ways to mix and match.`

   `Buy 3 Luma tees and get a 4th free.`

   `Shop Tees >`

   ![Entering text for the column](./assets/pb-tutorial2-column-text-editor.png)<!-- zoom -->

1. Select all three lines of text and use the toolbar to set the **Line Height** to `40px`.

   ![Setting the line height](./assets/pb-tutorial2-column-text-editor-line-height.png)<!-- zoom -->

1. Set the **Font Size** for each line as follows:

   |Line | Font size |
   |-----| ---------- |
   | Line 1: | `28px` |
   | Line 2: | `24px` |
   | Line 3: | `18px` |

   Because this block could be placed anywhere on the page, use the default paragraph style, rather than heading levels. Also, don't worry that the text does not yet wrap correctly in the column.  

   ![Formatted text](./assets/pb-tutorial2-column-text-editor-text-formatted.png)<!-- zoom -->

**Task 4:** Add a Link

In the first exercise, you learned how to use the [Button](buttons.md) content type to create a link. This example shows how to insert a link from the editor toolbar.

1. In another browser tab, open the storefront and navigate to the page that is to be the target destination for the link.

   You can use the fully qualified URL or a relative URL that omits the reference to your store domain.

   Full URL
   : `https://mystore.com/women/tops-women/tees-women.html`

   Relative URL
   : `../women/tops-women/tees-women.html`

1. Return to the Page Builder workspace tab and text editor, select the `Shop Tees >` text in the third line, and choose **Bold** (![Bold button](./assets/editor-btn-bold.png)) in the editor toolbar.

1. With the `Shop Tees >` text in the third line still selected, choose **Insert/edit link** (![Insert/edit link button](./assets/pb-icon-add-link.png)) in the editor toolbar.

   ![Inserting a link](./assets/pb-tutorial2-column-text-editor-link-insert.png)<!-- zoom -->

1. For **Url**, enter the relative link that you prepared.

1. Set **Target** to `None`.

   This setting opens the page in the same browser window, rather than opening a new tab.

1. For **Title**, enter `Shop Tees`.

   The Title link attribute is used by some browsers as a tooltip.

1. To save the link and return to the Page Builder workspace, click **OK**.

   ![Link details](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png)<!-- zoom -->

1. In the upper-right corner of the stage, click the _Close Full Screen_ (![Close full screen icon](./assets/pb-icon-reduce.png)) icon.

   Clicking this icon returns you to the _Content_ section for the dynamic block with the preview displayed.

1. In the upper-right corner, click **Save**.

### Step 3: Add a price rule

1. Open the _Tee Shirt Promo_ dynamic block in edit mode again.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Related Promotions** section and click **Add Cart Price Rules**.

   ![Related promotions](./assets/pb-dynamic-blocks-related-promotions.png)<!-- zoom -->

1. On the _Add Related Cart Price Rules_ page, select the checkbox for the _Buy 3 tee shirts and get the 4th free_ price rule and click **Add Selected**.

   ![Adding a related cart price rule](./assets/pb-dynamic-block-add-related-cart-price-rules.png)<!-- zoom -->

   The price rule appears in the _Related Promotions_ section, under _Related Cart Price Rule_. You can associate multiple price rules with a dynamic block. However, this simple example uses just one.

   ![Selected cart price rule](./assets/pb-dynamic-block-related-cart-price-rule-list.png)<!-- zoom -->

1. In the upper-right corner, click **Save**.

### Step 4: Add the dynamic block to a page

1. In the _Admin_ sidebar, go to **Content** > _Element_ > **Pages**

1. Find the _Simple Page_ that you created in the [first walkthrough exercise](1-simple-page.md) and open it in edit mode.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Content** section and click **Edit with Page Builder**.

1. Hover over the top row with the same image as the dynamic block to display the toolbox and the _Remove_ (![Remove icon](./assets/pb-icon-remove.png))<!-- width="20px" --> icon.

   To confirm removal of the row from the page, click  **OK** .

1. In the Page Builder panel under _Layout_, drag a new **Row** placeholder to the top of the stage.

1. In the Page Builder panel, expand **Add Content** and drag a **Dynamic Block** placeholder to the new row.

   ![Dragging a dynamic block onto the row](./assets/pb-dynamic-block-drag.png)<!-- zoom -->

1. Hover over the dynamic block container to display the toolbox and choose the _Settings_ (![Settings icon](./assets/pb-icon-settings.png)<!-- width="20px" --> ) icon.

   ![Dynamic block toolbox](./assets/pb-dynamic-block-settings.png)<!-- zoom -->

1. On the _Edit Dynamic Block_ page, click **Select Dynamic Block**.

   ![Select Dynamic Block](./assets/pb-dynamic-block-select.png)<!-- zoom -->

1. Find the _Tee Shirt Promo_ dynamic block that you created and click **Select**.

   A summary of the dynamic block information appears below.

   ![Dynamic block information](./assets/pb-tutorial2-dynamic-block-edit.png)<!-- zoom -->

1. Accept the default **Template**, `Dynamic Block Block Template`.

1. When complete, click **Save** to save the settings and return to the Page Builder workspace.

   ![Dynamic Block in the page preview](./assets/pb-tutorial2-dynamic-block-on-page.png)<!-- zoom -->

1. In the upper-right corner of the stage, click the _Close Full Screen_ (![Close full screen icon](./assets/pb-icon-reduce.png)) icon.

   Clicking this icon returns you to the _Content_ section for the page with the preview displayed.

1. In the upper-right corner, click the **Save** arrow and choose **Save & Close**.

**Congratulations!** You have completed the second part of the Block exercise. Make sure to keep your work for reference.

## Part 3: Update the dynamic block

In this final part of the exercise, you edit a dynamic block while the page is live in your store. Then, log in to the store as a member of the customer segment to make the block appear.

![Sample dynamic block in the storefront](./assets/pb-tutorial2-dynamic-block-storefront.png)<!-- zoom -->

### Step 1: Edit the dynamic block

1. In the _Admin_ sidebar, go to **Content** > _Elements_ > **Dynamic Blocks**.

1. Find your _Tee Shirt Promo_ dynamic block in the grid and open it in edit mode.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Content** section and click **Edit with Page Builder**.

1. Change the column width:

   - Hover over the border between the two columns.

   - Hold down the mouse button and drag the border two divisions to the left.

      ![Grid divisions](./assets/pb-tutorial2-dynamic-block-edit-column-width.png)<!-- zoom -->

      The first column is now four of 12 (4/12) grid divisions wide, and the second column is eight of 12 (8/12) divisions wide.

      ![Two unequal columns](./assets/pb-tutorial2-dynamic-block-edit-column-width-changed.png)<!-- zoom -->

1. Change the text color:

   - Select the first two lines of text.

   - On the editor toolbar, choose **Text Color** and click the **White** swatch.

   ![Text color](./assets/pb-tutorial2-dynamic-block-edit-text-color.png)<!-- zoom -->

1. In the upper-right corner of the stage, click the _Close Full Screen_ (![Close full screen icon](./assets/pb-icon-reduce.png)) icon.

   Clicking this icon returns you to the _Content_ section for the dynamic block with the preview displayed.

1. In the upper-right corner, click **Save**.

### Step 2: View the Dynamic Block

Because this dynamic block is visible only to members of a specific customer segment, you must log in as a customer who is a member of the customer segment to see the promotion. In this example, the block appears only to female customers.

1. Open a browser window to your storefront.

1. To view your sample page, modify the URL in the address bar as follows:

      mystore.com/sample-page

   If your store is configured to include the html suffix, include the suffix as follows:

      mystore.com/sample-page.html

1. Sign in as a female customer:

   - In the upper-right corner of your home page, click **Sign In**.

   - If the sample Luma data is installed on your system, use the following credentials:

      **Email** - `roni_cost@example.com`

      **Password** -  `roni_cost3@example.com`

   - Click **Sign In**.

   - Return to the sample page to see the dynamic block that you created with the Tee Shirt Promo.

   ![Dynamic block displayed for a customer segment](./assets/pb-tutorial2-dynamic-block-storefront.png)<!-- zoom -->

**Congratulations!** You have completed the third part of the Block exercise. Make sure to keep your work for reference.

When you are ready, proceed to [Part 3: Catalog Content](3-catalog-content.md)

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://docs.magento.com/m2/downloads/simple-page-assets.zip
