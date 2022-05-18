---
title: Add Customers to a Company
description: Learn about adding an existing customer to a company account.
---
# Add Customers to a Company

When enabled in the configuration, the company administrator adds users to the company. However, the company assignment of a customer profile can also be made or changed from the Admin.

>[!NOTE]
>
>If an individual already has a personal account with your store, and later goes to work for a company, do not assign the person’s individual account to the company. Instead, create a company user account for the person with a company email address.

1. On the _Admin_ sidebar, go to **Customers** > **All Customers**.

1. Find the customer in the grid and click **Edit** in the _Action_ column.

1. In the left panel, choose **Account Information**.

1. Click **Associate to Company** and type the first few letters of the company name in the input box.

   The system generates a list of all possible matches.

   ![Associate to Company](./assets/company-assign-customer-account.png)<!--- zoom --->

1. In the list, select the company where you want to assign the customer and click **Done**.

1. If the customer was previously assigned to a different company, click **Confirm**.

   The customer is reassigned to the customer group (or [shared catalog](catalog-shared.md)) of the company and added to its [company structure](account-company-structure.md).

1. When complete, click **Save Customer**.

   The following columns are updated in the [Customers](https://docs.magento.com/user-guide/customers/customers-all.html) grid:

   - The _Group_ column changes to the name of the customer group (or shared catalog) that is assigned to the company.
   - The _Company_ column displays the name of the company to which the customer profile is now associated.
