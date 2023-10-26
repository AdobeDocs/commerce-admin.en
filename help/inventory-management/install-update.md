---
title: "Install, update, and remove [!DNL Inventory Management]"
description: Learn how to manage the [!DNL Inventory Management] metapackage.
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
---
# Install, update, and remove [!DNL Inventory Management]

[!DNL Inventory Management] modules provide all inventory features and options for single- and multi-source merchants to manage product quantities and stock for sales channels. These features are available in 2.4.x releases of Adobe Commerce and Magento Open Source.

These features and extensions were developed as part of the [Inventory project](https://github.com/magento/inventory) through the Magento Open Source Community Engineering program.

[!DNL Inventory Management] installs in 2.3.x and 2.4.x releases of Adobe Commerce and Magento Open Source, with all features enabled by default. No additional steps are required for enabling these inventory features. Upgrades from v2.1.x or 2.2.x may require additional steps. See [Upgrade Inventory Management](#upgrade-inventory-management).

Installation according to [Quick start on-premises installation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"} is recommended. Install with a metapackage to receive all [!DNL Inventory Management] modules.

The following line in the `composer.json` metapackage installs [!DNL Inventory Management]:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

For a list of [!DNL Inventory Management] metapackage versions, see the [release notes](release-notes.md).

The [!DNL Inventory Management] installation process adds all modules to the `<Magento_installation_directory>/app/etc/config.php` file. A `1` value indicates that the corresponding module is enabled. The following list of modules is added:

```php
        'Magento_Inventory' => 1,
        'Magento_InventoryAdminUi' => 1,
        'Magento_InventoryAdvancedCheckout' => 1,
        'Magento_InventoryApi' => 1,
        'Magento_InventoryBundleProduct' => 1,
        'Magento_InventoryBundleProductAdminUi' => 1,
        'Magento_InventoryCatalog' => 1,
        'Magento_InventorySales' => 1,
        'Magento_InventoryCatalogAdminUi' => 1,
        'Magento_InventoryCatalogApi' => 1,
        'Magento_InventoryCatalogSearch' => 1,
        'Magento_InventoryConfigurableProduct' => 1,
        'Magento_InventoryConfigurableProductAdminUi' => 1,
        'Magento_InventoryConfigurableProductIndexer' => 1,
        'Magento_InventoryConfiguration' => 1,
        'Magento_InventoryConfigurationApi' => 1,
        'Magento_InventoryDistanceBasedSourceSelection' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionAdminUi' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionApi' => 1,
        'Magento_InventoryElasticsearch' => 1,
        'Magento_InventoryExportStockApi' => 1,
        'Magento_InventoryIndexer' => 1,
        'Magento_InventorySalesApi' => 1,
        'Magento_InventoryGroupedProduct' => 1,
        'Magento_InventoryGroupedProductAdminUi' => 1,
        'Magento_InventoryGroupedProductIndexer' => 1,
        'Magento_InventoryImportExport' => 1,
        'Magento_InventoryCache' => 1,
        'Magento_InventoryLowQuantityNotification' => 1,
        'Magento_InventoryLowQuantityNotificationApi' => 1,
        'Magento_InventoryMultiDimensionalIndexerApi' => 1,
        'Magento_InventoryProductAlert' => 1,
        'Magento_InventoryRequisitionList' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryExportStock' => 1,
        'Magento_InventorySalesAdminUi' => 1,
        'Magento_InventorySalesFrontendUi' => 1,
        'Magento_InventorySetupFixtureGenerator' => 1,
        'Magento_InventoryShipping' => 1,
        'Magento_InventorySourceDeductionApi' => 1,
        'Magento_InventorySourceSelection' => 1,
        'Magento_InventorySourceSelectionApi' => 1,
        'Magento_InventoryLowQuantityNotificationAdminUi' => 1,
        'Magento_InventoryShippingAdminUi' => 1,
        'Magento_InventoryGraphQl' => 1,
```

## Enable [!DNL Inventory Management] features

When installed, upgraded, or updated, the _[!UICONTROL Manage Stock]_ option in the Admin is enabled by default. This option enables inventory tracking and management, but does not affect module status. To disable modules, see the next section.

For more information about configurations, see [Configure Inventory Management](configuration.md).

## Disable Inventory Management

>[!IMPORTANT]
>
>Using the default [!DNL Inventory Management] modules is highly recommended. The alternative [!DNL CatalogInventory] module, which is used for systems with disabled [!DNL Inventory Management] modules, is now deprecated. Disabling the [!DNL Inventory Management] modules can cause an unstable system and result in various issues.

You may want to disable [!DNL Inventory Management] modules to:

* Speed up the upgrade process for merchants migrating from 2.0.x, 2.1.x, 2.2.x, or 2.3.x to 2.4.x.
* Use custom or third-party inventory and order management system modules.

See the [Enable or disable modules](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) page in the _Installation Guide_ for information about how to disable the applicable modules.

When complete, the system provides a list of modules and values in `<Magento_installation_directory>/app/etc/config.php`, beginning with:

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>If you have the OMS Connector modules installed, make sure that you do not disable the `Magento_InventoryMessageBus` module, which is a Connector module. It is required to use the Connector with OMS.

## Remove Inventory Management

>[!IMPORTANT]
>
>Using the default [!DNL Inventory Management] modules is highly recommended. The alternative [!DNL CatalogInventory] module, which is used for systems with removed [!DNL Inventory Management] modules, is now deprecated. Removing the [!DNL Inventory Management] modules can cause an unstable system and result in various issues.

If you choose not to use the [!DNL Inventory Management] functionality, you can remove (uninstall) these modules. To remove all the modules through the composer file, add the following to `composer.json`:

```
"replace": {
        "magento/module-inventory": "*",
        "magento/module-inventory-admin-ui": "*",
        "magento/module-inventory-advanced-checkout": "*",
        "magento/module-inventory-api": "*",
        "magento/module-inventory-bundle-product": "*",
        "magento/module-inventory-bundle-product-admin-ui": "*",
        "magento/module-inventory-cache": "*",
        "magento/module-inventory-catalog": "*",
        "magento/module-inventory-catalog-admin-ui": "*",
        "magento/module-inventory-catalog-api": "*",
        "magento/module-inventory-catalog-search": "*",
        "magento/module-inventory-configurable-product": "*",
        "magento/module-inventory-configurable-product-admin-ui": "*",
        "magento/module-inventory-configurable-product-indexer": "*",
        "magento/module-inventory-configuration": "*",
        "magento/module-inventory-configuration-api": "*",
        "magento/module-inventory-distance-based-source-selection": "*",
        "magento/module-inventory-distance-based-source-selection-admin-ui": "*",
        "magento/module-inventory-distance-based-source-selection-api": "*",
        "magento/module-inventory-export-stock": "*",
        "magento/module-inventory-export-stock-api": "*",
        "magento/module-inventory-elasticsearch": "*",
        "magento/module-inventory-graph-ql": "*",
        "magento/module-inventory-grouped-product": "*",
        "magento/module-inventory-grouped-product-admin-ui": "*",
        "magento/module-inventory-grouped-product-indexer": "*",
        "magento/module-inventory-import-export": "*",
        "magento/module-inventory-indexer": "*",
        "magento/module-inventory-low-quantity-notification": "*",
        "magento/module-inventory-low-quantity-notification-admin-ui": "*",
        "magento/module-inventory-low-quantity-notification-api": "*",
        "magento/module-inventory-multi-dimensional-indexer-api": "*",
        "magento/module-inventory-product-alert": "*",
        "magento/module-inventory-requisition-list": "*",
        "magento/module-inventory-reservations": "*",
        "magento/module-inventory-reservations-api": "*",
        "magento/module-inventory-reservation-cli": "*",
        "magento/module-inventory-sales": "*",
        "magento/module-inventory-sales-admin-ui": "*",
        "magento/module-inventory-sales-api": "*",
        "magento/module-inventory-sales-frontend-ui": "*",
        "magento/module-inventory-setup-fixture-generator": "*",
        "magento/module-inventory-shipping": "*",
        "magento/module-inventory-shipping-admin-ui": "*",
        "magento/module-inventory-source-deduction-api": "*",
        "magento/module-inventory-source-selection": "*",
        "magento/module-inventory-source-selection-api": "*"
        "magento/module-inventory-visual-merchandiser": "*",
        "magento/module-inventory-swatches-frontend-ui": "*",
        "magento/module-inventory-quote-graph-ql": "*",
        "magento/module-inventory-in-store-pickup": "*",
        "magento/module-inventory-in-store-pickup-sales": "*",
        "magento/module-inventory-in-store-pickup-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-sales-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-api": "*",
        "magento/module-inventory-in-store-pickup-sales-api": "*",
        "magento/module-inventory-in-store-pickup-frontend": "*",
        "magento/module-inventory-in-store-pickup-shipping": "*",
        "magento/module-inventory-in-store-pickup-graph-ql": "*",
        "magento/module-inventory-in-store-pickup-shipping-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-multishipping": "*",
        "magento/module-inventory-in-store-pickup-shipping-api": "*",
        "magento/module-inventory-in-store-pickup-quote": "*",
        "magento/module-inventory-in-store-pickup-webapi-extension": "*",
        "magento/module-inventory-in-store-pickup-quote-graph-ql": "*",
        "magento/module-inventory-configurable-product-frontend-ui": "*",
        "magento/module-inventory-catalog-search-configurable-product": "*",
        "magento/module-inventory-catalog-search-bundle-product": "*",
        "magento/module-inventory-catalog-frontend-ui": "*",
        "magento/module-inventory-bundle-import-export": "*",
        "magento/module-inventory-bundle-product-indexer": "*"
    }
```

When this change is complete, run composer install, and it automatically removes these Inventory Management modules.

## Upgrade Inventory Management

### Previous [!DNL Commerce] versions

When upgrading or updating an existing 2.1.x, 2.2.x, or 2.3.x installation to Adobe Commerce or Magento Open Source 2.4.x, [!DNL Inventory Management] modules are disabled by default. This default setting is a precaution to prevent backward-incompatible upgrades and to better support Order Management (OMS).

>[!NOTE]
>
>Order Management does not support [!DNL Inventory Management]. When upgrading, [!DNL Inventory Management] modules are disabled to allow OMS and [!DNL Commerce] 2.3.x to work seamlessly.


To enable [!DNL Inventory Management] modules:

1. Edit the `<Commerce_installation_directory>/app/etc/config.php` file.
1. Modify all Inventory modules from `0` to `1` to enable.
1. Update the database:

   ```bash
   bin/magento setup:upgrade
   ```

1. Clean the cache:

   ```bash
   bin/magento cache:clean
   ```

It is recommended that you use the [reservation inconsistencies commands](cli.md) after upgrading. When upgrading, all of your products are added to the Default Stock. If you have pending orders, the commands correctly update your salable quantity and reservations for sales and order fulfillment.

### Previous [!DNL Inventory Management] versions

When upgrading from previous releases of [!DNL Inventory Management] to the latest version, follow normal extension upgrade steps.

For the latest, update your metapackage version:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

See the following guides for more information about Commerce upgrades:

* [Commerce Update Guide](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [Enable or disable modules](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}
