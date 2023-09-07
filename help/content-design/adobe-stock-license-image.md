---
title: License an Adobe Stock image
description: To ensure you have legal access and to eliminate the Adobe Stock watermark, license your Adobe Stock images.
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
---
# License an Adobe Stock image

Adobe Stock assets that you want to use for your production Adobe Commerce and Magento Open Source stores should be licensed. This licensing ensures you have legal access to the image and to eliminate the Adobe Stock watermark that is present on all [image previews][save-preview]. To license images or to save already-licensed images, you must be logged in to your Adobe account.

The new [[!DNL Media Gallery]](media-gallery.md) provides a direct integration with Adobe Stock, making it easy to license your images directly from the gallery page.

## Prerequisites

This feature requires the [Adobe Stock Integration][adobe-stock-integration] module and configuration. Licensing [Adobe Stock][adobe-stock] images requires a paid Adobe Stock plan and an [Adobe account][adobe-signin].

## License an image from the new [!DNL Media Gallery]

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Media]_ > **[!UICONTROL Media Gallery]**.

1. Follow the steps on [Using Adobe Stock Images][using-adobe-stock] to log in and save preview images to the [media storage][media-storage].

    ![Saved preview image](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. Click the three dots below the image (![Asset menu icon](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), and then click **[!UICONTROL License]**.

    ![Adobe Stock image actions](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >If you are not logged in, the login form appears. For more information about login, see [Using Adobe Stock Images][using-adobe-stock].

1. In the licensing confirmation dialog, click **[!UICONTROL Confirm]** to license the image.

    ![License Confirmation](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >You must have available [Adobe Stock credits][stock-credits] in your account to license the image.

## License an image from the standard media storage

1. [Access the Adobe Stock Search grid][access-search].

1. To [view the image details][view-details], click an image in the search grid in order.

1. Depending on the current licensing status of the image, do one of the following:

   - If the image is already licensed, click **[!UICONTROL Save]**.

   - If the image is _not_ licensed, click **[!UICONTROL License and Save]**.

      >[!NOTE]
      >
      >You must have available [Adobe Stock credits][stock-credits] in your account to license the image.

    This action displays a prompt for you to specify a file name that is used to save the image to the [media storage][media-storage]. A default file name is provided, but you can customize the name to your preferences.

    ![Save Adobe Stock licensed image](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. Click **[!UICONTROL Confirm]**.

    The page redirects to the media storage and your saved preview is displayed.

[adobe-stock-integration]: adobe-stock.md
[media-storage]: media-storage.md
[using-adobe-stock]: adobe-stock-manage.md
[save-preview]: adobe-stock-save-preview.md
[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
