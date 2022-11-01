---
title: Action log archive
description: Placeholder
---
# Action log archive

{{ee-feature}}

The Admin Actions archive lists the CSV log files that are stored on the server. In the configuration, you can specify how long the log entries are stored, and how often they are archived. By default, the file name includes the current date in ISO format:  `yyyyMMddHH`

>[!NOTE]
>
>Log archiving requires a [cron job](cron.md) to be set up.

## Configure the Log Archive

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Advanced** and choose **System**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Admin Actions Log Archiving** section and set these options:

   - **Log Entry Lifetime, Days** — Enter the number of days that you want to keep the log entries in the database before they are removed.
   - **Log Archiving Frequency** — Set to `Daily`, `Weekly`, or `Monthly`.

   ![Advanced configuration - admin actions log archiving](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png)<!-- zoom -->

   [_Admin Actions Log Archiving_](https://docs.magento.com/user-guide/configuration/advanced/system.html)

1. When complete, click **Save Config**.

## View the Archive

On the _Admin_ sidebar, go to **System** > _Actions Logs_ > **Archive**.

![Action log archive](./assets/action-log-archive.png)<!-- zoom -->
