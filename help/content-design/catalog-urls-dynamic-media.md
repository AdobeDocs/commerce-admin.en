---
title: Dynamic media URLs
description: Learn about using a dynamic media URL as a relative reference to an image or other media asset.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
---
# Dynamic media URLs

A dynamic media URL is a relative reference to an image or other media asset. When enabled, dynamic media URLs can be used to link directly to assets on your server, or to files stored on a [content delivery network](media-storage-content-delivery-network.md). The use of dynamic media URLs can impact catalog performance, and the [editor](editor.md#configure-the-editor) can be configured to use either static or dynamic media URLs.

As with all [markup tags](../systems/markup-tags.md), the directive is enclosed in double curly braces. The format of a dynamic media URL looks like the following:

`\{\{media url="path/to/image.jpg"}}`

Dynamic URL directives are processed from saved HTML content when the page is rendered on the storefront. Each time the page is rendered, the content is scanned for `\{\{media url="..."}}` and each directive is replaced with the corresponding media URL.

{{$include /help/_includes/directives-caution.md}}

## Configure static media URLs

By default, images inserted into the catalog from the WYSIWYG editor have relative, dynamic URLs. If you prefer to use a static URL, you can change the configuration setting.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel under _[!UICONTROL General]_, choose **[!UICONTROL Content Management]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL WYSIWYG Options]** section.

   ![WYSIWYG Options](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** to one of the following:

   - `Yes` - Uses static URLs for media content that is inserted with the WYSIWYG editor. Static URLs are absolute and break if the [base URL](../stores-purchase/store-urls.md) of the store changes.

   - `No` - (Default) Uses dynamic URLs for media content that is inserted with the WYSIWYG editor, based on the `\{\{media url="..."}}` directive. Dynamic URLs are relative and do not break if the base URL of the store changes.

1. When complete, click **[!UICONTROL Save Config]**.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
