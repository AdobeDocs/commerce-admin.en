---
title: "[!UICONTROL Services] &gt; ACO Catalog View"
description: Review and update the Adobe Commerce Optimizer configuration settings on the [!UICONTROL Services] &gt; [!UICONTROL ACO Catalog View] page of the Commerce Admin.
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
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View]

[!BADGE Private Beta]{type=Caution tooltip="Requires the Adobe Commerce Optimizer Connector for B2B extension, which is currently in private beta."}

Use these settings to control the access tokens issued by the [!DNL Adobe Commerce Optimizer Connector for B2B]. Storefronts use these tokens to authenticate to Commerce Optimizer private catalog views populated with data synchronized from custom shared catalogs configured in the Admin.

{{config}}

![Adobe Commerce Admin showing ACO Catalog View access-token settings, with a 3,600-second TTL and token issuance enabled.](./assets/aco-catalog-view-access-token-config.png)<!-- zoom -->

## [!UICONTROL Access Token Configuration]

| Field | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| --- | --- | --- |
| [!UICONTROL Token TTL (seconds)] | Global | Number of seconds an access token remains valid after it is generated. This setting is read only at the default scope. Values configured at the website or store-view scope are ignored. Defaults to: 3600 seconds. |
| [!UICONTROL Issue Access Tokens] | Store View | Controls whether the storefront can obtain an access token for a catalog view. When set to `No`, `Company.catalogViewContext` returns the catalog view ID but no access token, so storefronts cannot authenticate to read from  [!DNL Adobe Commerce Optimizer] private catalog views synchronized from Adobe Commerce. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [ACO Catalog View Sync](./aco-catalog-view-sync.md) — Configure how catalog views are synchronized into [!DNL Adobe Commerce Optimizer]
> - [Catalog View Sync Status monitoring](../../systems/catalog-view-sync-status.md) — Monitor sync health and reconcile drift
