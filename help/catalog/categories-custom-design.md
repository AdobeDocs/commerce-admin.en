---
title: Categories - Design settings
description: Learn about using the [!UICONTROL Design] settings to define the look and feel of a category, all associated product pages, and page layout.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/cRTRPl-UTfAKXY8rmtVKlnAZooVWpTCjSkVSdNHXp28
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
    internal-label: Categories
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
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Categories - Design settings

The _[!UICONTROL Design]_ section gives you control over the look and feel of a category, all associated product pages, and page layout. You can customize a category page and its associated products for a promotion, or to differentiate the category. For example, you might develop a distinctive design for a brand or special line of products, or apply an update for a specific time period.

![Design settings for a category](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>When the same product is assigned to several categories with different design settings for each category, it is recommended to set **Use Categories Path for Product URLs** = `Yes` in the [Search Engine Optimization configuration options](../configuration-reference/catalog/catalog.md#search-engine-optimization). To access this setting, go to  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**, expand **[!UICONTROL Catalog]** and choose **Catalog** underneath in the left panel, and then expand the **Search Engine Optimization** section on the page.

|Field|Description|
|--- |--- |
|[!UICONTROL Use Parent Category Settings]|Allows the current category to inherit the design settings from the parent category. If used, all other fields in the Design section become unavailable. Options: `Yes` / ` No`|
|[!UICONTROL Theme]|Applies a custom theme to the category.|
|[!UICONTROL Layout]|Applies a different layout to the category page. Options: <br/>**[!UICONTROL No layout updates]** - By default, layout updates are not available for category pages. <br/>**[!UICONTROL Empty]** - Use to define your own page layout. (Requires an understanding of XML.) <br/>**[!UICONTROL 1 column]** - Applies a one-column layout to the category page. <br/>**[!UICONTROL 2 columns with left bar]** - Applies a two-column layout with a left sidebar to the category page. <br/>**[!UICONTROL 2 columns with right bar]** - Applies a two-column layout with a right sidebar to the category page. <br/>**[!UICONTROL 3 columns]** - Applies a three-column layout to the category page.<br/>**[!UICONTROL Page -- Full Width]** - (Requires [Page Builder](../page-builder/introduction.md)) Applies the full-width layout for CMS pages to the category page. <br/>**[!UICONTROL Category -- Full Width]** - (Requires Page Builder) Applies the full-width layout for category pages to the category page. <br/>**[!UICONTROL Product -- Full Width]** - (Requires Page Builder) Applies the full-width layout for product pages to the category page.|
|[!UICONTROL Custom Layout Update]|Lists the available custom layout update files on the server. Choose the custom layout update that you want to apply to the category.|
|[!UICONTROL Apply Design to Products]|When selected, applies the custom settings to all products in the category.|

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

The _[!UICONTROL Scheduled Design Update]_ section determines the range of dates when a custom design is applied to category pages.

|Field|Description|
|--- |--- |
|[!UICONTROL Schedule Update From/To]|Determines the range of dates when a custom layout is applied to the category.|

![Scheduled Design Update](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
