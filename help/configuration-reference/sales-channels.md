---
title: Sales Channels > Global Settings
description: Placeholder
---
# Sales Channels > Global Settings

{{config}}

These settings are available when [Amazon Sales Channel](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) is installed.

![Sales Channel Settings](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

|Field|[Scope](../getting-started/websites-stores-views.md#scope-settings)|Description|
|Clear Log History|Global|Options:<br/><br/>**Once Daily**: Select this option to clear your store's activity history once daily.<br/><br/>**Once Weekly**: Select this option to clear your store's activity history once weekly.<br/><br/>**Once Monthly**: (Default) Select this option to clear your store's activity history once monthly.|
|Background Tasks (CRON) Source|Global|Select `Magento CRON` to specify that the Amazon Sales Channel uses your Commerce cron settings to determine communication and data sync intervals with Amazon Seller Central.|
|Enable Debug Logging|Global|Select `Enabled` to collect additional synchronization data when troubleshooting is needed.<br/><br/>This option is disabled by default and should only be enabled when needed for troubleshooting, as continued logging negatively impacts performance. If enabled for troubleshooting, it should be disabled when complete.<br/><br/>**Note**: Amazon Sales Channel logging is written to the `{Commerce Root}/var/log/channel_amazon.log` file and can be viewed in [[developer mode](https://docs.magento.com/user-guide/magento/installation-modes.html).|
|Read-Only Mode|Global|Select `Enabled` to block all outgoing state-changing API requests. Potential changes are saved, but not sent, until Read-Only Mode is disabled. To start the data transfers again, select `Disabled`.<br/><br/>When a database is migrated to a new copy of the instance (detected when a store's URL changes in the configuration), Read-Only Mode is automatically enabled.<br/><br/>Read-Only Mode is designed for use on copies of the production instance, like _Staging_ or _QA_, and should not be used on the production instance.<br/><br/>**Note**: Configuration cache must be cleared for Read-Only Mode to enable.|
