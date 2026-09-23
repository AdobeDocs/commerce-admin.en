---
title: Catalog View Sync Status Monitoring
description: Monitor B2B shared catalog projection health and reconcile catalog views, policies, price books, and access keys for the Adobe Commerce Optimizer Connector.
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---

# Catalog view sync status monitoring

[!BADGE Private Beta]{type=Caution tooltip="Requires the Adobe Commerce Optimizer Connector for B2B extension, which is currently in private beta."}

Commerce administrators use the [!UICONTROL Catalog View Sync Status] page to monitor and repair shared catalog projections to [!DNL Adobe Commerce Optimizer]. [!DNL Adobe Commerce Optimizer Connector for B2B] creates a projection. For each store view within the shared catalog's website scope, the connector creates an [!DNL Adobe Commerce Optimizer] catalog view and synchronizes its associated product assortment policy, price book reference, and restricted access key configuration.

Use the [!UICONTROL Catalog View Sync Status] page to troubleshoot a company seeing the wrong assortment, pricing, or catalog access.

>[!NOTE]
>
>To track the synchronization status for catalog data feeds, use the [[!UICONTROL Data Feed Sync Status]](data-feed-sync-status.md) page.

## Audience and availability {#audience}

[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud Infrastructure and on-premises projects only."}

The [!UICONTROL Catalog View Sync Status] page is available to Adobe Commerce on Cloud Infrastructure and on-premises merchants who use B2B shared catalogs with the [!DNL Adobe Commerce Optimizer Connector for B2B] integration. The page is installed and enabled automatically when the connector extension is installed.

## Access the Catalog View Sync Status page {#access-catalog-view-sync-status-page}

From the Admin area, navigate to **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Catalog View Sync Status]**.

![Catalog View Sync Status page listing catalog views with their sync health](assets/catalog-view-sync-status.png){width="600" zoomable="yes"}

The page has three tabs:

- **[!UICONTROL Catalog Views]**—Catalog views created by the connector, with sync health for each. See [Catalog View Sync Status summary](#catalog-view-sync-status-summary).
- **[!UICONTROL Orphaned in ACO]**—Entities that exist in [!DNL Adobe Commerce Optimizer] with no corresponding [!DNL Adobe Commerce] source. See [Orphaned in ACO tab](#orphaned-in-aco-tab).
- **[!UICONTROL Deleted]**—A record of catalog view projections removed because their shared catalog was deleted. See [Deleted tab](#deleted-tab).

## Catalog View Sync Status summary {#catalog-view-sync-status-summary}

Summary cards at the top of the page show the number of catalog views in each health state, plus a count of restricted access keys expiring within 30 days:

| Card | Description |
| --- | --- |
| **Healthy** | Catalog views with no detected drift. |
| **Degraded** | Catalog views with repairable drift. |
| **Failed** | Catalog views that were never created, or were deleted directly in [!DNL Adobe Commerce Optimizer]. |
| **Keys ≤ 30D** | Restricted access keys expiring within 30 days. |

The grid lists one row per catalog view:

| Field | Description |
| --- | --- |
| **Catalog View** | The identifier of the catalog view projected into [!DNL Adobe Commerce Optimizer]. |
| **Source** | The shared catalog the catalog view was projected from. Select the link to open the shared catalog in the Admin. |
| **Store View** | The store view the catalog view represents. |
| **Companies** | The number of companies currently linked to this catalog view. |
| **Status** | The catalog view's overall sync health. See [Sync status values](#sync-status-values). |
| **Policy** | Whether the assortment policy assigned to this catalog view matches your [!DNL Adobe Commerce] configuration. |
| **Price Book** | Whether the price book assigned to this catalog view matches your [!DNL Adobe Commerce] configuration. |
| **Access Key** | Whether a restricted access key is linked to this catalog view. |
| **Key Expires** | The expiration date of the catalog view's restricted access key, and the number of days remaining. |
| **Drift** | The type of drift detected, if any. |
| **Last Reconciled** | When the reconciliation process last checked this catalog view. |
| **Action** | Row-level actions. See [Reconcile and repair drift](#reconcile-and-repair-drift). |

## Sync status values {#sync-status-values}

| Status | Meaning |
| --- | --- |
| **Healthy** | No drift detected. The catalog view, policy, price book, and keys match your [!DNL Adobe Commerce] configuration. |
| **Degraded** | Drift was detected and is repairable—for example, a policy or price book was changed directly in [!DNL Adobe Commerce Optimizer]. |
| **Failed** | The catalog view was never created, or was deleted directly in [!DNL Adobe Commerce Optimizer]. |
| **Pending** | The catalog view has not been reconciled yet, or is waiting on its first projection. |
| **Retiring** | The shared catalog was deleted in [!DNL Adobe Commerce], and the catalog view is inside its deletion grace period. |
| **Deleted** | The catalog view projection was removed after its grace period. It is kept as a record on the [!UICONTROL Deleted] tab for 90 days. |
| **Orphaned** | The catalog view or key exists in [!DNL Adobe Commerce Optimizer] but has no corresponding [!DNL Adobe Commerce] source. See [Orphaned in ACO tab](#orphaned-in-aco-tab). |

### Configure the deletion grace period {#configure-the-deletion-grace-period}

The deletion grace period specifies the data retention window for catalog views and associated data after the associated shared catalog is deleted. The value defaults to 7 days.
After the window expires, all data is removed.

#### Change the data retention setting

1. Open the [!DNL Adobe Commerce] Admin.

1. From the  **[!UICONTROL Stores]** menu, select  **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Catalog View Sync]** > **[!UICONTROL Deletion]** > **[!UICONTROL Deletion Grace Period (days)]**.

1. Update the **[!UICONTROL Deletion Grace Period (days)]** value as needed.

   To remove a catalog view ACO projection immediately after deleting a shared catalog, set this value to `0`.

1. Select **[!UICONTROL Save Config]**.


For details, see [Services > ACO Catalog View Sync](../configuration-reference/services/aco-catalog-view-sync.md) for all available sync and drift reconciler settings.


## Reconcile and repair configuration differences {#reconcile-and-repair-drift}

[!DNL Adobe Commerce] is the authoritative source for B2B shared catalog projection. Reconciliation compares your [!DNL Adobe Commerce] configuration against [!DNL Adobe Commerce Optimizer] and reports or repairs any differences.

>[!IMPORTANT]
>
>Changes made directly in [!DNL Adobe Commerce Optimizer] to a connector-managed catalog view, policy, price book, or key are not the primary source of truth. Reconciliation reports these as configuration differences and, when you repair, reverts them to match [!DNL Adobe Commerce]. Make configuration changes in [!DNL Adobe Commerce], not in [!DNL Adobe Commerce Optimizer]. Repair does not remove policies you added manually alongside the connector-managed one.

Use the page-level buttons to reconcile:

- **[!UICONTROL Reconcile]**—Checks for configuration differences and updates the sync status without making any changes in [!DNL Adobe Commerce Optimizer].
- **[!UICONTROL Reconcile & Repair]**—Checks for configuration differences and automatically restores the expected configuration for any repairable differences.

  A successful repair updates the grid immediately, so you can confirm the fix without waiting for the next scheduled reconcile.

Use the **[!UICONTROL Action]** menu on a row to:

- **[!UICONTROL View details]**—Open the catalog view detail page, including its history of configuration differences and linked companies.
- **[!UICONTROL Open in ACO admin]**—Open the catalog view directly in [!DNL Adobe Commerce Optimizer] Studio.
- **[!UICONTROL Copy ID]**—Copy the catalog view's identifier.

## Orphaned in ACO tab {#orphaned-in-aco-tab}

The **[!UICONTROL Orphaned in ACO]** tab lists catalog views and restricted access keys that exist in [!DNL Adobe Commerce Optimizer] but have no corresponding [!DNL Adobe Commerce] source—for example, entities created manually in [!DNL Adobe Commerce Optimizer] Studio rather than by the connector. These entities cannot appear in the main grid because there is no [!DNL Adobe Commerce] record to match them against.

![Orphaned in ACO tab listing entities with no Adobe Commerce source](assets/catalog-view-sync-orphan.png){width="600" zoomable="yes"}

| Field | Description |
| --- | --- |
| **Type** | The category of the orphaned entity: [!UICONTROL Catalog View] or [!UICONTROL Access Key]. |
| **ACO ID** | The identifier of the entity in [!DNL Adobe Commerce Optimizer]. |
| **Detail** | Additional context about the entity, such as its policy. |
| **First Seen** | When reconciliation first detected this entity. |
| **Action** | Select **[!UICONTROL Copy ID]** to copy the entity identifier. Use the copied ID to locate and remove the entity from [!DNL Adobe Commerce Optimizer] Studio catalog views. |

>[!NOTE]
>
>This tab is report-only. Reconciliation never deletes orphaned entities. Remove them directly in [!DNL Adobe Commerce Optimizer] Studio if they are no longer needed.

## Deleted tab {#deleted-tab}

The **[!UICONTROL Deleted]** tab lists catalog view projections that were removed because their shared catalog was deleted in [!DNL Adobe Commerce]. Because the shared catalog and its catalog view no longer exist, these rows do not link anywhere. They are kept only as a record of what was removed.

![Deleted tab listing catalog view projections removed after their shared catalog was deleted](assets/catalog-view-sync-deleted.png){width="600" zoomable="yes"}

| Field | Description |
| --- | --- |
| **Catalog View** | The identifier of the removed catalog view. |
| **Source** | The shared catalog that was deleted. |
| **Store View** | The store view the catalog view represented. |
| **Deleted At** | When the projection was removed. |

Rows on this tab are cleared automatically after 90 days.

## Known limitations

- There is no visual indicator in [!DNL Adobe Commerce Optimizer] Studio that distinguishes connector-managed catalog views from manually created ones. Use this page, not the [!DNL Adobe Commerce Optimizer] Studio UI, to determine what the connector manages.
- The **[!UICONTROL Orphaned in ACO]** tab's **[!UICONTROL ACO ID]** column identifies a catalog view or key, not a unique identifier. Column naming is subject to change.
- Deep links from this page directly to the corresponding record in [!DNL Adobe Commerce Optimizer] Studio are not available yet, except through **[!UICONTROL Open in ACO admin]** on the [!UICONTROL Catalog Views] tab.

>[!MORELIKETHIS]
>
> - [Manage catalog view configuration](/help/b2b/catalog-views-manage.md) — Review catalog views from the shared catalog or company account
> - [Data Feed Sync Status](data-feed-sync-status.md)
> - [Services > ACO Catalog View Sync](../configuration-reference/services/aco-catalog-view-sync.md) — Configure the deletion and creation grace periods and the drift reconciler
> - [Restricted Access Keys management](restricted-access-keys.md) — Manage the keys whose expiration this page surfaces
> - [Monitor catalog view synchronization for B2B shared catalogs](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/catalog-view-sync-status) in the *Adobe Commerce Optimizer Connector Guide*
> - [Private catalog views](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/private-catalog-view)
> - [Restricted access keys](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys)
