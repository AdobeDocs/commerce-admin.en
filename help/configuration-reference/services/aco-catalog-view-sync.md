---
title: "[!UICONTROL Services] &gt; ACO Catalog View Sync"
description: Review the configuration settings on the [!UICONTROL Services] &gt; [!UICONTROL ACO Catalog View Sync] page of the Commerce Admin.
feature: Configuration, Security
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync]

[!BADGE Private Beta]{type=Caution tooltip="Requires the Adobe Commerce Optimizer Connector for B2B extension, which is currently in private beta."}

Use these settings to control how the [!DNL Adobe Commerce Optimizer Connector for B2B] synchronizes B2B shared catalog configurations—catalog view, policy, price book, and key—into [!DNL Adobe Commerce Optimizer] and how it resolves configuration differences between the two systems. See [Catalog View Sync Status monitoring](../../systems/catalog-view-sync-status.md) to monitor the results of these settings.

{{config}}

## [!UICONTROL Deletion]

![Deletion](./assets/aco-catalog-view-sync-configuration.png)<!-- zoom -->

| Field | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| --- | --- | --- |
| [!UICONTROL Deletion Grace Period (days)] | Global | Retention period for shared catalog data. Specifies the number of days a deleted shared catalog's catalog views, policies, and metadata are retained before being hard-deleted, allowing rollback. Set to `0` to hard-delete immediately. |

{style="table-layout:auto"}

## [!UICONTROL Creation]

| Field | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| --- | --- | --- |
| [!UICONTROL Creation Grace Period (days)] | Global | Number of days a newly registered catalog view can wait for the [!DNL Adobe Commerce Optimizer Connector for B2B] to complete its first synchronization of the catalog view, policy, price book, and key configurations, while its status is reported as [!UICONTROL Pending]. If the grace period lapses without a successful synchronization, the status changes to [!UICONTROL Failed]. Default value: `1` |

{style="table-layout:auto"}

## [!UICONTROL Drift Reconciler]

| Field | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| --- | --- | --- |
| [!UICONTROL Enabled] | Global | Runs the scheduled drift reconciler to detect and report differences between the catalog view projected from [!DNL Adobe Commerce] and the catalog view configuration in [!DNL Adobe Commerce Optimizer]. If `automatically repair drift` is enabled, it will also attempt to fix any repairable discrepancies. |
| [!UICONTROL Automatically Repair Drift] | Global | When set to `Yes`, the scheduled drift reconciler updates the [!DNL Adobe Commerce Optimizer] configuration to match the [!DNL Adobe Commerce] and re-synchronizes the configuration. When set to `No`, the run only detects and reports drift. Orphaned [!DNL Adobe Commerce Optimizer] entities are always reported, never automatically removed. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [ACO Catalog View](./aco-catalog-view.md) — Configure access tokens for storefront reads of a catalog view
> - [Catalog View Sync Status monitoring](../../systems/catalog-view-sync-status.md) — Monitor sync health and reconcile drift using these settings
> - [Restricted Access Keys management](../../systems/restricted-access-keys.md) — Manage the access keys assigned to synchronized catalog views
