---
title: Expand and restructure inventory
description: Learn how to expand to a multi-source merchant or reduce down to a single-source merchant.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/w4TV-BQrg0RzlHn4DVSdHFPD2M5CF11wA7I5OyA7jsY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Expand and restructure inventory

As your business grows and changes, [!DNL Inventory Management] supports your needs. You can expand to a multi-source merchant or reduce down to a single-source merchant with ease.

## Expand to multi-source

Single-source merchants may add new stores, warehouses, drop shippers, and more. Expanding requires only a few additions and stock updates to expand to multi-sourcing:

1. Add [custom sources](sources-add.md) for each new location.

   You use only the Default Source for Bundle products.

1. Add [custom stocks](stocks-add.md) as needed for your new sources.

   For example, you may want to create stocks per website, country, locale, or other method. You can assign sources to your custom stocks. You use only the Default Stock for Bundle products.

1. Update [source assignments and quantities](quantities-manage.md) for your products.

   You can also use the [Mass Actions Tool](bulk-assignment.md) and [Import-Export](inventory-import-export.md) feature to quickly add sources and product data.

## Restructure to single-source

For multi-source merchants wanting to reduce online sales to one location for shipping, modify your sources, stock, and quantities to update:

1. Disable [custom sources](sources-disable.md).

1. Transfer product inventory to your Default Source.

   Using mass actions is recommended. See [Transferring Inventory to Source](inventory-transfer.md).

1. Assign all websites to the [Default Stock](stocks-manage.md).
