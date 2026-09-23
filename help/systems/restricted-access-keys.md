---
title: Manage Restricted Access Keys in Commerce
description: Create, assign, and delete the restricted access keys that secure B2B shared catalog views synchronized to Adobe Commerce Optimizer.
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
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---

# Manage restricted access keys

[!BADGE Private Beta]{type=Caution tooltip="Requires the Adobe Commerce Optimizer Connector for B2B extension, which is currently in private beta."}

Use the Restricted Access Keys page to manage access keys for private catalog views created by the [!DNL Adobe Commerce Optimizer Connector for B2B]. The connector synchronizes B2B shared catalog configurations from Adobe Commerce to Adobe Commerce Optimizer.

>[!NOTE]
>
>For manually created keys used to manage private catalogs in non-B2B scenarios, such as partner portals, manage keys from [[!DNL Adobe Commerce Optimizer Studio]](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"}.

## Audience and availability {#audience}

[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud Infrastructure and on-premises projects only."}

The [!UICONTROL Restricted Access Keys] page is available to Adobe Commerce on Cloud Infrastructure and on-premises merchants who use B2B shared catalogs with the [!DNL Adobe Commerce Optimizer Connector for B2B]. The connector installs and enables the page automatically.

When a catalog view is first created for a shared catalog, the connector automatically generates and assigns one key. Use this page to view that key, and to create, assign, or delete additional keys.

## Access the Restricted Access Keys page {#access-restricted-access-keys-page}

From the Admin area, navigate to **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Restricted Access Keys]**.

![Restricted Access Keys page listing keys and their assigned catalog views](assets/restricted-access-keys.png){width="600" zoomable="yes"}

This page lists every key regardless of whether it's assigned to a catalog view. To assign a key to a specific catalog view, use the [!UICONTROL Edit Restricted Access Keys] action on that catalog view instead. See [Assign keys to a catalog view](#assign-keys-to-a-catalog-view).

## Restricted Access Keys summary {#restricted-access-keys-summary}

The grid contains one key per row.

| Field | Description |
| --- | --- |
| **Key ID** | The unique key identifier. |
| **Title** | A label you provide to identify the key. |
| **Assigned Catalog Views** | The catalog views this key is currently assigned to. |
| **Expires At** | The key expiration date. |
| **Actions** | Row-level actions. See [Manage keys](#manage-keys). |

## Manage keys {#manage-keys}

- **[!UICONTROL Create Key]**—Generates a new, unassigned key pair. Commerce generates the key pair and stores the private key. The public key isn't registered with [!DNL Adobe Commerce Optimizer] until you assign the key to a catalog view.
- **[!UICONTROL View Public Key]**—Opens a read-only view of the key's public key, so you can copy it to re-register or re-sync the key if needed. The private key is never displayed.
- **[!UICONTROL Delete]**—Removes the key and revokes its remote registration in [!DNL Adobe Commerce Optimizer]. Storefront tokens already issued with this key remain valid until they expire. This action can't be undone.

>[!NOTE]
>
>An expired key can only be deleted. You cannot assign or unassign an expired key.

## Create a key

 On the [!UICONTROL Restricted Access Keys] page, create a key by selecting  **[!UICONTROL Create Key]**.

Commerce generates a new key pair and stores the private key. The Restricted Access Keys table updates with a new key entry showing the unique key ID. Use this [!UICONTROL Key ID] when you assign the key to a catalog view.

The public key is not registered with [!DNL Adobe Commerce Optimizer] until you assign the key to a catalog view. After registration, the Restricted Access Keys table entry is updated to show the catalog assignment and expiration date.

## Assign or remove restricted access keys {#assign-keys-to-a-catalog-view}

{{$include /help/_includes/edit-restricted-access-keys.md}}

## Key selection and rotation {#key-selection-and-rotation}

When more than one key is assigned to a catalog view, [!DNL Adobe Commerce Optimizer] automatically uses the assigned, unexpired key with the latest expiration date to sign tokens.

>[!IMPORTANT]
>
>Automatic key rotation is not available yet. Keys default to a long expiration period. To rotate a key manually, create a new key, assign it to the catalog view alongside the existing one. After confirming that the new key is being used, delete the old key.

To change the default expiration period applied to newly created keys, go to **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Restricted Access Keys]** > **[!UICONTROL Provisioning]** > **[!UICONTROL Default key lifetime (days)]**. See [Services > ACO Restricted Access Keys](../configuration-reference/services/aco-restricted-access-keys.md).

## Known limitations {#known-limitations}

- There is no active or status indicator on the main [!UICONTROL Restricted Access Keys] grid.

  You can see the link status on the [!UICONTROL Edit Restricted Access Keys] page. Use the dropdown to view available keys and their status. If a key is assigned to a catalog view, it is linked. If it is not assigned, it has no status. You can assign those keys to the catalog view you are editing.

  In the [!UICONTROL Catalog View Sync Status] page, you can see keys linked to a catalog view from the catalog view detail page (**[!UICONTROL View details]** action). The detail page also shows the key history, including when it was assigned or unassigned from a catalog view.

- Automatic key rotation is not available yet.

>[!MORELIKETHIS]
>
> - [Manage catalog view configuration](/help/b2b/catalog-views-manage.md) — Assign these keys from the shared catalog or company account
> - [Catalog View Sync Status monitoring](catalog-view-sync-status.md) — Monitor and reconcile the catalog views these keys protect
> - [Services > ACO Restricted Access Keys](../configuration-reference/services/aco-restricted-access-keys.md) — Configure the default key expiration period
> - [Services > ACO Catalog View](../configuration-reference/services/aco-catalog-view.md) — Configure the storefront access-token lifetime and enable or disable issuance
> - [Manage restricted access keys](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/restricted-access-keys){target="_blank"} in the *Adobe Commerce Optimizer Connector Guide* — Learn how these keys fit into B2B shared catalog sync
> - [Restricted access keys](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"} in the *Adobe Commerce Optimizer Guide* — The manual, ACO Studio–based key flow for non-B2B use cases
