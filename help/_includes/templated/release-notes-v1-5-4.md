# Adobe Commerce B2B fixed issues (v1.5.4-alpha1)

23 issues have been fixed in the Adobe Commerce B2B 1.5.4-alpha1 code. A subset of the fixed issues included in this release is described below.

### Admin UI

#### [B2B] Bundle products quantities not preserved after Update Prices in backend quotes

Fixed an issue where the quantity of a bundle item in an admin negotiable quote reverted to its previous value after editing the quantity in the grid following a configuration change via the Configure dialog.

_ACP2E-5005_

### B2B

#### [B2B] Quote Detail page (storefront and Admin) loses the item/product information when the related product is deleted from the catalog

Fixed the issue where non-salable products disappear from finalized negotiable quotes

_ACP2E-4680_

#### Bundle Product Qty not updated correctly after sending Quote from backend

Fixed the issue where bundle product option quantities were not updated when reconfiguring a negotiable quote from the admin panel. Previously, changes made to bundle option quantities via the Configure button were silently discarded.

_ACP2E-4801_

#### [CLOUD] [B2B] Admin Companies grid causes high MySQL CPU — correlated company_type / COUNT query

Fixed the issue where the Admin Companies grid (Customers → Companies) caused high MySQL CPU usage and long-running database sessions. Previously, determining the Company Type (Parent / Child / Company) for each row required a correlated subquery against the company_relation table that fired once per company row, making both the listing and total-count queries O(N²) at scale; the fix replaces this with a single pre-aggregated JOIN that executes once regardless of dataset size.

_ACP2E-4846_

#### Payment on Account (B2B) – Edit Order button missing for Pending orders while visible for COD

The edit order button is now available for orders placed with Payment on account. Previously it was not possible to edit an order placed with Payment on account while the order is pending

_ACP2E-4877_

#### PHP timeout saving B2B company with multi-company super-user

Saving a B2B company or loading the company's super-user page in the admin no longer exceeds the PHP maximum execution time when the company's super-user is assigned to a very large number of companies.

_ACP2E-4967_

#### [ON-PREM] negotiable quotes not updated as expected

Fixed the issue where negotiable quotes were not updated when a product present in an active negotiable quote was deleted.

_ACP2E-5001_

#### Volatile 'Payment on Account' additional checks

Fixed the issue where Payment on Account, a payment method intended exclusively for B2B company members, could be selected by individual (B2C) customers during checkout. Previously, such customers were incorrectly allowed to proceed with Payment on Account instead of receiving a "payment method not available" error.

_ACP2E-5013_

#### The shared catalog wizard save action erases the pricing structure of a shared catalog

Fixed an issue when the shared catalog wizard's save action erases the pricing structure of a shared catalog save

_ACP2E-5015_

#### GraphQL customer.role returns "Internal server error" for B2C customers without company

Fixed the issue where querying customer { role { ... } } via GraphQL returns an "Internal server error" for B2C customers not assigned to any company. Previously, this query triggered a PHP TypeError because a null company ID was passed to a method with a strict integer type hint.

_ACP2E-5017_

#### [B2B] Bundle product item discount is not applied when option quantities are updated in backend Quotes

Fixed the issue where an item-level discount applied to a Dynamic Price Bundle product in the backend Quote admin was not reflected in the Subtotal or Subtotal (Excl. Tax) columns when the bundle's option quantities had been updated via the Configure dialog. Previously, the discount appeared in the discount column but did not reduce the quoted subtotal.

_ACP2E-5034_

#### Requisition section reloads on every page navigation

Fixed the issue where the requisition section triggered an unnecessary AJAX reload on every product and category page navigation. Previously, the section was reloaded on every page load for any customer with non-empty requisition list data, even when no changes had been made.

_ACP2E-5037_

#### [B2B] Error when company address missing region data

Fixed an issue where the Company Profile page and the Admin Customer Edit page displayed an error when a company address had a region added to its country after the address was saved without a region. Now, the address correctly falls back to the stored region text instead of causing an error.

_ACP2E-5092_

#### Company update on admin with non-english locale resets credit limit

Fixed an issue where editing a B2B company's details could unintentionally reset the configured Credit Limit to 0 when the administrator's locale differed from the default locale. The Credit Limit is now preserved correctly unless it is explicitly modified.

_ACP2E-5127_

#### [CLOUD] Website-restricted admin cannot delete customers when their user_id collides with an inaccessible customer entity_id

Previously, when a website-restricted admin attempted to delete a customer, the system's permission-check plugin compared the admin's own user ID against
  customer entity IDs to enforce company-hierarchy restrictions, without verifying that the acting user was actually a customer; if the admin's user ID happened
  to coincide with the entity ID of an unrelated customer on a website the admin could not access, the plugin tried to load that inaccessible customer record
  and the delete failed with a "more permissions are needed" error, even though the admin had valid rights to the customer being deleted. This has been resolved
  by adding a condition so the customer-ID comparison only runs when the acting user is genuinely a customer, meaning admin-initiated deletes now bypass that check entirely — restricted admins can once again delete customers within their assigned website(s) without being blocked by unrelated, inaccessible customer records

_ACP2E-5146_

#### B2B Order shows incorrect Company Name in Admin Sales Orders

Fixed an issue where an incorrect company name was displayed for B2B purchase orders in Admin Sales Orders when a user was assigned to multiple companies.
The company name is now correctly displayed based on the company associated with the order.

_B2B-4656_

### B2B, Cart & Checkout

#### [ON PREM] [B2B] The Quick Order uploader freezes when attempting to upload a binary file ending in .CSV extension

Fixed the issue where the Quick Order file uploader accepted any file renamed with a .csv extension, including binaries. Previously, no MIME-type or content validation was performed, so non-CSV files (e.g. executables) could be uploaded and processed as if they were valid SKU/QTY lists.

_ACP2E-5212_

### B2B, GraphQL

#### Requisition List GQL Total Count Inaccuracy

Fixed the issue when the requisition_lists GraphQL query returned an incorrect total_count value that reflected only the number of items on the current page instead of the total number of requisition list entities matching the query criteria.

_ACP2E-4799_

### B2B, Order

#### Help on cleaning 59M+ quote tables (sales_clean_quotes is unable to run)

Fixed the issue where the `sales_clean_quotes` cron job timed out on instances with large quote tables. Previously, the cleanup query selected all columns from the `negotiable_quote` table unnecessarily, causing MySQL to perform a full filesort on millions of rows; and each quote was deleted individually via the PHP model layer, compounding the performance cost.

_ACP2E-4891 - [GitHub code contribution](https://github.com/magento/magento2/commit/b63925d9)_

### B2B, Performance

#### [CLOUD] Follow-up of ACSD-70033 : Deadlock on table magento_catalogpermissions_index_product. continuation

Previously, reindexing catalog permissions with Shared Catalog enabled could result in a deadlock error, causing the reindex to fail. Now, the reindex completes successfully even when multiple indexer processes run concurrently.

_ACP2E-4844_

### Content

#### CMS pages created for different websites are displaying wrong pages in frontend

Previously, in multi-website setups where the Website Restriction landing page cache key was not scoped per website, causing the wrong CMS page to be served on the secondary website storefront. The cache key in WebsiteRestriction/Controller/Index/Stub.php now correctly includes the current website ID resolved via the store manager.

_ACP2E-4593_

### Framework

#### [B2B] Purchase orders not auto-converting to sales order with ActiveMQ

Fixed an issue where consumers started by cron did not process messages when ActiveMQ was used with the STOMP protocol. As a result, auto-approved purchase orders were not converted to sales orders. Message processing for STOMP queues is now more reliable and consistent with the DB and AMQP queue implementations.

_ACP2E-4349 - [GitHub code contribution](https://github.com/magento/magento2/commit/08b91f1a) - [GitHub code contribution](https://github.com/magento/inventory/commit/239464da)_

### Install & Administer

#### [Cloud] Correction of Outdated Existing ISO Subdivision Codes

Updated region codes for 13 countries to match the ISO 3166-2 standard. Previously, some region codes did not match the standard, which could cause issues with third-party integrations and international compliance. New regions added for Belgium, Colombia, Spain, France, Italy, and Latvia. Region codes updated for Austria, Colombia, Costa Rica, Germany, Estonia, Spain, Finland, France, India, Iceland, and Latvia.

_ACP2E-4495 - [GitHub code contribution](https://github.com/magento/magento2/commit/9b6a8bd9)_
