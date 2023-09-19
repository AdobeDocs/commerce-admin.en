---
title: User roles
description: Learn how to create user roles and the associated permissions to manage access to Admin functions.
exl-id: a70f74d4-72b4-4639-a67d-9fc13df65924
feature: Admin Workspace, Roles/Permissions, Security
---
# User roles

To give someone restricted access to the Admin, the first step is to create a role that has the appropriate level of permissions. After the role is saved, you can add new users and assign the restricted role to grant them limited access to the Admin.

![Admin - user roles](./assets/permissions-role-grid.png){width="600" zoomable="yes"}

## Define a role

1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Permissions]_ > **[!UICONTROL User Roles]**.

1. In the upper-right corner, click **[!UICONTROL Add New Role]**.

1. Complete the steps to define the role:

### Step 1: Add the role name

1. Under _[!UICONTROL Role Information]_, enter a descriptive **[!UICONTROL Role Name]**.

1. Under _[!UICONTROL Current User Identity Verification]_, enter your password.

   ![System permissions - role information](./assets/permissions-role-info.png){width="600" zoomable="yes"}

### Step 2: Assign resources

>[!IMPORTANT]
>
>When assigning resources, be sure to disable access to the Permissions tool if you are limiting access for a given role. Otherwise, users are able to modify their own permissions.

1. Set **[!UICONTROL Role Scopes]** to one of the following:

   - `All`
   - `Custom`

   If set to `Custom` for a multisite installation, select the checkbox of the website and store where the role is to be used.

   ![User role resources - custom scope](./assets/permissions-role-scope-custom.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Users with a `Custom` role scope are not able to create websites and categories, assign products to categories, or edit products at _[!UICONTROL All Store Views]_ scope when they are assigned to restricted stores. These users also cannot perform other _global_ actions that affect scopes where they do not have access.

1. Under _[!UICONTROL Roles Resources]_, set **[!UICONTROL Resource Access]** to `Custom`.

1. In the **[!UICONTROL Resource]** tree structure, select the checkbox of each Admin capability that the role can access.

   To create an Admin role with access to tax settings, choose both the Sales/Tax and System/Tax resources. If setting up a website for a region that differs from your default [shipping point of origin](../stores-purchase/shipping-settings.md#point-of-origin), you must allow access to the System/Shipping resources for the role. The shipping settings determine the store tax rate that is used for catalog prices.

   ![Assigned user role resources](./assets/permissions-role-resources-product.png){width="600" zoomable="yes"}

   The list of available permissions may include additional options for bundled and installed extensions. By selecting the top-most permission for each feature, you assign all permissions available for the user.

   >[!NOTE]
   >
   >An Admin user must have **[!UICONTROL Sales / Archive]** permissions for their role scope to see the _[!UICONTROL Invoices]_, _[!UICONTROL Credit Memos]_, and _[!UICONTROL Shipments]_ order [tabs](../stores-purchase/order-processing.md).

1. When complete, click **[!UICONTROL Save Role]**.

   The role now appears in the grid and can be assigned to user accounts.

## Assign a role to users

1. From the _[!UICONTROL Roles]_ grid, open the record in edit mode.

1. Under _[!UICONTROL Current User Identity Verification]_, enter your user account password.

1. In the left panel, choose **[!UICONTROL Role Users]**.

   The _[!UICONTROL Role Users]_ option appears only after a new role is saved.

   ![User accounts assigned to the role](./assets/permissions-role-users.png){width="600" zoomable="yes"}

1. To search for a specific user record, do the following:

   - Enter the value in the search filter at the top of a column and press **Enter**.

   - When you are ready to return to the full list, click **[!UICONTROL Reset Filter]**.

1. Select the checkbox of any users to be assigned to the role.

1. Click **[!UICONTROL Save Role]**.

## Edit a role

1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Permissions]_ > **[!UICONTROL User Roles]**.

1. Locate the role using filters above the grid and click the role name.

1. Make needed changes.

   Review the steps for creating a user role for information about the role settings.

1. When prompted, enter your password to confirm your identity.

1. Click the **[!UICONTROL Save Role]**.

## Delete a role

1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Permissions]_ > **[!UICONTROL User Roles]**.

1. Locate the role using filters above the grid and open in edit mode.

1. In the upper-right corner, click **[!UICONTROL Delete Role]**.

1. To confirm the action, click **[!UICONTROL OK]**.

## User roles demo

Watch this video to learn about managing user roles:

>[!VIDEO](https://video.tv.adobe.com/v/343654?quality=12)

## Role resources

Access to the following resources can be assigned to a custom role. See the linked page to learn more about the capabilities that are associated with each resource.

![Adobe Commerce](../assets/adobe-logo.svg) - Adobe Commerce only

![B2B for Adobe Commerce](../assets/b2b.svg) - Available with B2B for Adobe Commerce only

| Resource |   |   |
| --- | --- | --- |
|[`Dashboard`](../getting-started/admin-dashboard.md)|||
|[`Sales`](../stores-purchase/sales-menu.md)|[`Operations`](../stores-purchase/orders.md)||
||[`Quotes`](../b2b/quotes.md) ![B2B for Adobe Commerce](../assets/b2b.svg) <br/>[`Orders`](../stores-purchase/orders.md)<br/>[`Invoices`](../stores-purchase/invoices.md)<br/>[`Shipments`](../stores-purchase/shipments.md)<br/>[`Credit Memos`](../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Transactions`](../stores-purchase/transactions.md)|
||[`Archive`](action-log-archive.md)![Adobe Commerce]||
||[`Shopping Cart Management`](../stores-purchase/cart.md)||
|[`Catalog`](../catalog/catalog-menu.md)|[`Category Permissions`](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg)||
||[`Inventory`](../inventory-management/introduction.md)|[`Products`](../catalog/products-list.md)<br/>[`Categories`](../catalog/categories.md)|
||[`Shared Catalog`](../b2b/catalog-shared-create.md) ![B2B for Adobe Commerce](../assets/b2b.svg) |[`Manage Shared Catalog`](../b2b/catalog-shared-manage.md)|
|[`Customers`](../customers/guide-overview.md) | [`All Customers`](../customers/customers-all.md)<br/>[`Now Online`](../customers/now-online.md)<br/>[`Customer Groups`](../customers/customer-groups.md)<br/>[`Segments`](../customers/customer-segments.md) ![Adobe Commerce](../assets/adobe-logo.svg)||
||[`Login as Customer`](../customers/login-as-customer.md)|`Allow Login as Customer Button`<br/>`View Login as Customer Log` ![Adobe Commerce](../assets/adobe-logo.svg)|
||[`Companies`](../b2b/account-companies.md) ![B2B for Adobe Commerce](../assets/b2b.svg) | [`Manage Companies`](../b2b/account-company-manage.md) <br/>`Add New Company` <br/>`Delete Company` <br/>`Reimburse Balance` |
|[`Carts`](../stores-purchase/shopping-assisted-cart-manage.md)|[`Manage carts`](../stores-purchase/shopping-assisted-cart-manage.md)||
|[`My Account`](../customers/account-dashboard-my-account.md)|||
|[`Marketing`](../merchandising-promotions/marketing-menu.md)|[`Promotions`](../merchandising-promotions/marketing-menu.md#uicontrol-promotions)|[`Catalog Price Rule`](../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../merchandising-promotions/price-rules-cart.md) <br/>[`Related Products Rules`](../merchandising-promotions/product-related-rules.md)![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Gift Card Accounts`](../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../assets/adobe-logo.svg)|
||[`Private Sales`](../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../assets/adobe-logo.svg)|[`Events`](../merchandising-promotions/event-create.md) <br/>[`Invitations`](../merchandising-promotions/invitations.md) |
||`Communications`|[`Email Templates`](email-templates.md) <br/>[`Newsletter Template`](../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../merchandising-promotions/email-reminder-rules.md) |
||`Sales Channel`|[`Amazon Sales Channel`](https://experienceleague.adobe.com/docs/commerce-channels/amazon/overview.html)|
||[`SEO & Search`](../merchandising-promotions/marketing-menu.md#uicontrol-seo--search)|[`Search Terms`](../catalog/search-terms.md) <br/>[`Search Synonyms`](../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../merchandising-promotions/url-rewrite-custom.md) <br/>[`Site Map`](../merchandising-promotions/sitemap-xml.md)|
||[`User Content`](../merchandising-promotions/product-reviews-moderate.md) | [`All Reviews`](../merchandising-promotions/product-reviews.md) <br/>[`Pending Reviews`](../merchandising-promotions/product-reviews-moderate.md) <br/> ||
|[`Content`](../content-design/content-menu.md) | [`Elements`](../content-design/content-menu.md#uicontrol-elements)) | [`Pages`](../content-design/pages.md)<br/>[`Hierarchy`](../content-design/page-hierarchy.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Blocks`](../content-design/blocks.md)<br/>[`Dynamic Blocks`](../content-design/dynamic-blocks.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Widgets`](../content-design/widgets.md)<br/>[`Media Gallery`](../content-design/media-gallery.md)||
||[`Design`](../content-design/introduction.md#design) | [`Themes`](../content-design/themes.md)<br/>[`Schedule`](../content-design/schedule.md)||
||[Content Staging](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br />||
|[`Reports`](../getting-started/reports-menu.md) | [`Marketing`](../getting-started/marketing-reports.md)|`Shopping Cart`<br />[`Search Terms`](../catalog/search-terms.md#search-terms-report)<br />`Newsletter Problem Reports`||
||[`Reviews`](../getting-started/review-reports.md)<br />||
||[`Sales`](../getting-started/sales-reports.md)||
||`System Insights` ![Adobe Commerce](../assets/adobe-logo.svg)|[`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html)|
||[`Customers`](../getting-started/customer-reports.md)<br/>[`Products`](../getting-started/product-reports.md)<br/>[`Private Sales`](../getting-started/private-sales-reports.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br />[`Statistics`](../getting-started/reports-menu.md#uicontrol-statistics)<br />[`Business Intelligence`](../getting-started/business-intelligence.md)||
|[`Stores`](../stores-purchase/stores.md) | [`Settings`](../stores-purchase/stores-menu.md) | [`All Stores`](../stores-purchase/stores.md)<br/>[`Configuration`](../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../stores-purchase/order-status.md)||
||[`Inventory`](../inventory-management/sources-stocks.md)|[`Sources`](../inventory-management/sources-manage.md)<br/>[`Stocks`](../inventory-management/stocks-manage.md)||
||[`Taxes`](../stores-purchase/taxes.md)|||
||[`Currency`](../stores-purchase/currency.md)|[`Currency Rates`](../stores-purchase/currency-update.md)<br/>[`Currency Symbols`](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional)||
||[`Attributes`](../catalog/product-attributes.md)|[`Product`](../catalog/attribute-product-create.md)<br/>[`Update Attributes`](../catalog/attribute-product-create.md)<br/>[`Attribute Set`](../catalog/attribute-sets.md)<br/>[`Ratings`](../merchandising-promotions/product-reviews.md#create-custom-ratings)|
||[`Other Settings`](../stores-purchase/stores-menu.md)|[`Customer Groups`](../customers/customer-groups.md)|
|[`System`](system-menu.md) | [`Data Transfer`](data-transfer.md) | [`Import`](data-import.md)<br/>[`Export`](data-export.md)<br/>[`Import/Export Tax Rates`](data-transfer-tax-rates.md)<br/>[`Import History`](data-import.md#import-history)||
||[`Magento Connect`](../getting-started/commerce-marketplace.md) | `Connect Manager`<br/>`Package Extensions`||
||[`Tools`](system-menu.md#tools) | [`Cache Management`](cache-management.md)<br/>[`Backups`](backups.md)<br/>[`Index Management`](index-management.md)<br/>[`Change Indexer Mode`](index-management.md) ||
||[`Permissions`](permissions.md) | [`All Users`](permissions-users-all.md)<br/>[`Locked Users`](permissions-users-all.md#locked-users)<br/>[`User Roles`](permissions-user-roles.md)|
|[`Action Log`](action-log.md)![Adobe Commerce](../assets/adobe-logo.svg)| [`Report`](action-log.md)<br/>[`Archive`](action-log-archive.md)|
||[`Other Settings`](system-menu.md)|[`Notifications`](notifications.md)<br/>[`Custom Variables`](variables-custom.md)<br/>[`Manage Encryption Key`](encryption-key.md)||
|[`Global Search`](../getting-started/admin-workspace.md#workspace-search)|||

{style="table-layout:auto"}
