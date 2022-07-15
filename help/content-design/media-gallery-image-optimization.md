---
title: Media Gallery Image Optimization
description: "Learn how to use image optimization for your [!DNL Commerce] media assets."
---
# Media Gallery Image Optimization

The new [Media Gallery](media-gallery.md) provides an _Image Optimization_ feature, which improves performance and decreases media file sizes on the storefront. This optimization is enabled by default and can be modified in the store configuration settings.

## Configure image optimization

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL System]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** and do the following:

   - Set **[!UICONTROL Enable Image Optimization]** to `Yes`.
   - Enter the **[!UICONTROL Maximum Width]** and **[!UICONTROL Maximum Height]** values (in pixels) according to your needs.

## Behavior

When Media Gallery Image Optimization functionality is enabled, an optimized copy of an image is automatically inserted in the content from the [Media Gallery](media-gallery.md) instead of the original file.

When the _Maximum Width_ and _Maximum Height_ values are changed in the configuration, it updates all the existing optimized images that were previously inserted.

The Media Gallery Image Optimization requires that the `media.gallery.renditions.update` queue consumers are running for regenerating optimized images when configuration is changed. See [Manage message queues](https://devdocs.magento.com/guides/v2.4/config-guide/mq/manage-message-queues.html) documentation for more details.
