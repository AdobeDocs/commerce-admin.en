---
title: Add users to a company account
description: Learn about adding an existing customer to a company account.
exl-id: ee2f9c27-37d6-4997-8285-1c4c84f8d04c
feature: B2B, Companies, Customers
role: Admin, User
TQID: https://experienceleague.adobe.com/vJaqCSxWxU67fRTwBDDHPGkzpwVma0mhpohWiCLonhM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Add users to a company account

When enabled in the configuration, the company administrator adds and manages company users from the storefront. However, company users accounts can also be added and managed from the Admin.

If needed, you can assign a user to more than one company. For example, if B2B buyers support multiple companies, you can add their user accounts to all companies they do business with. On the storefront, buyers that are assigned to multiple companies can switch between company accounts by selecting from the available companies in the *[!UICONTROL Company]* menu.

![Associate to Company](./assets/company-assign-multi-switcher.png){width="700"}

>[!NOTE]
>
>If an individual already has a personal account with your store, and later goes to work for a company, do not assign the person's individual account to the company. Instead, create a company user account for the person with a company email address.

## Add a company user

When you add a company user, the first company you associate with the user account is the default company.

1. On the Admin sidebar, go to **[!UICONTROL Customers > All Customers]**.

1. Click **[!UICONTROL Add new customer]**.

1. Configure the new account.

   1. Specify initial account status by setting the **[!UICONTROL Customer Active]** toggle.

      Turn it on to immediately activate the account, or disable it to create an inactive account.

   1. Select the website scope from the **[!UICONTROL Associate to Website]** list.

   1. Click **[!UICONTROL Associate to Company]** to view available companies.

      ![Associate to Company](./assets/company-assign-customer-account.png){width="675"}

      If needed, filter the list by typing the first few letters of the company name in the input box.

   1. In the list, select one or more companies where you want to assign the customer and click **[!UICONTROL Done]**.

      Company users are added automatically to the customer group (or [shared catalog](catalog-shared.md)) for each company associated with their account.

   1. Enter required user account information: **[!UICONTROL First Name]**, **[!UICONTROL Last Name]**, and **[!UICONTROL Email]**.

   1. Allow sales representatives to log in to the storefront on behalf of the customer by enabling **[!UICONTROL Allow remote shopping assistance]**.

   1. Apply the changes by clicking **[!UICONTROL Save Customer]**.

      ![Customer grid with company assignments](./assets/company-assign-user-assignments.png){width="675"}

The [!UICONTROL Customers grid] shows a separate row for each company that the user is assigned to. The following columns are updated.

- The _[!UICONTROL Customer Type]_ column updates to show the role assigned to the user.

  If this is the first time the customer has been assigned to a company, the _[!UICONTROL Customer Type]_ column updates from _[!UICONTROL Individual user]_ to _[!UICONTROL Company User]_.

- The _[!UICONTROL Group]_ column changes to the name of the customer group (or shared catalog) that is assigned to the company.

- The _[!UICONTROL Company]_ column displays the name of the company to which the customer profile is now associated.

## Assign a user to one or more company accounts

When you assign a new user, the first company you associate with the user account is the default company.

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Find the customer in the grid and click **[!UICONTROL Edit]** in the _[!UICONTROL Action]_ column.

1. In the left panel, choose **[!UICONTROL Account Information]**.

1. From the **[!UICONTROL Associate to Company]** list, select one or more companies to assign to the company user and click **[!UICONTROL Done]**.

1. Apply the changes by clicking **[!UICONTROL Save Customer]**.

## Remove company assignment from a user account

Removing a company from a user profile revokes user access to that company. User data remains accessible in the Admin. If you remove all company assignments, the _[!UICONTROL Customer Type]_ changes to *[!UICONTROL Individual user]* disabling B2B capabilities for the account.

1. From the Customer grid in the Admin, edit the customer profile to update.

1. In the *[!UICONTROL Account Information] section, remove an assigned company from the **[!UICONTROL Associate to Company]** field by clicking the **[!UICONTROL X]** in the company name label.

1. Apply the changes by clicking **[!UICONTROL Save Customer]**.

>[!NOTE]
>
>If a company user is assigned as the company administrator, you cannot  the company association from this user until you update the Company account to assign a new company administrator.
