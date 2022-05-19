---
title: Company Accounts
description: Learn how company accounts allow for joining multiple buyers that belong to the same company into a single company account. 
---
# Company Accounts

When you incorporate B2B company accounts in your store, you can simplify the corporate shopping experience by enabling companies to create multiple subaccounts with flexible permissions based on user roles in their organization. Depending on the customer groups of the company, a store administrator can adjust promotions and prices to suit their needs, and create highly customized offers that cater to the shoppers’ demands and increase orders. Adding a company account association to a standard [individual](https://docs.magento.com/user-guide/customers/account-create.html) allows the customer to use the specific purchasing workflows defined for the company.

Advantages of a company account:

- Offers unlimited [company users](account-company-users.md) and the creation of additional accounts, which simplifies corporate purchases.

- Includes support for a _smart_ company account hierarchy with different [roles and permissions](account-company-roles-permissions.md) for placing orders.

- Provides a mechanism for merchants to increase income by offering [company store credit](credit-company.md) as a payment method.

- Supports the [management](account-company-manage.md) of all company accounts in the Admin.

## Company structure

A company account can be set up to reflect the structure of the business. Initially, the company structure includes only the company administrator, but can be expanded to include teams of users. The users can be associated with teams or organized within a hierarchy of divisions and subdivisions within the company.

![Company Structure with Divisions](./assets/company-structure-diagram.png)<!-- zoom -->

In the customer’s account dashboard, the company structure is represented as a tree and initially consists of only the company administrator.

![Company Structure with Company Administrator](./assets/company-structure-tree-admin.png)<!-- zoom -->

When the account is created, the company administrator can use the company email address or be assigned a different email address.

It is possible that the person who serves as company administrator has multiple roles within the company. If a separate email address is entered for the company administrator, the initial company structure includes the company administrator plus an individual user account in the name of the company administrator. In such a case, the company administrator can sign in to the account as the company or as an individual user.

![Company Structure with Administrator and User Account](./assets/company-structure-tree-admin-user.png)<!-- zoom -->

The full company structure is reflected in the Companies and Customers grids. The Companies grid lists all companies regardless of status. The following example shows accounts for two companies: the “ABC Company” and the “XYZ Company”.

![Companies Grid](./assets/companies-grid.png)<!-- zoom -->

The following example shows the Customers grid with the initial company administrator account for the “XYZ Company”.

![Customers grid with company administrator account](./assets/company-admin-user-account.png)<!-- zoom -->

After creating the account, the company administrator must define the company structure of [teams](account-company-structure.md), set up the [company users](account-company-users.md), and establish [roles and permissions](account-company-roles-permissions.md) for each.

## View company accounts

The _Companies_ grid lists all active company accounts and pending requests, regardless of status setting. It also provides the tools for [creating](account-company-create.md) and [managing](account-company-manage.md) company accounts. Use the standard grid controls to filter the list, and adjust the column layout. For a list of column descriptions, see the _Column Descriptions_ section in [Managing Company Accounts](account-company-manage.md).

Customers can create a company account from the storefront, or a merchant can create one from the Admin. By default, the ability to create company accounts from the storefront is enabled. If allowed by the configuration, a visitor to the store can request to open a company account. After the company account is approved, the company administrator can set up the company structure and users with various levels of permission.

In the _Admin_ sidebar, go to **Customers** > **Companies**.

![Companies grid](./assets/companies-grid.png)<!-- zoom -->
