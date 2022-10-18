---
title: Scheduled order operations
description: Learn about the scheduled order operations and orders cron settings that support this functionality.
---
# Scheduled order operations

Use [Cron](https://docs.magento.com/user-guide/system/cron.html) jobs to schedule the following order processing tasks:

![Orders grid](./assets/orders-grid.png)<!-- zoom -->

## Set pending payment order lifetime

The lifetime of orders with pending payments is determined by the _Orders Cron Settings_ configuration. The default value is set to 480 minutes, which is eight hours.

1. On the _Admin_ sidebar, click **Stores**.

1. In the _Settings_ section, choose **Configuration**.

1. On the left panel in the _Sales_ section, choose **Sales**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Orders Cron Settings** section.

   ![Orders Cron Settings](../configuration-reference/sales/assets/sales-orders-cron-settings.png)<!-- zoom -->

1. For **Pending Payment Order Lifetime (minutes)**, enter the number of minutes before a pending payment expires.

1. Click **Save Config**.

## Enable scheduled grid updates and reindexing

The Grid Settings configuration schedules updates to the following order management grids, and reindexes the data as scheduled by [Cron](https://docs.magento.com/user-guide/system/cron.html):

- [Orders](orders.md#orders-workspace)
- [Invoices](invoices.md)
- [Shipments](shipments.md)
- [Credit Memos](credit-memos.md)

By scheduling these tasks, you can avoid the locks that occur when data is saved and reduce processing time. When enabled, any updates take place only during the scheduled cron job. For best results, Cron should be configured to run once every minute.

To enable the updates and reindexing:

1. On the _Admin_ sidebar, click **Stores**.

1. In the _Settings_ section, choose **Configuration**.

1. On the left panel in the _Advanced_ section, choose **Developer**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Grid Settings** section.

1. Set **Asynchronous Indexing** to `Enable`.

   ![Grid Settings](../configuration-reference/advanced/assets/developer-grid-settings.png)<!-- zoom -->

1. Click **Save Config**.
