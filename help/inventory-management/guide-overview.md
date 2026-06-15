---
title: Inventory Management Guide [!DNL Inventory Management] Guide
description: Comprehensive information about [!DNL Inventory Management] for Adobe Commerce and Magento Open Source administrators, including migration and configuration.
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
# [!DNL Inventory Management] Guide overview

This guide is intended for administrators working in the Adobe Commerce and Magento Open Source Admin. It provides detailed information about enabling this module, including configuration and management of its features. It assumes a basic understanding of the core [!DNL Commerce] configuration and functionality.

[!DNL Inventory Management] has two areas for administrators:

- The Admin: Use this area to access the configuration UI and reporting.
- The command-line interface: Use this tool to execute installation and backend configuration tasks.

This guide covers:

| Subject | Description |
| ------- | ----------- |
| [Introduction](introduction.md) | Overview of the [!DNL Inventory Management] features that you can use to manage stock in multiple locations so that your Commerce store accurately reflects the physical inventory. |
| [Release notes](release-notes.md) | Review the release notes for information about all [!DNL Inventory Management] releases. |
| Inventory basics | Learn the basics about managing inventory: [Stocks and sources](sources-stocks.md), [source selection and reservations](selection-reservations.md), [order and reservation status](order-status.md), and [product types](product-types.md) |
| Get started | Learn about the [!DNL Inventory Management] module and how it fits into your Commerce instance and store operations: [Commerce upgrades](migrate.md), [module installation and update](install-update.md), [merchant sourcing types](merchant-sourcing.md), and [sourcing structure changes](expand-restructure.md) |
| [Configuration](configuration.md) | Learn about the configuration of [!DNL Inventory Management] options that determine source availability, storefront products, and order shipment. |
| [Manage sources](sources-manage.md) | Learn about sources and how they define the physical locations where product inventory is managed and shipped for order fulfillment, or where services are available. |
| [Manage stocks](stocks-manage.md) | Learn how stock is used to represent a virtual, aggregated inventory of products for sources of your sales channels. |
| [Manage quantities](quantities-manage.md) | Learn how to assign sources and quantities for new products or change existing products. |
| [Manage orders and shipments](shipments.md) | Learn about the additional [!DNL Inventory Management] features and options for managing inventory quantities through the shipment process. |
| [CLI reference](cli.md) | Learn about the commands provided by the [!DNL Inventory Management] module to manage inventory data and configuration settings. |

{style="table-layout:auto"}

## Developer information

See [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) in the developer documentation for details about module architecture, APIs, and algorithm customization.

## Commerce documentation

{{docs-links}}

## Troubleshooting and support

If you need information or have questions that are not covered in this guide, use the following resources:

- [Stock status incorrect after Inventory install](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Support tickets](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket)---Submit a ticket to receive additional help.
