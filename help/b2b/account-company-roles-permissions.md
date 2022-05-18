---
title: Company Roles and Permissions
description: Learn about roles and permissions for company users, allowing for various levels access to order information and resources.
---
# Company Roles and Permissions

Roles for company users are set up with various levels of permission to access sales information and resources. By default, the company administrator is a _super user_ with full permissions. The [Access Denied](https://docs.magento.com/user-guide/cms/pages-core.html) page appears if the user does not have permission to access the page.

![Roles and Permissions page with default role](./assets/company-roles-permissions.png)<!--- zoom --->

The system has one predefined Default User role, which you can use _as is_ or modify to suit your needs. You can create as many roles as necessary to match your company structure and organizational responsibilities, such as the following:

- **Default User** — The default user has full access to activities related to sales and quotes, and view-only access to company profile and credit information.

- **Senior Buyer** — A senior buyer might have access to all Sales and Quotes resources, and view-only permissions to the Company Profile, User and Teams, Payment Information, and Company Credit.

- **Assistant Buyer** — An assistant buyer might have permission to place an order using _Checkout with Quote_, and to view orders, quotes, and information in the company profile.

## Manage roles and permissions

1. The company administrator signs in to their store account.

1. In the left panel, chooses **Roles and Permissions**.

1. Completes any of the following tasks.

### Create a role

1. Click **Add New Role**.

   ![Add New Role](./assets/company-roles-permissions-add-storefront.png)<!--- zoom --->

1. Enter a descriptive **Role Name**.

1. Under _Role Permissions_, do one of the following:

   - Select the checkbox of each resource or activity that users assigned the role have permission to access.

   - Select the **All** checkbox. Then, clear the checkbox of each resource or activity that users assigned to the role do not have permission to access.

1. Click **Save Role**.

1. Create as many roles as necessary by repeating these steps.

### Modify a role

1. For the role to be modified, click **Edit** in the _Actions_ column.

1. Make the necessary changes to the name and permission settings.

1. When complete, click **Save Role**.

### Duplicate a role

1. For the role to be duplicated, click **Duplicate** in the _Actions_ column.

1. Make the necessary changes to the name and permission settings.

1. When complete, click **Save Role**.

### Delete a role

1. Find the role to be deleted In the list of roles.

   Only roles without assigned users can be deleted.

1. Click **Delete** in the _Actions_ column.

1. When prompted to confirm, click **OK**.

## Actions

| Action    | Description |
|-----------| ----------- |
| Duplicate | Creates a copy of the selected role. The name of the duplicate role has `- Duplicated` added to the end. |
| Edit      | Change the name and/or set of permissions.                                                               |
| Delete    | Delete the role. Only roles without assigned users can be deleted.                                       |

{style="table-layout:auto"}

## Role Permissions

- All
   - Sales
      - Allow Checkout (place order)
         - Use Pay On Account method
      - View Orders
         - View orders of subordinate users
- Quotes
   - View
      - Request, Edit, Delete
      - Checkout with quote
      - View quotes of subordinate users
- Order Approvals
   - View My Purchase Orders
      - View for subordinates
      - View for all company
   - Auto-approve POs created within this role
   - Approve Purchase Orders without other approvals
   - View Approval Rules
      - Create, Edit and Delete
- Company Profile
   - Account Information (View)
      - Edit
   - Legal Address
      - Edit
   - Contacts (View)
   - Payment Information (View)
   - Shipping Information (View)
- Company User Management
   - View roles and permissions
      - Manage roles and permissions
   - View users and teams
      - Manage users and teams
- Company Credit
   - View

## Assign a role to a company user

After defining the roles that are needed, the store admin assigns a role to each company user.

1. Log in to your company account as the company administrator.

1. In the left panel, choose **Company Users**.

   ![Company Users](./assets/company-users-list-storefront.png)<!--- zoom --->

1. Find the user in the list and click **Edit**.

1. Choose the appropriate **User Role** for the user.

   ![Edit User - choose a user role](./assets/company-user-assign-role.png)<!--- zoom --->

1. Click **Save**.
