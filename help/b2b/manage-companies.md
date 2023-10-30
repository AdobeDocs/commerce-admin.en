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

The **Company Hierarchy** view provides visibility on all the information related to company management in B2B. The main columns shown are as follows:

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
1. Toggle the _[!UICONTROL ID]_ values to see results for only selected company IDs.
1. Select the _[!UICONTROL Company Name]_ to see results for only that selected company name.
1. Select the _[!UICONTROL Company Email]_ to see results for only that selected company email.
1. Select the _[!UICONTROL Phone Number]_ to see results for only that phone number.
1. Select the _[!UICONTROL Country]_ to see results for only that specific country.
1. Select the _[!UICONTROL State/province]_ to see results for only that specific State or Province.
1. Select the _[!UICONTROL City]_ to see results for only that specific city.
1. Toggle the _[!UICONTROL Group/Shared Catalog]_ values to see results for only that specific group or shared catalog.
1. Select the _[!UICONTROL Company Admin]_ to see results for only that selected company admin.
1. Select the _[!UICONTROL Job Title]_ to see results for only that job title.
1. Select the _[!UICONTROL Email]_ to see results for only that email.
1. Click **[!UICONTROL Apply filters]** to apply desired filters.

### Search filter

You can search by keyword in this filter for the **Company Hierarchy** view. If you are searching for a parent company, the search returns the parent company and all related companies.

### Actions control options

|Option|Description|
|--- |--- |
|[!UICONTROL Set Active]|Sets the status of all selected company records to `Active`. Company administrators receive instructions to set their passwords so they can access their accounts and manage their companies from the storefront.|
|[!UICONTROL Block]|Restricts company accounts that are not in good standing, while preserving the account. The status of users who are associated with a blocked company is changed to `Inactive`. They cannot sign in to their accounts, or place orders on behalf of the company.|
|[!UICONTROL Delete]|Deletes selected company accounts. The status of user accounts that are associated with a deleted company is set to `Inactive` and the Company ID is removed from the profiles of user accounts. Information about company activity and transactions is retained in the system.|
|[!UICONTROL Edit]|Allows some values of the selected company record to be edited from the grid. By default, the Company Name, Company Email, and Phone Number values are available for a quick edit.|
|[!UICONTROL Convert Credit]|Converts the credit on account for the selected companies according to the rates of the specified currency.|

{style="table-layout:auto"}

## Export report

Download a file with all the companies listed in this view.

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]** > **[!UICONTROL Export]**.
1. You can select an specific file to export the report as:
   * .csv file
   * Excel (xml) file
1. Click the _Export_ button.
