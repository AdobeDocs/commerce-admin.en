---
title: Expand and Restructure Inventory
description: Learn how to expand to a multi-source merchant or reduce down to a single-source merchant.
---
# Expand and Restructure Inventory

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
