---
title: Media Gallery image optimization
description: Learn how to use image optimization for your [!DNL Commerce] media assets.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
---
# Media Gallery image optimization

The new [Media Gallery](media-gallery.md) provides an _image optimization_ feature, which improves performance and decreases media file sizes on the storefront. This optimization is enabled by default and can be modified in the store configuration settings.

## Configure image optimization

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL System]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** and do the following:

   - Set **[!UICONTROL Enable Image Optimization]** to `Yes`.
   - Enter the **[!UICONTROL Maximum Width]** and **[!UICONTROL Maximum Height]** values (in pixels) according to your needs.

## Behavior

When Media Gallery image optimization functionality is enabled, an optimized copy of an image is automatically inserted in the content from the [Media Gallery](media-gallery.md) instead of the original file.

When the _Maximum Width_ and _Maximum Height_ values are changed in the configuration, it updates all the existing optimized images that were previously inserted.

The Media Gallery Image Optimization requires that the `media.gallery.renditions.update` queue consumers are running for regenerating optimized images when configuration is changed. See [Manage message queues](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) in the _Configuration Guide_ for more details.
