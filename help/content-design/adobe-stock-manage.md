---
title: Use Adobe Stock Images
description: Placeholder
---
# Use Adobe Stock Images

[Adobe Stock][adobe-stock] images can be used in place of uploading your own image content. One common use case is, when creating a new page, it is desirable to upload and place image content.

The new [Media Gallery](media-gallery.md) provides a direct integration with Adobe Stock, making it easy to license your images directly from the gallery page.

## Access the Adobe Stock search grid

The Adobe Stock search panel is accessible when you [add or edit a page](page-add.md), when you [create or edit a category](https://docs.magento.com/user-guide/catalog/category-create.httml), or when you [insert images via the Content Editor](editor-insert-image.md).

To search Adobe Stock assets and add a stock image to a page:

1. On the _Admin_ sidebar, go to **Content** > _Elements_ > **Pages**.

1. Click **Add a New Page**.

   If you want to edit an existing page, you can use the _Action_ column to click **Select** and choose **Edit**.

1. Expand ![Expansion selector](./assets/icon-display-expand.png) the **Content** section and do the following:

   - If you have the [WYSIWYG editor enabled](editor-configure.md), click **Show/Hide Editor** and then click **Insert Image**.

   - If you have [Page Builder enabled](../page-builder/page-builder-setup.md), expand the **Media** panel and drag an **Image** placeholder to the target container. Then click **Select from Gallery**.

      ![Dragging an image to the Page Builder stage](./assets/pb-media-image-drag.png)<!-- zoom -->

1. Click **Search Adobe Stock**.

To search Adobe Stock assets and add a stock image to a category:

1. On the _Admin_ sidebar, go to **Catalog** > **Categories**.

1. Click **Add Root Category** or **Add Subcategory**.

   If you want to add the image to an existing category, click the category name in the list on the left.

1. Expand the **Content** section, and under **Category Image** click **Select from Gallery**.

1. Click **Search Adobe Stock**.

To search Adobe Stock assets and add a stock image from the WYSIWYG Editor:

1. Click **Show/Hide Editor**.

1. Click **Insert Image**.

1. Click **Search Adobe Stock**.

   ![Adobe Stock search results](./assets/adobe-stock-search-grid.png)<!-- zoom -->

## Filter and search for Adobe Stock assets

The [Adobe Stock Search Grid][access-search] provides querying and filtering functionality to help you find the perfect image for your Commerce stores.

By default, the search results shown are from an Adobe Stock curated gallery of a few hundred results. As soon as you apply your own keyword search, you will be
searching the millions of assets available via Adobe Stock.

### Search for Adobe Stock assets by keywords

1. [Access the Adobe Stock Search grid][access-search].

1. Enter your keyword search into the **Search by keyword** input field in the top-left and click the magnifying glass or press **Enter**.

   ![Adobe Stock Search Results for the "mango" keyword](./assets/adobe-stock-search-keyword.png)<!-- zoom -->

### Filter Adobe Stock assets

1. [Run a keyword search for Adobe Stock assets][search-by-keywords].

1. Click **Filters**.

   There are several filters available to refine your search results:

   |Filter|Description|
   |---|---|
   |Subcategory|Filter for images that are **Photos** or **Illustrations**|
   |Orientation|Filter for images by size, shape, and aspect|
   |Color|Use a color palette to filter for images by color|
   |Price|Filter for images based on their cost|
   |Safe search|Enable or disable Safe search|
   |Isolated Assets|Show only Isolated Assets, which have subjects appear alone on a solid background|

   {style="table-layout:auto"}

   ![Adobe Stock search filters](./assets/adobe-stock-filters.png)<!-- zoom -->

1. Click **Apply Filters**.

   The search result grid is updated with your refined search.

## View image details

Each image has details available for viewing. Additional image-specific actions, such as [saving image previews][save-preview] or [saving (and optionally licensing) images][save-licensed], are available via this detailed view.

1. [Access the Adobe Stock Search grid][access-search].

1. Click an image in the search results.

   Further image details are displayed, such as:

   - A larger version of the image
   - Image metadata, such as _Dimensions_, _File type_, _Category_, _File_, and _Keywords_
   - Related images, such as images from the same _series_ or _model_
   - Action buttons, such as [Save Preview][save-preview] and [Save (and optionally license) Image][save-licensed]

   ![Adobe Stock image details](./assets/adobe-stock-image-details.png)<!-- zoom -->

## Log in to your Adobe account

To gain complete access to an image and eliminate the Adobe Stock watermark, you must [sign in with an Adobe account][adobe-signin] and purchase credits to license rights to use an image.

1. [Access the Adobe Stock Search grid][access-search].

1. Click **Sign In** at the top-right.

   A new browser window guides you through the [Adobe sign-in process][adobe-signin].

   After completing the sign-in process, the [licensed state][licensed-state] of images is displayed in search results as an additional label.

   ![Adobe sign in](./assets/adobe-stock-account-login.png)<!-- zoom -->

### View the licensed state of search results

[Log in to your Adobe account][log-in-to-adobe-account].

All licensed images associated to your Adobe account will have an additional label displayed on them, making it clear which images you have licensed.

![Adobe Stock search results with licensed images](./assets/adobe-stock-licensed-images.png)<!-- zoom -->

### Save images to the Media Storage

Images searched using the Adobe Stock integration can be saved to the Commerce [Media Storage][media-storage] for easy re-use across your Commerce store.

You can save two types of images: an [image preview][save-preview] or a [licensed image][save-licensed].

#### Save an image preview

An image preview is a watermarked version of an Adobe Stock asset. Image previews are free and are a good way to experiment with different images before you decide to purchase a license for specific images and use them on your production stores.

1. [Access the Adobe Stock Search grid][access-search].

1. Click an image in the search grid in order to [view the image details][view-details].

1. Click **Save Preview**.

    This displays a prompt for you to specify a file name that is used to save the image to the [Media Storage][media-storage]. A default file name is provided, but you can customize the name to your preferences.

    ![Save Adobe Stock preview image](./assets/adobe-stock-save-preview.png)<!-- zoom -->

1. Click **Confirm**.

    The page redirects to the [Media Storage][media-storage] and your saved preview is displayed.

#### Save a licensed image

Adobe Stock assets that you want to use for your production Commerce stores should be licensed to ensure you have legal access to the image as well as to eliminate the Adobe Stock watermark that is present on all [image previews][save-preview]. To license images or to save already-licensed images, you must be logged in to your Adobe account.

1. [Log in to your Adobe account][log-in-to-adobe-account].

1. Click an image in the search grid in order to [view the image details][view-details].

1. Depending on the current licensing status of the image, do one of the following:

   - If the image is already licensed, click **Save**.

   - If the image is _not_ licensed, click **License and Save**.

      >[!NOTE]
      >
      >You must have available [Adobe Stock credits][stock-credits] in your account to license the image.

   This displays a prompt for you to specify a file name that is used to save the image to the [Media Storage][media-storage]. A default file name is provided, but you can customize the name to your preferences.

   ![Save Adobe Stock licensed image](./assets/adobe-stock-save-licensed.png)<!-- zoom -->

1. Click **Confirm**.

    The page redirects to the [Media Storage][media-storage] and your saved preview is displayed.

[adobe-stock]: https://stock.adobe.com
[media-storage]: media-storage.md
[access-search]: #access-the-adobe-stock-search-grid
[search-by-keywords]: #search-for-adobe-stock-assets-by-keywords
[view-details]: #view-image-details
[log-in-to-adobe-account]: #log-in-to-your-adobe-account
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[licensed-state]: #view-the-licensed-state-of-search-results
[save-to-media-storage]: #save-images-to-the-media-storage
[save-preview]: adobe-stock-save-preview.md
[save-licensed]: adobe-stock-license-image.md
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
