---
title: Install the [!DNL B2B for Adobe Commerce] extension
description: Learn how to install the [!DNL B2B for Adobe Commerce] metapackage.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
---

# Install the [!DNL B2B for Adobe Commerce] extension

These installation instructions apply to Adobe Commerce deployed on premises. Installation instructions for projects deployed on cloud infrastructure are available in the [Commerce Cloud Infrastructure Guide](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html).

Install the most recent version of the B2B extension that is supported on the deployed Adobe Commerce version.

## Requirements

- Adobe Commerce version 2.3.x or later
- [Supported version of the B2B extension](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html#compatibility)
- Valid [authentication keys](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) to download Adobe Commerce extensions.

  Save authentication keys for installation by defining them globally in your [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) directory. Or, save them to an `[auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file))` file in the Adobe Commerce application root directory.

## Installation steps

  Save authentication keys for installation by defining them globally in your [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) directory. Or, save them to an `[auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file)` file in the Adobe Commerce application root directory.

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   If an error occurs, for example:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Check the package spelling, your version constraint, and that the package is available and matches your minimum-stability (stable) requirement.

1. If prompted, enter your [authentication keys](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

   Your _public key_ is your username; your _private key_ is your password. If you have stored your public and private keys in `auth.json`, you are not prompted to authenticate.

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
   >In Production mode, you might receive a message to `Please rerun Magento compile command`. Enter the commands to complete the installation. Adobe Commerce does not prompt you to run the compile command in Developer mode.

After completing the installation, configure and start message consumers, including [specifying parameters for message consumers](#specify-parameters-for-message-consumers).

## Message consumers

The B2B for Adobe Commerce extension uses MySQL for message queue management. The following table lists the message consumers that support B2B capabilities. After you install the extension, start the message consumers for the B2B capabilities required for your Commerce storefront.

| Consumer                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice`               | Updates price for each product in a shared catalog. Required when the [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) option is enabled in the Admin system configuration settings.                                                                                                                                                                                                                                                                                                                                |
| `sharedCatalogUpdateCategoryPermissions` | Updates categories assigned to a shared catalog category. Required when the [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) option is enabled in the Admin system configuration settings.                                                                                                                                                                                                                                                                                                                          |
| `negotiableQuotePriceUpdate`             | Updates prices for negotiable quotes. Required when the [**[!UICONTROL Quotes]**](quotes.md) option is enabled in the Admin system configuration settings.                                                                                                                                                                                                                                                                                                                                                               |
| `purchaseorder.toorder`                  | Converts purchase order to order. Required when the [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) option is enabled in the Admin system configuration settings.                                                                                                                                                                                                                                                                                                                                             |
| `purchaseorder.transactional.email`      | Send purchase order emails. Required when the [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) option is enabled in the Admin system configuration settings.                                                                                                                                                                                                                                                                                                                                                   |
| `purchaseorder.validation`               | Validates purchase order against relevant [approval rules](account-dashboard-approval-rules.md). Required when the [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) option is enabled in the Admin system configuration settings.                                                                                                                                                                                                                                                                              |
| `quoteItemCleaner`                       | Deletes invalid or inactive price quotes when a product is deleted from the catalog or removed from the cart. Required when the [**[!UICONTROL Quotes]**](quotes.md) option is enabled in the Admin system configuration settings.                                                                                                                                                                                                                                                                                       |
| `inventoryQtyCounter`                    | Asynchronously corrects the stock index after an order is placed or a product is removed. Required when the [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) option is enabled for Inventory Management in the Admin configuration settings. See [Performance Best Practices](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update).                                       |
| `async.operations.all`                   | Creates messages for each individual task of a [bulk operation](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), such as importing or exporting items, changing prices on a mass scale, and assigning products to a warehouse. Required when the [**Admin bulk operations**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) option for [!DNL Inventory Management] is set to **Run asynchronously** in the Admin system configuration settings. |

{style="table-layout:auto"}

>![NOTE]
>
>For a list of all Adobe Commerce message consumers, see [Message queue consumers](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/consumers.html) in the _Configuration Guide_.

### Configure message consumers

Prevent possible processing issues or delays by using the following parameters when you start the message consumers for B2B capabilities.

- `--max-messages`—Specifies the maximum number of messages each consumer must process before terminating (default = 10000). Although we do not recommend it, you can use 0 to prevent the consumer from terminating. The best practice for a PHP application is to restart long-running processes to prevent possible memory leaks.

- `--batch-size`— Allows you to limit the system resources consumed by the consumers (CPU, memory). Using smaller batches reduces resource usage and, thus, leads to slower processing.  If specified, messages in a queue are consumed in batches of <value> each. This option is applicable for the batch consumer only. If `--batch-size` is not defined, the batch consumer receives all available messages in a queue.

You specify these parameters on the command line when you start the message consumers.

For details, see [Message consumers configuration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) in the _Adobe Commerce Configuration Guide_.

### Start message consumers

To enable asynchronous operations for B2B capabilities, you must start multiple message consumers.

1. List the available message consumers:

   ```bash
   bin/magento queue:consumers:list
   ```

   The command returns available message consumers including all [B2B message consumers](#message-consumers).

1. Start each consumer separately:

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>

   ```

   For example:

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>To run it in the background, append `&` to the command, return to a prompt, and continue running commands. For example: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

For more information, see [Manage message queues](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) in the _Configuration Guide_.

### Add message consumers to cron

You have the option to add the `SharedCatalogUpdateCategoryPermissions` and `SharedCatalogUpdatePrice` message consumers to the cron configuration file (`[/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#process-management)`) to automate the run schedule.

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

You can also configure schedules for message consumers from the [Store Configuration settings](../systems/cron.md) in the Admin.

## Enable B2B features in the Admin

After installing the B2B for Adobe Commerce extension and starting message consumers (if you want to enable the Shared Catalog feature), you must also [enable B2B features in the Admin](enable-basic-features.md).