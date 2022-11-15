---
title: vGeneral > Content Management
description: Placeholder
---
# General > Content Management

{{config}}

## WYSIWYG Options

![WYSIWYG Options](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- WYSIWYG Options](https://docs.magento.com/user-guide/cms/editor.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Enable WYSIWYG Editor|Store View|Determines if the editor is enabled for the store. Options: Enabled by Default/Disabled by Default/Disabled Completely|
|WYSIWYG Editor|Website|Determines the version of the TinyMCE editor that is used for the WYSIWYG editor. Options: <br/>**TinyMCE 5** - (Default) Uses the TinyMCE version 5 as the default WYSIWYG editor.<br><br>_**Note:**_ An update to the TinyMCE 5.10 library in Adobe Commerce and Magento Open Source 2.4.5 resolves a vulnerability that allowed arbitrary JavaScript execution when updating an image or link using some types of URLs. TinyMCE 3 was deprecated in the 2.4.0 release and removed in the 2.4.3 release. TinyMCE 4 was removed in the 2.4.4 release.|
|Use Static URLs for Media Content in WYSIWYG|Global|Determines if [static URLs](https://docs.magento.com/user-guide/catalog/catalog-urls-dynamic-media.html) are used for media content that is referenced from the WYSIWYG editor. The setting applies to all places where the WYSIWYG editor is available, including products, categories, pages, blocks, etc. Options: <br/>**Yes** - Uses static URLs for media content that is inserted with the WYSIWYG editor. Static URLs are absolute and break if the [base URL](https://docs.magento.com/user-guide/stores/store-urls.html) of the store changes. <br/>**No** (Default) - Uses dynamic URLs for media content that is inserted with the WYSIWYG editor, based on the  `{{media url="..."}}` directive. Dynamic URLs are relative and do not break if the [base URL](https://docs.magento.com/user-guide/stores/store-urls.html) of the store changes.|

## CMS Page Hierarchy

{{ee-feature}}

![CMS Page Hierarchy](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Enable Hierarchy Functionality|Global|Activates the use of page hierarchy for your content pages. Options: `Yes` / `No`|
|Enable Hierarchy Metadata|Global|Gives you the ability to associate meta data with pages in the hierarchy. Options: `Yes` / `No`|
|Default Layout for Hierarchy Menu|Global|Determines the default menu style. Options: Content / Left Column / Right Column|

## Advanced Content Tools

![Advanced Content Tools](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!--Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Enable Page Builder|Global|Determines if the Page Builder Advanced Content tools are available. Options: <br/>**Yes** - The Page Builder workspace appears in the Content section of pages, blocks, products, and categories. <br/>**No** - The standard CMS editing tools appear in the Content section of pages, blocks, products, and categories.|
|Enable Page Builder Content Preview|Global|Determines if the Page Builder content previews are enabled for products and categories. Options: `Yes` / `No` <br/>**_Note:_** This is set to `Yes` by default, but turning the preview off can prevent any performance issues resulting from loading previews within a product or category form.|
|Google Maps API Key|Global|The Google Maps API key from your Google account.|
|Test Key||Validates the Google Maps API key.|
|Google Maps Style|Global|Paste the Google Maps style JSON code here to change the look and feel of the Map content type.|
|Default Column Grid Size|Global|Determines the default number of columns in the Page Builder grid.|
|Maximum Column Grid Size|Global|Determines the maximum number of columns in the Page Builder grid.|

>[!TIP]
>
>Page Builder makes it easy to create content-rich pages with custom layouts that enhance your visual storytelling and to drive customer engagement and loyalty. These features are designed to improve quality and reduce the time and expense of producing custom pages. For more information about these features and how you can use them to create engaging content for your Adobe Commerce or Magento Open Source store, see the [_Page Builder User Guide_](https://experienceleague.adobe.com/docs/commerce-admin/page-builder/guide-overview.html).

