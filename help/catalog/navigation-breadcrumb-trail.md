---
title: Breadcrumb trails
description: Learn about the different breadcrumb trail patterns and how to configure them to appear on content and catalog pages.
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
TQID: https://experienceleague.adobe.com/v1hA4y0MmxxTtH3WbspqosZM1JMk4PMyhK1xeLxALOE
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Breadcrumb trails

A _breadcrumb trail_ is a set of links that shows the customer where they are in relation to other pages in the store. They can click any link in the breadcrumb trail to return to the previous page.

The breadcrumb trail can be configured to appear on content pages and on catalog pages. The format and position of the breadcrumb trail varies by theme, but it is typically located just below the header. By default, the breadcrumb trail appears on CMS pages.

![Breadcrumb trail displayed in the storefront](./assets/storefront-breadcrumb-trail.png){width="700" zoomable="yes"}

## General types of bread crumbs

Breadcrumbs can be divided into three main types, which differ in their purpose. The essence and main principles of the implementation of each type of bread crumbs are described below.

### Hierarchy-based breadcrumbs

This type of breadcrumb is based on the category hierarchy set up on the site. The chains presented tell the user where in the structure they are. In this case, each text link is intended for a page that is one level higher than the previous one.

Example: `Men > Tops > Hoodies & Sweatshirts`

The advantage of this type is that users can easily see which category level they are in and have easy access to navigation between catalog pages.

### History-based breadcrumbs

History- (or path-) based navigation is similar to the back button in a browser. This type of navigation allows users to quickly return to the previous pages they have visited without changes.

The advantage of this type is that it is most helpful when customers want to return to a previous page after selecting multiple filters on a category page.

Example: `Home > What's New > Gear > Bags`

### Attribute-based breadcrumbs

This type of breadcrumb displays the attributes selected on the category page. The main difference from the other types is that the attribute-based breadcrumbs represent the filters and options the customer has selected in the navigation layer for certain products (such as price, quality, and color).

Example: `Home > Suits > All Suits > Refined by > Slim Fit`

## Add/Remove the breadcrumbs from CMS pages

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel under _[!UICONTROL General]_, choose **[!UICONTROL Web]**.

   ![Show Breadcrumbs for CMS Pages](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. Expand the _[!UICONTROL Default Pages]_ section.

1. Deselect the **[!UICONTROL Use system value]** checkbox.

1. Set **[!UICONTROL Show Breadcrumbs for CMS Pages]** to `No` or `Yes`.

1. When complete, click **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Parent category is not displayed on the Breadcrumb Trail, on the child category page, when it has `Browsing Category`= `Deny` [category permission](category-permissions.md) settings.
