---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL System]'
description: Review the configurations settings on the [!UICONTROL Advanced] &gt; [!UICONTROL System] page of the Commerce Admin.
exl-id: ffdaf7b5-c508-4fab-93ec-21f28cff6d3d
---
# [!UICONTROL Advanced] > [!UICONTROL System]

{{config}}

## [!UICONTROL Cron (Scheduled Tasks)]

![Advanced configuration - Cron (Scheduled Tasks)](./assets/system-cron.png)<!-- zoom -->

For more information about changing these configuration settings, see [Cron (scheduled tasks)](../../systems/cron.md).

### [!UICONTROL index]

![Advanced configuration - Cron Group: Index](./assets/system-cron-group-index.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Generate Schedules Every]|Global|Determines the frequency in minutes, that schedules are generated.|
|[!UICONTROL Schedule Ahead for]|Global|Determines the number of minutes in advance that schedules are generated.|
|[!UICONTROL Missed if Not Run Within]|Global|Determines the number of minutes before a cron job that hasn't yet executed is marked as missed.|
|[!UICONTROL History Cleanup Every]|Global|Determines the number of minutes that pass before the cron history is cleaned.|
|[!UICONTROL Success History Lifetime]|Global|Determines the number of minutes that the record of successfully completed cron jobs is kept in the database.|
|[!UICONTROL Failure History Lifetime]|Global|Determines the number of minutes that the record of failed cron jobs is kept in the database.|
|[!UICONTROL Use Separate Process]|Global|Determines if cron jobs are executed in parallel as separate processes. Options: `Yes` / `No`|

{style="table-layout:auto"}

### [!UICONTROL default]

![Cron Group: Default](./assets/system-cron-group-default.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Generate Schedules Every]|Global|Determines the frequency in minutes, that schedules are generated.|
|[!UICONTROL Schedule Ahead for]|Global|Determines the number of minutes in advance that schedules are generated.|
|[!UICONTROL Missed if Not Run Within]|Global|Determines the number of minutes before a cron job that hasn't yet executed is marked as missed.|
|[!UICONTROL History Cleanup Every]|Global|Determines the number of minutes that pass before the cron history is cleaned.|
|[!UICONTROL Success History Lifetime]|Global|Determines the number of minutes that the record of successfully completed cron jobs is kept in the database.|
|[!UICONTROL Failure History Lifetime]|Global|Determines the number of minutes that the record of failed cron jobs is kept in the database.|
|[!UICONTROL Use Separate Process]|Global|Determines if cron jobs are executed in parallel as separate processes. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL MySQL Message Queue Cleanup]

{{ee-feature}}

![Advanced configuration - MySQL Message Queue Cleanup](./assets/system-mysql-message-queue-cleanup.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Successful Messages Lifetime]|Global|Determines the lifetime of successful messages in minutes. Enter zero to skip the cleanup. Default: `10080` (7 days)|
|[!UICONTROL New Messages Lifetime]|Global|Determines the lifetime of new messages in minutes. Enter zero to skip the cleanup. Default: `10080` (7 days)|
|[!UICONTROL Failed Messages Lifetime]|Global|Determines the lifetime of failed messages in minutes. Enter zero to skip the cleanup. Default: `10080` (7 days)|
|[!UICONTROL Retry Messages in Progress After]|Global|Determines how long the system waits for a message in progress before retrying. Default: `1440` (24 hours)|

{style="table-layout:auto"}

## [!UICONTROL Mail Sending Settings]

![Advanced configuration - Mail Sending Settings](./assets/system-mail-sending-settings.png)<!-- zoom -->

For more information about changing these settings, see [Configure email communications](../../systems/email-communications.md) in the _Admin Systems Guide_.

>[!IMPORTANT]
>
>**Security Notice** We recommend that all merchants immediately set their mail sending configuration to protect against a recently identified potential remote code execution exploit. Until this issue is resolved, it is highly recommended that you avoid using [!DNL Sendmail] for email communications. In the [!UICONTROL Mail Sending Settings], make sure that [!UICONTROL Set Return Path] is set to `No`.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Disable Email Communications]|Store View|Determines if email communications are activated for the store. Options: `Yes` / `No`|
|[!UICONTROL Transport] |Store View| Determines the transport type for email communications from the store. Options: `Sendmail` / `SMTP` |
|[!UICONTROL Host]|Store View|(For SMTP and Windows servers only) Determines the name that is used to refer to the host. Default value: `localhost`|
|[!UICONTROL Port (25)]|Store View|(For SMTP and Windows servers only) Identifies the port used for email communications. Default value: `25`|
|[!UICONTROL Set Return-Path]|Store View|Determines if a routing address is used for returned emails. Options: `No` / `Yes` / `Specified`|

{style="table-layout:auto"}

### SMTP options

When you select SMTP at the transport type, additional options are available to configure the SMTP server connection.

![Advanced configuration - Mail Sending Settings with SMTP](./assets/system-mail-sending-settings-smtp.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Username] | Store View | Login user name for the SMTP server. |
|[!UICONTROL Password] | Store View | Password for the SMTP server login. |
|[!UICONTROL Auth] | Store View | Determines th authentication type for the SMTP server connection. Options: `NONE` / `PLAIN` / `LOGIN` |
|[!UICONTROL SSL] | Store View | Determines verification type for the host security certificate. Options: `SSL` / `TLS` |

{style="table-layout:auto"}

## [!UICONTROL Currency]

![Advanced configuration - Currency](./assets/system-currency.png)<!-- zoom -->

For more information about changing this setting, see [Currency configuration](../../stores-purchase/currency-configuration.md) in the _Stores and Purchase Experience Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Installed Currencies]|Global|Indicates the currencies that are currently available to the Commerce installation. Options include all available currencies, with installed currencies selected.|

{style="table-layout:auto"}

## [!UICONTROL Security]

![Advanced configuration - Security](./assets/system-security.png)<!-- zoom -->

For more information about changing these settings, see [Session management](../../systems/security-session-management.md) in the _Admin Systems Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Max Session Size in Admin]|Global|Limit the maximum session size in bytes. Use `0` to disable.|
|[!UICONTROL Max Session Size in Storefront]|Global|Limit the maximum session size in bytes. Use `0` to disable.|

{style="table-layout:auto"}

## [!UICONTROL Notifications]

![Advanced configuration - Notifications](./assets/system-notifications.png)<!-- zoom -->

For more information about changing these settings, see [System notifications](../../systems/notifications.md) in the _Admin Systems Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Use HTTPS to Get Feed]|Global|Determines if Admin notifications are delivered over a secure channel. Options: `Yes` / `No`|
|Update Frequency|Global|Determines the frequency of Admin message updates. Options: `1 Hour` / `2 Hours` / `6 Hours` / `12 Hours` / `24 Hours`|
|[!UICONTROL Last Update]|Global|Indicates the date and time of the last message update.|

{style="table-layout:auto"}

## [!UICONTROL Scheduled Backup Settings]

![Advanced configuration - Scheduled Backup Settings](./assets/system-scheduled-backup-settings.png)<!-- zoom -->

For more information about changing these settings, see [System backups](../../systems/backups.md) in the _Admin Systems Guide_.

{{$include /help/_includes/backups-note.md}}

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Scheduled Backup]|Global|Determines if the Commerce instance is automatically backed up on a regular schedule. Options: `Yes` / `No`|
|[!UICONTROL Backup Type]|Global|Determines the elements of the Commerce instance that are included in the backup. Options: `Database` / `Database and Media` / `System` / `System (excluding Media)`|
|[!UICONTROL Start Time]|Global|Specifies the hour, minute, and second that the scheduled backup begins.|
|[!UICONTROL Frequency]|Global|Determines how often the scheduled backup takes place. Options: `Daily` / `Weekly` / `Monthly`|
|[!UICONTROL Maintenance Mode]|Global|Determines if the store is put in maintenance mode during the scheduled backup. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Log Archiving]

{{ee-feature}}

![Advanced configuration - Admin Actions Log Archiving](./assets/system-admin-actions-log-archiving.png)<!-- zoom -->

For more information about changing these settings, see [Action log archive](../../systems/action-log-archive.md) in the _Admin Systems Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Log Entry Lifetime, Days]|Store View|Determines the number of days that admin actions are kept in the Admin Actions archive. Default: `60`|
|[!UICONTROL Log Archiving Frequency]|Store View|Determines how often the Admin Actions logs are archived. Options: `Daily` / `Weekly` / `Monthly`|

{style="table-layout:auto"}

## [!UICONTROL Full Page Cache]

![Advanced configuration - Full Page Cache](./assets/system-full-page-cache.png)<!-- zoom -->

For more information about changing these settings, see [Full-page caching](../../systems/cache-management.md#full-page-caching) in the _Admin Systems Guide_.

![Advanced configuration - Varnish Configuration](./assets/system-full-page-cache-varnish.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Caching Application]|Global|Determines the application that is used to manage the full-page cache. Options: <br/>**`Built-in Application`** - Not recommended for the production environment. <br/>**`Varnish Caching`** - Recommended for the production environment.|
|[!UICONTROL TTL for public content]|Global|Determines the lifetime of the public content cache in seconds. Default value: `120`|
|**[!UICONTROL Varnish Configuration]**|||
|[!UICONTROL Access list]|Global|Specifies the IP addresses that can purge the Varnish configuration to generate a config file. Separate multiple entries with a comma. Default value: `localhost`|
|[!UICONTROL Backend host]|Global|Specifies the backend host that generates config files. Default value: `localhost`|
|[!UICONTROL Backend port]|Global|Specifies the backend port that is used to generate config files. Default value: `8080`|
|[!UICONTROL Grace period]|Global|Specifies the grace period in seconds for generating a config file. Default value: `300`|
|**[!UICONTROL Export Configuration]**|||
|[!UICONTROL Export VCL for Varnish 4]|Global|Exports the `varnish.vcl` file for version 4.|
|[!UICONTROL Export VCL for Varnish 5]|Global|Exports the `varnish.vcl` file for version 5.|
|[!UICONTROL Export VCL for Varnish 6]|Global|Exports the `varnish.vcl` file for version 6.|

{style="table-layout:auto"}

## [!UICONTROL Storage Configuration for Media]

![Advanced configuration - Storage Configuration for Media - File System](./assets/system-storage-config-media.png)<!-- zoom -->

For more information about changing these settings, see [Use a Media Database](../../content-design/media-storage-database.md) in the _Content and Design Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Media Storage]|Global|Determines the method used to store media files. Default setting: `File System`|
|[!UICONTROL Environment Update Time]|Global|Determines the frequency of the media file environment updates in seconds. Default value: `3600`|

{style="table-layout:auto"}

![Advanced configuration - Storage Configuration for Media - Database](./assets/database-storage-deprecated.png)<!-- zoom -->

>[!IMPORTANT]
>
>The database media storage method has been deprecated as of Adobe Commerce and Magento Open Source 2.4.3.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Media Storage]|Global|Specifies database as the method used to store media files.|
|[!UICONTROL Select Media Database]|Global|Identifies the name of the database used for media storage. Default setting: `default_setup`|
|[!UICONTROL Synchronize]||Synchronizes the transfer of all media to the specified database location.|
|Environment Update Time|Global|Determines the frequency of the media file environment updates in seconds. Default value: `3600`|

{style="table-layout:auto"}

## [!UICONTROL Bulk Actions]

{{ee-feature}}

![Advanced configuration - Bulk Actions](./assets/system-bulk-actions.png)<!-- zoom -->

For more information about changing these settings, see [Bulk actions](../../systems/action-log-bulk-actions.md) in the _Admin Systems Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Days Saved in Log]|Global|Determines the number of days that bulk actions are kept in the _Bulk Actions Log_ archive. Default: `60`|

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import/Export File History Cleaning]

{{ee-feature}}

![Advanced configuration - Scheduled Import/Export File History Cleaning](./assets/system-schedule-history-cleaning.png)<!-- zoom -->

For more information about changing these settings, see [Scheduled import and export](../../systems/data-scheduled-import-export.md) in the _Admin Systems Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Save File, Days]|Global|Determines the number of days that import/export history files are saved.|
|[!UICONTROL Enable Scheduled File History Cleaning]|Global|Enables the scheduled file cleanup of import/export files. Options: `Yes` / `No`|
|[!UICONTROL Clean Now]||Overrides the scheduled cleanup, and immediately cleans the import/export history files.|
|[!UICONTROL Start Time]|Global|Specifies the hour, minute, and second of the import/export history file cleanup.|
|[!UICONTROL Frequency]|Global|Determines how often the import/export history files are cleaned. Options: `Daily` / `Weekly` / `Monthly`|
|[!UICONTROL Error Email Recipient]|Global|The email address of the person who is to receive notification if an error occurs while the import/export file history is cleaned. Separate multiple addresses with a comma.|
|[!UICONTROL Error Email Sender]|Global|Identifies the store contact that appears as the sender of the notification. Default sender: `General Contact`|
|[!UICONTROL Error Email Template]|Global|Identifies the email template that is used for the import/export file cleaning-error notification. Default template: `File History Clean Failed`|

{style="table-layout:auto"}

## [!UICONTROL Image Upload Configuration]

![Advanced configuration - Image Upload Configuration](./assets/system-image-upload-configuration.png)<!-- zoom -->

<!-- [Image Upload Configuration](https://docs.magento.com/user-guide/system/action-log-bulk-actions.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Quality]|Global|Determines the JPG quality for the resized image. Lower quality reduces the file size. Use 80-90% to help reduce file size with high quality. Default: `80`|
|[!UICONTROL Enable Frontend Resize]|Global|Enable this setting to allow Commerce to resize large, oversized images you may upload for the _Product Details_ page. Commerce resizes the image files using JavaScript before uploading the file. When the image is resized, it keeps the exact proportions to meet and not exceed the largest size for Maximum Width or Maximum Height. Default: `Yes`|
|[!UICONTROL Maximum Width]|Global|Determines the maximum pixel width for the image. When the image is resized, it does not exceed this width. Default: `1920`|
|[!UICONTROL Maximum Height]|Global|Determines the maximum pixel height for the image. When the image is resized, it does not exceed this height. Default: `1200`|

{style="table-layout:auto"}

## [!UICONTROL Media Gallery]

![Advanced configuration - Media Gallery](./assets/system-media-gallery.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Old Media Gallery]|Global|Enables or disables the old Media Gallery.|

{style="table-layout:auto"}

## [!UICONTROL Media Gallery Image Optimization]

![Advanced configuration - Media Gallery Image Optimization](./assets/system-media-image-optimization.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Image Optimization]|Global|Determines if images are resized to decrease the file size of the images inserted to the content. Original images are preserved in the Media Gallery.|
|[!UICONTROL Maximum Width]|Global|The maximum width (in pixels) for images inserted from Media Gallery into the content.|
|[!UICONTROL Maximum Height]|Global|The maximum height (in pixels) for images inserted from Media Gallery into the content.|

{style="table-layout:auto"}

## [!UICONTROL Adobe Stock Integration]

![Advanced configuration - Adobe Stock integration](./assets/system-adobe-stock-integration.png)<!-- zoom -->

For more information about configuring these settings, see [Adobe Stock Integration](../../content-design/adobe-stock.md) in the _Content and Design Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled Adobe Stock]|Global|Enables or disables the Adobe Stock Integration.|
|[!UICONTROL API Key (Client ID)]|Global|An API key is required to connect your store to the Adobe Stock service.|
|[!UICONTROL Client Secret]|Global|The Client Secret for your Adobe Stock integration is required.|
|[!UICONTROL Test Connection]||Runs a test to verify that the API key is valid for use with the Adobe Stock service.|

{style="table-layout:auto"}
