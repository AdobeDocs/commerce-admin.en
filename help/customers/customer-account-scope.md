---
title: Customer Account Scope
description: The scope of customer accounts can be limited to the website where the account was created, or shared with all websites and stores in the store hierarchy.
---

# Customer Account

The header of every page in your store extends an invitation for shoppers to _Log in or register_ for an account with your store. Customers who open an account enjoy a range of benefits, including:

* [!UICONTROL **Create customer account**] - Visitors can create a new customer account so that they can use the storefront as a registered customer.
* [!UICONTROL **Create Individual or Company Account**] Depending on the configuration, a visitor to your store can choose to create either an individual or company account. For more information see [B2B for Adobe Commerce](../b2b/introduction.md).
* [!UICONTROL **Faster checkout**] — Registered customers move through checkout faster because much of the information is already in their accounts.
* [!UICONTROL **Self service**] — Registered customers can update their information, check the status of orders, and even reorder from their accounts.

Customers can access their account by clicking the [!UICONTROL **My Account**] link in the header of the store. From their account, customers can view and modify information, including past and current addresses, billing and shipping preferences, newsletter subscriptions, wishlist, and more.

![My Account](/assets/account-dashboard-my-account.png)<!-- zoom -->

{:.b2b-only}
## Account types

With B2B features enabled, there are two basic types of accounts that can be created:

* Individual — An [individual]({% link customers/account-create.md %}) customer account is similar to a standard Adobe Commerce customer account.
* Company — A [company]({% link customers/account-companies.md %}) account can be set up as a structure with teams of multiple users.

|Field|Description|
|--- |--- |
|Individual User|An individual customer account is similar to a standard Adobe Commerce customer account.|
|Company|A [company]({% link customers/account-companies.md %}) account can be set up as a structure of divisions, subdivisions with multiple users. Companies can be enabled or disabled for each store. Some B2B features, such as Shared Catalog and Quotes are available only for Company accounts. <br/>**Company Admin** - The company administrator is responsible to build the company structure that is needed for the customer account, and define the roles and permissions for  Admin users. The company administrator is set up when creating a company account, but is represented as an individual account in the system. <br/>**Company User** - Company users are authorized to make purchases on behalf of the company, and team, division, or subdivision to which they are associated. Company user accounts are set up by the company administrator, and are represented as individual accounts in the system.|

## Customer Account Scope

The scope of customer accounts can be limited to the website where the account was created, or shared with all websites and stores in the store hierarchy.

## Set the scope of customer accounts

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Customers** and choose **Customer Configuration**.

1. Expand ![Expansion selector]({% link assets/icon-display-expand.png %}) the **Account Sharing Options** section.

   ![]({% link configuration/customers/assets/customer-configuration-account-sharing-options.png %}){: .zoom}
   [_Account Sharing Options_]({% link configuration/customers/customer-configuration.md %})

1. Set **Share Customer Accounts** to one of the following:

   | Global | Shares customer account information with every website and store in the installation. |
   | Per Website | Limits customer account information to the website where the account was created. |

   If necessary, clear the **User system value** checkbox to make the change.

1. When complete, click <span class="btn">Save Config</span>.

   {:.bs-callout-info}
   If the [website is excluded from the customer group]({{ site.devdocs_url }}/guides/v{{ site.version }}/extension-dev-guide/indexer-optimization.html#customer-group-limitations-by-websites), the customer is not allowed to log in to the website when the scope of customer accounts is limited to the website or shared with all websites.
