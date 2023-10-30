---
title: Company management
description: Learn about company management and how they function between companies in B2B.
feature: B2B, Companies, Storefront
role: Admin
hide: yes
hidefromtoc: yes
---

# Company management

The Company management feature streamlines business operations for companies with complex organizational structures. B2B company administrators can create a company hierarchy by assigning companies to a designated parent company. Then, the parent company administrator can view and manage the assigned companies as a group.

From a business point of view, the controlling or owning company is generally called a parent company. While many parent companies completely own their related companies, a parent company can also be just one of the owners or a member as well. In most cases, however, the parent company is the majority shareholder. Although the parent and related companies are connected, they are distinct legal entities.

Each company contains unique identifiers, such as:

* Company ID
* Company name
* Company type
* Company email
* Phone number
* Country
* State/Province
* City
* Company admin

## Company Hierarchy

In the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Companies Grid](./assets/companies-grid.png){width="700" zoomable="yes"}

The [!UICONTROL Companies] grid lists all companies regardless of status. 

When a company administrator has created a new company, you can select the dropdown called **Company Hierarchy** to view the parent company and its related companies. You can also manage the hierarchy by [assigning or unassigning companies](assign-companies.md).

>[!IMPORTANT]
>
> The **Company Hierarchy** view for a parent company appears as empty.

## Column descriptions

The **Company Hierarchy** view provides information about any company relationships defined for the specified company. For example, on the detail page for a parent company, the [!UICONTROL Company Hierarchy] displays all companies assigned to the parent. On a detail page for an assigned company, the view displays the parent company and any other companies assigned to the same parent.  The main columns shown are as follows:

|Columns|Description|
|--- |--- |
|[!UICONTROL Company Name]|The full name of the company.|
|[!UICONTROL Company Type]|The type of the company. Options: <br/>**[!UICONTROL Company]** - By default new companies are created as single companies. <br/>**[!UICONTROL Parent]** - The company is a parent company of other companies. <br/>**[!UICONTROL Child]** - This company is related to a parent company.|
|[!UICONTROL Parent]|Shows the parent company for this specific company.|
|[!UICONTROL Company Email]|The email address that is associated with the company account.|
|[!UICONTROL Phone Number]|The primary phone number of the company.|
|[!UICONTROL State/Province]|The state or province where the company is registered to conduct business.|
|[!UICONTROL City]|The city where the company is registered to conduct business.|
|[!UICONTROL Customer Group]|(Admin Only) Indicates the [customer group](../customers/customer-groups.md) or [shared catalog](catalog-shared.md) that is assigned to the company.|
|[!UICONTROL Company Admin]|The full name of the company administrator.|
|[!UICONTROL Action]|The list of possible actions for that company line.|

{style="table-layout:auto"}

### Show/Hide columns

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]** > **[!UICONTROL Columns]** button.
1. Click the **[!UICONTROL Column]** .
1. To customize which columns that you see in this view, check or uncheck columns in the list.

The **Company Hierarchy** view immediately shows any changes you made in the Column selector. The column preferences are saved and remain in effect if you navigate away from the view.

## Apply an action

The following actions can be applied to either single or multiple company lines.

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. In the first column of the grid, select the checkbox of each company that you want to update and follow the instructions for the action that you want to apply.

See [assign and unassign companies](assign-companies.md) for more information on available actions in this view.

## Filter info

From the **Company Hierarchy** view, you can filter the companies shown in the list by selecting a filter criteria.

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.
1. Click the **[!UICONTROL Filters]** selector.
1. Complete as many filters as necessary to describe the record you want to find.
1. Click **[!UICONTROL Apply filters]** to apply desired filters.

### Search by keyword

You can search by keyword in the **Company Hierarchy** grid view. If you are searching for a parent company, the search returns the parent company and all related companies.

## Export report

Download a file with all the companies listed in this view.

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]** > **[!UICONTROL Export]**.
1. You can select an specific file to export the report as:
   * .csv file
   * Excel (xml) file
1. Click the **[!UICONTROL Export]** button.
