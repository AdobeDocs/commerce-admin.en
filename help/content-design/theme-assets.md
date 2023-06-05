---
title: Theme Assets
description: Learn how to manage your theme assets, such as CSS, fonts, images, and JavaScript files.
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
---
# Theme Assets

The term _static files_ refers to the collection of assets, such as CSS, fonts, images, and JavaScript, that is used by a theme. The location of static files is specified in the [Base URL](../stores-purchase/store-urls.md) configuration. You can add a digital signature to the URL of each static file to make it possible for browsers to detect when a newer version is available. The newer version of the file is used if the signature differs from what is stored in the browser cache.

For a standard installation, the assets associated with a theme are organized in the `web` folder at the following location below the [!DNL Commerce] root.

   `[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## Add a digital signature to static file URLs

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL Developer]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Static Files Settings]** section.

   ![Static Files Settings](./assets/developer-static-files-settings.png){width="400" zoomable="yes"}

1. Set **[!UICONTROL Sign Static Files]** to `Yes`.

1. When complete, click **[!UICONTROL Save Config]**.

|File type|Description|
|--- |--- |
|CSS|Control the visual styling that is associated with the skin. Example location on server: `[commerce]/app/design/frontend/Magento/[theme]/web/css`|
|Fonts|Supply the fonts that are available to be used by the theme. Location on server: `[commerce]/app/design/frontend/Magento/[theme]/web/fonts`|
|Images|Provide the graphical assets used by the theme, including buttons, background textures, and so on. Example location on server: `[commerce]/app/design/frontend/Magento/[theme]/web/images`|
|JS|Theme-specific JavaScript routines and callable functions. Example location on server: `[commerce]/app/design/frontend/Magento/[theme]/web/js`|

{style="table-layout:auto"}

## Merge CSS files

As part of an effort to optimize your site and reduce page load time, you can reduce the number of separate CSS files by merging them into a single, condensed file. If you open a merged CSS file, you will find one continuous stream of text, with line breaks removed. You cannot edit the merged file, so it is best to wait until you are out of the development mode and no longer making frequent changes to the CSS.

>[!NOTE]
>
>CSS files can be merged from the _Admin_ panel only when working in [developer mode](../systems/developer-tools.md#operation-modes).

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, **[!UICONTROL Advanced]** and choose **[!UICONTROL Developer]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL CSS Settings]** section.

   ![CSS Settings](./assets/developer-css-settings.png){width="400" zoomable="yes"}
   
   For detailed descriptions of these configuration options, see [CSS Settings](../configuration-reference/advanced/developer.md#css-settings) in the _Configuration Reference_.

1. Set **[!UICONTROL Merge CSS Files]** to `Yes`.

1. When complete, click **[!UICONTROL Save Config]**.

## Merge JavaScript files

Multiple JavaScript files can be merged into a single, condensed file to reduce page load time. If you open a merged JavaScript file, you will find one continuous stream of text, with line breaks removed. If you are finished with the development process and the code contains no errors, you might consider merging the files.

>[!NOTE]
>
>JavaScript files can be merged from the _Admin_ panel only when working in [Developer Mode](../systems/developer-tools.md#operation-modes).

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, **[!UICONTROL Advanced]** and choose **[!UICONTROL Developer]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL JavaScript Settings]** section.

   ![JavaScript Settings](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   For detailed descriptions of these configuration options, see [JavaScript Settings](../configuration-reference/advanced/developer.md#javascript-settings) in the _Configuration Reference_.

1. Set **[!UICONTROL Merge JavaScript Files]** to `Yes`.

1. When complete, click **[!UICONTROL Save Config]**.
