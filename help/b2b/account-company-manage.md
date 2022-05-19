---
title: Manage Company Accounts
description: Learn about the Companies page and the tools available in the grid that help you to manage company accounts.
---
# Manage Company Accounts

The _Companies_ page lists all current company accounts, regardless of status. Any pending requests for approval appear at the top of the list. The standard [workplace controls](https://docs.magento.com/user-guide/stores/admin-workspace.html) can be used to filter the list, change the [column layout](https://docs.magento.com/user-guide/stores/admin-grid-controls.html), save views, and export data.

The Actions control above the grid can be used to apply an action to multiple company records. For example, rather than approving each individual company request, you can select multiple requests and activate the accounts in a single action. The actions that are available depend on the [permissions](https://docs.magento.com/user-guide/system/permissions.html) for the role that is assigned to your Admin user account.

![Companies Grid](./assets/companies-grid.png)<!-- zoom -->

## Company role resources

The [Role Resources](https://docs.magento.com/user-guide/system/permissions-role-resources.html) settings determine the ability to:

- Add a company
- Delete a company
- Apply a balance reimbursement
- View companies

These role resources must be set for the [User Role](https://docs.magento.com/user-guide/system/permissions-user-roles.html) that is assigned for the Admin user account.

## Apply an action

The following actions can be applied to either single or multiple records.

1. On the _Admin_ sidebar, go to **Customers** > **Companies**.

1. In the first column of the grid, select the checkbox of each record that you want to update and follow the instructions for the action that you want to apply:

### Activate company accounts

1. Set the **Actions** control to `Set Active`.

1. When prompted to confirm, click **OK**.

### Block company accounts

Users who are associated with a blocked company account cannot access the account, or place orders from the store. A company with an account that is not in good standing might be blocked temporarily until the matter is resolved.

1. Set the **Actions** control to `Block`.

1. When prompted to confirm, click **OK**.

### Delete company accounts

Deleted company accounts cannot be restored. The status of user accounts that are associated with the company is set to `Inactive` and the Company ID is removed from the profiles of user accounts. Information about company activity and transactions is retained in the system.

1. Set the **Actions** control to `Delete`.

1. When prompted to confirm, click **OK**.

### Convert the credit currency

The credit in the accounts of selected companies is converted to the current rate of the selected currency.

1. Set the **Actions** control to `Convert Currency`.

1. When prompted to confirm, click **OK**.

1. Choose the **Credit Currency** to be used for the selected company accounts.

   The amounts are recalculated according to the current conversion rates, if available. If not available, you can manually enter custom conversion rates. The system displays as many conversion calculations are needed for the credit currency that is used by the selected companies.

1. Click **Proceed** to complete the conversion.

### Edit a company account

Method 1: **Quick edit**

1. In the first column, select the checkbox of the company account to be edited.

1. Set the **Actions** column to `Edit`.

   Each value that can be updated appears in a text box.

   ![](./assets/companies-grid-quick-edit.png)<!-- zoom -->
   _Quick Edit_

1. Update any of the following values as needed:

   - **Company Name**

   - **Company Email**

   - **Phone Number**

1. Click **Save**.

Method 2: **Full edit**

1. In the grid, find the company record to be edited.

1. Click **Edit** in the _Action_ column.

1. Make the necessary changes to the company information.

   For field descriptions, see [Manage Company Accounts](account-company-manage.md).

1. When complete, click **Save**.

## Assign a sales representative

The sales representative is an [Admin user](https://docs.magento.com/user-guide/system/permissions.html) who is assigned as the point of contact for a company account and receives all automated [email messages](https://docs.magento.com/user-guide/marketing/email-company-configuration.html) related to the company. Only one sales representative can be assigned per company account, but a single sales representative can manage multiple company accounts. The default admin account is assigned as the sales representative, unless a different admin user is assigned.

The name and email address of the assigned sales representative is visible to company members from the company account and quotes page.

1. On the _Admin_ sidebar, go to **Customers** > **Companies**.

1. Find the company in the grid and open in edit mode.

1. Set **Sales Representative** to the Admin user that you want to assign as the point of contact for the company.

1. When complete, click **Save**.

   The assigned sales representative receives email notification of the assignment.

## Update a company profile

The company profile can be maintained from the storefront by the company administrator, and also from the Admin by a store administrator.

![Company Profile](./assets/company-update.png)<!-- zoom -->

1. On the _Admin_ sidebar, go to **Customers** > **Companies**.

1. Find the company in the grid and click **Edit** in the _Action_ column.

1. Update the field values in each section as needed using the field descriptions for reference.

1. When complete, click **Save**.

## Company options and columns

The following sections provide a reference for the available actions, options, and displayed information available for managing company accounts.

## Actions control options

|Option|Description|
|--- |--- |
|Set Active|Sets the status of all selected company records to `Active`. Company administrators receive instructions to set their passwords so they can access their accounts and manage their companies from the storefront.|
|Block|Restricts company accounts that are not in good standing, while preserving the account. The status of users who are associated with a blocked company is changed to `Inactive`. They cannot sign in to their accounts, or place orders on behalf of the company.|
|Delete|Deletes selected company accounts. The status of user accounts that are associated with a deleted company is set to `Inactive` and the Company ID is removed from the profiles of user accounts. Information about company activity and transactions is retained in the system.|
|Edit|Allows some values of the selected company record to be edited from the grid. By default, the Company Name, Company Email, and Phone Number values are available for a quick edit.|
|Convert Credit|Converts the credit on account for the selected companies according to the rates of the specified currency.|

{style="table-layout:auto"}

### Column descriptions

#### Default column layout

|Column|Description|
|--- |--- |
|Select|Checkboxes used to select company records that are to be subjects of an action or use the selection control in the column header to select/deselect all.|
|ID|A unique numeric identifier that is assigned when the request to create a company is submitted.|
|Company Name|The company name is entered when the company account is first created, and can be a shortened version of the full legal name.|
|Company Email|The email address that is associated with the company account.|
|Phone Number|The primary phone number of the company.|
|Country|The country where the company is registered to conduct business.|
|State Province|The state or province where the company is registered to conduct business.|
|City|The city where the company is registered to conduct business.|
|Group/Shared Catalog|The column name depends on whether Shared Catalog is enabled in the configuration. Options: <br/>**Customer Group** - If Shared Catalog is not enabled in the configuration, specifies the name of the [customer group](https://docs.magento.com/user-guide/customers/customer-groups.html) to which the company belongs. <br/>**Shared Catalog** - If Shared Catalog is enabled in the configuration, specifies the name of the shared catalog that is assigned to the customer.|
|Outstanding Balance|The outstanding balance on the company account. the column is blank if the company does not have a credit history, and its credit limit is zero.|
|Company Admin|The first and last name of the company administrator.|
|Job Title|The job title of the company administrator.|
|Email|The email address of the company administrator.|
|Action|**Edit** - Opens the company account in edit mode.|

{style="table-layout:auto"}

#### Additional columns

The following columns are available by changing the [column layout](https://docs.magento.com/user-guide/stores/admin-grid-controls.html) of the grid.

|Column|Description|
|--- |--- |
|Company Legal Name|The full legal name of the company.|
|Street Address|The street address where the company is registered to conduct business.|
|ZIP|The ZIP or postal code where the company  is registered to conduct business.|
|Reseller ID|The resale number that is assigned to the company for tax reporting purposes.|
|VAT/TAX ID|The [value-added tax](https://docs.magento.com/user-guide/tax/vat.html) number that is assigned to the company by some jurisdictions for tax reporting purposes. To configure the customer VAT/TAX ID to appear in the storefront, see [Create New Account Options](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html).|
|Credit Limit|The credit limit that is extended to the company account.|
|Credit Currency|The currency that is accepted by the store for purchases on company credit.|
|[Status](account-company-approve.md)|Indicates the current state of the company account. Options: <br/>**Active** - The company account is approved by the store administrator. The company administrator and associated members can log in the account from the storefront and make purchases. <br/>**Pending Approval** - A request to open a company account has been submitted, but is not yet approved by the store administrator. <br/>**Rejected** - A request to open a company account was submitted, but not approved by the store administrator. The initial login credentials that were used to submit the request are blocked. <br/>**Blocked** - Company members can log in and access the catalog, but cannot make purchases. The store administrator might block a company account that is not in good standing. The block on the account can be removed by the store administrator at any time.|
|Gender|The gender of the company administrator. Options: Male / Female / Not Specified|
|Comment|Notes about the company account for reference and visible only from the Admin.|

{style="table-layout:auto"}

### Button bar

| Button     | Description   |
| ---------- | ------------- |
| Back | Returns to the Companies page without saving changes. |
| Login as Customer | Allows an Admin user to log in to the storefront as the customer and help with their orders. |
| Delete Company | Deletes the company account. The status of user accounts that are associated with the company is set to `Inactive` and the Company ID is removed from the profiles of user accounts. Information about company activity and transactions is retained in the system. |
| Reset | Restores the original values to any fields with unsaved changes. |
| Reimburse Balance | Allows the administrator to reimburse the balance from store credit, referenced by PO number. |
| Save | Saves changes to the company and keeps the profile open.|
| Save & Close | Saves changes to the company and closes the profile.|

{style="table-layout:auto"}

### Field descriptions

|Field|Description|
|--- |--- |
|Company Name|The company name is entered when the company account is first created, and can be a shortened version of the full legal name.|
|[Status](account-company-approve.md)|Indicates the current state of the company account. Options: <br/>**Active** - The company account is approved by the store administrator. The company administrator and associated members can log in the account from the storefront and make purchases. <br/>**Pending Approval** - A request to open a company account has been submitted, but is not yet approved by the store administrator. <br/>**Rejected** - A request to open a company account was submitted, but not approved by the store administrator. The initial login credentials that were used to submit the request are blocked. <br/>**Blocked** - Company members can log in and access the catalog, but cannot make purchases. The store administrator might block a company account that is not in good standing. The block on the account can be removed by the store administrator at any time.|
|Company Email|The email address that is associated with the company account.|
|Sales Representative|The Admin user who is the primary contact for the company account.|

{style="table-layout:auto"}

#### Account Information

|Field|Description|
|--- |--- |
|Company Legal Name|The full legal name of the company.|
|VAT / TAX ID|The tax or [value-added tax](https://docs.magento.com/user-guide/tax/vat.html) number that is assigned to the company for tax reporting purposes.|
|Reseller ID|The resale number that is assigned to the company for tax reporting purposes.|
|Comment|These notes about the company account are for reference and visible only from the Admin.|
|**Legal Address**||
|Street Address|The street address where the company is registered to conduct business.|
|City|The city where the company is registered to conduct business.|
|Country|The country where the company is registered to conduct business.|
|State/Province|The state or province where the company is registered to conduct business.|
|ZIP/Postal Code|The ZIP or postal code where the company is registered to conduct business.|
|Phone Number|The primary phone number of the company.|

{style="table-layout:auto"}

#### Company Admin

|Field|Description|
|--- |--- |
|Job Title|The title of the company administrator who manages the company account.|
|Email|The email address of the company administrator can be the same as the company email address. If a different email address is entered, a separate individual account is created for the company administrator in addition to the company account.|
|Prefix|If applicable, the prefix that is associated with the name of the company administrator (such as `Mr.`, `Ms.`, `Mrs.`, or `Dr.`). Depending on the configuration, the input field might be a text field or list.|
|First Name|The first name of the company administrator.|
|Middle Name/Initial|The middle name or initial of the company administrator.|
|Last Name|The last name of the company administrator.|
|Suffix|If applicable, the suffix that is associated with the name of the company administrator (such as `Jr.`, `Sr.`, or `III`). Depending on the configuration, the input field might be a text field or list.|
|Gender|The gender of the company administrator. Options: `Male` / `Female` / `Not Specified`|

{style="table-layout:auto"}

#### Company Credit

|Field|Description|
|--- |--- |
|Credit Currency|The currency that is accepted by the store for purchases on company credit.|
|Credit Limit|The credit limit that is extended to the company account.|
|Allow to Exceed Credit Limit|Indicates if the company has permission to exceed the credit limit. Options: Yes / No|
|Reason for Change|A note that explains why the company is allowed, or disallowed to exceed the credit limit. This field is active only if the permission to exceed the credit limit changes.|

{style="table-layout:auto"}

#### Advanced Settings

|Field|Description|
|--- |--- |
|Customer Group|Indicates the [customer group](https://docs.magento.com/user-guide/customers/customer-groups.html) or [shared catalog](https://docs.magento.com/user-guide/catalog/catalog-shared.html) that is assigned to the company.|
|Allow Quotes|Determines if company members can prepare and submit negotiable quotes on behalf of the company.|
|Enable Purchase Orders|Determines if Purchase Orders are permitted for the company. For purchase orders to function for company member accounts, the company administrator must also enable this feature on the storefront. | 
|Applicable Payment Methods|Indicates the payment methods that are available for company purchases. Options: B2B Payment Methods / All Enabled Payment Methods / Specific Payment Methods|
|Payment Methods|(Admin Only) Becomes active if specific payment methods are indicated. To select multiple payment methods, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.|

{style="table-layout:auto"}
