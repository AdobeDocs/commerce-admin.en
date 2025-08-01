---
title: Page layouts
description: Learn about the page layout sections and how to configure default layouts.
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
---
# Page layouts

The layout of each page in your store consists of distinct sections, or containers, that define the header, footer, and content areas of the page. Depending on the layout, each page might have one, two, three columns, or more. You can think of the layout as the _floor plan_ of the page, and assign a specific layout to be used as the default for CMS, product, and category pages.

On the page, content blocks float to fill the available space, according to the section of the [page layout](layout-updates.md) where they are assigned to appear. Notice that if you change the layout from a three-column to a two-column layout, the content of the main area expands to fill the available space. Also notice that any blocks that are associated with the unused side bar seem to disappear. However, if you restore the three-column layout, the blocks reappear. This fluid approach, or _liquid layout_, makes it possible to change the page layout without having to rework the content. If you are used to working with individual HTML pages, this modular, _building block_ approach requires a different way of thinking.

![Standard two-column with left bar page layout](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## Configure default layouts

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel under _[!UICONTROL General]_, choose **[!UICONTROL Web]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Default Layouts]** section.

   ![Default layouts](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. Choose the **[!UICONTROL Default Product Layout]** that you want to use for product pages.

   This setting determines the layout that is used by default for product pages.

   - `No layout updates` - Layout updates are not available for product pages.
   - `Empty` - Uses a blank layout for product pages.
   - `1 column` - Uses a single column layout for product pages.
   - `2 columns with left bar` - Uses a two-column layout with the sidebar on the left for product pages.
   - `2 columns with right bar` - Uses a two-column layout with the sidebar on the right for product pages.
   - `3 columns` - Uses a three-column layout with sidebars on the left and right for product pages.

   When [Page Builder](../page-builder/introduction.md) is enabled, there are additional full width options available. You can then use the Page Builder content tools to design the layout for your product pages.

   - `Page -- Full Width` - Uses the _Page - Full Width_  layout for product pages.
   - `Category -- Full Width` - Uses the _Category - Full Width_ layout for product pages.
   - `Product -- Full Width` - (Recommended) Uses the _Product - Full Width_ layout for product pages.

1. Choose the **[!UICONTROL Default Category Layout]** that you want to use for category pages.

   This setting determines the layout that is used by default for category pages.

   - `No layout updates` - Layout updates are not available for category pages.
   - `Empty` - Uses a blank layout for category pages.
   - `1 column` - Uses a single column layout for category pages.
   - `2 columns with left bar` - Uses a two-column layout with the sidebar on the left for category pages.
   - `2 columns with right bar` - Uses a two-column layout with the sidebar on the right for category pages.
   - `3 columns` - Uses a three-column layout with sidebars on the left and right for category pages.

   When [Page Builder](../page-builder/introduction.md) is enabled, there are additional full width options available. You can then use the Page Builder content tools to design the layout for your category pages.

   - `Page -- Full Width` - Uses the _Page - Full Width_ layout for category pages.
   - `Category -- Full Width` - (Recommended) Uses the _Category - Full Width_ layout for category pages.
   - `Product -- Full Width` - Uses the _Product - Full Width_ layout for category pages.

1. Choose the **[!UICONTROL Default Page Layout]** that you want to use for CMS pages.

   This setting determines the layout that is used by default for CMS pages.

   - `No layout updates` - Layout updates are not available for CMS pages.
   - `Empty` - Uses a blank layout for CMS pages.
   - `1 column` - Uses a single column layout for CMS pages.
   - `2 columns with left bar` - Uses a two-column layout with the sidebar on the left for CMS pages.
   - `2 columns with right bar` - Uses a two-column layout with the sidebar on the right for CMS pages.
   - `3 columns` - Uses a three-column layout with sidebars on the left and right for CMS pages.

   When [Page Builder](../page-builder/introduction.md) is enabled, there are additional full width options available. You can then use the Page Builder content tools to design the layout for your CMS pages.

   - `Page -- Full Width` - (Recommended) Uses the _Page - Full Width_ layout for CMS pages.
   - `Category - Full Width` - Uses the _Category - Full Width_ layout for CMS pages.
   - `Product - Full Width` - Uses the _Product - Full Width_ layout for CMS pages.

1. When complete, click **[!UICONTROL Save Config]**.

## Standard Page Layouts

### One Column

![Diagram - one-column layout](./assets/layout-1-col-th.png){zoomable="yes"}

The _[!UICONTROL 1 Column]_ layout can be used to create a dramatic home page with a large image or focal point. It is also a good choice for a landing page, or any other page that has a combination of text, images, and video.

### Two columns with left bar

![Diagram - two-column layout with left bar](./assets/layout-2-col-lft-bar-th.png){zoomable="yes"}

The _[!UICONTROL 2 Columns with Left Bar]_ layout is often used for pages with navigation on the left, such as a catalog or search results pages with layered navigation. It is also an excellent choice for home pages that need additional navigation or blocks of supporting content on the left.

### Two columns with right bar

![Diagram - two-column layout with right bar](./assets/layout-2-col-rt-bar-th.png){zoomable="yes"}

With a _[!UICONTROL 2 Columns with Right Bar]_ layout, the main content area is large enough for an eye-catching image or banner. This layout is also often used for Product pages with blocks of supporting content on the right.

### Three columns

![Diagram - three-column layout](./assets/layout-3-col-th.png){zoomable="yes"}

The _[!UICONTROL 3 Column]_ layout has a center column that is wide enough for the main text of the page, with room on each side for additional navigation and blocks of supporting content.

### Empty

![Diagram - empty layout](./assets/layout-blank-th.png){zoomable="yes"}

The _[!UICONTROL Empty]_ layout can be used to define custom page layouts.
