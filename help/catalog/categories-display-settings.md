---
title: Categories - Display settings
description: Learn about using the [!UICONTROL Display] settings to define which content elements appear on a category page and the order in which products appear.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/t5UfvWvJ7R-kZb5kyMwpzwI2gfs3x3g1amlfWzQcAsw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
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
# Categories - Display settings

Display settings determine which content elements appear on a category page and the order in which products appear. You can enable CMS blocks, set the anchor status of the category, and manage sorting options from the _[!UICONTROL Display Settings]_ tab. For examples of how categories are reflected in the storefront, see [Catalog Navigation](navigation.md).

![Display Settings for categories](./assets/category-display-settings.png){width="600" zoomable="yes"}

|Field|Description|
|--- |--- |
|[!UICONTROL Display Mode]|Determines the content elements displayed on the category page. Options: `Products Only` / `Static Block Only` / `Static Block and Products`|
|[!UICONTROL Anchor]|When set to `Yes`, displays products from the sub-categories in the category even if they haven't been explicitly added to the category, and enables the display of the _[!UICONTROL filter by attribute]_ section in the layered navigation. Options: `Yes` / `No`|
|[!UICONTROL Available Product Listing Sort By]|(Required) The default values are `Position`, `Name`, and `Price`. To customize the sorting option, deselect the **[!UICONTROL Use All Available Attributes]** checkbox and select the attributes you want to use. You can define and add attributes as needed. This setting does not apply to the [!DNL Live Search] [Product Listing Page Widget](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling).|
|[!UICONTROL Default Product Listing Sort By]|(Required) To define the default _[!UICONTROL Sort By]_ option, deselect the **[!UICONTROL Use Config Settings]** checkbox and select an attribute. This setting does not apply to the [!DNL Live Search] [Product Listing Page Widget](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling).|
|[!UICONTROL Layered Navigation Price Step]|By default, Commerce displays the price range in increments of 10, 100, and 1000, depending on the products in the list. To change the Price Step range, deselect the **[!UICONTROL Use Config Settings]** checkbox.|

{style="table-layout:auto"}
