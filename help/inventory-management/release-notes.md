---
title: '[!DNL Inventory Management] release notes'
description: Review the release notes for information about all [!DNL Inventory Management] releases.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
---
# [!DNL Inventory Management] release notes

These release notes describe releases of [!DNL Inventory Management] and include:

![New](../assets/new.svg) New features
![Fixed issue](../assets/fix.svg) Fixes and improvements
![Known issue](../assets/bug.svg) Known issues

[!DNL Inventory Management] is a Magento Open Source Community Engineering special project open to contributors. To take part and contribute, see the [GitHub project](https://github.com/magento/inventory) repository and [wiki](https://github.com/magento/inventory/wiki) to get started. To discuss the project, join the [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) channel ([self signup](https://opensource.magento.com/slack)).

[Release schedule](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} for supported and compatible releases.

## v1.2.6

[!DNL Inventory Management] 1.2.6 (module version: `magento/inventory-metapackage = 1.2.6`) is supported with version 2.4.6 and compatible with version 2.4.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![Fixed issue](../assets/fix.svg) The storefront now displays composite products (configurable, bundle, and grouped) as in-stock when child products that had been sold out are returned to stock. Previously, the storefront indicated that the composite product was out of stock under these conditions. <!-- ACP2E-1106-->

![Fixed issue](../assets/fix.svg) Configurable product options are now displayed as expected as out of stock on the storefront if the option was created with quantity set to 0 and **[!UICONTROL Display out-of-stock products]** is enabled. <!-- ACP2E-1148-->

![Fixed issue](../assets/fix.svg) Category page caches are no longer invalidated when stock quantity changes and the product is still in stock. Adobe Commerce now loads pages from the cache instead of regenerating them when product quantity (and nothing else) on the storefront category page changes. <!-- ACP2E-118-->

![Fixed issue](../assets/fix.svg) The category list product count is now correct when using Inventory in single-source mode with the **[!UICONTROL Display Out-Of-Stock Products]** setting enabled. Adobe Commerce now checks whether a product is salable when counting. <!-- ACP2E-1033-->

![Fixed issue](../assets/fix.svg) Cart Price rules for In-Store Delivery now work as expected when Inventory is enabled. Previously, cart price rule-generated discounts were not applied under these conditions. <!-- ACP2E-1015-->

![Fixed issue](../assets/fix.svg) Updating product inventory in scheduled mode no longer clears all caches. Previously, the Inventory indexer cleared all configuration caches. <!-- ACP2E-1003-->

![Fixed issue](../assets/fix.svg) The value for the **[!UICONTROL Allow Multiple Boxes for Shipping]** attribute for a product in Advanced Inventory is now saved as expected. <!-- ACP2E-992-->

![Fixed issue](../assets/fix.svg) Adobe Commerce now issues accurate reservation compensation after a partial refund credit memo for an order that was placed with in-store pickup. Previously, an incorrect reservation saved to the `inventory_reservation` table when an admin user created a credit memo without selecting the **[!UICONTROL Return to Stock]** checkbox. <!-- ACP2E-979-->

![Fixed issue](../assets/fix.svg) Adobe Commerce no longer displays configurable products as out of stock on the storefront when one of its variations has been manually returned to stock in deployments implementing multi-source inventory. <!-- ACP2E-952-->

![Fixed issue](../assets/fix.svg) Column position on the product grid (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) no longer reverts to its previous position after the page reloads in deployments with multiple inventory sources configured. <!-- ACP2E-925-->

![Fixed issue](../assets/fix.svg) Stock quantity is now correct after a credit memo is issued for a virtual product when the **[!UICONTROL Back to stock]** checkbox is not selected. <!-- ACP2E-908-->

![Fixed issue](../assets/fix.svg) You can now save categories with automatic product sorting and scope that is assigned to non-default stock. Previously, Adobe Commerce did not save the category and displayed this error: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Fixed issue](../assets/fix.svg) Configurable product stock status is now updated as expected when the product is created with all out-of-stock configurable variations. <!-- ACP2E-813-->

![Fixed issue](../assets/fix.svg) The reservation inconsistency analyzer tool now works correctly with partially shipped orders that contain configurable, bundle, and grouped products. Composite product types are now analyzed. Previously, cancellations and refunds were saved only for parent products, not for subproduct order items of configurable and ship-together bundle products. <!-- ACP2E-924-->

![Fixed issue](../assets/fix.svg) Adobe Commerce no longer displays an error when an admin user tries to assign 200 or more inventory sources to a stock or product. <!-- ACP2E-1180-->

![Fixed issue](../assets/fix.svg) Adobe Commerce now supports the creation of a credit memo for an order from which a product has been deleted. Previously, merchants could not create a credit memo when products had been deleted from the order after an invoice had been created. The application displayed this error: `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Fixed issue](../assets/fix.svg) Stores are now filtered based on both single and multiple store IDs. The `event` product attribute code has been added to the list of reserved attribute codes. Previously, the Low Stock Report threw an exception when the Inventory module was installed. <!-- ACP2E-1017-->

![Fixed issue](../assets/fix.svg) Layered navigation filters now work as expected, and out-of-stock products are now appended to the storefront category product list. The new `is_out_of_stock` sorting attribute uses the Elasticsearch dynamic field mapper for the storefront product collection. <!-- ACP2E-748-->

![Fixed issue](../assets/fix.svg) Composite product (bundle, grouped, and configurable) stock status is updated as expected when child product stock status is changed by a REST `POST /rest/V1/inventory/source-items` call. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (module version: `magento/inventory-metapackage = 1.2.5`) is supported with version 2.4.5 and compatible with version 2.4.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![Fixed issue](../assets/fix.svg) The default inventory stock status of bundle and grouped products is now updated as expected when a merchant creates a shipment from the Admin. Previously, the status of these products remained unchanged after a shipment was created. <!--- ACP2E-418-->

![Fixed issue](../assets/fix.svg) Configurable products are now returned back to stock when one of these conditions is met: the parent product has at least one saved child in stock, or the configurable product itself was updated and set as **in stock** and had at least one child in stock. <!--- ACP2E-443-->

![Fixed issue](../assets/fix.svg) Inventory changes implemented through the REST API are now reflected as expected on product detail pages. The cache for catalog products is now cleaned after comparing the last and current stock statuses. Previously, omitting the callback function resulted in the incorrect evaluation of stock status changes, which did not trigger the necessary cache cleaning. As a result, the storefront did not reflect the inventory changes. <!--- ACP2E-161-->

![Fixed issue](../assets/fix.svg) Products that are assigned to default stock and that were previously out of stock are now visible on the storefront after updating the source item using `/V1/inventory/source-items`. Previously, this REST API endpoint set the wrong `stock_status`. <!--- ACP2E-562-->

![Fixed issue](../assets/fix.svg) Unassigning inventory sources through bulk action (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) now works as expected when sources include SKUs that are duplicates except for a leading zero (for example, `01234` and `1234`). Previously, the application did not unassign inventory sources and threw an error. <!--- ACP2E-2641-->

![Fixed issue](../assets/fix.svg) Product stock status is now always **in stock** on the storefront when infinite back orders are enabled and the product is assigned to a custom stock, regardless of the quantity backordered. Previously, products went out of stock even when back orders were enabled. <!--- ACP2E-664-->

![Fixed issue](../assets/fix.svg) Configurable product parent and child product stock is now updated correctly after the source item is updated with `POST /V1/inventory/source-items`. After the child product is updated through the API, a new Inventory plugin for default stock checks and updates configurable product quantity and status. <!--- ACP2E-442-->

![Fixed issue](../assets/fix.svg) Out-of-stock grouped products are no longer listed on the storefront Category page. <!--- ACP2E-2082-->

![Fixed issue](../assets/fix.svg) Corrected the package name in `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![Fixed issue](../assets/fix.svg) Back order status is now correctly represented in the Admin after placing an order with zero quantity product in a multi source/stock deployment. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Fixed issue](../assets/fix.svg) Out-of-stock bundle products are no longer displayed on the storefront Category page when the bundle product is updated from the stocks section. <!--- ACP2E-2012-->

![Fixed issue](../assets/fix.svg) Compatibility issues with PHP 7.4 are resolved. <!--- AC-3192-->

![Fixed issue](../assets/fix.svg) The performance of save operations that include bundle products that contain many options (several hundred) is improved. Previously, saving these large bundle products took several minutes and sometimes resulted in timeouts in deployments with Inventory services enabled. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Fixed issue](../assets/fix.svg) The product bulk action tool (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) now works as expected when assigning inventory source to multiple products when SKUs are duplicated with the exception of a leading 0 (for example, 01234 and 1234). Previously, only one product was assigned an Inventory source. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Fixed issue](../assets/fix.svg) The `ProductInterface.only_x_left_in_stock` field now returns 0 if inventory is 0. Previously, it returned null. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Fixed issue](../assets/fix.svg) You can now edit default stock from Admin **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Previously, a JavaScript error was displayed in the console when you tried to add or remove sources from default stock, although you could assign websites to default stock. <!--- ACP2E-545-->

![Fixed issue](../assets/fix.svg) <!--- ACP2E-274--> The category list product count is now correct when using inventory single-source mode with the **[!UICONTROL Display Out-Of-Stock Products]** setting enabled. A new plugin now uses `AreProductsSalableInterface` and `StockConfigurationInterface` to determine the total number of products. Previously, the category product list returned the wrong product quantity.

![Fixed issue](../assets/fix.svg) <!--- ACP2E-322--> Configurable products are now moved to the last position in the product listing after stock is updated when the **[!UICONTROL Move out of stock to the bottom]** setting is enabled. A new custom database query is implemented to negate Elasticsearch index sort order, which disregards Admin-enabled sort order. Previously, configurable products and their child products were not moved to the bottom of the list when this setting was enabled.

## v1.2.4

Inventory Management 1.2.4 (module version: `magento/inventory-metapackage = 1.2.4`) is supported with version 2.4.4 and compatible with version 2.4.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![Fixed issue](../assets/fix.svg) Commerce now displays an accurate salable quantity value for all products in the Admin product list view. Previously, it displayed a blank value for salable quantity of in-stock products with SKUs that contained special characters. <!--- MC-41936-->

![Fixed issue](../assets/fix.svg) Performance has improved for cart-and-checkout actions such as adding products to the cart in deployments with many (approximately 10,000) inventory sources. <!--- MC-42570-->

![Fixed issue](../assets/fix.svg) The `bin/magento inventory:reservation:list-inconsistencies` command now handles orders with partial shipments correctly even if the reservations are missed from the database and the cache has been cleared. Previously, when this command was executed with a pre-cleared cache, Commerce displayed the following error: `Area code is not set`. <!--- MC-42142-->

![Fixed issue](../assets/fix.svg) Incremental indexing of grouped product child products no longer causes other grouped products to be incorrectly indexed when children are shared. <!--- MC-41963-->

![Fixed issue](../assets/fix.svg) The storefront category page now displays the correct product count after removing a product from a category by API. Previously, the category page product count was incorrect until reindexing occurred. <!--- MC-42287-->

![Fixed issue](../assets/fix.svg) Configurable products can now be returned to stock when creating a credit memo when the **[!UICONTROL Manage Stock]** option is disabled. Previously, Commerce did not display the **Return to stock** checkbox on the credit memo creation page when this option was disabled. <!--- MC-42002-->

![Fixed issue](../assets/fix.svg) Management of Inventory stock that exceeds 10,000 items has improved. Previously, performance issues sometimes prevented merchants from editing stock in the Admin before launching their website. <!--- MC-42643-->

![Fixed issue](../assets/fix.svg) The **[!UICONTROL User Roles]** page in the Admin is updated to provide administrators with restricted permissions access to the delivery methods configuration. The _Shipping methods_ section has been renamed to _[!UICONTROL Delivery methods]_, and _[!UICONTROL In-Store Pickup]_ is moved under the _[!UICONTROL Delivery methods]_ section. [GitHub-30053](https://github.com/magento/magento2/issues/30053)  <!--- MC-41545-->

![Fixed issue](../assets/fix.svg) Adobe Commerce no longer creates a duplicate product reservation after a credit memo is updated by API. <!--- MC-41757-->

![Fixed issue](../assets/fix.svg) Switching from the _[!UICONTROL Pick up in Store]_ tab to the _[!UICONTROL Shipping]_ tab in the checkout workflow no longer triggers a JavaScript error when only In-Store Pickup Delivery is available. <!--- MC-42808-->

![Fixed issue](../assets/fix.svg) Saleable product quantity and in-stock product quantity are now synced correctly. Previously, inventory reservation compensation was not recreated for canceled orders. <!--- MC-42485-->

![Fixed issue](../assets/fix.svg) The performance of the validator is optimized to prevent adding new source to a bundled product's child product with shipment type `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (module version: `magento/inventory-metapackage = 1.2.3`) is supported with version 2.4.3 and compatible with version 2.4.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![Fixed issue](../assets/fix.svg) Fixed several issues related to the composite product visibility on the frontend.

![Fixed issue](../assets/fix.svg) Improved cart page management performance with the minimum required quantity.

![Fixed issue](../assets/fix.svg) Several fixes targeted to resolve issues with source creation, out of stock items, stock sourcing, sorting allocated sources, in-store delivery, and inventory commands.

![Fixed issue](../assets/fix.svg) [!DNL Commerce] now supports three-digit Canadian postal codes for in-store delivery. Six-digit codes are not supported due to limitations set by `geonames.org`.

![Fixed issue](../assets/fix.svg) The Admin now displays the correct quantity of default stock for disabled products on the **Products** grid and the **Edit Product** page for multi-store deployments.

![Fixed issue](../assets/fix.svg) [!DNL Commerce] now refreshes the category product cache when a bundle product comes back in stock.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (module version: `magento/inventory-metapackage = 1.2.2`) is supported with version 2.4.2 and compatible with version 2.4.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![Fixed issue](../assets/fix.svg) Fixed several issues related to the composite product visibility on the frontend.

![Fixed issue](../assets/fix.svg) Improved cart page performance during quantity update on B2B.

![Fixed issue](../assets/fix.svg) Several fixes targeted to resolve issues with in-store pickup, mass updates, and inventory threshold.

![New](../assets/new.svg) **Functional tests.** Introduced new functional tests and provided fixes for existing tests to make them more stable.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (module version: `magento/inventory-metapackage = 1.2.1`) is supported with version 2.4.1 and compatible with version 2.4.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![Fixed issue](../assets/fix.svg) Fixed known issue related to the `inventory_cleanup_reservations` cron job and addressed an issue related to In-Store Pickup functionality for bundle products. This update also includes general improvements to stock calculation, bundle product support, and backorders functionality.

![New](../assets/new.svg) **Functional tests.** Introduced new functional tests to provide additional coverage for In-Store Pickup functionality.

## 1.2.0

[!DNL Inventory Management] 1.2.0 (module version: `magento/inventory-metapackage = 1.2.0`) is supported with version 2.4.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![Fixed issue](../assets/fix.svg) Numerous fixes to resolve issues with source assignment, scalable environment feature support, and compatibility with PHP 7.4, MySQL 8, and PHPUNIT 9.

![New](../assets/new.svg) **In-store delivery method.** Added an option for users to select a source to be used as a pickup location during checkout. See [In-store Delivery](../stores-purchase/shipping-in-store-delivery.md) in the _Sales and Purchase Experience Guide_.

![New](../assets/new.svg) **Bundle product support for multi-source mode.** Inventory supports all product types with multiple sources.

![New](../assets/new.svg) **Asynchronous stock reindexing.** Added the ability to asynchronously reindex stock and improved the performance of several critical scenarios.

![New](../assets/new.svg) **Bulk interfaces.** Introduced new bulk interfaces for salability check: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![New](../assets/new.svg) **Increased test coverage.** New functionality is covered with automated tests, including extended coverage for discovered and fixed issues.

![Known issue](../assets/bug.svg) **Known issue.** The absence of the `object_id` field in the reservations metadata is preventing the `inventory_cleanup_reservations` cron job from working properly. This issue was introduced in [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

   **Workaround:** Execute the following MySQL queries to manually clean up reservations:

   ```sql
   SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
   DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
   ```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (module version: `inventory-composer-metapackage = 1.1.6`) is supported with version 2.3.6 and compatible with version 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1, and 2.3.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![Fixed issue](../assets/fix.svg) Fixes to resolve issues related to backorders, credit memos, low stock report grid, fixes connected to "resolve inconsistencies" CLI tool and general improvements.

![New](../assets/new.svg) **Asynchronous stock reindexing.** Added the ability to asynchronously reindex stock and improved the performance of several critical scenarios.

## 1.1.5

[!DNL Inventory Management] 1.1.5 (module version: `inventory-composer-metapackage = 1.1.5`) is supported with version 2.3.5 and compatible with version 2.3.4, 2.3.3, 2.3.2, 2.3.1, and 2.3.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![New](../assets/new.svg) **Update inventory once product SKU is changed.** Introduced a new configuration setting to switch to the new behavior: "Synchronize with Catalog".

![New](../assets/new.svg) **Functional tests.** Introduced new functional tests to eliminate the test coverage gap. Fixed several issues to make tests more stable and reliable).

![Known issue](../assets/bug.svg) Fixes to prevent product oversell, "Out of stock" products visibility on the storefront, numerous fixes for scalable environment support and user interface improvements.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (module version: `inventory-composer-metapackage = 1.1.4`) is supported with version 2.3.4 and compatible with version 2.3.3, 2.3.2, 2.3.1, and 2.3.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![Fixed issue](../assets/fix.svg)**Increased performance.** Introduced bunching logic for Inventory Reservations CLI command to reduce memory usage and avoid cases when the process is stuck without any response.

![New](../assets/new.svg)**Increased test coverage.** Introduced many new Functional tests. Almost all manual Inventory scenarios are covered with automated tests.

![Known issue](../assets/bug.svg) Numerous fixes targeted to resolve issues with credit memos, grouped products, and source and stock mass actions.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (module version: `inventory-composer-metapackage = 1.1.3`) is supported with version 2.3.3 and compatible with version 2.3.2, 2.3.1, and 2.3.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![Fixed issue](../assets/fix.svg)**Better integration with Adobe Commerce and B2B features.** [!DNL Inventory Management] now works correctly with the following features for websites using non-default inventory sources and stocks:

- Order by SKU (Adobe Commerce)
- Quick order (B2B)
- Requisition lists (B2B)

![New](../assets/new.svg)**Increased performance.** Storefront catalog browsing performance is improved for websites running the default inventory stock and source.

![New](../assets/new.svg)**Increased test coverage.** The automated Functional and Integration test coverage has increased significantly.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (module version: `inventory-composer-metapackage = 1.1.2`) is supported with version 2.3.2 and compatible with version 2.3.1, and 2.3.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![Fixed issue](../assets/fix.svg) Added `source_code` to the response for the GET `/V1/shipments` REST endpoint. <!-- https://github.com/magento/inventory/pull/2142 -->

![Fixed issue](../assets/fix.svg) Resolved issue to correctly clear reservations and update product quantities after issuing a credit memo for an unshipped order. When you select the option to <!-- https://github.com/magento/inventory/pull/2179 -->

![Fixed issue](../assets/fix.svg) Resolved issue to correctly save quantity for configurable product children when entering quantities during product creation. <!-- https://github.com/magento/inventory/pull/2158 -->

New modules for [!DNL Inventory Management] 1.1.2 Beta include:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![New](../assets/new.svg) **Added a Bulk Partial Stock Transfer Endpoint** - Current bulk transfer endpoints move all assigned quantity from an origin to a destination source. The new `/rest/V1/inventory/bulk-partial-source-transfer` endpoint allows merchants to transfer partial stock from source to source as a bulk operation. To transfer a specific amount of quantity, enter a request to the endpoint with the `sku`, `qty`, `origin_source_code`, and `destination_source_code`. Transfers verify that the source is assigned to the `sku`, enough quantity exists to transfer, and so on. See [Inventory mass actions](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} in the REST API documentation. <!-- https://github.com/magento/inventory/pull/2117 -->

![New](../assets/new.svg) **Added Reservation CLI** - New commands give you options to detect and resolve reservation inconsistencies. As orders submit and change status, [!DNL Inventory Management] generates initial reservations and updates through compensation reservations. These commands return a list of detected inconsistencies by Order ID, SKU, and Stock ID and create reservations to resolve. See the [CLI reference](cli.md) for more information. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![New](../assets/new.svg) **Performance improvements for sources and SSA options** -  Sorting and selecting sources during shipment caused performance degradation for stocks with high numbers of sources. This release provides significant performance improvements to list and sort available sources when reviewing and selecting SSA options in shipments. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![New](../assets/new.svg) **Added GraphQL support for Inventory Management** - This release installs a new `magento/module-inventory-graph-ql` module. The GraphQL [ProductInterface attributes](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} now includes the `only_x_left_in_stock` and `stock_status` attributes for [!DNL Inventory Management] support. <!-- https://github.com/magento/inventory/pull/2124 -->

![New](../assets/new.svg) **Simplified UI for Assigned Sources** - The Assigned Sources table in product pages has simplified content for easier updates and increased performance when displaying many sources. All sources list by source name (hover over for `source_code`).

![New](../assets/new.svg) **Export Aggregated Stock Service** - This release provides a new export-aggregated stock service (retaining reservations in the system) to support external Sales Channels, such as Amazon, eBay, and Google Shopping ads.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (module version: `inventory-composer-metapackage = 1.1.0`)  is supported and compatible with version 2.3.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base. [!DNL Inventory Management] 1.1.1 is released only as a package name update, supported for version 2.3.1 and compatible with version 2.3.0 of Adobe Commerce, Adobe Commerce on cloud infrastructure, and the Magento Open Source code base.

![Fixed issue](../assets/fix.svg) **Added support for Elasticsearch for single and multi-source modes** — You can now configure and use Elasticsearch with custom stocks. See [Set up Elasticsearch service](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} for installation information. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Fixed issue](../assets/fix.svg) Resolved performance issues with Default Stock to drastically increase performance with numerous operations. Improvements increase performance for single-source mode, Transfer Inventory to Source, Storefront Category pages, and Salable Quantity calculations.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Fixed issue](../assets/fix.svg) Resolved issues with Out of Stock status and bulk Inventory Transfer to Stock for configurable and grouped products. Selecting the parent products and performing bulk actions does not affect the product status. If the parent product was In Stock, it remains In Stock.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![New](../assets/new.svg) **Distance Priority Algorithm** — The Distance Priority Algorithm is a new, out-of-the-box Source Selection Algorithm for distance-based shipping recommendations. This algorithm compares the location of the shipping destination address with source locations to determine the closest source to fulfill shipments. The distance may be determined by either physical distance or the time spent traveling from one location to another, using imported geocode location data or Google directions (driving, walking, or bicycling).

![New](../assets/new.svg) **Expanded source quantity list** — Merchants with a high number of sources can easily hover and view all sources per product through the Product Grid. Each product displays a minimum of five sources and matching quantities. When hovering over the sources, you can scroll through the entire list of sources and current quantities.

![Known issue](../assets/bug.svg) Known issue with Magento Open Source and Adobe Commerce v2.3.1 - Asynchronous migration of data between sources encounters issues due to changes in Asynchronous APIs with topic names reflecting PHP class and method names. Using synchronous operations, setting **[!UICONTROL Run asynchronously]** to `No`, is recommended.
