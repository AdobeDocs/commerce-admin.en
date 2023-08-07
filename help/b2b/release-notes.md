---
title: '[!DNL B2B for Adobe Commerce] release notes'
description: Review the release notes for information about changes in [!DNL B2B for Adobe Commerce] extension releases.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
---
# [!DNL B2B for Adobe Commerce] release notes

These release notes for the B2B extension capture additions and fixes that Adobe has added during a release cycle, including:

![New](../assets/new.svg) New features
![Fixed issue](../assets/fix.svg) Fixes and improvements


>[!NOTE]
>
>See [Product availability](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) for information about versions of the B2B Commerce extension supported for available Adobe Commerce releases.

## B2B v1.4.1

*August 7, 2023*

[!BADGE Compatibility]{type=Informative tooltip="Supported Versions"} Adobe Commerce 2.4.6

The B2B v1.4.1 release includes quality improvements and bug fixes.

![Fixed issue](../assets/fix.svg) <!--ACP2E-1825-->Purchase orders can no longer be placed by a user associated with the company after the company has been blocked. Previously, a user associated with the company could place purchase orders when the company was blocked.

![Fixed issue](../assets/fix.svg) <!--ACP2E-1943-->Product backordered status is now displayed correctly on the storefront. Previously, products that were available for shipment were incorrectly identified as backordered.

![Fixed issue](../assets/fix.svg) <!--ACP2E-1862-->If the company registration form includes a customer file type attribute, the file uploaded during the registration process is now included in the account information for the Company Administrator after the company is created. Previously, the attachment was missing.

![Fixed issue](../assets/fix.svg) <!--ACP2E-1793-->The swatch selector for a configurable product is now displayed as expected in the requisition list item configuration page. Previously, the swatch selector was displayed as a dropdown field in the requisition list item configuration page.

![Fixed issue](../assets/fix.svg) <!--ACP2E-1968-->When using the [Company GraphQL query](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) to return company details, results are now returned successfully without error.

## B2B v1.4.0

*June 13, 2023*

[!BADGE Compatibility]{type=Informative tooltip="Supported"} Supported on Adobe Commerce 2.4.6 and available 2.4.6 [security patch releases](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html).

This release includes new capabilities and enhancements for B2B negotiable quotes and multiple bug fixes.

![New](../assets/new.svg) B2B v1.4.0 is compatible with Adobe Commerce 2.4.7-beta1.

![New](../assets/new.svg) **Seller initiated quotes**—Sellers can now initiate a quote for a buyer directly from the Quote and Customer grids in the Admin. This capability streamlines the quote process and reduces complexity for customers. If a customer has not initiated an order, a seller can quickly create a quote on behalf of the customer and start the negotiation process. Previously, quotes could only be created from the storefront by the buyer, or by a seller logged in as the customer.

![New](../assets/new.svg) **Line item discounts and negotiation**—<!--B2B-2440--> Within a quote, B2B buyers and sellers can now negotiate at the line item level, applying discounts and exchanging notes until an agreement is reached. Note creation and updates are included in the line item and quote history to track communication. Previously, buyers and sellers could only exchange notes and apply discounts at the quote level.

![Fixed issue](../assets/fix.svg) Adobe Commerce now displays correct details during payment when the Purchase Orders option is enabled and a virtual quote that was created with the PayPal payment option has been selected. Previously, totals were displayed as zero under these conditions.

![Fixed issue](../assets/fix.svg) <!--ACP2E-1504--> Validation errors no longer occur when you try to save a company with a credit limit that exceeds 999. Previously, for company credit limits greater than 999, Adobe commerce inserted a comma separator, which caused a validation error that prevented updates from being saved.

![Fixed issue](../assets/fix.svg) <!--ACP2E-1474-->  The selected shipping address now remains unchanged when you place an order with a negotiable quote. Previously, when you placed an order, the selected shipping address was changed to the default shipping address.

![Fixed issue](../assets/fix.svg) <!--ACP2E-1429--> In the Store Configuration settings for B2B Features, the **[!UICONTROL Enable Shared Catalog direct products price assigning]** field is now disabled automatically. On the storefront, it is hidden when the **[!UICONTROL Enable Company]** setting or **[!UICONTROL Enable Shared Catalog]** setting is set to **[!UICONTROL No]**.

![Fixed issue](../assets/fix.svg) <!--ACP2E-1683--> When creating a company account from the storefront, Commerce now validates the email address before processing the company registration. If the email address is invalid, the operation fails and no account updates are processed. Previously, a customer account was created even if the request to create a company account failed because of an invalid email address.

![Fixed issue](../assets/fix.svg) <!--ACP2E-1664--> Product SKUs that include double quotation marks in the Shared Catalog and pricing structure no longer cause errors in the Admin.

![Fixed issue](../assets/fix.svg) <!--ACP2E-1498--> Updated the Varnish configuration for the Commerce application to prevent Guest users from seeing data from other customer groups.

### Known issue

If you install or upgrade B2B 1.4.0 on [Adobe Commerce version 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html), the following error occurs:

```terminal
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

### Workaround

Successfully install or upgrade to B2B version 1.4.0 on Adobe Commerce 2.4.6 and 2.4.6-p1 by adding manual dependencies for the B2B security package with a [stability tag](https://getcomposer.org/doc/04-schema.md#package-links).


1. From the Adobe Commerce installation directory, update `composer.json` with the required dependencies:

   ```terminal
   composer require magento/module-re-captcha-company=1.0.3-beta1@beta magento/  security-package-b2b=1.0.4-beta1@beta
   ```

   **Command Output:**

   ```terminal
   Running composer update magento/module-re-captcha-company magento/security-package-b2b
   Loading composer repositories with package information
   Updating dependencies
   Lock file operations: 2 installs, 0 updates, 0 removals
     - Locking magento/module-re-captcha-company (1.0.3-beta1)
     - Locking magento/security-package-b2b (1.0.4-beta1)
   Writing lock file
   Installing dependencies from lock file (including require-dev)
   Package operations: 2 installs, 0 updates, 0 removals
     - Downloading magento/module-re-captcha-company (1.0.3-beta1)
     - Installing magento/module-re-captcha-company (1.0.3-beta1): Extracting archive
     - Installing magento/security-package-b2b (1.0.4-beta1)
   1 package suggestions were added by new dependencies, use `composer suggest` to see details.
   Package sebastian/phpcpd is abandoned, you should avoid using it. No replacement was suggested.
   Generating autoload files
   132 packages you are using are looking for funding.
   Use the `composer fund` command to find out more!
   No security vulnerability advisories found
   ```

1. Update `composer.json` to add B2B version 1.4.0.

   ```terminal
   composer require magento/extension-b2b=1.4.0
   ```

   **Command output**

   ```terminal
   ./composer.json has been updated
   Running composer update magento/extension-b2b
   Loading composer repositories with package information
   Updating dependencies
   ...
   Generating autoload files
   132 packages you are using are looking for funding.
   Use the `composer fund` command to find out more!
   No security vulnerability advisories found
   ```

1. Complete the installation or upgrade process.

   - [Install B2B on cloud infrastructure](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html)
   - [Install on premises](install.md)

## B2B v1.3.5

*March 14, 2023*

[!BADGE Compatibility]{type=Informative tooltip="Compatibility"} Adobe Commerce 2.4.0 and newer versions

![New](../assets/new.svg) Added support for Adobe Commerce 2.4.6.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerce now displays correct details during payment when the Purchase Orders option is enabled and a virtual quote that was created with the PayPal payment option has been selected. Previously, totals were displayed as zero under these conditions.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-609--> The list of customer groups for the **Allow Browsing Category** setting no longer contains customer groups that are related to shared catalogs.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-1244--> The Tax/VAT Number customer attribute now works as expected with company admin accounts on both the Admin and storefront. Custom Tax/VAT attributes are no longer required to create a company account. Previously, when a merchant created a company account with a custom Tax/VAT attribute, Adobe Commerce threw a validation error on both the storefront and Admin.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-1236--> Disabling the shared catalog feature on a specific scope now works correctly. Previously, Adobe Commerce set an invalid scope when a merchant saved shared catalog configuration.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-1203--> Admin users can now save customer custom attribute values for company users. Previously, customer custom attributes for company users could not be saved.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-1221--> Performance issues are resolved with the validation of company permissions provided through GraphQL when many company permissions are already assigned.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce no longer throws an error on the cart page when Quick Order is used to add a product in a quantity that exceeds available inventory.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-1090--> The performance of `SELECT` company permissions operations has improved.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-2456--> Category queries now return product prices according to store configuration settings when there are no category permissions explicitly set on the category being queried.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-6829--> The **[!UICONTROL Place Order]** button now works as expected when completing a purchase with an approved quote request. Issues with the negotiable quote `negotiableQuoteCheckoutSessionPlugin` plugin have been resolved.

## B2B v1.3.4

*August 9, 2022*

[!BADGE Compatibility]{type=Informative tooltip="Compatibility"} Adobe Commerce 2.4.0 and newer versions

![New](../assets/new.svg) Added support for Adobe Commerce 2.4.5.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce no longer sends email notifications each time an existing Company is updated by an API call. Emails are now sent only when a company is created.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce now correctly calculates a grand total of a negotiable quote when the **[!UICONTROL Enable Cross Border Trade]** tax calculation setting is enabled.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-322-->Configurable products are now moved to the last position in the product listing after stock is updated when the **[!UICONTROL Move out of stock to the bottom]** setting is enabled. A new custom database query is implemented to ensure that the Elasticsearch index sort order now honors the Admin-enabled sort order. Previously, configurable products and their child products were not moved to the bottom of the list when this setting was enabled.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-308-->Purchase Order email now honors the email sending setting of each website in a multi-site deployment. A check for the **[!UICONTROL Disable Email Communications]** setting is added to the custom logic for email queues. Previously, Adobe Commerce did not honor the email sending setting for the secondary website.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-302-->The title of the SKU field of the Quick Order page is changed for clarity.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce now displays a more informative error message when a shopper enters an invalid SKU in the **Enter SKU or Product Name** field.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-1753-->The **[!UICONTROL Account Created in]** field for a company administrator now retains its value as expected after you save the company.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-722 -->The `customer` query no longer returns empty results when it retrieves requisition lists that are filtered by `uid`.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-210 -->Added a plugin before the `collectQuoteTotals` call to ensure that store credits are applied only once.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-665 -->Customers are now redirected to the login page when their account is deleted by an administrator from the Admin. Previously, Adobe Commerce threw an error. The plugin (`SessionPlugin`) code block is now inside the `try…catch` block. Previously, this code was not wrapped inside the generic exception-handling block.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-661 --> On the Quick Order page in mobile mode, pressing **Enter** after entering a valid product name or SKU now takes the shopper to the next field as expected.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-607 -->Company name is now visible as expected in the billing and shipping address sections of the checkout workflow.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-375 -->Store credit is now unavailable when the **[!UICONTROL Zero Subtotal Checkout]** payment method is disabled. Previously, the Store Credit checkbox was not functional during order placement from the Admin. The application did not place the order with the store credit and displayed this error: `The requested Payment Method is not available`.

## B2B v1.3.3

*August 9, 2022*

[!BADGE Compatibility]{type=Informative tooltip="Compatibility"} Adobe Commerce 2.4.0 and newer versions

![New](../assets/new.svg) Added support for Adobe Commerce 2.4.4.

![Fixed issue](../assets/fix.svg) <!--- MC-41985--> The time required to upgrade from Adobe Commerce 2.3.x to Adobe Commerce 2.4.x in deployments with more than 100,000 company roles has been substantially reduced.

![Fixed issue](../assets/fix.svg) <!--- MC-42153--> The POST `V1/order/:orderId/invoice` request now supports the creation of partial invoices when the **[!UICONTROL Payment on Account]** payment method is enabled. Previously, Adobe Commerce threw this error: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Fixed issue](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro now works as expected with B2B negotiable quote when the customer's cart contains other products. Adobe Commerce now successfully processes the order and sends an email to the customer as expected. Previously, Adobe Commerce threw a fatal error and sent a confirmation email to the customer that contained zero values.

![Fixed issue](../assets/fix.svg) <!--- MC-41819--> Pagination is now correctly displayed on catalog search result page after excluding some products in shared catalog.

![Fixed issue](../assets/fix.svg) <!--- MC-42886--> Customer custom attributes are now saved as expected when creating or saving a company user in the Admin.

![Fixed issue](../assets/fix.svg) <!--- MC-42927--> The **[!UICONTROL Submit]** button on the Create New Company form is now disabled after one click to prevent multiple form submissions. Previously, you could submit this form multiple times by clicking this button repeatedly, which generated an error.

![Fixed issue](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce no longer displays the reorder link on the storefront when a shopper logs into a store for which reorders have been disabled.

![Fixed issue](../assets/fix.svg) <!--- MC-43115--> Quick Order search by SKU is now case-insensitive when shared catalog is enabled.

![Fixed issue](../assets/fix.svg) <!--- MC-42203--> You can now update a file for a customer attribute when creating a company. Previously, when you tried to create a company with an attachment of type `File`, Adobe Commerce did not create the company and logged this error in the exception log: `Something went wrong while saving file`.

![Fixed issue](../assets/fix.svg) <!--- MC-42242--> You can now create a company with a customer account that has a custom attribute with a (`File`) or (`Image`) type. Previously, if the account had one of these customizable options, the Company edit page loader did not resolve, which prevented the editing of company details.

![Fixed issue](../assets/fix.svg) <!--- MC-42268--> The `products` query now returns an accurate `total_count` field when shared catalog is enabled.

![Fixed issue](../assets/fix.svg) <!--- MC-42203-->  You can now update a file for a customer attribute when creating a company. Previously, when you tried to create a company with an attachment of type `File`, Adobe Commerce did not create the company and logged this error in the exception log: `Something went wrong while saving file`.

![Fixed issue](../assets/fix.svg) <!--- MC-43178--> The _Company Configuration_ and _Create Company_ pages now work as expected after you disable an online shipping method. Verification has been added to prevent the attempted processing of disabled Shipping modules. Previously, Adobe Commerce displayed this error: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Fixed issue](../assets/fix.svg) <!--- MC-42214--> The _Category_ page now displays consistent product data while permissions are being generated during partial indexing. A new partial indexer for directory permissions has been added to this process. Previously, the data displayed while the indexer ran was incorrect.

![Fixed issue](../assets/fix.svg) <!--- MC-42567--> The `categoryList` query now returns the correct number of products when catalog permissions are used and products are assigned to a shared catalog.

![Fixed issue](../assets/fix.svg) <!--- MC-42528--> The `categoryList` query now respects category permissions and returns only permitted categories. Previously, it returned all assigned and unassigned categories.

![Fixed issue](../assets/fix.svg) <!--- MC-42399--> The `rest/V1/company/{id}` request now returns `is_purchase_order_enabled` attribute values as expected.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-128--> Custom customer attributes are now displayed as expected in the _Company Admin_ tab.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-130--> The My Wish List block on the My Account page is now displayed as expected for Company Admins and Company Users.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-133--> Quick Order errors are no longer displayed in the shopping cart. Previously, Adobe Commerce displayed this error in the shopping cart when the SKU was not found in the catalog:  `The SKU was not found in the catalog`.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-194--> Shared catalog save operations have been optimized to execute faster. Previously, saving a shared catalog with many customer groups could take several minutes.

![Fixed issue](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce now deletes all subcategory permissions from the `sharedcatalog_category_permissions` table when the parent category is deleted. Previously, only the parent category data was removed.

## B2B v1.3.2

*August 29, 2022*

[!BADGE Compatibility]{type=Informative tooltip="Compatibility"} Adobe Commerce 2.4.0 and newer versions

![New](../assets/new.svg) Added support for Adobe Commerce 2.4.3.

![Fixed issue](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce now successfully sends update emails about expired negotiable quotes. Previously, when a negotiable quote expired, Adobe Commerce did not send update emails.

![Fixed issue](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce now successfully sends update emails about soon to expire and expired negotiable quotes when a `cron` job is missing.

### Company

![Fixed issue](../assets/fix.svg) <!--- MC-41542--> The Create New Company Account page country dropdown field no longer lists empty option values. Previously, the first two option values and the country code `AN` were empty.

![Fixed issue](../assets/fix.svg) <!--- MC-41260--> Clicking the **[!UICONTROL Return]** button for an order that was created by a company user now redirects an administrative user to the Create Return page as expected. Previously, the administrator was redirected to the Order History page.

![Fixed issue](../assets/fix.svg) <!--- MC-40798--> Adobe Commerce no longer fails with an out-of-memory error when executing the `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` method during `bin/magento setup:upgrade`. Previously, Adobe Commerce did not use batch size for collection when initializing permissions, but instead loaded a collection of all company roles.

![Fixed issue](../assets/fix.svg) <!--- MC-40551--> Company users can now edit and update customer custom attribute values. Previously, these attributes did not bind properly with the create and edit user form. A company user could enter different attribute values, but Adobe Commerce did not save these values correctly.

![Fixed issue](../assets/fix.svg) <!--- MC-32653--> The resource tree for company role permissions can now be translated as expected. Previously, the permissions tree was not translated even though valid translation files were present.

![Fixed issue](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce now saves custom customer attribute values for B2B users as expected. Previously, creating a company account that contained custom customer attributes triggered a template error, and Adobe Commerce did not successfully load the form. Adding an argument to the layout of `company_create_account` resolved this issue.

![Fixed issue](../assets/fix.svg) <!--- MC-41721--> Company user filters such as Show All Users, Show Active Users, and Show Inactive Users now work as expected. Previously, filtering actions on the company user page caused a JavaScript error.

### Company credit

![Fixed issue](../assets/fix.svg) <!--- MC-41551--> Administrators with restricted accounts that include only website-level privileges can now create a company that uses a different currency than the website.

![Fixed issue](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce now sends company emails from the correct `from` email address and scope. Previously, Adobe Commerce did not consider website scope when sending company credit assignment or update email.

### Quick Order

![Fixed issue](../assets/fix.svg) <!--- MC-42104--> Creating an order using Quick Order from a CSV file now works as expected with nonexistent SKUs.

![Fixed issue](../assets/fix.svg) <!--- MC-40268--> Using Quick Order to search on multiple SKUs now works as expected. Previously, results included duplicate entries.

![Fixed issue](../assets/fix.svg) <!--- MC-40261--> The Added Product list display now treats SKUs entered in lowercase and uppercase the same when you use SKUs to select multiple products during Quick Order.

![Fixed issue](../assets/fix.svg) <!--- MC-40225--> Using Quick Order now adds products in the quantity specified by the shopper. Previously, Adobe Commerce added one product only even when shopper-specified quantities exceed one.

![Fixed issue](../assets/fix.svg) <!--- MC-41283--> The Quick Order autocomplete feature now works with partial SKUs.

![Fixed issue](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce now displays products that have been configured as **Not visible individually** on the Quick Order page's auto-suggest list and search results.

![Fixed issue](../assets/fix.svg) <!--- MC-42402--> Shoppers can now use the Quick Order form to add multiple products by SKUs that include upper-case characters. Previously, only the first product was added.

### Negotiable quote

![Fixed issue](../assets/fix.svg) <!--- MC-41232--> Shoppers are now redirected to the negotiable quote page after pasting the link to a negotiable quote in the URL field and successfully logging in. Previously, shoppers were redirected to the My Account page.

![Fixed issue](../assets/fix.svg) <!--- MC-39317--> Reordering now works as expected for orders that contain a product with a Date Customizable Option for a customer account that was created during checkout. Previously, Adobe Commerce did not process the reorder and displayed this error: `The product has required options. Enter the options and try again`.

![Fixed issue](../assets/fix.svg) <!--- MC-39063--> The shipping address for a negotiable quote is no longer editable during checkout when the Purchase Order module is disabled. This behavior resulted from a previous fix in which `isQuoteAddressLocked` was removed from the negotiable quote checkout renderer.

![Fixed issue](../assets/fix.svg) <!--- MC-38967--> Merchants can now add products to a negotiable quote from the Admin.

### Purchase orders

![Fixed issue](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce now displays an informative error message as expected when you place a purchase order using PayPal Express Checkout when the **[!UICONTROL Name Prefix]** attribute is set to `required`. Previously, Adobe Commerce did not place the order or display an error message.

![Fixed issue](../assets/fix.svg) <!--- MC-39620--> The UI component for the billing address in the Purchase Order module now uses quote address correctly when Google Tag Manager is enabled. Previously, a JavaScript error occurred on the payment page.

### Requisition lists

![Fixed issue](../assets/fix.svg) <!--- MC-40426--> Merchants can now use the POST `rest/all/V1/requisition_lists` endpoint to create a requisition list for a customer. Previously, Adobe Commerce threw this 400 error when you tried to create a requisition list: `Could not save Requisition List`.

![Fixed issue](../assets/fix.svg) <!--- MC-41123--> The **[!UICONTROL Add to Requisition List]** button now appears for a shopping cart's in-stock products when the cart also contains out-of-stock products. Previously, if a cart contained two products, one of which was out-of-stock, the _[!UICONTROL Add to Requisition List]_ button did not appear for either products.

![Fixed issue](../assets/fix.svg) <!--- MC-40877--> You can now use the REST API to add a product to a requisition list.

![Fixed issue](../assets/fix.svg) <!--- MC-40155--> Requisition list **[!UICONTROL Latest Activity Date]** values now adhere to locale format.

![Fixed issue](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce no longer throws a fatal error when you edit a bundle product from a requisition list.

![Fixed issue](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce now displays the correct product price when you add a product with a customizable option `(File)` to a wish list from a requisition list. The link to the uploaded file is also visible as expected. Previously, Adobe Commerce displayed incorrect product prices and did not display the link to the file.

![Fixed issue](../assets/fix.svg) <!--- MC-36383--> Products with a customizable option `(File)` can now be added to a shopping cart from a requisition list. 

### Shared catalog

![Fixed issue](../assets/fix.svg) <!--- MC-40497--> An administrator with a role limited to a specific website can now create, view, and edit a shared catalog. Previously, Adobe Commerce threw a fatal error when an administrator with a limited role tried to create a shared catalog.

![Fixed issue](../assets/fix.svg) <!--- MC-41337--> Layered navigation results now include an accurate count of products with filtered attributes, and shoppers can now apply multiple filters. Previously, only one filter could be applied, and Adobe Commerce displayed an inaccurate product count in layered navigation.

![Fixed issue](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce now correctly displays product counts in layered navigation filters in search results. Previously, a plugin for the Search Results page did not use ElasticSearch but issued a new query to the database.

![Fixed issue](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce no longer deletes tier prices when a merchant deletes all products from a default shared catalog.

![Fixed issue](../assets/fix.svg) <!--- MC-39802--> Filters are now filtered by the current category and displayed correctly on all pages when shared catalogs are enabled. Previously, filters were wrongly calculated for the current page only and were not filtered by the current category.

![Fixed issue](../assets/fix.svg) <!--- MC-39522--> The GraphQL `products` query no longer returns  a product's price range and category for products that are not assigned to a shared catalog when shared catalog is enabled. Previously, the query returned the product's aggregations, even though the product itself was not returned in the `items` array.

## B2B v1.3.1

*February 9, 2021*

[!BADGE Compatibility]{type=Informative tooltip="Compatibility"} Adobe Commerce 2.4.0 and newer versions

![New](../assets/new.svg) Added support for Adobe Commerce 2.4.2.

![New](../assets/new.svg) Online payment methods are now supported for purchase orders.

![Fixed issue](../assets/fix.svg) Adding a configurable product to the shopping cart directly from a requisition list when this product was used in a prior order no longer returns a system error.

![Fixed issue](../assets/fix.svg) Adobe Commerce now displays the Requires My Approval tab correctly for purchase orders when a split database configuration is deployed.

![Fixed issue](../assets/fix.svg) Adobe Commerce now displays details about bundle products and gift card when you view purchase orders.

![Fixed issue](../assets/fix.svg) Shoppers are now redirected as expected after logging into their account while browsing in a store where **[!UICONTROL Website Restriction]** is enabled and **[!UICONTROL Restriction Mode]** is set to `Private Sales: Login Only`. Previously, shoppers were redirected to the store home page. <!--- MC-38934-->

![Fixed issue](../assets/fix.svg) Order history now loads as expected in a company administrator's account dashboard page in deployments with a B2B company hierarchy that contains many customers (greater than 13000). Previously, order history loaded slowly or not at all, and Adobe Commerce displayed a 503 error. <!--- MC-38830-->

![Fixed issue](../assets/fix.svg) Adobe Commerce no longer displays multiple identical warning messages when you add an unconfigured product with customizable options to a Requisition List from a Category page. <!--- MC-38342-->

![Fixed issue](../assets/fix.svg) New and duplicated products are now visible as expected on the category page when B2B shared catalogs are enabled. <!--- MC-38307-->

![Fixed issue](../assets/fix.svg) Adobe Commerce now maintains the correct `store_id` that is associated with a company administrator when the customer group for a company is updated. Previously, the `store_id` changed to the default store when the group was updated. <!--- MC-38196-->

![Fixed issue](../assets/fix.svg) Adobe Commerce now saves a grouped product to a requisition list as a list of simple products in the same way as it adds a grouped product to a shopping cart. Previously, due to how Adobe Commerce saved grouped products, the link for a grouped product from the requisition list always redirected to simple products and not to the grouped product. <!--- MC-38049-->

![Fixed issue](../assets/fix.svg) You can now filter orders by the **[!UICONTROL Company Name]** field when exporting order information in CSV format. Previously, Adobe Commerce logged an error in `var/export/{file-id}`. <!--- MC-37785-->

![Fixed issue](../assets/fix.svg) Adobe Commerce now displays the Create Requisition List popup as expected when you select the Create New Requisition List tab on the storefront. <!--- MC-37915-->

![Fixed issue](../assets/fix.svg) Requisition lists now include all grouped products and quantities that have been added to the list. Previously, when a merchant navigated to a requisition list after adding products to it from a product detail page, Adobe Commerce displayed this error: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Fixed issue](../assets/fix.svg) The correct store view is now associated with the relevant website when you create a company in a multi-site deployment. Previously, you could not create a company, and Adobe Commerce displayed this error: `The store view is not in the associated website`. <!--- MC-37488-->

![Fixed issue](../assets/fix.svg) Ordering products by SKU using Quick Order no longer results in duplicate product quantities in the CSV file. <!--- MC-37427-->

![Fixed issue](../assets/fix.svg) The **[!UICONTROL Add to Cart]** button is no longer blocked when the _[!UICONTROL Enter Multiple SKUs]_ section of the Quick Order page contains an empty value. Instead, Adobe Commerce now displays a message prompting you to enter valid SKUs. <!--- MC-37387-->

![Fixed issue](../assets/fix.svg) Adobe Commerce now displays this message on the product page when you submit a product review from a requisition list: `You submitted your review for moderation`. The review also appears on the Pending Reviews page (Admin **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). Previously, although Adobe Commerce added the review to the list of pending reviews, it threw a 404 error on the product page. <!--- MC-37119-->

![Fixed issue](../assets/fix.svg) The performance of the `sharedCatalogUpdateCategoryPermissions` consumer has been improved. After creating a shared catalog, the catalog permission indexer now uses only the customer group ID from the shared catalog, not all customer groups. <!--- MC-36770-->

![Fixed issue](../assets/fix.svg) Custom customer address attribute fields that are associated with a shopper's non-default address are now saved as expected in the storefront checkout workflow. <!--- MC-36630-->

![Fixed issue](../assets/fix.svg) Orders for products that belong to a store's default shared catalog can now be placed for shoppers through the Admin REST API (`rest/V1/carts/{<CART_ID>/items`) as expected. Adobe Commerce now checks if the product was assigned to a public catalog before shared catalog permissions validation in `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. Previously, Adobe Commerce did not add the product to the shopper's cart and threw this error: `No such shared catalog entity`. <!--- MC-36535-->

![Fixed issue](../assets/fix.svg) Adobe Commerce now sends new company user registration emails from the Adobe Commerce store's address. Previously, this email was sent from the company administrator's address. <!--- MC-36480-->

![Fixed issue](../assets/fix.svg) Adobe Commerce now checks custom attributes for duplication of reserved company attribute names before permitting a merchant to save a new attribute. <!--- MC-36282-->

![Fixed issue](../assets/fix.svg) The `credit_history` query now returns the specified company's credit history for both the originally allocated amount and the purchased amount. Previously, this query returned an error.

![Fixed issue](../assets/fix.svg) The **[!UICONTROL Company]** and  **[!UICONTROL Job Title]** fields on the Edit Account Information page are no longer editable.

### Known issues

- B2B buyers can use online payment methods to bypass the usual purchase order flow. This scenario can occur if the buyer can reduce their entire checkout total to a 0 — for example, by a promo code or gift card —  and then remove the code or gift card. Even under those conditions, Adobe Commerce still places the order for the correct amount based on the prices of the items in their assigned catalog. **_Workaround_**: Disable gift cards and coupon codes when online payment methods are enabled for purchase order approval. <!--- B2B-1603-->

- Buyers are redirected to the shopping cart when trying to place an order from a purchase order using PayPal Express Checkout when **[!UICONTROL In-Context Mode]** is disabled. <!--- B2B-1604-->

- Adobe Commerce sometimes displays a 404 error when a buyer creates a purchase order and then navigates to the checkout page. This error occurs when a buyer has previously created a different purchase order with an online payment method before navigating to the checkout page without completing the previous purchase. The buyer can still place the purchase order. **_Work around_**: None. <!--- B2B-1605-->

- Discounts for a specific payment method persist during checkout for a purchase order even when the buyer changes their payment method during final checkout. As a result, customers can receive a discount that they are not entitled to. This issue occurs because a cart rule for the original payment method is still applied despite the change in payment method. **_Work around_**: None. See the [Adobe Commerce 2.4.2 B2B known issue: discount remains for online Purchase Orders after payment method is changed](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _Knowledge Base_ article. <!-- B2B-1012 -->

- The `deleteRequisitionListOutput` query returns details about the deleted requisition list instead of the remaining requisition lists. <!--- MC-39894-->

## B2B v1.3.0

*October 15, 2020*

[!BADGE Compatibility]{type=Informative tooltip="Compatibility"} Adobe Commerce 2.4.0 and newer versions

This release includes improvements to order approvals, shipping methods, shopping cart, and logging of Admin actions.

![New](../assets/new.svg) Added support for Adobe Commerce 2.4.1.

![New](../assets/new.svg) B2B order approvals have been enhanced to improve usability and to allow for bulk actions on purchase orders.

![New](../assets/new.svg) B2B merchants can now control shipping methods that are offered to each Company.<!--- BUNDLE-160 161 162 -->

![New](../assets/new.svg) Merchants can now allow users to clear the contents of their shopping cart in a single action and can configure this ability independently on each website <!--- BUNDLE-108 -->

![New](../assets/new.svg) B2B buyers can now add individual items or the entire contents of their shopping cart directly to a requisition list. <!--- BUNDLE-145 144-->

![New](../assets/new.svg) B2B merchants can create orders from the Admin on behalf of customers using Payment on Account as the payment method. <!--- BUNDLE-166 178-->

![New](../assets/new.svg) Merchants can now directly view all quotes associated with a user from the customer's detail page. <!--- BUNDLE-139 -->

![New](../assets/new.svg) Merchants can now filter the Customers Now Online grid by Company. <!--- BUNDLE-137 -->

![New](../assets/new.svg) Admins can now filter customers in the Admin by Sales Rep. <!--- BUNDLE-110 -->

![New](../assets/new.svg) To reduce creation of fraudulent or spam accounts, merchants can now enable Google reCAPTCHA on the New Company Request form on the storefront. <!--- BUNDLE-154 -->

![New](../assets/new.svg) Admin actions taken in the Company modules are now logged in the Admin Actions Log. Actions are logged from all relevant company modules: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`.  <!--- BUNDLE-180 181 182 183 -->

![Fixed issue](../assets/fix.svg) Adobe Commerce no longer displays the **[!UICONTROL Delete customer]** button on the **Customers** page when the logged-in administrator does not have rights to delete customers in deployments where B2B is installed. <!--- MC-35655-->

![Fixed issue](../assets/fix.svg) Customer group is no longer changed automatically for a customer who is assigned to a Company when you edit the customer on the Customer grid. <!--- MC-35254-->

![Fixed issue](../assets/fix.svg) When a merchant creates a shared catalog, permissions are now automatically set to `Allow` for the **[!UICONTROL Display Product Prices]** and **[!UICONTROL Add to Cart]** features in categories when the customer group is assigned this access in catalog permission settings. Previously, these settings were automatically set to `Deny` even when catalog permissions were set to `Allow`.<!--- MC-34792-->

![Fixed issue](../assets/fix.svg) Shared catalog category permissions are no longer overwritten when a product is edited from the product edit page.<!--- MC-34777-->

![Fixed issue](../assets/fix.svg) Adobe Commerce now sends an email notification confirming that a customer has permission to exceed the designated credit limit when a merchant enables the **[!UICONTROL Allow To Exceed Credit Limit]** setting. Previously, the notification email sent by Adobe Commerce indicated that the customer did not have permission to exceed the limit. <!--- MC-34584-->

![Fixed issue](../assets/fix.svg) The HTML container that surrounds product price on requisition lists is now rendered correctly for the children of bundled products. <!--- MC-36331-->

![Fixed issue](../assets/fix.svg) Merchants can now designate the language in which company user email is sent when creating a company in multi-language deployments. Previously, the drop-down menu the enables merchants to select the appropriate store view and language was not displayed.  <!--- MC-35777-->

![Fixed issue](../assets/fix.svg) Custom customer address attributes fields are now displayed as expected in the storefront checkout workflow. <!--- MC-35607-->

![Fixed issue](../assets/fix.svg) The B2B Features configuration tab now opens correctly. <!--- MC-35458-->Guests can now use QuickOrder to add products to their cart and then successfully remove items. Previously, when a shopper used QuickOrder to add multiple products to their cart, and then removed a product, the product was not removed. <!--- MC-35327-->

![Fixed issue](../assets/fix.svg) A company can now be updated using the REST API PUT `/V1/company/:companyId` request without specifying the `region_id` when state is configured as **not required**. Previously, even though `region_id` was not required, Adobe Commerce threw an error if it was not specified. <!--- MC-35304-->

![Fixed issue](../assets/fix.svg) When you create or update a B2B Company using the REST API (`http://magento.local/rest/V1/company/2`, where `2` represents the company ID), the response now includes the settings for `applicable_payment_method` or `available_payment_methods` as expected. <!--- MC-35248-->

![Fixed issue](../assets/fix.svg) Adobe Commerce no longer displays a 404 page when a merchant uses the **Enter** button instead of clicking the **[!UICONTROL Save]** button when creating a requisition list on the storefront.<!--- MC-35094-->

![Fixed issue](../assets/fix.svg) Category permissions no longer change when a new product is assigned to a public shared catalog. Previously, category permissions were duplicated. <!--- MC-34386-->

![Fixed issue](../assets/fix.svg) The REST API endpoint PUT `rest/default/V1/company/{id}`, which is used to update Company email, is no longer case-sensitive. <!--- MC-34308-->

![Fixed issue](../assets/fix.svg) Disabling reward modules no longer affects B2B features on customer accounts. Previously, when reward modules were disabled, the following B2B-related tabs were not displayed: Company Profile, Company Users, and Roles and Permissions.<!--- MC-34191-->

![Fixed issue](../assets/fix.svg) Adobe Commerce now uses the correct sender name on email notifications when changes are made to company accounts. Previously, Adobe Commerce used the general contact sender name defined in the default scope for all emails. <!--- MC-33917-->

![Fixed issue](../assets/fix.svg) You can now successfully implement multishipping for orders that contain both physical and virtual products. <!--- MC-33818-->

![Fixed issue](../assets/fix.svg) Merchants can now create company users from the _[!UICONTROL Company Users]_ section in My Account and Company Structure pages when **[!UICONTROL Access Restriction]** is enabled and **[!UICONTROL Restriction Mode]** is set to `Sales: Login Only`. Previously, Adobe Commerce threw this error when a merchant tried to create a user: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Fixed issue](../assets/fix.svg) Adobe Commerce no longer resets a customer's customer group to the default when a customer saves their account information. <!--- MC-33554-->

![Fixed issue](../assets/fix.svg) Adobe Commerce no longer throws a fatal error when an administrator assigns a customer who has an active shopping cart to a customer group. <!--- MC-33313-->

![Fixed issue](../assets/fix.svg) Adobe Commerce now provides an `addToCart` DataLayer event for Quick Order and Requisition lists pages.  <!--- MC-33295-->

![Fixed issue](../assets/fix.svg) Notification emails that are sent to sales representatives assigned to a company now include the assigned corporate logo. Previously, the notification email included the default LUMA logo, not the uploaded corporate logo. <!--- MC-33232-->

![Fixed issue](../assets/fix.svg) A requisition list now includes all grouped products and quantities that have been added to the list. Previously, when a merchant navigated to a requisition list after adding products to it from a product detail page, Adobe Commerce displayed this error: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Fixed issue](../assets/fix.svg) The `products` query now returns an accurate `total_count` field when shared catalog is enabled. <!--- MC-42268-->

![Fixed issue](../assets/fix.svg) The Company Configuration and Create Company pages now work as expected after you disable an online shipping method. Verification has been added to prevent the attempted processing of disabled Shipping modules. Previously, Adobe Commerce displayed this error: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Fixed issue](../assets/fix.svg) Integration test memory consumption has been reduced, which improves test performance and reduces the time required for test completion. <!--- AC-266-->

## B2B v1.2.0

*July 28, 2020*

[!BADGE Compatibility]{type=Informative tooltip="Compatibility"} Adobe Commerce 2.4.0 and newer versions

![New](../assets/new.svg) Added support for Adobe Commerce 2.4.0.

![New](../assets/new.svg) Storefront Order Search, with added thanks for contribution by Marek Mularczyk from [Divante](https://www.divante.com/) and community members.

![New](../assets/new.svg) Purchase Orders are enhanced and rewritten. They are now included by default in Adobe Commerce.

![New](../assets/new.svg) Purchase Order Approval Rules have been implemented. These rules allow users to control the Purchase Order workflow by creating purchasing rules for orders.

![New](../assets/new.svg) Login as Customer is now included by default in Adobe Commerce. This feature allows site employees to assist customers by logging in as the customer to see what they see.

![Fixed issue](../assets/fix.svg) Attribute aggregations are now working correctly for Layered Navigation with Elasticsearch

![Fixed issue](../assets/fix.svg) Searching orders by special characters is now working properly.

![Fixed issue](../assets/fix.svg) Clicking the **[!UICONTROL Clear All]** Button now expands all the filters, rather than collapsing them.

![Fixed issue](../assets/fix.svg) Product SKU/Name is now included in the Order History search filter summary.

![Fixed issue](../assets/fix.svg) Sorting Indicator is now displayed properly in the My Purchase Orders Grid.

![Fixed issue](../assets/fix.svg) Now, you can click the Approve, Cancel, Reject, and Purchase Order buttons only once. Previously, you could click the button multiple times.

![Fixed issue](../assets/fix.svg) The Purchase Order Approve, Reject, Cancel, and Validate buttons now render correctly on mobile devices.

![Fixed issue](../assets/fix.svg) Previously, approving a Purchase Order with a discount that has expired placed the order at the full amount and did not update the Purchase Order total. Now, the Purchase Order total is updated to show the correct total.

![Fixed issue](../assets/fix.svg) An issue was introduced in 2.3.4 where custom extension attributes would not be copied from the Customer Address to the Quote Address. This issue has been fixed.

![Fixed issue](../assets/fix.svg) With B2B installed, a SQL error would appear when assigning categories to shared catalogs. This issue has been fixed.

![Fixed issue](../assets/fix.svg) Due to an incorrect variable type value, admins could not add configurable products to an order. The option dropdowns would not populate. This feature now works properly.

![Fixed issue](../assets/fix.svg) Previously, when editing Category Permissions for the Not Logged In group, an error would occur when saving the changes. This issue has been fixed.

![Fixed issue](../assets/fix.svg) A fix is added to allow store administrators to add products to an order that are not in the shared catalog. Previously, an error message would appear when adding an item not in the catalog.

![Fixed issue](../assets/fix.svg) Previously, after running the command `php bin/magento indexer:set-dimensions-mode catalog_product_price website` and then trying to create a shared catalog, an error would occur. This issue has been fixed.

![Fixed issue](../assets/fix.svg) When adding a company and assigning the company administrator to a non-default website, the wrong site ID was sent, causing an error. This issue has been fixed.

![Fixed issue](../assets/fix.svg) Previously, after a customer was moved to another customer group, adding a product to an order using _Quick Order_ would fail with an error. This issue has been fixed.

![Fixed issue](../assets/fix.svg) Previously, when attempting to check out using the WebAPI with a B2B quote, an incorrect value was sent to the API, causing an error to occur. This issue has been fixed.

![Fixed issue](../assets/fix.svg) Previously, when setting a company to "Active" via the API, an error would occur. This issue has now been fixed.

![Fixed issue](../assets/fix.svg) Due to an unneeded `form` tag, the order page automatically refreshed when you pressed Enter after changing a proposed shipping charge. This issue has been fixed.

![Fixed issue](../assets/fix.svg) Previously, when setting a product display limit on a catalog page and that limit was less than the number of total products, an error occurred. That feature now works as expected.

![Fixed issue](../assets/fix.svg) Previously, when changing the admin of a company, the original admin address would be copied to the new admin, giving them two addresses. Now, only the correct address is added.

![Fixed issue](../assets/fix.svg) Previously, using the API to save a quote item when backorder is set to "Allowed and Notify Customer" would fail. This API call now works as expected.

![Fixed issue](../assets/fix.svg) The Fixed Product Tax is now displayed on the Quotes detail page.

![Fixed issue](../assets/fix.svg) Previously, clicking an attachment in the Comments tab of the My Quotes page would fail to download the file. This behavior now works as expected.

### Known issues

- Adobe Commerce throws an exception during upgrade to B2B 1.2.0 in a multi-website deployment. When `setup:upgrade` runs, this error occurs on the `PurchaseOrder` module: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Workaround**: Install the `B2B-716 Add NonTransactionableInterface` interface to the `InitPurchaseOrderSalesSequence` data patch hotfix, which is now available from the **My Account** > **Downloads** section of `magento.com`.
- If a discount code expires before a Purchase Order (PO) is approved, the PO continues to display the discounted amount, but once the PO is approved, the order is placed at the non-discounted total. **Workaround**: Install the `B2B-709 Purchase Order Discount patch` hotfix for this issue, which is now available from the **My Account** > **Downloads** section of `magento.com`.
- If items in a purchase order are out of stock, or of insufficient quantity when the purchase order is converted into an actual order, an error occurs. If backorders are enabled, the order is processed normally.
