---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap]'
description: Review the configurations settings on the [!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap] page of the Commerce Admin.
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
---
# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![Categories Options](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Frequency]|Store View|Determines how often sitemap categories are updated. Options: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never`|
|[!UICONTROL Priority]|Store View|A value between `0.0` and `1.0` that determines the priority of category sitemap updates in relation to other content. Zero (`0.0`) has the lowest priority.|

{:style="table-layout:auto"}

## [!UICONTROL Products Options]

![Products Options](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Frequency]|Store View|Determines how often sitemap products are updated. Options: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never`|
|[!UICONTROL Priority]|Store View|A value between `0.0` and `1.0` that determines the priority of product sitemap updates in relation to other content. Zero (`0.0`) has the lowest priority.|
|[!UICONTROL Add Images into Sitemap]|Store View|Determines the extent that images are included in the sitemap. Options: `None` / `Base Only` / `All`|

{:style="table-layout:auto"}

## [!UICONTROL CMS Pages Options]

![CMS Pages Options](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Frequency]|Store View|Determines how often sitemap CMS pages are updated. Options: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never`|
|[!UICONTROL Priority]|Store View|A value between `0.0` and `1.0` that determines the priority of CMS page sitemap updates in relation to other content. Zero (`0.0`) has the lowest priority.|

{:style="table-layout:auto"}

## [!UICONTROL Store Url Options]

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Frequency]|Store View|Determines how often store URLs are updated. Options: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never`|
|[!UICONTROL Priority]|Store View|A value between `0.0` and `1.0` that determines the priority of store URL updates in relation to other content. Zero (`0.0`) has the lowest priority.|

{:style="table-layout:auto"}

## [!UICONTROL Generation Settings]

![Generation Settings](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled]|Store View|Determines if an XML sitemap is available for the store. Options: `Yes` / `No`|
|[!UICONTROL Start Time]|Store View|Specifies the hour, minute, and second of the day that the sitemap is updated.|
|[!UICONTROL Frequency]|Store View|Determines how often the sitemap is updated. Options: `Daily` / `Weekly` / `Monthly`|
|[!UICONTROL Error Email Recipient]|Store View|The email address of the person who receives notification if an error occurs during the sitemap update process. For multiple addresses, separate each with a comma.|
|[!UICONTROL Error Email Sender]|Website|Identifies the store contact that appears as the sender of the error notification. Options: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2`|
|[!UICONTROL Error Email Template]|Website|Identifies the email template that is used for the error notification. Default template: `Sitemap generate Warnings`|

{:style="table-layout:auto"}

## [!UICONTROL Sitemap File Limits]

![Sitemap File Limits](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Maximum No of URLs Per File]|Store View|Determines the maximum number of URLs that can be included in a single sitemap.|
|[!UICONTROL Maximum File Size]|Store View|Determines the maximum size of the generated sitemap, in bytes.|

{:style="table-layout:auto"}

## [!UICONTROL Search Engine Submission Settings]

![Search Engine Submission Settings](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Submission to Robots.txt]|Store View|Enables directives to be submitted for the robots.txt file. Options: `Yes` / `No`|

{:style="table-layout:auto"}
