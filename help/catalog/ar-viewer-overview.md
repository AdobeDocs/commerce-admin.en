---
title: "[!DNL AR Viewer] for Adobe Commerce"
description: Learn how the [!DNL AR Viewer] could benefit your Adobe Commerce instance and how to successfully onboard and setup the extension.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
TQID: https://experienceleague.adobe.com/ofebqdDS0exPDKJMLB-mpE0eVjRKT5ck91Fm2-7CVjA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
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
  - id: a09a5a04-e30b-4d55-b031-38e6f5ec86db
    internal-label: Experience design
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# [!DNL AR Viewer] for Adobe Commerce

Augmented reality (AR) describes user experiences that add 2D or 3D elements to the live view from a device's camera in a way that makes those elements appear to inhabit the real world.

The [!DNL AR Viewer] for Adobe Commerce extension powers a seamless experience designed to display rendered 3D graphics for the user.

The information in this guide provides an overview of the onboarding experience for the [!DNL AR Viewer] in Adobe Commerce and how the [!DNL AR Viewer] benefits the user, as well as best practices to follow along that journey.

Developed by Pixar, [Universal Scene Description (USD)](https://openusd.org/release/index.html){target=_blank} is the first open-source software that can robustly and scalably interchange 3D scenes that may be composed of many different assets, sources, and animations, while fostering highly collaborative workflows. This USD is used within `.USDZ` files. This `.USDZ` file delivers AR and 3D content to the user's devices.

>[!NOTE]
>
> The [!DNL AR Viewer] supports only `.USDZ` files.

## [!DNL AR Viewer] requirements

The [!DNL AR Viewer] is compatible with both [!DNL Magento Open Source] and Adobe Commerce. See [Lifecycle Policy](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} for more information about supported versions.

See [Install the [!DNL AR Viewer] extension](../catalog/ar-viewer-setup.md) for more information.

In order to use [!DNL AR Viewer], you must have the following available for your instance:

* PHP 8.1.0
* Adobe Commerce version 2.4.4 and newer
* Magento Open Source (CE) version 2.4.x

## Compatibility limitations

[!DNL AR Viewer] existing compatibility limitations:

* `.USDZ` only: This feature only supports `.USDZ` files.
* `qr-code`: Requires `endroid/qr-code` version 4.5.
* `Catalog module`: Requires `magento/module-catalog` version 104.0.0.
