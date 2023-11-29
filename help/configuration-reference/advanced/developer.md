---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Developer]'
description: Review the configurations settings on the [!UICONTROL Advanced] &gt; [!UICONTROL Developer] page of the Commerce Admin.
exl-id: 2ef4ba6a-b5a5-419d-8d61-e535e3366370
role: Admin, Developer
feature: Site Management, Configuration, System
---
# [!UICONTROL Advanced] > [!UICONTROL Developer]

{{config}}

>[!NOTE]
>
>These configuration settings are available in [developer mode](../../systems/developer-tools.md#operation-modes) only.

## [!UICONTROL Frontend Development Workflow]

![Frontend Development Workflow](./assets/developer-frontend-development-workflow.png)<!-- zoom -->

For more information about changing these settings, see [Frontend development workflow](../../systems/developer-tools.md#frontend-development-workflow) in the _Admin Systems Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Workflow Type]|Global|Determines if Less compilation takes place on the client or server side during development. Options: <br/>**`Client side less compilation`** - Compilation takes place in the browser using the native less.js library. <br/>**`Server side less compilation`** - Compilation takes place on the server using the Less PHP library. This is the default mode for production.|

{style="table-layout:auto"}

## [!UICONTROL Developer Client Restrictions]

![Developer Client Restrictions](./assets/developer-developer-client-restrictions.png)<!-- zoom -->

For more information about changing this setting, see [Client restrictions](../../systems/developer-tools.md#client-restrictions) in the _Admin Systems Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Allow IPs (comma separated)]|Store View|Creates an allowlist of IP addresses that  can use developer tools on a live site, without interfering with customers in the store. Any changes to the site when using a developer tool such  as _Inline Translation_, are visible only from the IP addresses on the allowlist.|

{style="table-layout:auto"}

## [!UICONTROL Template Settings]

![Template Settings](./assets/developer-template-settings.png)<!-- zoom -->

For more information about changing these settings, see [Optimizing resource files](../../systems/developer-tools.md#optimizing-resource-files) in the _Admin Systems Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Allow Symlinks]|Store View|Enabling [symbolic links](https://en.wikipedia.org/wiki/Symbolic_link) can expose your site to security risks and is not recommended for a production store.|
|[!UICONTROL Minify Html]|Store View|Determines if the HTML for store templates is minimized. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL Debug]

![Debug](./assets/developer-debug.png)<!-- zoom -->

For more information about changing these settings, see [Template path hints](../../systems/developer-tools.md#template-path-hints) in the _Admin Systems Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Template Path Hints for Storefront]|Store View|Adds notation to storefront that indicates the path to each template that is used on the page. Options: `Yes` / `No`|
|[!UICONTROL Enable Template Path Hints for Admin]|Global|Adds notation to the Admin that indicates the path to each template that is used on the page. Options: `Yes` / `No`|
|[!UICONTROL Add Block Class Type to Hints]|Store View|Includes the names of blocks in the template path hints. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL Translate Inline]

![Translate Inline](./assets/developer-translate-inline.png)<!-- zoom -->

For more information about changing these settings, see [Translate inline](../../systems/developer-tools.md#translate-inline) in the _Admin Systems Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable for Storefront]|Store View|Activates the Inline Translator for the storefront. The interface text can be edited for each store view. To use the Inline Translator without interfering with the live store, add your IP address to the Developer Client Restrictions allowlist.|
|[!UICONTROL Enable for Admin]|Global|Activates the Inline Translator for the Admin. Unlike the storefront, the Admin cannot be translated into multiple languages. However, the field labels and other text in the interface can be changed.|

{style="table-layout:auto"}

## [!UICONTROL JavaScript Settings]

![JavaScript Settings](./assets/developer-javascript-settings.png)<!-- zoom -->

For more information about changing these settings, see [Optimizing resource files](../../systems/developer-tools.md#optimizing-resource-files) in the _Admin Systems Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Merge JavaScript Files]|Store View|Merges multiple JavaScript files into a single file to improve page load time.|
|[!UICONTROL Enable JavaScript Bundling]|Store View|Determines if multiple JavaScript files can be bundled into one file. Options: `Yes` / `No`|
|[!UICONTROL Minify JavaScript Files]|Store View|Removes unnecessary characters, spaces, and indentation to reduce the size of the code.|
|[!UICONTROL Move JS code to the bottom of the page]|Global|If enabled, moves the JS code to the bottom of the page. Options: `Yes` / `No`|
|[!UICONTROL Translation Strategy]|Global|Determines the translation methodology that is used by the system. Options: <br/>**`Dictionary`** - Translation on storefront side. <br/>**`Embedded`** - Translation on Admin side.|
|[!UICONTROL Log JS Errors to Session Storage]|Global|If enabled, can be used by functional tests for reporting. Options: `Yes` / `No`|
|[!UICONTROL Log JS Errors to Session Storage Key]|Global|Identifies the key that is used to retrieve collected js errors.|

{style="table-layout:auto"}

## [!UICONTROL CSS Settings]

![CSS Settings](./assets/developer-css-settings.png)<!-- zoom -->

For more information about changing these settings, see [Optimizing resource files](../../systems/developer-tools.md#optimizing-resource-files) in the _Admin Systems Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Merge CSS Files]|Store View|Merges multiple CSS files into a single file to improve page load time. Options: `Yes` / `No`|
|[!UICONTROL Minify CSS Files]|Store View|Removes unnecessary characters, spaces, and indentation to reduce the size of the code. Options: `Yes` / `No`|
|[!UICONTROL Use CSS critical path]|Global|The _CSS critical path_ delivers minified critical CSS inline in `<head>` and defers all non-critical styles that are loaded asynchronously. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL Image Processing Settings]

![Image Processing Settings](./assets/developer-image-processing-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Image Adapter]|Global|Specifies the adapter that is used to render images. After changing the adapter setting, flush the catalog images cache. Options: `PHP GD2` / `ImageMagick` <br/><br/>**_Note:_** The ICO file type is supported only by the ImageMagik adapter.|

{style="table-layout:auto"}

## [!UICONTROL Caching Settings]

![Caching Settings](./assets/developer-cache-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
| [!UICONTROL Cache User Defined Attributes] | Global | When enabled, caches user-defined and system Entity Attribute Value (EAV) attributes. This option may increase performance but also requires additional space for caching. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL Static Files Settings]

![Static Files Settings](./assets/developer-static-files-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Sign Static Files]|Global|When enabled, adds a digital signature to the URL of static files to make it possible for browsers to detect when a newer version of the file is available. If a file's signature differs from what is stored in the browser's cache, then the newer version of the file is used. Static files that can be signed include JavaScript, CSS, images, and fonts. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL Grid Settings]

![Grid Settings](./assets/developer-grid-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Asynchronous Indexing|Global]|Determines when order processing system entities, such as orders, invoices, shipments, and credit memos, are added to the grid and reindexed. Asynchronous Indexing can be used to avoid locks on data during save operations, and to reduce processing time. Options: <br/>**`Disable`** - (Default) Order-related entities are added to the grid at various times. as they are saved. <br/>**`Enable`** - Order-related entities are added to the grid only during a scheduled cron job. Cron should be configured to run once every minute.|

{style="table-layout:auto"}
