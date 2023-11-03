---
title: Company management
description: Learn about company management and how they function between companies in B2B.
feature: B2B, Companies, Storefront
role: Admin
hide: yes
hidefromtoc: yes
---

# Company management

The Company management feature streamlines business operations for companies with complex organizational structures. Admin users can create company hierarchy by assigning companies to a designated parent company.

Each company contains unique identifiers, such as:

* Company ID
* Company name
* Company type
* Company email
* Phone number

The _[!UICONTROL Companies]_ page lists all current companies, regardless of status. The standard [workplace controls](../getting-started/admin-workspace.md) can be used to filter the list, change the [column layout](../getting-started/admin-grid-controls.md), save views, or export data.

The _[!UICONTROL Actions]_ control above the grid can be used to apply an action to multiple company line items. The actions that are available depend on the [permissions](../systems/permissions.md) for the role that is assigned to your Admin user account.

## Company Hierarchy

In the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Companies Grid](./assets/companies-grid-view.png){width="700" zoomable="yes"}

The [!UICONTROL Companies] grid lists all companies regardless of status. 

Company hierarchy allows Commerce B2B admin users with the appropriate permissions to create a parent company  and assign companies, then this parent company admin can manage the company accounts for the parent and all assigned companies.

You can also manage the hierarchy by [assigning or unassigning companies](assign-companies.md).

>[!IMPORTANT]
>
> The **Company Hierarchy** view for a parent company appears as empty.

The standard [workplace controls](../getting-started/admin-workspace.md) can be used to filter the list, change the [column layout](../getting-started/admin-grid-controls.md), save views, and export data.

The _[!UICONTROL Actions]_ control above the grid can be used to apply an action to multiple company records. For example, rather than approving each individual company request, you can select multiple requests and activate the accounts in a single action. The actions that are available depend on the [permissions](../systems/permissions.md) for the role that is assigned to your Admin user account.

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

## Apply an action

The following actions can be applied to either single or multiple company lines.

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. In the first column of the grid, select the checkbox of each company that you want to update and follow the instructions for the action that you want to apply.

See [assign and unassign companies](assign-companies.md) for more information on available actions in this view.

## Filter info

From the **Company Hierarchy** view, you can filter the companies shown in the list by selecting a filter criteria.

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.
1. Click the **[!UICONTROL Filters]** selector.
1. Complete as many filters as necessary to describe the company you want to find.
1. Click **[!UICONTROL Apply filters]** to apply desired filters.

### Search by keyword

Use the search filter to find parent companies in the **Company Hierarchy** view by keyword. When you search for a parent company, the search returns the parent company and all assigned companies. If you search for a child company, the search returns only that specific company.
