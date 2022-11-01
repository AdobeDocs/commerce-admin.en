---
title: Order Management System for Adobe Commerce
description: Placeholder
---
# Order Management System for Adobe Commerce

{{ee-feature}}

Learn how to manage your stock aggregates and the Order Management integration, available if you use the Order Management System (OMS) Connector with Adobe Commerce, as well as view both the message log and changelog.

## MCOM menu

If you use the Order Management System (OMS) with Adobe Commerce, an **MCOM** option is available in the left menu of the Admin.

With this MCOM option, you can manage stock aggregates and integrations, and access both the message log and changelog.

**_To display the MCOM menu:_**

On the _Admin_ sidebar, choose **MCOM**.

![MCOM menu](./assets/admin-menu-mcom-ee.png)<!-- zoom -->

## Manage stock aggregates

Manage Stock Aggregates provides information about existing stock aggregates, and allows you to add new stock aggregates or edit or delete existing ones.

![Manage Stock Aggregates](./assets/manage-stock-aggregates.png)<!-- zoom -->

You [create sources](https://omsdocs.magento.com/en/features-processes/stock-sourcing/inventory/#configure-sources) and [aggregates](https://omsdocs.magento.com/en/features-processes/stock-sourcing/inventory/#configure-stock-aggregates) in the Order Management System (OMS) Admin. Then you assign which website(s) are associated with each aggregate via Manage Stock Aggregates in the Adobe Commerce Admin.

### Add a new stock aggregate

1. On the _Admin_ sidebar, go to **MCOM** > **Manage Stock Aggregates**.
1. Click **Add New Stock Aggregate**.
1. Enter a **Stock code** (name) for this stock aggregate.

   >[!NOTE]
   >
   >The stock code you enter should match the [stock aggregate code](https://omsdocs.magento.com/en/features-processes/stock-sourcing/inventory/#configure-stock-aggregates) in the OMS.

1. Choose a **Website** from the populated list.
1. When complete, click **Save Stock Aggregate**.

   ![Create new stock aggregate](./assets/manage-stock-aggregates-new.png)<!-- zoom -->

### Edit or delete a stock aggregate

1. On the _Admin_ sidebar, go to **MCOM** > **Manage Stock Aggregates**.
1. In the _Action_ column, click **Edit** for an existing stock aggregate.
1. To edit the stock aggregate, revise the **Stock code** or **Website** information and click **Save Stock Aggregate**.
1. To delete the stock aggregate, click **Delete** and then click **OK** in the confirmation dialog that appears.

## Message Log

Message Log enables you to view message processing logs, message history, and full error traces for the Connector.

![Message Log](./assets/message-log.png)<!-- zoom -->

### Enable message performance logs

1. Log into the Adobe Commerce Admin.
1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.
1. In the left panel, expand **MCOM Connector** and choose **Configuration**.
1. Scroll down to the Performance Monitor section and enable desired New Relic or Logger Output options.
1. Click **Save Config**.

See the [Message performance section](https://omsdocs.magento.com/integration/connector/view-logs/#message-performance) of the Views logs topic in the Order Management System (OMS) documentation for more information about what metrics are available out-of-the-box, an example log file, and more.

### View message processing logs

1. On the _Admin_ sidebar, go to **MCOM** > **Message Log**.
1. Click **Filters** and add any search criteria you want to employ, such as Topic (message) and direction (ingoing or outgoing).
1. Click **Apply Filters** to see your query results.

   ![Apply filters for your search query](./assets/message-log-filters.png)<!-- zoom -->

1. Click **View** for the message you want to view.

   The Details view for that message appears, including information about the message body and other related history.

1. If the message was processed with an error, you can click within the _History_ section to see a full error trace.

   ![Click the History section to see a full error trace](./assets/message-log-trace.png)<!-- zoom -->

Information about fatal errors is located in the `apache/nginx` error log (the [same place logs are located](https://devdocs.magento.com/cloud/project/log-locations.html#application-logs) for the Connector-less Adobe Commerce installation).

If you are working in Developer mode, all errors will be visible on your screen.

### Retry a topic (message)

You can retry a failed topic (message) in Message Log.

1. On the _Admin_ sidebar, go to **MCOM** > **Message Log**.
1. To determine whether a topic was successful, see the _Status_ column.

   Successful topics will show a `SUCCESS` status.

1. In the leftmost column, select the checkbox for the topic you want to retry.
1. Click **Actions** and select **Retry**.

   The topic (message) is resubmitted.

   ![Retry a topic (message)](./assets/message-log-retry.png)<!-- zoom -->

## Integration

Integration enables you to add or disable the Order Management System (OMS) integration for Adobe Commerce and view details of the integration.

### Register the integration

1. On the _Admin_ sidebar, go to **MCOM** > **Integration**.
1. Click **Register** to register the MCOM (also known as OMS) integration.

### Disable or enable the integration

1. On the _Admin_ sidebar, go to **MCOM** > **Integration**.
1. Check the status of the integration in the _Status_ row---either `Enabled` or `Disabled`.
   * To enable a disabled integration, click **Enable**. A confirmation message appears to inform you the integration has been enabled.
   * To disable an enabled integration, click **Disable**. A confirmation message appears to inform you the integration has been disabled.

   ![Disable or enable integration](./assets/integration-enable-disable.png)<!-- zoom -->

## Changelog

On the _Admin_ sidebar, go to **MCOM** > **Changelog**. You are immediately redirected to the Adobe Commerce version 2.2 Connector changelog. Change the version number in the URL to `2.3` to access the 2.3 Connector changelog.

## Export full catalog

You can manually request a full catalog export from Adobe Commerce. This feature queues all products from the catalog for export to the Order Management System (OMS).

Outside of manually exporting the full catalog, products are added to this queue after a new product is created, an existing product is updated, or after a bulk update to product attributes.

When requested, these outgoing messages are exported to a .csv file in chunks of 5,000.

**_To export the full catalog:_**

1. On the _Admin_ sidebar, go to **Catalog** > **Products**.
1. Click **Export Full Catalog**.

   ![Export Full Catalog](./assets/products-export-full.png)<!-- zoom -->
   _Export Full Catalog_

1. Click **OK** in the confirmation dialog.

   A progress bar will appear showing the status of the requested catalog export. When the export is complete, a confirmation message will appear confirming the action.

To manually export the catalog from the command line, see the [Export full catalog section](https://omsdocs.magento.com/integration/connector/setup-tutorial/#export-full-catalog) of the OMS Connector documentation.
