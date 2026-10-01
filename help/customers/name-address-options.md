---
title: Customer name and address options
description: The customer name and address options determine which fields are included in the name and address forms.
exl-id: 28949cfc-2c96-4d0a-a35b-b37b3aa2d1e9
feature: Customers, Configuration
TQID: https://experienceleague.adobe.com/qMXVcVWZJCrCNywOJF3psuO5vLWkNt9LoNtgFfFBzT8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
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
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
---
# Customer name and address options

The _Name and Address Options_ determine which fields are included in the name and address forms when customers create an [account](../customers/account-create.md) with your store.

![Customer Account sign up form](assets/storefront-customer-account-address-book.png){width="500" zoomable="yes"}

The steps for configuring the name and address options are different for Adobe Commerce and Magento Open Source.

## Configure name and address options for Adobe Commerce

You can configure the name and address options that are presented to customers on the storefront when they create their account.

### Step 1: Set the scope of the configuration

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Customers]** and choose **[!UICONTROL Customer Configuration]**.

1. Expand the **[!UICONTROL Name and Address Options]** section.

   >[!INFO]
   >
   >Notice that the scope of the name and address options applies at the `website` level.

1. Scroll up to the top of the page and set the scope of the configuration to one of the following:

   - `Default Config`
   - `Main Website` (or specific site for multi-site installations)

   >[!INFO]
   >
   >The _[!UICONTROL Name and Address Options]_ section doesn't appear when the scope is set to `Default Store View`.

   ![Configuration Scope](assets/customer-configuration-scope-ee.png){width="700" zoomable="yes"}

### Step 2: Configure the name and address options

1. Return to the [!UICONTROL _Name and Address Options_] section of the Customer Configuration page.

   >[!INFO]
   >
   > If you are not using the `Default config` scope setting, you must clear the `Use Default` checkbox for each field before changing the value.

   ![Name and Address Options](../configuration-reference/customers/assets/customer-configuration-name-address-options-ee.png){width="600" zoomable="yes"}

1. For **[!UICONTROL Prefix Dropdown Options]**, enter each prefix that you want to appear in the list, separated by a semicolon.

   >[!IMPORTANT]
   >
   >Place a semicolon before the first value to display a blank value at the top of the list.

1. For **[!UICONTROL Suffix Dropdown Options]**, enter each suffix that you want to appear in the list, separated by a semicolon.

1. To include the following fields in customer forms, set the value of each to `Optional` or `Required`, as needed.

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### Step 3: Save and refresh

1. When complete, click **[!UICONTROL Save Config]**.

1. In the message at the top of the page, click **[!UICONTROL Cache Management]** and [refresh](../systems/cache-management.md) each invalid cache.

## Configure name and address options for Magento Open Source

Configure the name and address options that are presented to customers on the storefront when they create their account.

![Customer Account sign up form](assets/storefront-customer-account-signup.png){width="500" zoomable="yes"}

### Step 1: Set the scope of the configuration

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Customers]** and choose **[!UICONTROL Customer Configuration]**.

1. Expand the **[!UICONTROL Name and Address Options]** section.

   >[!IMPORTANT]
   >
   > Notice that the scope of the name and address options applies at the `website` level.

   ![Name and Address Options](../configuration-reference/customers/assets/customer-configuration-name-address-options-ce.png){width="600" zoomable="yes"}

1. Scroll back up to the top of the page and set the scope of the configuration to one of the following:

   - `Default Config`
   - `Main Website` (or specific site for multi-site installations)

   >[!NOTE]
   >
   >The _Name and Address Options_ section doesn't appear when the scope is set to `Default Store View`.

   ![Configuration Scope](assets/configuration-scope.png){width="600" zoomable="yes"}

### Step 2: Configure the name and address options

1. Return to the [!UICONTROL _Name and Address Options_] section of the Customer Configuration page.

   >[!INFO]
   >
   >If you are not using the `Default config` scope setting, you must clear the `Use Default` checkbox for each field before changing the value.

1. For **Number of Lines in a Street Address**, enter a number from 1 to 4.

   >[!WARNING]
   >
   >By default, the street address is three lines.

1. To include a prefix (such as Mr. or Ms.) as part of the name, set **Show Prefix** to `Yes`.

   ![Prefix in customer sign up form](assets/storefront-customer-account-prefix.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >For **Prefix Dropdown Options**, enter each prefix that you want to appear in the list, separated by a semicolon. You can place a semicolon before the first value to display a blank value at the top of the list.

1. To include an optional field for the customer's middle name or initial, set **[!UICONTROL Show Middle Name (initial)]** to `Yes`.

1. To include a suffix (such as Jr. or Sr.) after the customer name, set **[!UICONTROL Show Suffix]** to one of the following:

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >For **Suffix Dropdown Options**, enter each suffix that you want to appear in the list, separated by a semicolon. You can place a semicolon before the first value to display a blank value at the top of the list.

1. To include the date of birth, set **[!UICONTROL Show Date of Birth]** to one of the following:

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >In keeping with current security and privacy best practices, be aware of any potential legal and security risks associated with the storage of customers' full date of birth (month, day, year) with other personal identifiers. It is recommended that you limit the storage of customers' full birth dates and suggest using customer year of birth as an alternative.

   Customers can use the Calendar icon after the field to choose the birth date from a pop-up calendar.

   ![Date of Birth in customer sign up form](assets/storefront-customer-account-date-of-birth.png){width="600" zoomable="yes"}

1. To allow customers to enter their tax or [VAT](../stores-purchase/vat.md) number, set **[!UICONTROL Show Tax/VAT Number]** to one of the following:

   - `Optional`
   - `Required`

1. To include a field for gender in the customer form, set **[!UICONTROL Show Gender]** to one of the following:

   - `Optional`
   - `Required`

   ![Gender Options in customer sign up form](assets/storefront-customer-account-gender.png){width="600" zoomable="yes"}

1. To include the following fields in customer forms, set the value of each to `Optional` or `Required`, as needed.

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### Step 3: Save and refresh

1. When complete, click **[!UICONTROL Save Config]**.

1. In the message at the top of the page, click **[!UICONTROL Cache Management]** and [refresh](../systems/cache-management.md) each invalid cache.
