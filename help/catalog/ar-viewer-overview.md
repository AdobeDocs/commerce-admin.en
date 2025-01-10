---
title: '[!DNL AR Viewer] for Adobe Commerce'
description: Learn how the [!DNL AR Viewer] could benefit your Adobe Commerce instance and how to successfully onboard and setup the extension.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
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
