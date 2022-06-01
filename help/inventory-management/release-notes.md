---
title: "[!DNL Inventory Management] Release Notes"
description: Review the release notes for information about all [!DNL Inventory Management] releases.
---
# Release Notes

These release notes describe releases of [!DNL Inventory Management] and include:

![New](../assets/new.svg) New features
![Fixed issue](../assets/fix.svg) Fixes and improvements
![Known issue](../assets/bug.svg) Known issues

[!DNL Inventory Management] is a Magento Open Source Community Engineering special project open to contributors. To take part and contribute, see the [GitHub project](https://github.com/magento/inventory) repository and [wiki](https://github.com/magento/inventory/wiki) to get started. To discuss the project, join the [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) channel ([self signup](https://opensource.magento.com/slack)).

[Upcoming releases](https://devdocs.magento.com/release/){target="_blank"} for supported and compatible releases.

## v1.2.4

Inventory Management 1.2.4 (module version: `magento/inventory-metapackage = 1.2.4`) is supported with version 2.4.4 and compatible with version 2.4.0 of Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure.

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

![Fixed issue](../assets/fix.svg) The performance of the validator is optimized to prevent adding new source to a bundled product’s child product with shipment type `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (module version: `magento/inventory-metapackage = 1.2.3`) is supported with version 2.4.3 and compatible with version 2.4.0 of Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure.

![Fixed issue](../assets/fix.svg) Fixed several issues related to the composite product visibility on the frontend.

![Fixed issue](../assets/fix.svg) Improved cart page management performance with the minimum required quantity.

![Fixed issue](../assets/fix.svg) Several fixes targeted to resolve issues with source creation, out of stock items, stock sourcing, sorting allocated sources, in-store delivery, and inventory commands.

![Fixed issue](../assets/fix.svg) [!DNL Commerce] now supports three-digit Canadian postal codes for in-store delivery. Six-digit codes are not supported due to limitations set by `geonames.org`.

![Fixed issue](../assets/fix.svg) The Admin now displays the correct quantity of default stock for disabled products on the **Products** grid and the **Edit Product** page for multi-store deployments.

![Fixed issue](../assets/fix.svg) [!DNL Commerce] now refreshes the category product cache when a bundle product comes back in stock.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (module version: `magento/inventory-metapackage = 1.2.2`) is supported with version 2.4.2 and compatible with version 2.4.0 of Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure.

![Fixed issue](../assets/fix.svg) Fixed several issues related to the composite product visibility on the frontend.

![Fixed issue](../assets/fix.svg) Improved cart page performance during quantity update on B2B.

![Fixed issue](../assets/fix.svg) Several fixes targeted to resolve issues with in-store pickup, mass updates, and inventory threshold.

![New](../assets/new.svg) **Functional tests.** Introduced new functional tests and provided fixes for existing tests to make them more stable.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (module version: `magento/inventory-metapackage = 1.2.1`) is supported with version 2.4.1 and compatible with version 2.4.0 of Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure.

![Fixed issue](../assets/fix.svg) Fixed known issue related to the `inventory_cleanup_reservations` cron job and addressed an issue related to In-Store Pickup functionality for bundle products. This update also includes general improvements to stock calculation, bundle product support, and backorders functionality.

![New](../assets/new.svg) **Functional tests.** Introduced new functional tests to provide additional coverage for In-Store Pickup functionality.

## 1.2.0

[!DNL Inventory Management] 1.2.0 (module version: `magento/inventory-metapackage = 1.2.0`) is supported with version 2.4.0 of Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure.

![Fixed issue](../assets/fix.svg) Numerous fixes to resolve issues with source assignment, scalable environment feature support, and compatibility with PHP 7.4, MySQL 8, and PHPUNIT 9.

![New](../assets/new.svg) **In-store delivery method.** Added an option for users to select a source to be used as a pickup location during checkout. See [In-store Delivery](https://docs.magento.com/user-guide/shipping/shipping-in-store-delivery.html){target="_blank"}.

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

[!DNL Inventory Management] 1.1.6 (module version: `inventory-composer-metapackage = 1.1.6`) is supported with version 2.3.6 and compatible with version 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1, and 2.3.0 of Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure.

![Fixed issue](../assets/fix.svg) Fixes to resolve issues related to backorders, credit memos, low stock report grid, fixes connected to "resolve inconsistencies" CLI tool and general improvements.

![New](../assets/new.svg) **Asynchronous stock reindexing.** Added the ability to asynchronously reindex stock and improved the performance of several critical scenarios.

## 1.1.5

[!DNL Inventory Management] 1.1.5 (module version: `inventory-composer-metapackage = 1.1.5`) is supported with version 2.3.5 and compatible with version 2.3.4, 2.3.3, 2.3.2, 2.3.1, and 2.3.0 of Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure.

![New](../assets/new.svg) **Update inventory once product SKU is changed.** Introduced a new configuration setting to switch to the new behavior: "Synchronize with Catalog".

![New](../assets/new.svg) **Functional tests.** Introduced new functional tests to eliminate the test coverage gap. Fixed several issues to make tests more stable and reliable).

![Known issue](../assets/bug.svg) Fixes to prevent product oversell, "Out of stock" products visibility on the storefront, numerous fixes for scalable environment support and user interface improvements.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (module version: `inventory-composer-metapackage = 1.1.4`) is supported with version 2.3.4 and compatible with version 2.3.3, 2.3.2, 2.3.1, and 2.3.0 of Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure.

![Fixed issue](../assets/fix.svg)**Increased performance.** Introduced bunching logic for Inventory Reservations CLI command to reduce memory usage and avoid cases when the process is stuck without any response.

![New](../assets/new.svg)**Increased test coverage.** Introduced many new Functional tests. Almost all manual Inventory scenarios are covered with automated tests.

![Known issue](../assets/bug.svg) Numerous fixes targeted to resolve issues with credit memos, grouped products, and source and stock mass actions.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (module version: `inventory-composer-metapackage = 1.1.3`) is supported with version 2.3.3 and compatible with version 2.3.2, 2.3.1, and 2.3.0 of Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure.

![Fixed issue](../assets/fix.svg)**Better integration with Adobe Commerce and B2B features.** [!DNL Inventory Management] now works correctly with the following features for websites using non-default inventory sources and stocks:

-  Order by SKU (Adobe Commerce)
-  Quick order (B2B)
-  Requisition lists (B2B)

![New](../assets/new.svg)**Increased performance.** Storefront catalog browsing performance is improved for websites running the default inventory stock and source.

![New](../assets/new.svg)**Increased test coverage.** The automated Functional and Integration test coverage has increased significantly.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (module version: `inventory-composer-metapackage = 1.1.2`) is supported with version 2.3.2 and compatible with version 2.3.1, and 2.3.0 of Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure.

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

![New](../assets/new.svg) **Added a Bulk Partial Stock Transfer Endpoint** - Current bulk transfer endpoints move all assigned quantity from an origin to a destination source. The new `/rest/V1/inventory/bulk-partial-source-transfer` endpoint allows merchants to transfer partial stock from source to source as a bulk operation. To transfer a specific amount of quantity, enter a request to the endpoint with the `sku`, `qty`, `origin_source_code`, and `destination_source_code`. Transfers verify that the source is assigned to the `sku`, enough quantity exists to transfer, and so on. See [Inventory Bulk Actions](https://devdocs.magento.com/guides/v2.4/rest/modules/inventory/bulk-inventory.html){target="_blank"} in the REST API documentation. <!-- https://github.com/magento/inventory/pull/2117 -->

![New](../assets/new.svg) **Added Reservation CLI** - New commands give you options to detect and resolve reservation inconsistencies. As orders submit and change status, [!DNL Inventory Management] generates initial reservations and updates through compensation reservations. These commands return a list of detected inconsistencies by Order ID, SKU, and Stock ID and create reservations to resolve. See the [CLI reference](cli.md) for more information. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![New](../assets/new.svg) **Performance improvements for sources and SSA options** -  Sorting and selecting sources during shipment caused performance degradation for stocks with high numbers of sources. This release provides significant performance improvements to list and sort available sources when reviewing and selecting SSA options in shipments. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![New](../assets/new.svg) **Added GraphQL support for Inventory Management** - This release installs a new `magento/module-inventory-graph-ql` module. The GraphQL [ProductInterface attributes](https://devdocs.magento.com/guides/v2.4/graphql/interfaces/product-interface.html){target="_blank"} now includes the `only_x_left_in_stock` and `stock_status` attributes for [!DNL Inventory Management] support. <!-- https://github.com/magento/inventory/pull/2124 -->

![New](../assets/new.svg) **Simplified UI for Assigned Sources** - The Assigned Sources table in product pages has simplified content for easier updates and increased performance when displaying many sources. All sources list by source name (hover over for `source_code`).

![New](../assets/new.svg) **Export Aggregated Stock Service** - This release provides a new export-aggregated stock service (retaining reservations in the system) to support external Sales Channels, such as Amazon, eBay, and Google Shopping ads.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (module version: `inventory-composer-metapackage = 1.1.0`)  is supported and compatible with version 2.3.0 of Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure. [!DNL Inventory Management] 1.1.1 is released only as a package name update, supported for version 2.3.1 and compatible with version 2.3.0 of Magento Open Source, Adobe Commerce, and Adobe Commerce on cloud infrastructure.

![Fixed issue](../assets/fix.svg) **Added support for Elasticsearch for single and multi-source modes** — You can now configure and use Elasticsearch with custom stocks. This update resolves a [known issue](https://devdocs.magento.com/guides/v2.3/release-notes/ReleaseNotes2.3.0OpenSource.html#known-issues) in version 2.3.0 of Magento Open Source and Adobe Commerce. See [Set up Elasticsearch service](https://devdocs.magento.com/cloud/project/services-elastic.html){target="_blank"} for installation information. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Fixed issue](../assets/fix.svg) Resolved performance issues with Default Stock to drastically increase performance with numerous operations. Improvements increase performance for single-source mode, Transfer Inventory to Source, Storefront Category pages, and Salable Quantity calculations. This update resolves a [known issue](https://devdocs.magento.com/guides/v2.3/release-notes/ReleaseNotes2.3.0OpenSource.html#known-issues){target="_blank"} requiring custom stocks creation for single-source merchants in version 2.3.0 of Magento Open Source and Adobe Commerce.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Fixed issue](../assets/fix.svg) Resolved issues with Out of Stock status and bulk Inventory Transfer to Stock for configurable and grouped products. Selecting the parent products and performing bulk actions does not affect the product status. If the parent product was In Stock, it remains In Stock.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![New](../assets/new.svg) **Distance Priority Algorithm** — The Distance Priority Algorithm is a new, out-of-the-box Source Selection Algorithm for distance-based shipping recommendations. This algorithm compares the location of the shipping destination address with source locations to determine the closest source to fulfill shipments. The distance may be determined by either physical distance or the time spent traveling from one location to another, using imported geocode location data or Google directions (driving, walking, or bicycling).

![New](../assets/new.svg) **Expanded source quantity list** — Merchants with a high number of sources can easily hover and view all sources per product through the Product Grid. Each product displays a minimum of five sources and matching quantities. When hovering over the sources, you can scroll through the entire list of sources and current quantities.

![Known issue](../assets/bug.svg) Known issue with Magento Open Source and Adobe Commerce v2.3.1 - Asynchronous migration of data between sources encounters issues due to changes in Asynchronous APIs with topic names reflecting PHP class and method names. Using synchronous operations, setting **[!UICONTROL Run asynchronously]** to `No`, is recommended.
