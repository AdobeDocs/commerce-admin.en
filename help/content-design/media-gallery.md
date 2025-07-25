---
title: The [!DNL Media Gallery]
description: Use the Media Gallery to organize and manage your media files on the server.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
---
# The [!DNL Media Gallery]

With Adobe Commerce or Magento Open Source 2.4, merchants can use the new _enhanced_ [!DNL Media Gallery] to organize and manage their media files on the server. This new [!DNL Media Gallery] contains the same functionalities as the existing media storage, but includes an improved user interface and a closer integration with [Adobe Stock][adobe-stock].

![Images displayed in the Media Gallery grid](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Product images added to the [_[!UICONTROL Images and Videos]_ product section](../catalog/product-image.md#upload-an-image) are not managed by the [!DNL Media Gallery]. Only images used in the _[!UICONTROL Content]_ product section fields are displayed and filtered in the new [!DNL Media Gallery].

## Enable the new [!DNL Media Gallery]

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL System]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Advanced configuration - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Enable Old Media Gallery]** to `No`.

1. Click **[!UICONTROL Save Config]**.

1. When prompted, click the **[!UICONTROL Cache Management]** link in the system message and refresh the invalid cache.

   The [[!UICONTROL Content] menu](/help/content-design/content-menu.md) now displays the new _[!UICONTROL Media Gallery]_ option.

>[!NOTE]
>
>Full functionality for new [!DNL Media Gallery] requires `media.gallery.synchronization` and `media.content.synchronization` queue consumers to be started for initial synchronization. See [Manage message queues](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) in the _Configuration Guide_ for more details.

## Access the new [!DNL Media Gallery]

The new [!DNL Media Gallery] is accessible from the Content menu or when you [add or edit a page](/help/content-design/page-add.md). You can also access it when you [create or edit a category](/help/catalog/category-create.md), or when you [insert images using the Content Editor](/help/content-design/editor-insert-image.md).

To access the new [!UICONTROL Media Gallery] through the [!UICONTROL Content] menu:

- On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Media]_ > **[!UICONTROL Media Gallery]**.

To access the new Media Gallery when you are adding or editing a page:

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Elements]_ > **[!UICONTROL Pages]**.

1. Click **[!UICONTROL Add a New Page]**.

   If you want to edit an existing page, you can use the _[!UICONTROL Action]_ column to click **[!UICONTROL Select]** and choose **[!UICONTROL Edit]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Content]** section and do the following:

   - If you have [Page Builder enabled](../page-builder/setup.md), expand the **[!UICONTROL Media]** panel and drag an **[!UICONTROL Image]** placeholder to the target container. Then click **[!UICONTROL Select from Gallery]**.

      ![Drag image to stage](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - If you have the [WYSIWYG editor enabled](/help/content-design/editor.md), click **[!UICONTROL Show/Hide Editor]** and then click **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] demo

To learn more about the [!DNL Media Gallery], watch this video:

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12&learn=on)

[adobe-stock]: https://stock.adobe.com

