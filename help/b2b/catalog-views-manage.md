---
title: Manage Catalog View Configuration
description: Learn how to review the Adobe Commerce Optimizer catalog views created for B2B shared catalogs, and assign the restricted access keys that protect them.
feature: B2B, Companies, Catalog Management
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Manage catalog view configuration

With the [!DNL Adobe Commerce Optimizer Connector for B2B] extension installed, the _[!UICONTROL Catalog Views]_ page lists the [!DNL Adobe Commerce Optimizer] (ACO) catalog views projected from a shared catalog.  A _projection_ is the catalog view created when the connector synchronizes shared catalog data to [!DNL Adobe Commerce Optimizer]. The connector creates a separate projection for each store view in the shared catalog, so a shared catalog can have multiple catalog views. In storefront experiences, these catalog views are accessible only to companies assigned to the associated shared catalog.

For example, suppose Acme Industrial is assigned to one shared catalog, EU Business, which belongs to the EU Website. That website has two store views:

- `English (UK)`

- `German (Germany)`

The connector projects the shared catalog into two [!DNL Adobe Commerce Optimizer] catalog views:

- `EU Business – English (UK)`

- `EU Business – German (Germany)`

The company has English and German catalog views, but only one shared catalog assignment. Each store view displays data from its corresponding catalog view.

Both catalog views can share the same price book when they use the same website and customer-group pricing scope.

## Catalog view authentication

The connector protects catalog views with restricted access keys. Adobe Commerce uses the private key to sign an access token for an authorized buyer. Before returning protected catalog data, [!DNL Adobe Commerce Optimizer] validates the token against the corresponding public key associated with the requested catalog view.

To configure the token lifetime or disable token issuance, see [Services > ACO Catalog View](/help/configuration-reference/services/aco-catalog-view.md).

You can review these catalog views and manage their assigned keys from either the shared catalog's _[!UICONTROL Catalog Views]_ tab or the associated company's _[!UICONTROL Catalog Views]_ section—both list the same catalog views and current key assignments. See [Edit restricted access keys](#edit-restricted-access-keys) for the exact navigation path from each location.

To monitor shared catalog data synchronization to [!DNL Adobe Commerce Optimizer], see [Catalog view sync status monitoring](/help/systems/catalog-view-sync-status.md).

## Catalog views reference

{{$include /help/_includes/catalog-views-reference-table.md}}

## Edit restricted access keys

{{$include /help/_includes/edit-restricted-access-keys.md}}

For additional details, see [Manage restricted access keys](/help/systems/restricted-access-keys.md).

>[!MORELIKETHIS]
>
> - [Services > ACO Catalog View](/help/configuration-reference/services/aco-catalog-view.md)
> - [Catalog View Sync Status monitoring](/help/systems/catalog-view-sync-status.md)
> - [Manage your shared catalogs](catalog-shared-manage.md)
> - [Manage company accounts](account-company-manage.md)
