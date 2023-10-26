---
title: Company management
description: Learn about company management and how they function between companies in B2B.
feature: B2B, Companies, Management, Storefront
role: Admin
hide: yes
hidefromtoc: yes
---

# Company management

The Company management feature allows company Administrators to view and manage the parent company and its internal organization with all related companies. Administrators will be able to assign or unassign companies to the parent company or manage the roles and permissions within those companies. B2B company management is an excellent opportunity to improve the performance within a company.

From a business point of view, the controlling or owning company is generally called a parent company. While many parent companies will completely own their related companies, they can also be just one of the owners or members as well. In most cases, however, the parent company will be the majority shareholder. Although those companies are connected, they are two distinct legal entities.

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

When a company administrator has created a new company, you can select the dropdown called **Company Hierarchy** where you can view the parent company and its related companies, or [assign and unassign companies](assign-companies.md) to that parent company.

>[!IMPORTANT]
>
> The **Company Hierarchy** view for a parent company appears as empty.

Once the [company account](account-company-create.md) is created and the company administrator and other users have been setup, you can specify the inheritance in the company management:

* Full Inheritance: Shared catalogs, quotes, payment and shipping methods are replicated between the parent company to its related companies.
* Partial Inheritance: Specify what is inherited between the parent company to its related companies.
* No Inheritance: No inheritance between the parent company and its related companies.

## Column descriptions

The **Company Hierarchy** view provides visibility on all the information related to company management in B2B. The main columns shown are as follows:

|Columns|Description|
|--- |--- |
|[!UICONTROL Company Name]|The full name of the company.|
|[!UICONTROL Company Type]|The type of the company. Options: <br/>**[!UICONTROL Parent]** - The company is the parent company of other companies. <br/>**[!UICONTROL Company]** - This company is related to a parent company. |
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

From the **Company Hierarchy** view, you can filter the companies shown in the list by selecting filter criteria.

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.
1. Click the **[!UICONTROL Filters]** selector.
1. Toggle the _[!UICONTROL Transaction Result]_ options to see report results for only selected order transactions.
1. Select the _[!UICONTROL Company Type]_ to see report results for only that selected type of card. A tooltip is shown when the payment processor is unable to identify the card type.
1. Select the _[!UICONTROL Card Brand]_ to see report results for only that selected card brand. A tooltip is shown when the payment processor is unable to identify the card brand.
1. Toggle the _[!UICONTROL Payment Method]_ options to see report results for only selected payment methods.
1. Enter a _Min Order Amount_ or _Max Order Amount_ to see report results within that order amount range.
1. Enter an _[!UICONTROL Order ID]_ to search for a specific transaction.
1. Enter the _[!UICONTROL Card Last Four Digits]_ to search for a specific credit or debit card.
1. Click **[!UICONTROL Apply filters]** to apply desired filters.

### Search filter

You can search by keyword in this filter for the **Company Hierarchy** view.

## Export report

You can download a file with all the companies listed in this view.

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]** > **[!UICONTROL Export]**.
1. You can select an specific file to export the report as:
   * .csv file
   * Excel (xml) file
1. Click the _Export_ button.
