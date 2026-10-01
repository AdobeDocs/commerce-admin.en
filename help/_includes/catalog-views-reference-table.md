---
title: Catalog views reference table
description: Reused reference table for the Catalog Views grid
---
# Catalog views reference table

The grid lists one row for each catalog view created when a shared catalog is synchronized to [!DNL Adobe Commerce Optimizer]. The grid is read-only apart from the key-assignment action. Catalog views are created and removed automatically as the connector synchronizes shared catalogs configured in Adobe Commerce. If a catalog is removed, there is a [grace period](/help/systems/catalog-view-sync-status.md#configure-the-deletion-grace-period) before the corresponding catalog view and data are deleted.

To assign or unassign restricted access keys, see [Assign keys to a catalog view](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view).

| Field | Description |
| --- | --- |
| [!UICONTROL ACO Catalog View ID] | The identifier of the corresponding catalog view in [!DNL Adobe Commerce Optimizer]. See [Catalog View Sync Status summary](/help/systems/catalog-view-sync-status.md#catalog-view-sync-status-summary) to check its sync health. |
| [!UICONTROL Store View] | The store view that the catalog view represents. See [Store views](/help/stores-purchase/store-views.md). |
| [!UICONTROL Access Keys] | The titles of the restricted access keys currently assigned to the catalog view. See [Restricted Access Keys management](/help/systems/restricted-access-keys.md). |
| [!UICONTROL Actions] | Select **[!UICONTROL Edit Restricted Access Keys]** to assign or unassign keys for the catalog view. See [Assign keys to a catalog view](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view). |

{style="table-layout:auto"}
