---
title: Create a Company Account
description: Learn about company account creation in the Admin and on the storefront.
exl-id: 8c06395b-102b-4a41-8eb3-e6a344feac70
---
# Create a Company Account

Company accounts can be set up from the storefront by the customer, or from the Admin. All requests to create a company account must be approved by the store administrator before the account becomes active.

The person who sets up a company account from the storefront is assigned a role as the [company administrator](account-company-admin.md). After the request to create a company account is approved, the company administrator can set an account password and log in to the account.

## Method 1: Customer creates the account from the storefront

>[!IMPORTANT]
>
>To support this method (allowing customers to register their company from the storefront), make sure that the [B2B Features](enable-basic-features.md) are configured so that **[!UICONTROL Allow Company Registration from the Storefront]** is set to `Yes`.

1. In the upper-right corner of the storefront header, the customer clicks **[!UICONTROL Create an Account]** and chooses **[!UICONTROL Create New Company Account]**.

   ![Create New Company Account](./assets/company-account-create-storefront-options.png)<!-- zoom -->

   >[!NOTE]
   >
   >If a visitor is logged in to a registered user account, they can create a company account by navigating to _[!UICONTROL Customer Profile]_ > **[!UICONTROL Company Structure]** > **[!UICONTROL Create a Company Account]**. Upon creation of the company account, the customer's account is assigned as the primary contact. Otherwise, the system creates a customer, who receives an email to set a password.

1. In the _[!UICONTROL Company Information]_ section, does the following:

   - Completes the required fields:

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - If the information is available, completes the remaining fields, as applicable:

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Re-seller ID]**

   ![Company Information](./assets/company-information-storefront.png)<!-- zoom -->

1. Completes the required fields in the _[!UICONTROL Legal Address]_ section.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

   ![Legal Address](./assets/company-legal-address-storefront.png)<!-- zoom -->

1. In the _[!UICONTROL Company Administrator]_ section, does the following:

   - Enters the **[!UICONTROL Email address]** for the company administrator.

      The email address for the company administrator can be the same as the company email address or a different email address. If a different email address is entered, a company user account is created, in addition to the company administrator account.

   - Enters the **[!UICONTROL First Name]** and **[!UICONTROL Last Name]** of the company administrator.

   - Optionally completes the following fields:

      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Gender]**

   ![Company Administrator](./assets/company-administrator-account-storefront.png)

1. If reCAPTCHA is enabled for this storefront function, completes the validation.

1. When complete, clicks **[!UICONTROL Submit]**.

   When the request to create a company account is approved by the merchant, email notification is sent to the company administrator.

   ![](./assets/company-admin-welcome-email.png)<!-- zoom -->

   When the password is set, the company administrator can [sign in](https://docs.magento.com/user-guide/customers/customer-sign-in.html) to the account.

## Method 2: Merchant creates the account from the Admin

The process of creating a company from the Admin is essentially the same as from the storefront, but with additional fields.

![New Company](./assets/company-create-admin.png)<!-- zoom -->

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Click **[!UICONTROL Add New Company]** and do the following:

   - Complete these required fields:

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - If you are not ready for the account to go live, set **[!UICONTROL Status]** to `Pending Approval`. (Set to `Active` by default.)

   - If applicable, choose the Admin account of the **[!UICONTROL Sales Representative]** who is to manage the account.

1. In the _[!UICONTROL Account Information]_ section, do the following:

   - Complete the following fields as applicable:

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   - For **[!UICONTROL Comment]**, enter any additional information about the customer that might be needed.

      The comments are visible only from the Admin.

   ![Account Information](./assets/company-create-account-information-admin.png)<!-- zoom -->

1. In the _[!UICONTROL Legal Address]_ section, complete these required fields:

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City Country]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

1. In the _[!UICONTROL Company Admin]_ section, do the following:

   - Complete these required fields:

      - **[!UICONTROL Email]**
      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**

   - Complete the following optional parts of the name, which might be applicable to some customer names more than others and can be used at your discretion:

      - **[!UICONTROL Prefix]**
      - **[!UICONTROL Middle Name/Initial]**
      - **[!UICONTROL Suffix]**

   - If the information is available, complete the remaining fields to describe the company administrator:

      - **[!UICONTROL Website]**
      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Gender]**
      - **[!UICONTROL Send Welcome Email From]**

    ![Company Admin](./assets/company-create-company-admin.png)<!-- zoom -->

1. In the _[!UICONTROL Company Credit]_ section, which displays a summary of the customer’s credit activity, complete as many of the fields in the lower part of the section as applicable:

   - **[!UICONTROL Credit Currency]**
   - **[!UICONTROL Credit Limit]**
   - **[!UICONTROL Allow to Exceed Credit Limit]**
   - **[!UICONTROL Reason for Change]**

   ![Company Credit](./assets/company-create-credit-admin.png)<!-- zoom -->

1. In the _[!UICONTROL Advanced Settings]_ section, do the following:

   >[!NOTE]
   >
   >The customer group assignment determines which shared catalog is available to the company and its employees. By default, the company is assigned to the customer group that is set as the default in the configuration.

   - You can change the **[!UICONTROL Customer Group]** assignment for the company and its employees to a group that has access to a different shared catalog or to a standard customer group. You are prompted to confirm before the group is changed.

      ![Changing the customer group](./assets/company-advanced-settings-customer-group-admin.png)<!-- zoom -->

   - If you want to allow company employees to generate quotes from their account, set **[!UICONTROL Allow Quotes]** to `Yes`.

   - If you want to allow company employees to use purchase orders from their account, set **[!UICONTROL Enable Purchase Orders]** to `Yes`.

   - To change the **[!UICONTROL Applicable Payment Methods]** that are available to the company, clear the **[!UICONTROL Use config settings]** checkbox and choose one of the following:

      | Option | Description |
      | ------ | ----------- |
      |`B2B Payment Methods`|(Default) Enables all [payment methods set as default](https://docs.magento.com/user-guide/configuration/general/b2b-features.html#default-b2b-payment-methods) for B2B orders.|
      |`All Enabled Payment Methods`|Makes all [enabled payment methods](https://docs.magento.com/user-guide/configuration/sales/payment-methods.html) available for customer accounts associated with the company account.|
      |`Selected Payment Methods`|Allows you to select the payment methods that are available for customer accounts associated with the company account. To select multiple payment methods, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.|

      {style="table-layout:auto"}

   - To change the **[!UICONTROL Applicable Shipping Methods]** that are available to the company, clear the **[!UICONTROL Use config settings]** checkbox and choose one of the following:

      | Option | Description |
      | ------ | ----------- |
      |`B2B Shipping Methods`|(Default) Enables all [shipping methods set as default](https://docs.magento.com/user-guide/configuration/general/b2b-features.html#default-b2b-shipping-methods) for B2B orders.|
      |`All Enabled Shipping Methods`|Makes all [enabled shipping methods](https://docs.magento.com/user-guide/configuration/sales/delivery-methods.html) available for customer accounts associated with the company account.|
      |`Selected Shipping Methods`|Allows you to select the shipping methods that are available for customer accounts that are associated with the company account. To select multiple shipping methods, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.|

      {style="table-layout:auto"}

1. When complete, click **[!UICONTROL Save]**.

   When the request to create a company account is approved by the merchant, an email notification is sent to the email address of the company administrator.

   When the password is set, the company administrator can [sign in](https://docs.magento.com/user-guide/customers/customer-sign-in.html) to the account.

## Button bar

| Button | Description |
|------- | ----------- |
| [!UICONTROL Back ]| Returns to the Companies page without saving changes.|
| [!UICONTROL Reset] | Restores the original values to any fields with unsaved changes.|
| [!UICONTROL Save] | Saves changes to the company, and keeps the profile open.|
| [!UICONTROL Save & Close] | Saves changes to the company and closes the profile.|

{style="table-layout:auto"}

## Field descriptions

|Field|Description|
|--- |--- |
|[!UICONTROL Company Name]|The company name is entered when the company account is first created, and can be a shortened version of the full legal name.|
|[!UICONTROL Status]|(Admin Only) Indicates the current state of the company account. Options: <br/>**[!UICONTROL Active]** - The company account is approved by the store administrator. The company administrator and associated members can log in the account from the storefront and make purchases. <br/>**[!UICONTROL Pending Approval]** - A request to open a company account has been submitted, but is not yet approved by the store administrator. <br/>**[!UICONTROL Rejected]** - A request to open a company account was submitted, but not approved by the store administrator. The initial login credentials that were used to submit the request are blocked. <br/>**Blocked** - Company members can log in and access the catalog, but cannot make purchases. The store administrator might block a company account that is not in good standing. The block on the account can be removed by the store administrator at any time.|
|[!UICONTROL Company Email]|The email address that is associated with the company account.|
|[!UICONTROL Sales Representative]|(Admin Only) The Admin user who is the primary contact for the company account.|

{style="table-layout:auto"}

### [!UICONTROL Account Information]

|Field|Description|
|--- |--- |
|[!UICONTROL Company Legal Name]|The full legal name of the company.|
|[!UICONTROL VAT / TAX ID]|The [value-added tax](https://docs.magento.com/user-guide/tax/vat.html) number that is assigned to the company by some jurisdictions for tax reporting purposes. To configure the customer VAT/TAX ID to appear in the storefront, see [Create New Account Options](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html). <br/> **_Note:_** The company administrator and other company users do not have their own separate VAT/TAX ID numbers in their customer accounts.|
|[!UICONTROL Reseller ID]|The resale number that is assigned to the company for tax reporting purposes.|
|[!UICONTROL Comment]|(Admin Only) These notes about the company account are for reference and visible only from the Admin.|

{style="table-layout:auto"}

### [!UICONTROL Legal Address]

|Field|Description|
|--- |--- |
|[!UICONTROL Street Address]|The street address where the company is registered to conduct business.|
|[!UICONTROL City]|The city where the company is registered to conduct business.|
|[!UICONTROL Country]|The country where the company is registered to conduct business.|
|[!UICONTROL State/Province]|The state or province where the company is registered to conduct business.|
|[!UICONTROL ZIP/Postal Code]|The ZIP or postal code where the company is registered to conduct business.|
|[!UICONTROL Phone Number]|The primary phone number of the company.|

{style="table-layout:auto"}

### [!UICONTROL Company Admin]

|Field|Description|
|--- |--- |
|[!UICONTROL Website]|Determines the website the company administrator belongs to.|
|[!UICONTROL Job Title]|The title of the company administrator who manages the company account.|
|[!UICONTROL Email]|The email address of the company administrator can be the same as the company email address. If a different email address is entered, a separate individual account is created for the company administrator, in addition to the company account.|
|[!UICONTROL Prefix]|If applicable, the prefix that is associated with the name of the company administrator (such as `Mr.`, `Ms.`, `Mrs.`, or `Dr.`). Depending on the configuration, the input field might be a text field or list.|
|[!UICONTROL First Name]|The first name of the company administrator.|
|[!UICONTROL Middle Name/Initial]|The middle name or initial of the company administrator.|
|[!UICONTROL Last Name]|The last name of the company administrator.|
|[!UICONTROL Suffix]|If applicable, the suffix that is associated with the name of the company administrator (such as `Jr.`, `Sr.`, or `III.`). Depending on the configuration, the input field might be a text field or list.|
|[!UICONTROL Gender]|The gender of the company administrator. Options: `Male` / `Female` / `Not Specified`|
|[!UICONTROL Send Welcome Email From]|The store view from which the Welcome email is to be sent.|

{style="table-layout:auto"}

### [!UICONTROL Company Credit]

|Field|Description|
|--- |--- |
|[!UICONTROL Credit Currency]|(Admin Only) The currency that is accepted by the store for purchases on company credit.|
|[!UICONTROL Credit Limit]|(Admin Only) The credit limit that is extended to the company account.|
|[!UICONTROL Allow to Exceed Credit Limit]|(Admin Only) Indicates if the company has permission to exceed the credit limit. Options: `Yes` / `No`|
|[!UICONTROL Reason for Change]|(Admin Only) A note that explains why the company is allowed, or disallowed to exceed the credit limit. This field is active only if the permission to exceed the credit limit changes.|

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings]

|Field|Description|
|--- |--- |
|[!UICONTROL Customer Group]|(Admin Only) Indicates the [customer group](https://docs.magento.com/user-guide/customers/customer-groups.html) or [shared catalog](catalog-shared.md) that is assigned to the company.|
|[!UICONTROL Allow Quotes]|(Admin Only) Determines if company members can prepare and submit negotiable quotes on behalf of the company.|
|[!UICONTROL Enable Purchase Orders]|(Admin Only) Determines if company members can submit orders as [purchase orders](account-dashboard-my-purchase-orders.md) on behalf of the company.|
|Applicable Payment Methods|(Admin Only) Indicates the payment methods that are available for company purchases. Options: `B2B Payment Methods` / `All Enabled Payment Methods` / `Selected Payment Methods`|
|[!UICONTROL Payment Methods]|(Admin Only) Becomes active if specific payment methods are activated. To make multiple payment methods available for the company account, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.|
|[!UICONTROL Applicable Shipping Methods]|(Admin Only) Indicates the payment methods that are available for company purchases. Options: `B2B Shipping Methods` / `All Enabled Shipping Methods` / `Selected Shipping Methods`|
|[!UICONTROL Shipping Methods]|(Admin Only) Becomes active if specific shipping methods are activated. To make multiple payment methods available for the company account, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.|

{style="table-layout:auto"}
