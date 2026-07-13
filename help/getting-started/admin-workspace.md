---
title: The Admin tools and workspace
description: Learn about the Admin workspace, which provides access to all the tools, data, and content used to run your store.
exl-id: 61cc53ab-e1c5-4349-b306-a15eb7c5ab57
TQID: https://experienceleague.adobe.com/RGT21TI5joLEYx3fiOErU5ZoIrXsq0nqZpnI8c40hz4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
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
# The Admin tools and workspace

The Admin workspace provides access to all the tools, data, and content used to run your store. The default startup page can be set in the configuration. Many Admin pages have a grid that lists the data for the section, with a set of tools to search, sort, filter, select, and apply actions. By default, the [Dashboard](admin-dashboard.md) is the startup page for the Admin. However, you can choose any other page to appear as the startup page when you log in. You can click the logo in the Admin sidebar to return to the Admin startup page.

![Admin - workspace](./assets/admin-workspace.png){zoomable="yes"}

## Workspace controls

|Control|Description|
|--- |--- |
|[!UICONTROL Global Search]|The search icon at the top right can be used to find any value in the database, including product, customer, and order records.|
|[!UICONTROL Grid Search]|The search box above the grid can be used to quickly filter the grid display based on key words found in the records.|
|[!UICONTROL Sort]|The header of each column can be used to sort the list in ascending or descending order.|
|[!UICONTROL Filters]|Defines a set of search parameters that determines the records that appear in the grid. In addition, the filters in the header of some columns can be used to limit the list to specific values. Some filters have additional options that can be selected from a list box.|
|[!UICONTROL Default View]|Determines the default column layout of the grid.|
|[!UICONTROL Columns]|Determines the selection of [columns](admin-grid-controls.md) and their order in the grid. The column layout can be changed and saved as a _view_. By default, only some of the columns are included in the grid.|
|[!UICONTROL Paginate]|The pagination controls are used to view the additional pages of results.|
|[!UICONTROL Actions]|The Actions control applies an operation to all selected records.|
|[!UICONTROL Select]|The Select control is used to select multiple records that are to be the target of action. Options: `Select All` / `Deselect All`|

{style="table-layout:auto"}

## Workspace search

To find any record in the database, use the magnifying glass icon in the header of the _Admin_. The results can include customers, products, orders, or any related attribute. For example, if you enter a customer name, the results might include the customer record and any orders that are associated with the name.

![Admin search tool](./assets/admin-search.png){width="700" zoomable="yes"}

1. In the header, click the _Search_ (![magnifying glass](../assets/icon-magnify-search.png)) icon to open the search box.

1. Do one of the following:

   - To find a close match, enter the first few letters of what you want to find.
   - To find an exact match, enter the word or multiple words that you want to find.

1. In the displayed search results, click any item to open the record.

## Change the Admin startup page

The [dashboard](admin-workspace.md#the-dashboard) is the default startup page for the Admin, although you can configure a different startup page.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left navigation panel under **[!UICONTROL Advanced]**, choose **[!UICONTROL Admin]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Startup Page]** section.

   ![Advanced configuration - Admin startup page setting](./assets/admin-startup-page.png){width="600"}

1. Set **[!UICONTROL Startup Page]** to the page that you want to appear first after you log in to the Admin.
   
   For a detailed list of all Admin options, see [Admin](../configuration-reference/advanced/admin.md) in the _Configuration Reference_.

1. When complete, click **[!UICONTROL Save Config]**.
