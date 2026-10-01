---
title: "[!UICONTROL Services] &gt; [!UICONTROL ACO Restricted Access Keys]"
description: Review the configuration settings on the [!UICONTROL Services] &gt; [!UICONTROL ACO Restricted Access Keys] page of the Commerce Admin.
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
# [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]

Use this setting to control the default expiration period that the [!DNL Adobe Commerce Optimizer Connector for B2B] applies to restricted access keys it provisions for B2B shared catalog views. To create, assign, and delete these keys, see [Restricted Access Keys management](../../systems/restricted-access-keys.md).

{{config}}

## [!UICONTROL Provisioning]

![Provisioning](./assets/optimizer-restricted-access-key-config.png)<!-- zoom -->

| Field | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description |
| --- | --- | --- |
| [!UICONTROL Default key expiry (days)] | Global | Validity period for newly provisioned restricted access keys. [!DNL Adobe Commerce Optimizer] requires an expiration date at least one minute in the future on every key, and excludes expired keys from gateway reads, so a value of at least one day is always applied. Default value: `36500` |

{style="table-layout:auto"}

>[!NOTE]
>
>The default expiry is set to a long expiration period because automatic key rotation is not yet available. See [Key selection and rotation](../../systems/restricted-access-keys.md#key-selection-and-rotation).

>[!MORELIKETHIS]
>
> - [ACO Catalog View](./aco-catalog-view.md) — Configure storefront access tokens for catalog views
> - [Restricted Access Keys management](../../systems/restricted-access-keys.md) — Create, assign, and delete restricted access keys
> - [Catalog View Sync Status monitoring](../../systems/catalog-view-sync-status.md) — Monitor keys nearing expiration
