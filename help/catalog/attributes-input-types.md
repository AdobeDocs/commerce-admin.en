---
title: Attribute input types
description: Learn about the input types available for product attributes, which determine the type of data that can be entered and the format of the field or input control.
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/8WwqU3ZSqmORqSD2061Pa5MTRqYbH71dOxouz-nLwbo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Attribute input types

When viewed from the Admin, attributes are the fields that you complete when you create a product. The input type that is assigned to an attribute determines the type of data that can be entered and the format of the field or input control. From the standpoint of the customer, attributes provide information about the product, and are the options and data entry fields that must be completed to purchase a product.

## Input types

|Property|Description|
|--- |--- |
|[!UICONTROL Text Field]|A single-line input field for text.|
|[!UICONTROL Text Area]|A multiple-line input field for entering paragraphs of text, such as a product description. You can use the WYSIWYG Editor to format the text with HTML tags, or enter the tags directly into the text.|
|[!UICONTROL Text Editor]|A fully functioning text editor at the attribute location.|
|[!UICONTROL Date]|Displays a date value in the [preferred format](#date-and-time-options) and [time zone](../getting-started/store-details.md#locale-options). Date values can be selected from a list or a calendar ( ![Calendar icon](../assets/icon-calendar.png) ). <br/><br/>**_Note:_** Depending on your system configuration, _Admin_ users can enter dates directly into a field or select a date from the calendar or list. For information about specifying date and time values, see [Date and time options](#date-and-time-options).|
|[!UICONTROL Date and Time]|Displays a date and time value in the [preferred format](#date-and-time-options) and [time zone](../getting-started/store-details.md#locale-options). The date and time can be entered manually or selected from a calendar. Example format: MM/DD/YYYY HH:MM|
|[!UICONTROL Yes/No]|Displays a drop-down list with pre-defined options of `Yes` and `No`.|
|Dropdown|Displays a drop-down list of values that accepts only a single selection. The Dropdown input type is a key component of [configurable products](../catalog/product-create-configurable.md).|
|[!UICONTROL Multiple Select]|Displays a drop-down list of values that accepts multiple selections.|
|[!UICONTROL Number] [!BADGE SaaS only]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service and Adobe Commerce Optimizer projects only (Adobe-managed SaaS infrastructure)."} |A numeric input field that stores decimal values. Unlike the **Price** input type, it does not apply currency formatting and accepts negative values. Use this input type for measurements, dimensions, or technical specifications such as temperature ranges.|
|[!UICONTROL Price]|This input type is used to create price fields that are in addition to the predefined attributes: `Price`, `Special Price`, `Tier Price`, and `Cost`. The currency used is determined by your system configuration.|
|[!UICONTROL Media Image]|Associates an extra image with a product, such as a product logo, care instructions, or ingredients from a food label. When you add a media image attribute to the attribute set of a product, it becomes an extra image type, along with Base, Small, and Thumbnail. The media image attribute can be excluded from the [storefront media browser](catalog-images-video.md#storefront-media-browser).|
|[!UICONTROL File] [!BADGE SaaS only]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service and Adobe Commerce Optimizer projects only (Adobe-managed SaaS infrastructure)."} |Allows a file to be uploaded and associated with a product attribute. Supported file types and maximum file size are configured in [Product File Attributes](../configuration-reference/catalog/product-file-attributes.md). Use this input type for documents such as product manuals, specification sheets, or certificates.|
|[!UICONTROL Fixed Product Tax]|Lets you define [FPT rates](../stores-purchase/fixed-product-tax.md) based on the requirements of your locale.|
|[!UICONTROL Visual Swatch]|Displays a swatch that depicts the color, texture, or pattern of a configurable product. A [visual swatch](swatches.md) can be filled with a hexadecimal color value, or display an uploaded image that represents the color, material, texture, or pattern of the option.|
|[!UICONTROL Text Swatch]|A text-based representation of a configurable product option that is frequently used for size. [Text swatches](swatches.md) can also include hexadecimal color values.|
|[!UICONTROL Page Builder]|A [[!DNL Page Builder]](../page-builder/workspace.md) workspace at the attribute location that makes it easy to add engaging content to the product page.|

{style="table-layout:auto"}

## Date and time options

You can customize the format of date and time fields, and select the input control that is used for data entry. Dates values can be selected from a drop-down list, or pop-up calendar.

![Example - storefront popup calendar](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_To format date/time fields:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the panel on the left, expand **[!UICONTROL Catalog]** and click the **[!UICONTROL Catalog]** subitem.

1. Expand the **[!UICONTROL Date & Time Custom Options]** section.

   ![Catalog configuration - date and time options](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   For a detailed listing of these options, see [_Date & Time Custom Options_](../configuration-reference/catalog/catalog.md) in the _Configuration Reference_.

1. To use a popup calendar as the input control for date fields, set **[!UICONTROL Use JavaScript Calendar]** to `Yes`.

1. To establish the **[!UICONTROL Date Fields Order]**, set the order of each part of the date field as needed:

   - Month
   - Day
   - Year

1. To set your preferred time format, set **Time Format** to one of the following:

   - `12h AM/PM`
   - `24h`

1. To establish the **[!UICONTROL Year Range]** for the drop-down values, enter the year (YYYY) to set the **[!UICONTROL from]** and **[!UICONTROL to]** dates.

   If blank, the field defaults to the current year.

1. When complete, click **[!UICONTROL Save Config]**.

