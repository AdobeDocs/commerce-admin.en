---
title: Data Feed Sync Status Monitoring
description: Monitor data export synchronization and identify any issues or delays with feed processing for [!DNL Catalog Service], [!DNL Live Search], and [!DNL Product Recommendations].
feature: Products, Customers, Data Import/Export
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
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
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Data Feed Sync Status Monitoring

Adobe Commerce administrators can monitor the synchronization status of data exported from Adobe Commerce to connected Commerce services using the Data Feed Sync Status page in the Commerce Admin.

![Data Feed Sync Status detail page with feed item status reporting](assets/data-feed-sync-status.png)

This page provides real-time insights into the health and performance of data export feeds that transfer product and category data from Commerce to external services such as [!DNL Product Recommendations], [!DNL Live Search], and [!DNL Catalog Service].

The sync status page shows only the export status. A success status indicates that the data is successfully exported and will eventually be available in connected Commerce services.

Monitoring feed status helps ensure data consistency and enables prompt resolution of any issues that arise during the export process. Administrators can:

* **View the synchronization status** for all data feeds
* **Identify and troubleshoot errors** in feed processing
* **Access detailed status information** for individual feed items

Status is tracked for the following feeds:

* Products Feed
* Product Attributes Feed
* Categories Feed
* Product Overrides Feed
* Product Prices Feed
* Product Variants Feed

## Verify data successfully synchronized to Commerce Services

Use the following methods to verify that data has successfully synchronized with connected Commerce services:

* For Adobe Commerce on cloud or on premises, or Adobe Commerce as a Cloud Service deployments, check the [Data management dashboard](data-dashboard.md).
* For Adobe Commerce on cloud or on premises deployments configured with the [Adobe Commerce Optimizer Connector](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview), check the [Data Sync page](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/data-sync) in Commerce Optimizer Studio.

>[!TIP]
>
>To learn more about the data synchronization process, see [Synchronize data with SaaS data export](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/data-synchronization)in the *SaaS Data Export Guide*.

## Install the extension

The Data Feed Status page is available to all Commerce merchants with active licenses for the following Commerce services:

* [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview)
* [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/en/docs/commerce/live-search/guide-overview)
* [[!DNL Catalog Service v1.17+]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview) with an active license

>[!NOTE]
>
>You do not need to install the Data Feed Status extension on [[!DNL Adobe Commerce as a Cloud Service]](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/overview) instances.
>The extension is available by default if at least one of the following services is enabled in the Commerce deployment:  Product Recommendations v6+, Live Search v4.1+, or Catalog Service v1.17+.

**Requirements**

* PHP 8.1, 8.2, 8.3, or 8.4
* Adobe Commerce 2.4.4+
* [Adobe Commerce Data Export Extension](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/manage-extension), version 103.4.15 or later
* Access to [repo.magento.com](https://repo.magento.com)

  To generate keys and obtain the necessary rights, see [Get your authentication keys](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). For cloud installations, see the [Commerce on Cloud Infrastructure Guide](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/develop/authentication-keys).

* Access to the command line of the Adobe Commerce application server.

### Installation steps

Add the `magento/module-data-exporter-status` module using Composer:

```shell
composer require magento/module-data-exporter-status
```

For detailed installation steps, see the following guides:

* [Install extension on Adobe Commerce on Cloud Infrastructure](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/configure-store/extensions)

* [Install extension Adobe Commerce on-premises](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/tutorials/extensions)

## Access the Data Feed Status page

From the Commerce Admin, Access the Data Feed Status page from the Commerce Admin at **[!DNL System]** > Data Transfer > **[!DNL Data Feed Sync Status]**.

![Data Feed Sync Status page summarizing data feed export activity](assets/data-feed-sync-status.png)

Data Feed Status monitoring provides two interfaces:

* The [Data Feed Sync Status summary page](#data-feed-sync-status-summary) that lists the available feeds and current state
* The [Data Feed Sync Status - Details page](#data-feed-sync-status-details) that shows detailed information about a selected feed.

## Data Feed Sync Status summary

The Feed Sync Status summary page provides information about data feed export activity including the following information:

| Field | Description |
|-------|-------------|
| **Feed Name** | The name of the feed indexer responsible for synchronizing a specific entity or its part, for example product or product price.|
| **Source Records** | Number of records available for export from the Commerce database. This number can be larger than the number of records displayed in the Commerce Admin as each feed item belongs to a specific scope, such as Store View code.|
| **Successfully Sent Records** | Number of records successfully transmitted to Commerce SaaS for further processing. If errors occurred during transmission, the number of records successfully transmitted to external services. |
| **Failed Records** | Number of records that failed to export and require attention. |
| **Action** | Select **[!UICONTROL Details]** to view the sync activity for a feed.|

## Data Feed Sync Status Details

From the Data Feed Status summary page, click a feed name or use the [!DNL View Details] action to access detailed information about individual records within a feed.

![[!UICONTROL Data Feed Sync Status - Details] page with feed item status reporting](assets/data-feed-sync-status-details.png)

The detail view provides the following information for each feed item:

| Field | Description |
|-------|-------------|
| **Feed Item ID** | Internal identifier for the feed record |
| **Entity ID** | The source entity ID (product ID, category ID, and so on) |
| **Export Status** | The [synchronization status](#export-status-types) of the feed item. Current status of the export attempt with color-coded indicators |
| **Last Sync Date** | Timestamp when the record was last sent to Commerce Services |
| **Is entity deleted?** | Indicates whether the entity or its part (product or product price for example) has been deleted in Adobe Commerce. Items are displayed only if an error occurred during synchronization. |
| **Request ID** | A unique identifier for the synchronization request. Provide this ID to Support when troubleshooting specific entity updates. |
| **Error** | Detailed error information if the feed item failed to synchronize. |

You can manage the view using the following controls:

* [!DNL Mass Action] to schedule resync for selected feed items
* [!DNL Filters]
* [!DNL Default View] to create and save a filtered view, and switch between views
* [!DNL Columns] to show and hide columns in the table.

### Feed health indicators

At the top of each feed detail page, critical health indicators provide system status for each feed:

#### Indexer status

* **Valid**: Data is synchronized; no reindex required.
* **Invalid**: Original data was changed; the index should be updated.
* **Processing**: Indexing in progress.

>[!TIP]
>
>To learn more about index processing, see the [Index Management](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/index-management) topic.

#### Changelog backlog

* **All synced**: No pending changes to process
* **Items in backlog**: Number of pending changes waiting to be processed

### Export status types

The system provides status indicators to help you quickly identify issues:

#### Status categories

| **Status** | **Description** | **Action required** |
|--------|-----------|-------------|
| **Submitted to service** | Feed item successfully exported to Commerce service. | None |
| **Failed, will retry** | Temporary failure. The system will automatically retry. | Monitor for resolution |
| **Failed, requires attention** | Failed due to application or data error. | Investigate and resolve the issue in the [!DNL Error] column|
| **Awaiting submission** | Queued for export but not yet processed. | Normal processing state |

## Monitor data feed status

When you update product and category related entities in the Commerce database, the data transfers to Commerce services according to your feed configuration. You can monitor this process in real time from the Data Feed Sync Status summary page.

>[!IMPORTANT]
>
>The time it takes to complete data synchronization varies based on your catalog size, the volume of updated data, and external service performance.

When the number of successfully sent records matches the number of source records, it indicates that the sync is complete and all data has been transmitted successfully.

>[!NOTE]
>
>Adobe also provides command-line interface tools and system logs that developers and system integrators can use to manage and track sync operations. For details, see the [SaaS Data Export Guide](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### Managing failed exports

To see the details of failed exports and take corrective action:

1. From the Feed Sync Status page, find the feed with failed records.
1. Click **[!DNL Details]**.

1. Review error messages for specific failure reasons.

1. Use mass actions to schedule resync operations for failed items.

### Resync failed data

You can manually resync failed or problematic data feeds by using the [!DNL Actions] menu on the [!DNL Data Feed Sync Status - Details] page.

While the system automatically retries certain types of failures, manual intervention may be necessary in the following scenarios:

* You notice authentication or permission errors (401, 403 status codes).
* After resolving data format issues that caused payload errors.
* Following updates to external service configurations or endpoints.
* You are deploying customizations that impact data export processes.

By proactively monitoring feed status and addressing failures promptly, you can maintain data consistency and reliability across your Commerce ecosystem.

#### Manually resync feed items

If you need to resync specific feed items:

1. **Select Records**: Use checkboxes to select failed records that need attention.
2. **Choose Action**: Select **[!DNL Schedule Resync]** from the mass action dropdown.
3. **Confirm**: Click **[!DNL Submit]** and confirm the resync operation.
4. **Monitor Results**: Check the success message and monitor status changes.

## Best practices

### Regular monitoring

1. **Daily Checks**: Review the overview page daily for any feeds showing high failure rates
1. **Weekly Deep Dive**: Examine the detailed status for critical feeds (products, prices)
1. **Monthly Analysis**: Track trends in export success rates and performance

### Troubleshooting workflow

1. **Identify Issues**: Look for errors and high failure counts
1. **Check Indexer Health**: Ensure that indexers are valid and backlog is manageable
1. **Review Error Details**: Click on failed records to see specific error messages
1. **Schedule Resync**: Use mass actions to retry failed exports
1. **Monitor Resolution**: Verify that resynchronized items show successful status

### Fix common issues

#### High failure rates

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

#### Slow export performance

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

#### Authentication Failures

**Symptoms**: 401 or 403 status codes

**Resolution Steps**:

1. Verify API credentials and tokens
1. Check external service account permissions
1. Renew expired authentication tokens
1. Contact your service provider for access issues

>[!MORELIKETHIS]
>
>* [Data Management Dashboard](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/data-transfer/data-sync/data-dashboard)
>* [SaaS Data Export Guide](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview)
