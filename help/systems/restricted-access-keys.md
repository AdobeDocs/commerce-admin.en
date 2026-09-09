---
title: Manage Restricted Access Keys in Commerce
description: Create, assign, and delete the restricted access keys that secure B2B shared catalog projections for the Adobe Commerce Optimizer Connector.
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

# Restricted Access Keys management

[!BADGE Private Beta]{type=Caution tooltip="Requires the Adobe Commerce Optimizer Connector B2B extension, which is currently in private beta."} Learn how to create, assign, and delete the RSA key pairs that the [!DNL Adobe Commerce Optimizer Connector B2B extension] uses to secure private catalog views in [!DNL Adobe Commerce Optimizer].

>[!NOTE]
>
>This page manages keys for B2B shared catalog projections from the Commerce Admin. It's a different page from [!UICONTROL Restricted Access Keys] in [!DNL Adobe Commerce Optimizer] Studio, which manages keys you create manually for non-B2B use cases such as partner portals. See [Restricted access keys](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"} in the *Adobe Commerce Optimizer Guide* for that page.

## Audience and availability {#audience}

[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud Infrastructure and on-premises projects only."} The Restricted Access Keys page is available to Adobe Commerce on Cloud Infrastructure and on-premises merchants who use B2B shared catalogs with the [!DNL Adobe Commerce Optimizer Connector] B2B extension. The page is installed and enabled automatically with the extension—there is no separate installation step.

When a catalog view is first created for a shared catalog, the extension automatically generates and assigns one key. Use this page to view that key, and to create, assign, or delete additional keys.

## Access the Restricted Access Keys page {#access-restricted-access-keys-page}

From the Admin area, navigate to **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Restricted Access Keys]**.

![Restricted Access Keys page listing keys and their assigned catalog views](assets/restricted-access-keys-admin.png){width="600" zoomable="yes"}

This page lists every key regardless of whether it's assigned to a catalog view. To assign a key to a specific catalog view, use the [!UICONTROL Edit Restricted Access Keys] action on that catalog view instead. See [Assign keys to a catalog view](#assign-keys-to-a-catalog-view).

## Restricted Access Keys summary {#restricted-access-keys-summary}

The grid lists one row per key:

| Field | Description |
| --- | --- |
| **Key ID** | The key's unique identifier. |
| **Title** | A label you provide to identify the key. |
| **Assigned Catalog Views** | The catalog views this key is currently assigned to. |
| **Expires At** | The key's expiration date. |
| **Actions** | Row-level actions. See [Manage keys](#manage-keys). |

>[!NOTE]
>
>There's no status or "active" column on this grid. A key's link status (assigned, linking, or failed) appears only in the [!UICONTROL Edit Restricted Access Keys] picker for a specific catalog view. Which of a catalog view's assigned keys is used to sign tokens is determined automatically—see [Key selection and rotation](#key-selection-and-rotation).

## Manage keys {#manage-keys}

- **[!UICONTROL Create Key]**—Generates a new, unassigned key pair. Commerce generates the key pair and holds the private key; the public key isn't registered with [!DNL Adobe Commerce Optimizer] until you assign the key to a catalog view.
- **[!UICONTROL View Public Key]**—Opens a read-only view of the key's public key, so you can copy it to re-register or re-sync the key if needed. The private key is never displayed.
- **[!UICONTROL Delete]**—Removes the key and revokes its remote registration in [!DNL Adobe Commerce Optimizer]. Storefront tokens already issued with this key remain valid until they expire. This action can't be undone.

>[!NOTE]
>
>An expired key can only be deleted—you can't assign or unassign an expired key.

## Assign keys to a catalog view {#assign-keys-to-a-catalog-view}

Assign or unassign keys from the catalog view itself, not from the main [!UICONTROL Restricted Access Keys] grid.

1. Open the shared catalog's or company's catalog view list in the Admin.
1. Select **[!UICONTROL Edit Restricted Access Keys]** for the catalog view you want to update.

   ![Edit Restricted Access Keys picker showing keys assigned to a catalog view](assets/restricted-access-keys-edit-modal.png){width="500" zoomable="yes"}

1. In the **[!UICONTROL Access Keys]** field, select one to three keys to assign. Keys already assigned to a different catalog view are labeled accordingly.
1. Click **[!UICONTROL Save]**.

A catalog view must have at least one key and can have at most three. If you try to assign a fourth key, the save fails with a message telling you to remove one first.

## Key selection and rotation {#key-selection-and-rotation}

There's no manual "set active" action. When more than one key is assigned to a catalog view, [!DNL Adobe Commerce Optimizer] automatically uses the assigned, unexpired key with the latest expiration date to sign tokens.

>[!IMPORTANT]
>
>Automatic key rotation isn't available yet. Keys default to a long expiration period, so this isn't an immediate concern. To rotate a key manually, create a new key, assign it to the catalog view alongside the existing one, confirm the new key is being used, then delete the old key.

## Known limitations {#known-limitations}

- There's no "active" or status indicator on the main [!UICONTROL Restricted Access Keys] grid. A key's link status per catalog view is only visible in the [!UICONTROL Edit Restricted Access Keys] picker.
- Automatic key rotation isn't available yet. See [Key selection and rotation](#key-selection-and-rotation).

>[!MORELIKETHIS]
>
> - [Catalog View Sync Status monitoring](catalog-view-sync-status.md) — Monitor and reconcile the catalog views these keys protect
> - [Manage restricted access keys](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/restricted-access-keys){target="_blank"} in the *Adobe Commerce Optimizer Connector Guide* — Learn how these keys fit into B2B shared catalog sync
> - [Restricted access keys](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"} in the *Adobe Commerce Optimizer Guide* — The manual, ACO Studio–based key flow for non-B2B use cases
