---
title: Install the [!DNL B2B for Adobe Commerce] Extension
description: Learn how to install the [!DNL B2B for Adobe Commerce] metapackage.
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
---
# Install the [!DNL B2B for Adobe Commerce] Extension

>[!IMPORTANT]
>
>The B2B for Adobe Commerce extension is only available for Adobe Commerce v2.2.0 or later. You must install it after installing Adobe Commerce.

>[!NOTE]
>
>For Adobe Commerce on cloud infrastructure projects, see [Set up B2B](https://devdocs.magento.com/cloud/configure/setup-b2b.html) in the _Cloud Guide_.

1. Change to your Adobe Commerce installation directory and enter the following command to update your `composer.json` file and install the [!DNL B2B for Adobe Commerce] extension:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   >[!NOTE]
   >
   >You must specify a [Compatible B2B extension version](https://devdocs.magento.com/release/availability.html#compatibility) in the command, which can be found in the left column of the compatibility table.

   If you get an error when trying to install the B2B extension for a local instance of Adobe Commerce for example:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Check the package spelling, your version constraint, and that the package is available and matches your minimum-stability (stable).

   If not already defined globally in your [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home), you must create an `auth.json` file in the root directory and add the following code, using the actual values of your `public_key` and `private_key` for `username` and `password`:

   ```json
   {
      "http-basic": {
         "repo.magento.com": {
            "username": "<public_key>",
            "password": "<private_key>"
         }
      }
   }
   ```

1. When prompted, enter your [authentication keys](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html).

   Your *public key* is your username; your *private key* is your password. If you have stored your public and private keys in `auth.json`, you aren't asked to enter them here.

1. Run the following commands after Composer finishes updating modules:

   ```bash
   bin/magento setup:upgrade
   ```

   ```bash
   bin/magento setup:di:compile
   ```

   ```bash
   bin/magento setup:static-content:deploy -f
   ```

   ```bash
   bin/magento cache:clean
   ```

>[!NOTE]
>
>In Production mode, you may receive a message to `Please rerun Magento compile command`. Enter the commands. Adobe Commerce does not prompt you to run the compile command in Developer mode.

>[!IMPORTANT]
>
>After completing the installation, you must follow the [post-installation steps](#configure-b2b).

## Message consumers

The [!DNL B2B for Adobe Commerce] extension uses MySQL for message queue management. Start the corresponding message consumers for the needed B2B features after installation.

| Consumer | Description |
|----------|-------------|
| `sharedCatalogUpdatePrice` | Updates price for each product in a shared catalog. Required when the [**Shared Catalogs**](catalog-shared.md) option is enabled in the Admin system configuration settings. |
| `sharedCatalogUpdateCategoryPermissions` | Updates categories assigned to a shared catalog category. Required when the [**Shared Catalogs**](catalog-shared.md) option is enabled in the Admin system configuration settings. |
| `negotiableQuotePriceUpdate` | Updates prices for negotiable quotes. Required when the [**Quotes**](quotes.md) option is enabled in the Admin system configuration settings. |
| `purchaseorder.toorder` | Converts purchase order to order. Required when the [**Purchase Orders**](purchase-order-flow.md) option is enabled in the Admin system configuration settings.   |
| `purchaseorder.transactional.email` | Send purchase order emails. Required when the [**Purchase Order**](purchase-order-flow.md) option is enabled in the Admin system configuration settings. |
| `purchaseorder.validation` | Validates purchase order against relevant [approval rules](account-dashboard-approval-rules.md). Required when the [**Purchase Order**](purchase-order-flow.md) option is enabled in the Admin system configuration settings. |
| `quoteItemCleaner` | Deletes invalid or inactive price quotes when a product is deleted from the catalog or removed from the cart. Required when the [**Quotes**](quotes.md) option is enabled in the Admin system configuration settings. |
| `inventoryQtyCounter` | Asynchronously corrects the stock index after an order is placed or a product is removed. Required when the [**Use deferred stock update**](https://docs.magento.com/user-guide/configuration/catalog/inventory.html#product-stock-options) option is enabled for Inventory Management in the Admin configuration settings. See [Performance Best Practices](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update). |
| `async.operations.all` | Creates messages for each individual task of a [bulk operation](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), such as importing or exporting items, changing prices on a mass scale, and assigning products to a warehouse. Required when the [**Admin bulk operations**](https://docs.magento.com/user-guide/configuration/catalog/inventory.html#admin-bulk-operations) option for Inventory Management is set to **Run asynchronously** in the Admin system configuration settings. |

### Start message consumers

1. List the available message consumers:

   ```bash
   bin/magento queue:consumers:list
   ```

   You should see the following consumers:

   ```terminal
   sharedCatalogUpdatePrice
   sharedCatalogUpdateCategoryPermissions
   quoteItemCleaner
   inventoryQtyCounter
   async.operations.all
   ```

1. Start each consumer separately:

   ```bash
   bin/magento queue:consumers:start <consumer_name>
   ```

   For example:

   ```bash
   bin/magento queue:consumers:start sharedCatalogUpdatePrice
   ```

>[!TIP]
>
>Append `&` to the command to run it in the background, return to a prompt, and continue running commands. For example: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Refer to [Manage message queues](https://devdocs.magento.com/guides/v2.4/config-guide/mq/manage-message-queues.html) in the _Configuration Guide_ for more information.

### Add message consumers to cron

You can also add these two message consumers to the cron job (optional) by adding the following lines in your `crontab`:

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

### Specify parameters for message consumers

Depending on your system configuration, to prevent possible issues, specify the following parameters when starting the services:

-  `--max-messages`: manages the consumer's lifetime and allows you to specify the maximum number of messages processed by the consumer. The best practice for a PHP application is to restart long-running processes to prevent possible memory leaks.

-  `--batch-size`: allows you to limit the system resources consumed by the consumers (CPU, memory). Using smaller batches reduces resource usage and, thus, leads to slower processing.

## Enable B2B features in the Admin

After installing the B2B for Adobe Commerce extension and starting message consumers (if you want to enable the Shared Catalog feature), you must also [enable B2B features in the Admin](enable-basic-features.md).
