---
title: User roles
description: Placeholder
---
# User roles

To give someone restricted access to the Admin, the first step is to create a role that has the appropriate level of permissions. After the role is saved, you can add new users and assign the restricted role to grant them limited access to the Admin.

![Admin - user roles](./assets/permissions-role-grid.png)

## Define a role

1. On the _Admin_ sidebar, go to **System** > _Permissions_ > **User Roles**.

1. In the upper-right corner, click **Add New Role**. Then, complete the steps to define the role:

### Step 1: Add the role name

1. Under _Role Information_, enter a descriptive **Role Name**.

1. Under _Current User Identity Verification_, enter **Your Password**.

   ![System permissions - role information](./assets/permissions-role-info.png)<!-- zoom -->

### Step 2: Assign resources

>[!IMPORTANT]
>
>When assigning resources, be sure to disable access to the Permissions tool if you are limiting access for a given role. Otherwise, users will be able to modify their own permissions.

1. Set **Role Scopes** to one of the following:

    - `All`
    - `Custom`

   ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) If set to `Custom` for a multisite installation, select the checkbox of the website and store where the role is to be used.

   ![User role resources - custom scope](./assets/permissions-role-scope-custom.png)<!-- zoom -->

   >[!NOTE]
   >
   >Users with a `Custom` role scope are not able to create websites and categories, assign products to categories, edit products at _All Store Views_ scope when they are assigned to restricted stores as well, or do other _global_ actions that affect scopes where they do not have access.

1. Under _Roles Resources_, set **Resource Access** to `Custom`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) In the tree, select the checkbox of each Admin **Resource** that the role can access.

   To create an Admin role with access to tax settings, choose both the Sales/Tax and System/Tax resources. If setting up a website for a region that differs from your default [shipping point of origin](../stores-purchase/shipping-settings.md#point-of-origin), you must allow access to the System/Shipping resources for the role. The shipping settings determine the store tax rate that is used for catalog prices.

    ![Assigned user role resources](./assets/permissions-role-resources-product.png)<!-- zoom -->

   The list of available permissions may include additional options for bundled and installed extensions. By selecting the top-most permission for each feature, you assign all permissions available for the user.

   >[!NOTE]
   >
   >An Admin user must have **Sales / Archive** permissions for their role scope to see the _Invoices_, _Credit Memos_, and _Shipments_ order [tabs](../stores-purchase/order-processing.md).

1. When complete, click **Save Role**.

   The role now appears in the grid and can be assigned to user accounts.

## Assign a role to user(s)

1. From the **Roles** grid, open the record in edit mode.

1. Under _Current User Identity Verification_, enter your user account password.

1. In the left panel, choose **Role Users**.

    The _Role Users_ option appears only after a new role is saved.

1. To search for a specific user record, do the following:

    - Enter the value in the search filter at the top of a column. Then, press **Enter**.

    - When you are ready to return to the full list, click **Reset Filter**.

1. Select the checkbox of any user(s) to be assigned to the role.

1. Click **Save Role**.

    ![User accounts assigned to the role](./assets/permissions-role-users.png)<!-- zoom -->

## Edit a role

1. On the _Admin_ sidebar, go to **System** > _Permissions_ > **User Roles**.

1. Locate the role using filters above the grid and click the role name.

1. Make needed changes.

   Review the steps for creating a user role for information about the role settings.

1. When prompted, enter **Your Password** to confirm your identity.

1. Click the **Save Role**.

## Delete a role

1. On the _Admin_ sidebar, go to **System** > _Permissions_ > **User Roles**.

1. Locate the role using filters above the grid and open in edit mode.

1. In the upper-right corner, click **Delete Role**.

1. To confirm the action, click **OK**.

## User roles demo

Watch this video to learn about managing user roles:

<iframe title="Adobe Video Publishing Cloud Player" width="640" height="360" src="https://video.tv.adobe.com/v/343654/" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen scrolling="no"></iframe>

## Role resources

Access to the following resources can be assigned to a custom role. See the linked page to learn more about the capabilities that are associated with each role.

| Resource|   |   |
|--- |--- |--- |
|[Dashboard](../getting-started/admin-dashboard.md)|||
|[Sales](../stores-purchase/sales-menu.md)|[Operations](../stores-purchase/orders.md)||
||[Quotes](../b2b/quotes.md) ![B2B for Adobe Commerce](../assets/b2b.svg) (Available with B2B for Adobe Commerce only)<br/>[Orders](../stores-purchase/orders.md)<br/>[Invoices](../stores-purchase/invoices.md)<br/>[Shipments](../stores-purchase/shipments.md)<br/>[Credit Memos](../stores-purchase/credit-memos.md)<br/>[Billing Agreements](../stores-purchase/paypal-billing-agreements.md)<br/>[Returns](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)<br/>[Transactions](../stores-purchase/transactions.md)|
||[Archive](action-log-archive.md)![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)||
||[Shopping Cart Management](../stores-purchase/cart.md)||
|[Catalog](../catalog/catalog-menu.md)|[Category Permissions](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)||
||[Inventory](../inventory-management/introduction.md)|[Products](../catalog/products-list.md)<br/>[Categories](../catalog/categories.md)|
||[Shared Catalog](../b2b/catalog-shared-create.md) ![B2B for Adobe Commerce](../assets/b2b.svg) (Available with B2B for Adobe Commerce only)|[Manage Shared Catalog](../b2b/catalog-shared-manage.md)|
|[Customers](https://docs.magento.com/user-guide/customers/customers-menu.html) | [All Customers](https://docs.magento.com/user-guide/customers/customers-all.html)<br/>[Now Online](https://docs.magento.com/user-guide/customers/now-online.html)<br/>[Customer Groups](https://docs.magento.com/user-guide/customers/customer-groups.html)<br/>[Segments](https://docs.magento.com/user-guide/marketing/customer-segments.html) ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)<br/>||
||[Login as Customer](https://docs.magento.com/user-guide/customers/login-as-customer.html)|Allow Login as Customer Button<br/>View Login as Customer Log ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)|
||[Companies](../b2b/account-companies.md) ![B2B for Adobe Commerce](../assets/b2b.svg) (Available with B2B for Adobe Commerce only)| [ Manage Companies](../b2b/account-company-manage.md) <br/>Add New Company <br/>Delete Company <br/>Reimburse Balance |
|[Carts](../stores-purchase/shopping-assisted-cart-manage.md)|[Manage carts](../stores-purchase/shopping-assisted-cart-manage.md)||
|[My Account](https://docs.magento.com/user-guide/customers/customer-account.html)|||
|[Marketing](../merchandising-promotions/marketing-menu.md)|[Promotions](../merchandising-promotions/marketing-menu.md#uicontrol-promotions)|[Catalog Price Rule](../merchandising-promotions/price-rules-catalog.md) <br/>[Cart Price Rules](../merchandising-promotions/price-rules-cart.md) <br/>[Related Products Rules](../merchandising-promotions/product-related-rules.md)![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)<br/>[Gift Card Accounts](../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)
||[Private Sales](../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)|[Events](../merchandising-promotions/event-create.md) <br/>[Invitations](../merchandising-promotions/invitations.md)|
||[Communications](com)|[Email Templates](email-templates.md) <br/>[Newsletter Template](../merchandising-promotions/newsletter-template.md) <br/>[Newsletter Queue](../merchandising-promotions/newsletter-queue.md) <br/>[Newsletter Subscribers](../merchandising-promotions/newsletter-subscribers.md) <br/>[Email Reminders](../merchandising-promotions/email-reminder-rules.md) |
||Sales Channel|[Amazon Sales Channel](https://experienceleague.adobe.com/docs/commerce-channels/amazon/overview.html)|
||[SEO & Search](../merchandising-promotions/marketing-menu.md#uicontrol-seo--search)|[Search Terms](../catalog/search-terms.md) <br/>[Search Synonyms](../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)<br/>[URL Rewrites](../merchandising-promotions/url-rewrite-custom.md) <br/>[Site Map](../merchandising-promotions/sitemap-xml.md)|
||[User Content](../merchandising-promotions/product-reviews-moderate.md) | [All Reviews](../merchandising-promotions/product-reviews.md) <br/>[Pending Reviews](../merchandising-promotions/product-reviews-moderate.md) <br/> ||
|[Content](../content-design/content-menu.md) | [Elements](../content-design/content-menu.md#uicontrol-elements)) | [Pages](../content-design/pages.md)<br/>[Hierarchy](../content-design/page-hierarchy.md) ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)<br/>[Blocks](../content-design/blocks.md)<br/>[Dynamic Blocks](../content-design/dynamic-blocks.md) ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)<br/>[Widgets](../content-design/widgets.md)<br/>[Media Gallery](../content-design/media-gallery.md)||
||[Design](../content-design/introduction.md#design) | [Themes](../content-design/themes.md)<br/>[Schedule](../content-design/schedule.md)||
||[Content Staging](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)<br />s
|[Reports](../getting-started/reports-menu.md) | [Marketing](../getting-started/marketing-reports.md)|Shopping Cart<br />[Search Terms](../catalog/search-terms.md#search-terms-report)<br />Newsletter Problem Reports||
||[Reviews](../getting-started/review-reports.md)<br />
||[Sales](../getting-started/sales-reports.md)||
||System Insights ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)|[Site-Wide Analysis Tool](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html)|
||[Customers](../getting-started/customer-reports.md)<br/>[Products](../getting-started/product-reports.md)<br/>[Private Sales](../getting-started/private-sales-reports.md) ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)<br />[Statistics](../getting-started/reports-menu.md#uicontrol-statistics)<br />[Business Intelligence](../getting-started/business-intelligence.md)||
|[Stores](../stores-purchase/stores.md) | [Settings](../stores-purchase/stores-menu.md) | [All Stores](../stores-purchase/stores.md)<br/>[Configuration](https://docs.magento.com/user-guide/stores/configuration-overview.html)<br/>[Terms and Conditions](../stores-purchase/terms-and-conditions.md)<br/>[Order Status](../stores-purchase/order-status.md)||
||[Inventory](../inventory-management/sources-stocks.md)|[Sources](../inventory-management/sources-manage.md)<br/>[Stocks](../inventory-management/stocks-manage.md)||
||[Taxes](../stores-purchase/taxes.md)|||
||[Currency](../stores-purchase/currency.md)|[Currency Rates](../stores-purchase/currency-update.md)<br/>[Currency Symbols](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional)||
||[Attributes](https://docs.magento.com/user-guide/stores/attributes.html)|[Product](../catalog/attribute-product-create.md)<br/>[Update Attributes](../catalog/attribute-product-create.md)<br/>[Attribute Set](../catalog/attribute-sets.md)<br/>[Ratings](../merchandising-promotions/product-reviews.md#create-custom-ratings)|
||[Other Settings](../stores-purchase/stores-menu.md)|[Customer Groups](https://docs.magento.com/user-guide/customers/customer-groups.html)|
|[System](system-menu.md) | [Data Transfer](data-transfer.md) | [Import](data-import.md)<br/>[Export](data-export.md)<br/>[Import/Export Tax Rates](data-transfer-tax-rates.md)<br/>[Import History](data-import.md#import-history)||
||[Magento Connect](../getting-started/commerce-marketplace.md) | Connect Manager<br/>Package Extensions||
||[Tools](system-menu.md#tools) | [Cache Management](cache-management.md)<br/>[Backups](backups.md)<br/>[Index Management](index-management.md)<br/>[Change Indexer Mode](index-management.md) ||
||[Permissions](permissions.md) | [All Users](permissions-users-all.md)<br/>[Locked Users](permissions-users-all.md#locked-users)<br/>[User Roles](permissions-user-roles.md)|
|[Action Log](action-log.md)![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)| [Report](action-log.md)<br/>[Archive](action-log-archive.md)|
||[Other Settings](system-menu.md)|[Notifications](notifications.md)<br/>[Custom Variables](variables-custom.md)<br/>[Manage Encryption Key](encryption-key.md)||
|[Global Search](../getting-started/admin-workspace.md#workspace-search)|||

{style="table-layout:auto"}
