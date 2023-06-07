---
title: "[!DNL AR Viewer] requirements"
description: "Verify that your system meets the requirements necessary to use the [!DNL AR Viewer] for Adobe Commerce module."
---
# [!DNL AR Viewer] requirements

The [!DNL AR Viewer] is compatible with both [!DNL Magento Open Source] and Adobe Commerce. See [Lifecycle Policy](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} for more information about supported versions.

Refer to the [onboarding](../catalog/ar-viewer-onboarding.md) topic for more information.

## Compatibility limitations

In order to use [!DNL AR Viewer], you must have the following available for your instance:

* PHP 8.1.0
* Adobe Commerce version 2.4.x
* Magento Open Source (CE) version 2.4.x

[!DNL AR Viewer] existing compatibility issues:

| **Issue** | **Constraints** |
|----------------|-----------------|
| `.USDZ` only| This feature only supports `.USDZ` schemas. |
| `qr-code` | `endroid/qr-code` version 4.5. |
| `Catalog module` | `magento/module-catalog` version 104.0.0. |

{style="table-layout:auto"}
