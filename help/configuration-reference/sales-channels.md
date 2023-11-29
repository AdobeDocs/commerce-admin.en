---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Review the configurations settings on the [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] page of the Commerce Admin.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
---
# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

These settings are available when [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) is installed.

![Sales Channel Settings](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

|Field|[Scope](../getting-started/websites-stores-views.md#scope-settings)|Description|
|-----|---------|------|
|[!UICONTROL Clear Log History]|Global|Options:<br/><br/>**`Once Daily`**: Select this option to clear your store's activity history once daily.<br/><br/>**`Once Weekly`**: Select this option to clear your store's activity history once weekly.<br/><br/>**`Once Monthly`**: (Default) Select this option to clear your store's activity history once monthly.|
|[!UICONTROL Background Tasks (CRON) Source]|Global|Select `Magento CRON` to specify that the [!DNL Amazon Sales Channel] uses your Commerce cron settings to determine communication and data sync intervals with Amazon Seller Central.|
|[!UICONTROL Enable Debug Logging]|Global|Select `Enabled` to collect additional synchronization data when troubleshooting is needed.<br/><br/>This option is disabled by default and should only be enabled when needed for troubleshooting, as continued logging negatively impacts performance. If enabled for troubleshooting, it should be disabled when complete.<br/><br/>**_Note_**: Amazon Sales Channel logging is written to the `/var/log/channel_amazon.log` file and can be viewed in [developer mode](../systems/developer-tools.md#operation-modes).|
|[!UICONTROL Read-Only Mode]|Global|Select `Enabled` to block all outgoing state-changing API requests. Potential changes are saved, but not sent, until read-only mode is disabled. To start the data transfers again, select `Disabled`.<br/><br/>When a database is migrated to a new copy of the instance (detected when a store's URL changes in the configuration), read-only mode is automatically enabled.<br/><br/>This is designed for use on copies of the production instance, like _Staging_ or _QA_, and should not be used on the production instance.<br/><br/>**_Note_**: The configuration cache must be cleared for [!UICONTROL Read-Only Mode] to enable.|

{style="table-layout:auto"}
