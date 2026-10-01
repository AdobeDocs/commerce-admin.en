---
title: '[!DNL Inventory Management] Guide'
description: Admin and CLI guide for [!DNL Inventory Management] stocks, sources, quantities, configuration, orders, and shipments in Adobe Commerce and Magento Open Source.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
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
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# [!DNL Inventory Management] overview

This guide is for administrators who manage stock across multiple locations in Adobe Commerce and Magento Open Source. It provides configuration and management procedures for the [!DNL Inventory Management] module and assumes a basic understanding of core [!DNL Commerce] functionality.

Use the **Admin** for configuration, reporting, and day-to-day inventory tasks. Use the **command-line interface** for installation, upgrades, and backend configuration.

This guide covers:

| Subject | Description |
| ------- | ----------- |
| [Introduction](introduction.md) | Features, terminology, and how [!DNL Inventory Management] fits your store. |
| [Release notes](release-notes.md) | Module release history and known issues. |
| [Inventory basics](sources-stocks.md) | Concepts for [stocks and sources](sources-stocks.md), [source selection and reservations](selection-reservations.md), [order and reservation status](order-status.md), and [product types](product-types.md). |
| Get started | [Commerce upgrades](migrate.md), [installation and updates](install-update.md), [merchant sourcing types](merchant-sourcing.md), and [inventory restructuring](expand-restructure.md). |
| [Configuration](configuration.md) | Global, product, and algorithm settings for storefront display and shipment. |
| [Manage sources](sources-manage.md) | Create and maintain fulfillment locations. |
| [Manage stocks](stocks-manage.md) | Map sources to sales channels. |
| [Manage quantities](quantities-manage.md) | Assign and update product quantities per source. |
| [Manage orders and shipments](shipments.md) | Fulfill orders and manage shipments from inventory. |
| [CLI reference](cli.md) | Command-line inventory and configuration tasks. |

{style="table-layout:auto"}

## Developer information

Access advanced resources for APIs, customization, and module architecture. See [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) in the REST API developer documentation for technical details about APIs and algorithm customization.

## Commerce documentation

Find merchant, cloud, and developer guides to help with every part of Adobe Commerce. Use these resources for any setup or management need.

{{docs-links}}

## Troubleshooting and support

Use support articles and ticket systems to solve inventory issues fast. Get extra help for stock status or product management.

If you need information or have questions that are not covered in this guide, use the following resources:

- [Stock status incorrect after Inventory install](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-29910)
- [Support tickets](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide#support-case)—Submit a ticket to receive additional help.
