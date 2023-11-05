---
title: Company management
description: Learn about company management and how they function between companies in B2B.
feature: B2B, Companies, Storefront
role: Admin
hide: yes
hidefromtoc: yes
---

# Company management

The Company management capability streamlines business operations for companies with complex organizational structures. Admin users can manage companies as a group by building a company hierarchy that assigns related companies to a designated parent company. This assignment allows the parent company administrator to manage their own account and the company accounts for all assigned companies.

In the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Companies Grid](./assets/companies-grid-view.png){width="700" zoomable="yes"}

The _[!UICONTROL Companies]_ page lists all current companies, regardless of status. The standard [workplace controls](../getting-started/admin-workspace.md) can be used to filter the list, change the [column layout](../getting-started/admin-grid-controls.md), save views, or export data.

The _[!UICONTROL Actions]_ control above the grid can be used to apply an action to multiple company line items. The actions that are available depend on the [permissions](../systems/permissions.md) for the role that is assigned to your Admin user account.

## [!UICONTROL Company Hierarchy]

On initial company creation, the Company Hierarchy page control is empty when you expand it. After a company is created, Admin users with appropriate permissions can use the Company Hierarchy section to build a parent company organization by editing the designated parent company and assigning related companies.

![Companies Hierarchy Grid](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

See [assign and unassign companies](assign-companies.md) for more information on available actions in this view.

### Column descriptions

The **[!UICONTROL Company Hierarchy]** view provides information about any company relationships defined for the parent company. For example, on the detail page for a parent company, the [!UICONTROL Company Hierarchy] displays all companies assigned to the parent. On a detail page for an assigned company, the view displays the parent company and any other companies assigned to the same parent. The main columns shown are as follows:

|Columns|Description|
|--- |--- |
|[!UICONTROL Company ID]|The ID number of the company.|
|[!UICONTROL Company Name]|The full name of the company. Options: <br/>- A `current company indicator` appears if company is a parent company.<br/>- A `child company indicator` appears if company is a child company.|
|[!UICONTROL Company Email]|The email address that is associated with the company account.|
|[!UICONTROL Phone Number]|The primary phone number of the company.|
|[!UICONTROL State/Province]|The state or province where the company is registered to conduct business.|
|[!UICONTROL City]|The city where the company is registered to conduct business.|
|[!UICONTROL Customer Group]|(Admin Only) Indicates the [customer group](../customers/customer-groups.md) or [shared catalog](catalog-shared.md) that is assigned to the company.|
|[!UICONTROL Company Admin]|The full name of the company administrator.|
|[!UICONTROL Action]|The list of possible actions for that company line.|

{style="table-layout:auto"}

### Filter info

From the **Company Hierarchy grid** you can filter by **Company Type** to show specific companies in the list.

### Search

Use the search function to find the companies in the **Companies** view by keyword. It will find the company by searching the specified keyword on the text in Company Name column and Parent columns.
