---
title: Scheduled order operations
description: Learn about the scheduled order operations and orders cron settings that support this functionality.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
TQID: https://experienceleague.adobe.com/pViPmBFGErjXeFyvBNBVuJiw8Pn51JIGkeZ2mJAf72M
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Scheduled order operations

Use [Cron](../systems/cron.md) jobs to schedule the following order processing tasks:

![Orders grid](./assets/orders-grid.png){width="700" zoomable="yes"}

## Set pending payment order lifetime

The lifetime of orders with pending payments is determined by the _Orders Cron Settings_ configuration. The default value is set to 480 minutes, which is eight hours.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand the **[!UICONTROL Sales]** section and choose **[!UICONTROL Sales]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Orders Cron Settings]** section.

   ![Orders Cron Settings](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. For **[!UICONTROL Pending Payment Order Lifetime (minutes)]**, enter the number of minutes before a pending payment expires.

1. Click **[!UICONTROL Save Config]**.

## Enable scheduled grid updates and reindexing

The Grid Settings configuration schedules updates to the following order management grids, and reindexes the data as scheduled by [Cron](../systems/cron.md):

- [Orders](orders.md#orders-workspace)
- [Invoices](invoices.md)
- [Shipments](shipments.md)
- [Credit Memos](credit-memos.md)

By scheduling these tasks, you can avoid the locks that occur when data is saved and reduce processing time. When enabled, any updates take place only during the scheduled cron job. For best results, Cron should be configured to run once every minute.

**_To enable the updates and reindexing:_**

[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."} When [Production mode](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (the default mode used in Adobe Commerce on cloud infrastructure) is enabled, run the following command:

`bin/magento config:set dev/grid/async_indexing 1`

When [Default mode](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) is enabled, complete the following steps:

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand the **[!UICONTROL Advanced]** section and choose **[!UICONTROL Developer]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Grid Settings]** section.

1. Set **[!UICONTROL Asynchronous Indexing]** to `Enable`.

   ![Grid Settings](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save Config]**.
