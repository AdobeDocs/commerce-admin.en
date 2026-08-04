---
title: Monitor Data Feed Sync Status in Commerce
description: Track exports. Diagnose sync issues for [!DNL Catalog Service], [!DNL Live Search], [!DNL Product Recommendations], and [!DNL Adobe Commerce Optimizer Connector].
feature: Products, Customers, Data Import/Export
role: Admin
level: Beginner
exl-id: 4e1b9da0-450c-4488-8693-1938a948e792
TQID: https://experienceleague.adobe.com/Y8vYxKS-8iX-bCLSJpAiJOItWlJk348bSMWfk1Cgpbg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---

# Data Feed Sync Status monitoring

The [!UICONTROL Data Feed Sync Status] page lets Commerce administrators monitor export health for product and category data feeds in the Admin area.

## Audience and availability {#audience}

The Data Feed Sync Status page is available at no additional cost to Commerce merchants with an active license for one of the following services:

- [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)
- [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)
- [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview)
- [[!DNL Adobe Commerce Optimizer Connector]](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview)

The Data Feed Sync Status page is available automatically in supported Commerce service configurations. On Adobe Commerce on Cloud Infrastructure and on-premises deployments, if the page is missing after an eligible service or connector is enabled, follow the manual installation instructions below. Do not use the Composer installation procedure for product-managed SaaS experiences.

## Access the sync status page {#access-data-feed-sync-status-page}

From the Admin area, navigate to **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**.

![Data Feed Sync Status page summarizing data feed export activity](assets/data-feed-sync-status.png){width="600" zoomable="yes"}

>[!NOTE]
>
> This page reports export status only. A success status means data was exported successfully—it does not confirm that data is available in connected services. See [Confirm data in connected services](#confirm-data-in-connected-services) for details.

## Available export feeds

The list of available export feeds you can manage from the Data Sync Status page depend on which Commerce services are connected.

- **For [!DNL Adobe Commerce on Cloud, On Premises, and Commerce as a Cloud Service] with configured Commerce Services:** See [Supported Feeds](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/reference/feed-table-reference#supported-feeds) in the _SaaS Data Export Guide_.

- **For Adobe Commerce on Cloud or On-Premises deployments configured with the[!DNL Adobe Commerce Optimizer Connector]:** See [Supported feeds](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/reference/connector-reference#supported-feeds) in the _Adobe Commerce Optimizer Connector Guide_.


## Data Feed Sync Status summary {#data-feed-sync-status-summary}

The summary grid lists each feed and its export counts.

| Field | Description |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Feed Name** | Feed indexer for an entity or part of an entity (product, product price). |
| **Source Records** | Number of Commerce records that require synchronization. Can exceed the Admin grid count because feed items are scoped (for example, Store View code). |
| **Successfully Sent Records** | Number of feed items successfully submitted from Commerce to the configured service endpoint. This does not confirm downstream ingestion or catalog availability. If sync errors occurred, this number may be smaller than the number of source records. |
| **Failed Records** | Number of records that failed to be sent to connected Commerce services. |
| **Action** | Select **[!UICONTROL Details]** to view the sync activity for a feed. |

## Data Feed Sync Status details {#data-feed-sync-status-details}

From the summary page, select a feed name or select **[!UICONTROL Details]** to view export status for each feed item:

![Data Feed Sync Status details page with feed item status reporting](assets/data-feed-sync-status-details.png){width="600" zoomable="yes"}

| Field | Description |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Feed Item ID** | Autogenerated identifier used for system purposes |
| **Entity ID** | The unique identifier of the source entity (product ID, category ID, and so on) |
| **Feed Identifiers** | Unique identifiers for the feed item. For example, SKU and Store View code for the products feed. Values vary by feed. |
| **Export Status** | The [synchronization status](#export-status-types) of the feed item, with color-coded indicators |
| **Last Sync Date** | Date and time of the most recent export attempt or submission from Commerce. This timestamp does not confirm downstream availability. |
| **Is Entity Deleted?** | Indicates whether the entity has been deleted in Adobe Commerce. Deleted items are displayed only if sync failed. |
| **Request ID** | Unique ID for the sync request. Provide it to Support when troubleshooting entity updates. |
| **Error** | Detailed error information for synchronization failures |

You can manage the view using the following controls:

- [!UICONTROL Mass Action] to schedule resync for selected feed items
- [!UICONTROL Filters] and [!UICONTROL Columns]
- [!UICONTROL Default View] to create and save a filtered view, and switch between views

### Feed health indicators {#feed-health-indicators}

| **Indicator** | **Description** |
| ------------- | --------------- |
| Indexer status | <ul><li>**Ready**: The indexer is up to date. No reindex required.</li><li>**Reindex required**: Source data changed. Run a reindex to capture recent changes.</li><li>**Processing**: Indexing is in progress.</li></ul> |
| Changelog backlog | <ul><li>**All synced**: No pending changes to process.</li><li>**Items in backlog**: Number of pending changes waiting to be processed. A backlog of more than 1,000 items may indicate performance issues.</li></ul> |
| Indexer mode | <ul><li>**Schedule mode** (recommended): The indexer runs on schedule, which reduces the risk of data loss.</li><li>**Update on Save** (real time): Shown as a warning on the page. Real-time mode is not expected and increases the risk of data loss under load.</li></ul> |

>[!TIP]
>
> To learn more about index processing, see the [Index Management](index-management.md) topic.

### Export status types {#export-status-types}

| **Status** | **Description** | **Action required** |
| ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------ |
| **Submitted to service** | The feed item was successfully submitted from Commerce for downstream processing. | None |
| **Failed, will retry** | Failed to send, but the system will attempt to resend. | Monitor for resolution |
| **Failed, requires attention** | Failed due to application or data error. | Investigate and resolve the issue in the [!UICONTROL Error] column |
| **Awaiting submission** | Changes detected in the changelog but not yet processed. | Normal processing state |

## Monitor data feed status

When you update product- and category-related entities in the Commerce database, the data transfers to Commerce services according to your feed configuration. You can monitor export activity and its current status from the [!UICONTROL Data Feed Sync Status] summary page.

>[!IMPORTANT]
>
> The time it takes to complete data synchronization varies based on your catalog size, the volume of updated data, and external service performance.

When the successfully sent count matches the source count for a feed, and no items remain awaiting submission or failed, Commerce has completed export for that feed. Use the appropriate dashboard to [confirm downstream availability](#confirm-data-in-connected-services).

>[!NOTE]
>
> Adobe also provides command-line interface tools and system logs that developers and system integrators can use to manage and track sync operations. For details, see the [SaaS Data Export Guide](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview).

### Manage failed exports {#manage-failed-exports}

To review failed exports and schedule a resync:

1. From the summary page, find the feed with failed records.
1. Select **[!UICONTROL Details]**.
1. Review error messages in the [!UICONTROL Error] column.
1. Select the records to resync using the checkboxes.
1. From the [!UICONTROL Mass Action] menu, select **[!UICONTROL Schedule Resync]**, select **[!UICONTROL Submit]**, and confirm the operation.
1. Monitor status changes on the details page.

The system automatically retries certain failures.

#### When to resync manually {#resync-feed-items}

Manually resync in these cases:

- Authentication or permission errors (401 or 403 status codes) persist
- You fixed data format issues that caused payload errors
- External service configuration or endpoints changed
- Customizations affecting data export were deployed

### Confirm data in connected services {#confirm-data-in-connected-services}

To verify end-to-end synchronization after exports complete, use one of the following methods. For the limits of export status on this page, see the [note above](#export-status-scope).

- **[!DNL Adobe Commerce as a Cloud Service] with Commerce services:** Check the applicable [Data Management Dashboard](data-dashboard.md) to confirm downstream availability.
- **Adobe Commerce on Cloud or On-Premises with Adobe Commerce Optimizer Connector**: Check Commerce Admin export status first, then check the [Data Sync page](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync) in [!DNL Commerce Optimizer Studio]
- **[!DNL Adobe Commerce Optimizer] (stand-alone):**  Data is not exported from the Commerce backend. Use the [Data Sync page](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync) in [!DNL Commerce Optimizer Studio] to confirm data availability.

>[!TIP]
>
> To learn more about the data synchronization process, see [Synchronize data with SaaS data export](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/data-synchronization/data-sync-manage#view-and-manage-the-synchronization-process) in the *SaaS Data Export Guide*.

## Best practices {#best-practices}

- Review the summary page daily for feeds with high failure rates.
- Examine details weekly for critical feeds, such as products and prices.
- Track export success trends monthly to identify recurring issues.

## Troubleshoot common issues {#troubleshoot-common-issues}

| Issue | Symptoms | What to do |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| High failure rates | Many records show *Failed, require attention* status | <ul><li>Check external service status and configuration</li><li>Review error messages for patterns in the [!UICONTROL Error] column</li><li>After you resolve the underlying issue, see [Manage and resync failed exports](#manage-failed-exports)</li><li>Contact external service support if needed</li></ul> |
| Slow export performance | High changelog backlog or slow status updates | <ul><li>Check [feed health indicators](#feed-health-indicators) for indexer and backlog status</li><li>Rerun indexing if **Reindex required** is shown</li><li>Monitor external service response times</li><li>Schedule exports during off-peak hours when possible</li><li>Review system resources and performance</li></ul> |
| Authentication failures | 401 or 403 status codes in the [!UICONTROL Error] column | <ul><li>Verify API credentials and tokens</li><li>Check external service account permissions</li><li>Renew expired tokens or contact your service provider</li><li>After credentials are restored, [resync affected records](#manage-failed-exports)</li></ul> |
| Missing Data Feed Sync Status page | **[!UICONTROL Data Feed Sync Status]** is not listed under **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** after you enable a connected service | <ul><li>For Commerce as a Cloud Service, confirm an eligible service is enabled (see [Audience and availability](#audience))</li><li>For Commerce on Cloud or On Premises only, [Install the extension manually](#install-the-extension)</li></ul> |

Adobe Commerce on Cloud Infrastructure or on-premises: confirm that an eligible service or the Adobe Commerce Optimizer Connector is enabled; if the page is still missing, follow the manual installation instructions.
ACCS or Adobe Commerce Optimizer: do not install the module manually; use the product-managed synchronization experience or contact the appropriate service support team.

## Install the extension {#install-the-extension}

Manual installation is required for Adobe Commerce on Cloud or on-premises deployments only if the [!UICONTROL Data Feed Sync Status] page is missing from the Admin area after you enable an eligible service. See [Audience and availability](#audience).

### Prerequisites

- Adobe Commerce 2.4.4+. For detailed requirements, see [System requirements](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/system-requirements).
- [Adobe Commerce Data Export Extension](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/reference/manage-extension), version 103.4.15 or later
- Authentication keys with permission to download the required package from the Adobe Commerce repository. To create authentication keys and obtain the necessary package access, see [Get your authentication keys](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). For Cloud installations, see the [Commerce on Cloud Infrastructure Guide](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/authentication-keys).
- Access to the command line of the Adobe Commerce application server.

### Installation steps

Add the `magento/module-data-exporter-status` module using Composer:

```shell
composer require magento/module-data-exporter-status
```

For detailed installation steps, see the following guides:

- [Install extension for Adobe Commerce on Cloud Infrastructure](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure-store/extensions)
- [Install extension on Adobe Commerce on-premises](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/tutorials/extensions)

>[!MORELIKETHIS]
>
> - [Data Management Dashboard](data-dashboard.md)
> - [SaaS Data Export Guide](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview)
