---
title: Media Gallery Asset Management
description: Learn how to manage uploaded media files, and those that you acquire through an Adobe Stock integration.
---
# Media Gallery Asset Management

The new [Media Gallery](media-gallery.md) provides tools for managing uploaded media files, as well as those that you acquire through an [Adobe Stock integration][adobe-stock-integration]. If you have saved an Adobe Stock [image preview][save-preview], you can also [license][stock-license] the image in the new Media Gallery.

## Upload an asset

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Media]_ > **[!UICONTROL Media Gallery]**.

1. Click **[!UICONTROL Upload Image]**.

1. Select the file to be uploaded.

   The selected asset will automatically be uploaded to the selected folder (or to the storage root if no folder is selected).

## View asset details

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Media]_ > **[!UICONTROL Media Gallery]**.

1. Click the three dots below the asset (![Details icon](./assets/media-gallery-asset-menu-icon.png)), then click **[!UICONTROL View Details]**.

    ![Asset Actions](./assets/media-gallery-asset-actions.png)<!-- zoom -->

    The asset details will be displayed on a slide panel. They include the information where the asset is being used:

   - **[!UICONTROL Categories]**
   - **[!UICONTROL Products]**
   - **[!UICONTROL Pages]**
   - **[!UICONTROL Blocks]**

    ![Asset Details](./assets/media-gallery-asset-details.png)<!-- zoom -->

    Click the **[!UICONTROL Used In]** links to see the details. The grid in the following example shows all categories where a specific asset is used.

    ![Category Grid](./assets/media-gallery-asset-categories.png)<!-- zoom -->

    It is also possible to delete the asset from the _View Details_ section.

## Edit an asset

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Media]_ > **[!UICONTROL Media Gallery]**.

1. Click the three dots below the asset (![Asset menu icon](./assets/media-gallery-asset-menu-icon.png)), then click **[!UICONTROL Edit]**.

    ![Edit Asset](./assets/media-gallery-edit-asset.png)<!-- zoom -->

1. If needed, change one of the following metadata values:

   - **[!UICONTROL Title]**
   - **[!UICONTROL Description]**
   - **[!UICONTROL Tags/Keywords]**

   This data will be saved to the data base as well as to the file metadata itself. Currently, XMP and IPTC formats are supported.

   You can download the image with the updated metadata.

## Use an asset

Assets can be used extensively throughout the Admin, such as [add or edit a page][add-edit-page], [create or edit a category][create-edit-category], or [insert images from the Content Editor][editor-insert-media].

1. Access the new Media Gallery from an area that allows you to use media assets.

1. Select the asset and click **[!UICONTROL Add Selected]**.

    ![Add Selected](./assets/media-gallery-selected-assets.png)<!-- zoom -->

## Delete assets

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Media]_ > **[!UICONTROL Media Gallery]**.

1. Click **[!UICONTROL Delete Images...]** and select the checkbox for each asset that you want to delete.

1. In the confirmation dialog, click **[!UICONTROL Delete Image]**.

    ![Delete Confirmation](./assets/media-gallery-bulk-delete-confirm.png)<!-- zoom -->

## Search for assets

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Media]_ > **[!UICONTROL Media Gallery]**.

1. Use the **Search by keywords** input to perform image search by keywords/tags.
[!UICONTROL ]
    The search in the following example finds assets that contain a specific tag (`mountain`).

    ![Asset Search](./assets/media-gallery-asset-search.png)<!-- zoom -->

>[!NOTE]
>
>See the [Edit an asset][edit-asset] section to learn how you can update image tags.

## Filtering assets

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Media]_ > **[!UICONTROL Media Gallery]**.

1. Click the **[!UICONTROL Filters]** tab.

    ![Filters](./assets/media-gallery-filters.png)<!-- zoom -->

1. Set the filtering options.

   You can filter the assets according to usage by the entities:

   - **[!UICONTROL Used in Categories]**
   - **[!UICONTROL Used in Products]**
   - **[!UICONTROL Used in Pages]**
   - **[!UICONTROL Used in Blocks]**

   You can also filter the assets by **[!UICONTROL Store View]**, **[!UICONTROL License Status]**, and **[!UICONTROL Content Status]**. Set a date rage for **[!UICONTROL Uploaded Date]** and/or **[!UICONTROL Modification Date]** to filter assets according to file dates.

1. Click **[!UICONTROL Apply Filters]** to see the results.

   The filtering in the following example finds assets that are used in a specific category (`cars`) and are enabled.

    ![Filter for Enabled Assets by Category](./assets/media-gallery-filter-by-category.png)<!-- zoom -->

## Finding image duplicates

1. Click the **[!UICONTROL Filters]** tab and select the **[!UICONTROL Show duplicates]** checkbox.

1. Click **[!UICONTROL Appply Filters]** to see the results.

    ![Show Duplicates](./assets/media-gallery-filter-duplicates.png)<!-- zoom -->

[adobe-stock-integration]: adobe-stock.md
[save-preview]: adobe-stock-save-preview.md
[stock-license]: adobe-stock-license-image.md
[add-edit-page]: page-add.md
[create-edit-category]: https://docs.magento.com/user-guide/catalog/category-create.html
[editor-insert-media]: editor-insert-image.md
[edit-asset]: #edit-an-asset
