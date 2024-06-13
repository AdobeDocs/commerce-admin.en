---
title: Install the [!DNL Adobe Commerce B2B] extension
description: Learn how to install the [!DNL Adobe Commerce B2B] metapackage.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
---

# Install the [!DNL Adobe Commerce B2B] extension

The Adobe Commerce B2B extension is only available for Adobe Commerce v2.2.0 or later. It is installed after installing Adobe Commerce.

Install the most recent version of the B2B extension that is supported on the deployed Adobe Commerce version.

## Requirements

- Adobe Commerce version 2.3.x or later
- [Supported version of the B2B extension](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability)
- Valid [authentication keys](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys) to download Adobe Commerce extensions.

  Save authentication keys for installation by defining them globally in your [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) directory. Or, save them to an [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) file in the Adobe Commerce application root directory.

Before installing or upgrading the B2B extension, check the release notes for the most current information about version compatibility, updates, or changes that can affect installation or upgrade requirements.

- [B2B Release Notes](release-notes.md)
- [Adobe Commerce Release Notes](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

## Installation steps

>[!BEGINTABS]

>[!TAB Cloud infrastructure]

>[!TIP]
>
>When installing Adobe Commerce B2B on cloud infrastructure, Adobe recommends that you deploy your Adobe Commerce application to an Integration or Staging environment before beginning.

Adobe recommends working in a development branch when adding the B2B module to your project. If you do not have a branch, see [Create a branch for development](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches). When installing the B2B module, the `Magento_B2b` module name is automatically inserted in the `app/etc/config.php` file. There is no need to edit the file directly.

**To install the B2B module**:

1. On your local workstation, change to your project directory.

1. Create or check out a development branch.

1. Add the B2B module to the `require` section of the `composer.json` file.

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. Update the project dependencies.

   ```bash
   composer update
   ```

1. Add, commit, and push code changes.

   ```bash
   git add -A
   ```

   ```bash
   git commit -m "Install the B2B module."
   ```

   ```bash
   git push origin <branch-name>
   ```

1. After the build and deploy finishes, use SSH to log in to the remote environment and verify that the B2B module is installed.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   An extension name uses the format: `<VendorName>_<ComponentName>`.

   Sample response:

   ```terminal
   Magento_B2b : Module is enabled
   ```

   If you encounter deployment errors, see [Recover from component failure](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

>[!TAB On-premises]

1. From the Adobe Commerce application root directory, update the `composer.json` to add the dependencies for the B2B extension:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   If an error occurs, for example:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Check the package spelling, your version constraint, and that the package is available and matches your minimum-stability (stable) requirement.

1. If prompted, enter your [authentication keys](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

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

>[!ENDTABS]

After completing the installation, configure and start message consumers.

## Message consumers

The Adobe Commerce B2B extension uses MySQL for message queue management. The following table lists the message consumers that support B2B capabilities. After you install the extension, start the message consumers for the B2B capabilities required for your Commerce storefront.

| Consumer                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice`               | Updates the price for each product in a shared catalog. Required when the [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) option is enabled in the Admin System configuration settings.                                                                                                                                                                                                                                                                                                                                |
| `sharedCatalogUpdateCategoryPermissions` | Updates categories assigned to a shared catalog category. Required when the [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) option is enabled in the Admin System configuration settings.                                                                                                                                                                                                                                                                                                                          |
| `negotiableQuotePriceUpdate`             | Updates prices for negotiable quotes. Required when the [**[!UICONTROL Quotes]**](quotes.md) option is enabled in the Admin System configuration settings.                                                                                                                                                                                                                                                                                                                                                               |
| `purchaseorder.toorder`                  | Converts purchase order to order. Required when the [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) option is enabled in the Admin System configuration settings.                                                                                                                                                                                                                                                                                                                                             |
| `purchaseorder.transactional.email`      | Send purchase order emails. Required when the [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) option is enabled in the Admin System configuration settings.                                                                                                                                                                                                                                                                                                                                                   |
| `purchaseorder.validation`               | Validates purchase order against relevant [approval rules](account-dashboard-approval-rules.md). Required when the [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) option is enabled in the Admin System configuration settings.                                                                                                                                                                                                                                                                              |
| `quoteItemCleaner`                       | Deletes invalid or inactive price quotes when a product is deleted from the catalog or removed from the cart. Required when the [**[!UICONTROL Quotes]**](quotes.md) option is enabled in the Admin System configuration settings.                                                                                                                                                                                                                                                                                       |
| `inventoryQtyCounter`                    | Asynchronously corrects the stock index after an order is placed or a product is removed. Required when the [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) option is enabled for Inventory Management in the Admin configuration settings. See [Performance Best Practices](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update).                                       |
| `async.operations.all`                   | Creates messages for each individual task of a [bulk operation](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/) such as importing or exporting items, changing prices on a mass scale, and assigning products to a warehouse. Required when the [**Admin bulk operations**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) option for [!DNL Inventory Management] is set to **Run asynchronously** in the Admin System configuration settings. |

{style="table-layout:auto"}

>[!NOTE]
>
>For a list of all Adobe Commerce message consumers, see [Message queue consumers](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) in the _Configuration Guide_.

### Configure message consumers

Prevent possible processing issues or delays by adding the following parameters when you [start the message consumers](#start-message-consumers) for B2B capabilities.

- `--max-messages <value>`— Specifies the maximum number of messages each consumer must process before terminating (default = 10000). Although Adobe does not recommend it, you can use 0 to prevent the consumer from terminating. The best practice for a PHP application is to restart long-running processes to prevent possible memory leaks.

- `--batch-size <value>`— Allows you to limit the system resources consumed by the consumers (CPU, memory). Using smaller batches reduces resource usage and, thus, leads to slower processing.  If specified, messages in a queue are consumed in batches of `<value>` each. This option is applicable for the batch consumer only. If `--batch-size` is not defined, the batch consumer receives all available messages in a queue.

For information about additional configuration options, see [Specific-configuration](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

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

For more information, see [Manage message queues](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) in the _Configuration Guide_.

### Add message consumers to cron

You can automate the run schedule for the `SharedCatalogUpdateCategoryPermissions` and `SharedCatalogUpdatePrice` message consumers by adding the schedule to the cron configuration file [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

You can also configure schedules for message consumers from the [Store Configuration settings](../systems/cron.md) in the Admin.

## Enable B2B features in the Admin

After installing the Adobe Commerce B2B module and starting message consumers, you must also [enable B2B features in the Admin](enable-basic-features.md).

## Manage the B2B module

When you install the B2B module using Composer, the deployment process automatically enables the module. If you already have the B2B module installed, you can enable or disable the module using the CLI.

Enable the B2B module:

```bash
bin/magento module:enable Magento_B2b
```

Sample response:

```terminal
The following modules have been enabled:
- Magento_B2b

Cache cleared successfully.
Generated classes cleared successfully. Please run the 'setup:di:compile' command to generate classes.
Info: Some modules might require static view files to be cleared. To do this, run 'module:enable' with the --clear-static-content option to clear them.
```

See [Manage extensions](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure-store/extensions).
