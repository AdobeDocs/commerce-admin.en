---
title: Data Feed Status Monitoring
description: Monitor data export synchronization and identify any issues or delays with feed processing for [!DNL Catalog Service], [!DNL Live Search], and [!DNL Product Recommendations].
feature: Products, Customers, Data Import/Export
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
---

# Data Feed Status Monitoring

<!--Initial support for the Data Feed Status module is available only for Adobe Commerce PaaS or on-premises deployments--> 

Adobe Commerce administrators can monitor the synchronization status of product, category, pricing, and other data export feeds from the Data Feed Status page in the Commerce Admin. 
This page provides key insights and tools to help administrators:

* **View the synchronization status** for all data feeds
* **Identify and troubleshoot errors** in feed processing
* **Access detailed status information** for individual feed items

<!--TO DO: List what feeds are included in tracking data-->

## Availability

<!--TO DO: Check service versions where data feed status monitoring is supported-->

The Data Feed Status page is available at no additional cost to all Commerce merchants using [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview), [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/en/docs/commerce/live-search/guide-overview), or [[!DNL Catalog Service v1.17+]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview) with an active license.

From the Commerce Admin, access the Data Feed Status page at **[!DNL System]** > Data Transfer  > **[!DNL Data feed status]**.

<!--TO DO: Insert updated screen capture-->

![Data Feed Status Overview](data-feed-status-dashboard.png)

Data Feed Status monitoring provides two interfaces, an overview page that lists the available feeds and current state, and a detail page that shows detailed information about a selected feed.

### Installation

<!--TO DO: Add installation instructions for customers to install the Data Exporter Status extension (name?)-->

1. Install module independently?
1. Upgrade to a particular version of LS, CS, or PREX?

## Feed Status summary page

The main status page displays a summary of all active data feeds:

<!--To Do: Verify field names on overview page-->

| Field | Description |
|-------|-------------|
| **Feed Name** | The type of data feed (for example, products, product variants, and so on) |
| **Source Records Qty** | Total number of records available for export from the Commerce database |
| **Feed Records Qty** | Total number of records processed for export in the feed |
| **Successfully Sent Records Qty** | Number of records successfully transmitted to external services |
| **Failed Records Qty** | Number of records that failed to export and require attention |
| **Action** | Available actions for each feed (View Details, Resync) |

## Feed status detail page

From the Feed Status summary page, click a feed name or use the [!DNL View Details] action to access detailed information about individual records within a feed.

<!--TO DO: Insert updated screen capture-->

![Data Feed Status Details](data-feed-status-dashboard.png)

The detail view provides a table with the following columns:

<!--To Do: Verify files names in the detail view-->

| Field | Description |
|-------|-------------|
| **Feed Item ID** | Internal identifier for the feed record |
| **Feed Identifiers** | The unique identifier of the entity, such as Product ID or Category ID.|
| **Entity ID** | The source entity ID (product ID, category ID, and so on) |
| **Export Status** | The [synchronization status](#export-status-types) of the feed item. Current status of the export attempt with color-coded indicators |
| **Last Sync Date** | Timestamp when the record was last sent to Commerce Services |
| **Is entity deleted?** | Indicates whether the entity or its part (for example, product or product price) has been deleted in Adobe Commerce. Deleted
items are displayed only if an error occurred during synchronization. |
| **Error** | Detailed error information if the feed item failed to synchronize. |
| **Request ID** | A unique identifier for the synchronization request. Provide this ID to Support when troubleshooting updates for specific entities. |

<!--Validate the content below. Not sure it is implemented or applicable for initial release of the Data Feed Status extension-->

## Feed health indicators

At the top of each feed detail page, critical health indicators provide system status:

### Indexer status

* **Valid**: Indexer is up-to-date and functioning normally
* **Invalid**: Indexer needs to be rerun to capture recent changes.
* **Processing**: Indexer is currently running

### Changelog backlog

* **All synced**: No pending changes to process
* **Items in backlog**: Number of pending changes waiting to be processed
* **High backlog warning**: More than 1,000 items indicates potential performance issues

### Indexer mode

* **Schedule mode** (Recommended): Indexer runs on schedule, reducing risk of data loss
* **Realtime mode** (Warning): Immediate processing but higher risk of data loss under load

## Export status types

The system uses color-coded status indicators to help you quickly identify issues:

### Status categories

| **Status** | **Description** | **Action required** |
|--------|-----------|-------------|-----------------|
| **Submitted to service** | Feed item successfully exported to Commerce service | None |
| **Failed, will retry** | Temporary failure, system will automatically retry | Monitor for resolution |
| **Failed, requires attention** | Failed dut to application or data error. | Investigate and resolve issue in the [!DNL Error] column|
| **Awaiting submission** | Queued for export but not yet processed | Normal processing state |

### Detailed status codes

| Code | Status Label | Description |
|------|--------------|-------------|
| 200 | Submitted to service | Export completed successfully |
| 400 | Data payload error | Invalid data format or content |
| 401 | Unauthorized request | Authentication failure with Commerce service |
| 403 | Permission denied | Access denied by Commerce service |
| 429 | Too many requests | Rate limiting applied by Commerce service |
| 500 | Internal Server Error | External service error |
| 503 | Service Unavailable | External service temporarily unavailable |
| 0 | Application error | Internal Commerce application error |
| 1 | Client error | Partial success with some failed items |
| 2 | Not accepted | Retryable error condition |

## Monitor data feed status

When you update products, categories, or other entities in the Commerce database, the data transfers to Commerce services according to your feed configuration. The Data Feed Status dashboard allows you to monitor this process in real-time.

>[!IMPORTANT]
>
>The time it takes to complete data synchronization varies based on your catalog size, the volume of updated data, and external service performance.

When the number of successfully sent records matches the number of source records, it indicates that the sync is complete and all data has been transmitted successfully.

>[!NOTE]
>
>Adobe also provides command-line interface tools and system logs that developers and system integrators can use to manage and track sync operations. For details, see the [SaaS Data Export Guide](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### Managing failed exports

To see the details of failed exports and take corrective action:

1. Navigate to the feed with failed records.
1. Click **[!DNL View Details]** to see individual record status.
1. Review error messages for specific failure reasons.
1. Use mass actions to schedule resync for failed items.

![Feed Detail View](feed-detail-view.png)

### Resync failed data

To ensure that your external services receive the most current information, you can manually resync failed or problematic data feeds.

While the system automatically retries certain types of failures, manual intervention may be necessary in the following scenarios:

* When you notice authentication or permission errors (401, 403 status codes)
* After resolving data format issues that caused payload errors
* Following updates to external service configurations or endpoints
* When deploying customizations that impact data export processes

By proactively monitoring feed status and addressing failures promptly, you can maintain data consistency and reliability across your Commerce ecosystem.

#### Manually resync feed items

If you need to resync specific feed items:

1. **Select Records**: Use checkboxes to select failed records that need attention
2. **Choose Action**: Select **[!DNL Schedule Resync]** from the mass action dropdown
3. **Confirm**: Click **[!DNL Submit]** and confirm the resync operation
4. **Monitor Results**: Check the success message and monitor status changes

<!--TO DO: Is this feature supported by the DataExporterStatus module in initial release. Update or remove screen capture as needed.-->

![Manual Resync Dialog](manual-resync-dialog.png)

**Resync options:**

* **Selected Items**: Reschedule only the items you have selected
* **Full Feed Resync**: When no items are selected, this option triggers a complete feed resync

## Best practices

### Regular monitoring

1. **Daily Checks**: Review the overview page daily for any feeds showing high failure rates
1. **Weekly Deep Dive**: Examine detailed status for critical feeds (products, prices)
1. **Monthly Analysis**: Track trends in export success rates and performance

### Troubleshooting workflow

1. **Identify Issues**: Look for red status indicators and high failure counts
1. **Check Indexer Health**: Ensure indexers are valid and backlog is manageable
1. **Review Error Details**: Click on failed records to see specific error messages
1. **Schedule Resync**: Use mass actions to retry failed exports
1. **Monitor Resolution**: Verify that resynced items show successful status

### Performance optimization

* **Maintain Schedule Mode**: Keep indexers in schedule mode for optimal performance
* **Monitor Backlog**: Address high changelog backlogs promptly
* **Batch Operations**: Use mass actions for efficient bulk resync operations

## Troubleshooting common issues

### High failure rates

**Symptoms**: Large number of records showing "Failed, require attention" status

**Potential causes**:

* External service configuration changes
* Data format incompatibilities
* Authentication or permission issues

**Resolution steps**:

1. Check external service status and configuration
1. Review error messages for patterns
1. Verify authentication credentials
1. Contact external service support if needed

### Slow export performance

**Symptoms**: High changelog backlog, slow status updates

**Potential Causes**:

* Indexer performance issues
* High data volume
* External service rate limiting

**Resolution Steps**:

1. Check indexer status and rerun if invalid
2. Monitor external service response times
3. Consider scheduling exports during off-peak hours
4. Review system resources and performance

### Authentication Failures

**Symptoms**: 401 or 403 status codes

**Resolution Steps**:

1. Verify API credentials and tokens
1. Check external service account permissions
1. Renew expired authentication tokens
1. Contact service provider for access issues

>[!MORELIKETHIS]
>
>* [Data Management Dashboard](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/data-transfer/data-dashboard)
>* [SaaS Data Export Guide](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview)
