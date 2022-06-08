---
title: Translate a Content Page
description: Placeholder
---
# Translate a Content Page

If your store has multiple views in different [languages](https://docs.magento.com/user-guide/stores/store-language-add.html), and you have set the locale for each view to a different language, the result is a partially translated site. The next step is to create a translated version of each page that is available from the specific store view. The Store View column of the _Manage Pages_ list shows each view that has a translated version of the page.

To translate a content page, you must create a new page that has the same URL Key as the original, but is assigned to the specific store view. Then, update the page for the specific view with the translated text. The following example shows how to create a translated version of the About Us page for the Spanish store view.

## Step 1: Copy the URL key for the page to be translated

1. On the _Admin_ sidebar, go to **Content** > _Elements_ > **Pages**.

1. In the grid, find the page to be translated and open in _edit_ mode.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Search Engine Optimization** section and copy the **URL Key** to the clipboard.

1. Click **Back** in the top button bar to return to the _Pages_ grid.

## Step 2: Add a new page for the translated content

1. Click **Add New Page**.

1. Enter the translated **Page Title**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Content** section and complete the translated text for the page.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Search Engine Optimization** section and do the following:

   - Paste the **URL Key** that you copied from the original page.

   - Enter the translated text for the **Meta Title**, **Meta Keywords**, and **Meta Description**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Page in Websites** section and set **Store View** to the store view where the page is to be available.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the  **Design** section and set the column **Layout** of the page.

1. Click **Save**.

1. When prompted, refresh any invalid [caches](https://docs.magento.com/user-guide/system/cache-management.html).

## Step 3: Verify the translation

To verify the translation, go to the storefront and use the language chooser to change the store view.

Notice that there are still some elements on the page that need to be translated, including the company footer links[ block](block-add.md), the [welcome message](../getting-started/storefront-branding.md#change-the-welcome-message), and [product information](https://docs.magento.com/user-guide/catalog/product-translate.html).
