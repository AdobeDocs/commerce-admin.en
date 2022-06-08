---
title: Add a Rotating Dynamic Block
description: Placeholder
---
# Add a Rotating Dynamic Block

{{ee-feature}}

Multiple [dynamic blocks](dynamic-blocks.md) can be added to a rotator to present a slide show of interactive content. The [Widget](widgets.md) tool is used to place the rotator at a specific place on a either a single page, or on multiple pages throughout your store.

![Dynamic block rotator](./assets/widget-dynamic-block-rotator.png)<!-- zoom -->

## Step 1: Create individual dynamic blocks

Follow the instructions to [create the dynamic blocks](dynamic-blocks.md) that you want to place in the rotator.

## Step 2: Add a dynamic block rotator widget

1. On the _Admin_ sidebar, go to **Content** > _Elements_ > **Widgets**.

1. In the upper-right corner, click **Add Widget**.

1. Under _Settings_, set **Type** to `Dynamic Blocks Rotator`.

1. Choose the current **Design Theme** of the store.

   This identifies the current package or [theme](themes.md) that determines the page layout of the store.

1. Click **Continue**.

   ![Dynamic block rotator settings](./assets/widget-dynamic-block-rotator-settings.png)<!-- zoom -->

## Step 3: Complete the options

1. Under _Storefront Properties_, set the options:

   - Enter a **Title** for the rotator.

   - In the **Assign to Store Views** list, select the [store view(s)](https://docs.magento.com/user-guide/stores/websites-stores-views.html) where the rotator is available.

   - (Optional) Enter a **Sort Order** number to determine the position of the rotator in the target container. This is relative to other widgets that might be assigned to the same container.

   ![Rotator storefront properties](./assets/widget-dynamic-block-rotator-storefront-properties.png)<!-- zoom -->

1. Under _Layout Options_, click **Add Layout Update** and do the following:

   - Set **Display on** to the page, or type of page, where the rotator is to appear.

      - `Categories` - Displays the rotator on either [anchor](https://docs.magento.com/user-guide/catalog/navigation-layered.html) or non-anchor category pages. Options: Anchor Categories / Non-Anchor Categories
      - `Products` - Displays the rotator on either a specific type of product page, or on all product pages. Options: All Product Types / [Simple Product](https://docs.magento.com/user-guide/catalog/product-create-simple.html) /  [Virtual Product](https://docs.magento.com/user-guide/catalog/product-create-virtual.html) / [Bundle Product](https://docs.magento.com/user-guide/catalog/product-create-bundle.html) / [Downloadable Product](https://docs.magento.com/user-guide/catalog/product-create-downloadable.html) / [Gift Card](https://docs.magento.com/user-guide/catalog/product-gift-card.html) / [Configurable Product](https://docs.magento.com/user-guide/catalog/product-create-configurable.html) / [Grouped Product](https://docs.magento.com/user-guide/catalog/product-create-grouped.html)
      - `Generic Pages` - Displays the rotator on all pages, a specific page, or only on pages with a certain layout. Options: All Pages / Specified Page / Page Layouts

      In this example, the rotator is to be placed on a `Specified Page`.

   - Select the specific **Page** where the rotator is to appear.

   - Set **Container** to the part of the [page layout](page-layout.md#standard-page-layouts) where the rotator is to appear.

      If other widgets are assigned to the same container, they appear in sequence according to the sort order.

   - Accept `Dynamic Block Template` as the default **Template**.

      This determines the template that is used to format the rotator, based on whether the rotator is to stand alone, or be placed inside existing text.

      ![Rotator layout updates](./assets/widget-dynamic-block-rotator-layout-updates.png)<!-- zoom -->

   - Click **Save and Continue Edit**.

1. In the left panel, choose **Widget Options**.

1. For the **Dynamic Blocks to Display**, accept `Specified Dynamic Blocks`.

   This setting determines the type of dynamic blocks are included in the rotator.

   - `Specified Dynamic Blocks` - Includes only specific dynamic blocks.
   - `Cart Price Rule Related` - Includes only dynamic blocks that are associated with a cart price rule.
   - `Catalog Price Rule Related` - Includes only dynamic blocks that are associated a with catalog price rule.

1. To **Restrict the Dynamic Block Types** that can be used with the widget, select `Content Area`.

   This limits the banner to a specific part of the page layout.

   - `Content Area` - Places the dynamic block in the main content area of the page.
   - `Footer` - Places the dynamic block in the page footer.
   - `Header` - Places the dynamic block in the page header.
   - `Left Column` - Places the dynamic block in the left column of the page layout, if available.
   - `Right Column` - Places the dynamic block in the right column of the page layout, if available.

1. Set **Rotation Mode** to one of the following:

   - `Display all instead of rotating` - Displays a stack of dynamic blocks, where all are visible.
   - `One at a time, Random` - Displays the specified dynamic blocks in a random order. When the page is refreshed, a different (and random) dynamic block appears.
   - `One at the time, Series` - Displays the specified dynamic blocks in the sequence they were added. When the page is refreshed, the next dynamic block in the sequence appears.
   - `One at the time, Shuffle` - Displays one dynamic block at a time in a shuffled order. This option is similar to the `One at a time, Random` option, except that the same dynamic block is not repeated.

   ![Rotator widget options](./assets/widget-dynamic-block-rotator-widget-options.png)<!-- zoom -->

1. In the **Specify Dynamic Blocks** grid, select the checkbox of each dynamic block that you want to include in the rotator.

1. When complete, click **Save**.
