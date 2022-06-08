---
title: Media Gallery Image Optimization
description: Placeholder
---
# Media Gallery Image Optimization

The new [Media Gallery](media-gallery.md) provides an _Image Optimization_ feature, which improves performance and decreases media file sizes on the storefront. This optimization is enabled by default and can be modified in the store configuration settings.

## Configure image optimization

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Advanced** and choose **System**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) **Media Gallery Image Optimization** and do the following:

   - Set **Enable Image Optimization** to `Yes`.
   - Enter the **Maximum Width** and **Maximum Height** values (in pixels) according to your needs..

## Behavior

When Media Gallery Image Optimization functionality is enabled, an optimized copy of an image is automatically inserted in the content from the [Media Gallery](media-gallery.md) instead of the original file.

Any time the _Maximum Width_ and _Maximum Heigh_ values are changed in the configuration, it updates all the existing optimized images that were previously inserted.

The Media Gallery Image Optimization requires `media.gallery.renditions.update` queue consumers to be running for regenerating optimized image when configuration is changed. See [Manage message queues](https://devdocs.magento.com/guides/v2.4/https://devdocs.magento.com/guides/v2.4/config-guide/mq/manage-message-queues.html) documentation for more details.
