---
title: Manage Company User Accounts
description: Learn about company user accounts and how they function within the associated company account.
---
# Manage Company User Accounts

Company users are assigned by the company administrator, and are visible from the Admin in the _Customers_ grid by the customer type, _Company User_. These individuals are typically buyers with varying levels of permission to access store services and resources.

The company administrator first sets up the [company structure](account-company-structure.md), and then completes the following tasks, as needed:

- Create company users and assign users to teams

- Define roles and permissions, and assign users to roles

>[!IMPORTANT]
>
>Company users can be added, edited, or removed only by the company administrator. Removal cannot be reversed because the user is removed from the company structure.

## Add company users

1. From the storefront, the company administrator signs in to their account.

1. In the left panel, chooses **Company Users**.

   ![Company Users](./assets/company-users-list-storefront.png)<!--- zoom --->

1. Clicks **Add New User** and does the following:

   - Enters the **Job Title** of the new user.

   - If the roles and permissions are defined, chooses the appropriate **User Role**. Otherwise, they can return later to assign the role.

      ![Add new user](./assets/company-structure-users-add.png)<!--- zoom --->

   - Completes the remaining fields as needed for the user:

      - **First Name** and **Last Name**
      - **Email**
      - **Phone Number**

   By default, the **Status** of the account is `Active`.

1. When complete, clicks **Save**.

1. Repeats the process to create as many company users as needed.

   The new users appear in the Company Users list, along with the Company Administrator.

To save time during their first order, the company administrator can remind each company user to add the default company billing and shipping address to their [address book](https://docs.magento.com/user-guide/customers/account-dashboard-address-book.html).

![List of Company Users](./assets/company-users-list-storefront.png)<!--- zoom --->

## Edit company users

1. From the storefront, the company administrator signs in to their account.

1. In the left panel, chooses **Company Users**.

1. Finds the user record to be updated, and clicks **Edit**.

1. Makes the needed changes.

1. When complete, clicks **Save**.

## Remove a company user

1. From the storefront, the company administrator signs in to their account.

1. In the left panel, chooses **Company Structure**.

1. Selects the company user in the company structure.

1. Clicks **Delete Selected**.

   ![Delete User](./assets/company-structure-delete-user.png)<!--- zoom --->

1. When prompted to confirm, clicks **Delete**.

In the Admin, the company user remains listed in the [Customers](https://docs.magento.com/user-guide/customers/customers-all.html) grid, but with an `Inactive` status.

## Field descriptions

| Field        | Description |
|--------------|---------------|
| Job Title    | The job title of the company user. |
| User Role    | The [role](account-company-roles-permissions.md) assigned to the company user. Options: Default User / (other roles) |
| First Name   | The first name of the company user.  |
| Last Name    | The last name of the company user.   |
| Email        | The email address of the company user.  |
| Phone Number | The phone number of the company user.  |
| Status       | The status of the company user account. Options: Active / Inactive  |

{style="table-layout:auto"}
