---
title: Media Gallery image optimization
description: Learn how to use image optimization for your [!DNL Commerce] media assets.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/BTjXX6X70q2Mwm0xPNx-t429R5m93VprCHBDcYgQNpY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
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

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

<!-- Last updated from includes: 2024-01-30 15:43:39 -->
