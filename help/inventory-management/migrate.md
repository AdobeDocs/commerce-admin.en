---
title: '[!DNL Commerce] upgrades'
description: Learn how Adobe Commerce and Magento Open Source upgrades affect catalog and [!DNL Inventory Management] configurations.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
---
# [!DNL Commerce] upgrades

If you used single-source inventory in a previous release, this information provides details on new features and changes to your existing catalog and inventory configurations.

[!DNL Inventory Management] for Adobe Commerce and Magento Open Source includes features, enhancements, and developer support that enhances and updates all product stock management and add new features. All features are available out-of-the-box including the Source Selection Algorithm and Concurrent Checkout to match order quantities to sources and order fulfillment. Depending on your websites, stores, and merchant type, you can create additional stock and sources, assign inventory amounts, and more. For complete information, see [Inventory Management](introduction.md).

When you install Magento Open Source 2.4.x or Adobe Commerce 2.4.x, the following initial changes occur:

- [Inventory Management](enable.md) enables at the global store or product level. The Manage Stock option enables or disables tracking of inventory quantities, calculations of aggregated salable quantities, and reservation management for tracking purchases through to invoice and shipment. You can disable this option to use an ERP and other third-party services for managing stock, orders, and shipments. For additional information, see [!DNL Inventory Management] Modules below.

- A [Default Source](sources-manage.md) and [Default Stock](stocks-manage.md) add to the system. Do not disable or remove these defaults. [!DNL Commerce] assigns existing and newly imported products to these defaults.

   >[!IMPORTANT]
   >
   >Using the Default Stock and the Default Source is highly discouraged because they are a part of the `CatalogInventory` module, which is now deprecated. It is recommended that you create and use custom stocks and sources instead.

  - Stocks provide an aggregated, virtual Salable Quantity with reservations to track shopping carts and orders, ensuring concurrent checkout.

  - All existing products in your catalog assign to the Default Source. Until you add new sources, the product interface does not change. If you only ship products from one location, there are no other differences for sources. You can create custom [sources](sources-add.md) and [assign quantities](quantities-manage.md) per shipment location.

  - You can configure a source as a Pickup Location and [assign quantities](quantities-manage.md) for that source.

  - Your website assigns to the Default Stock. You can create custom [stocks](stocks-add.md) to connect sales channels (websites) and sources (locations).

- Additional [configuration options](configuration.md) add to your products and global store. Some existing configurations options receive updated options and behaviors:

  - Notify for Quantity Below sends notifications and deducts from the Salable Quantity.

  - Out-of-Stock Threshold supports positive amounts, zero, and negative amounts. With Backorders enabled, positive amounts are ignored, considered zero (or infinite).

  - Backorders supports zero (infinite) and negative amounts. When enabled, the Notify for Quantity Below does not deduct from the Salable Quantity.

- New Reservations track potential sales, converting to quantity deductions when the order ships. You never directly access or create reservations. [!DNL Commerce] creates and manages reservations behind-the-scenes through orders, shipments, and credit memos.

- [Orders and shipments](shipments.md) include new features to recommend shipments using the Source Selection Algorithm and support partial shipments from multiple sources to fulfill an order.

- New [import/export features](inventory-import-export.md) allow you to mass add sources, update inventory quantities, and set stock status (in/out of stock) for all SKUs in your catalog. These features allow you to modify for one, selected, or all sources.

- New bulk options through the Product grid page support bulk [assigning and unassigning sources](bulk-assignment.md), and [transferring inventory to source](inventory-transfer.md).

- [!DNL Inventory Management] supports B2B catalogs. Currently, all B2B products must be assigned to the Default Source and Default Stock.

## [!DNL Commerce Order Management] and [!DNL Inventory Management]

[Commerce Order Management (MCOM)](https://commerce-docs.github.io/oms-documentation-archive/) is not compatible with the [!DNL Inventory Management]. When installed, MCOM modules provide all inventory management features to [!DNL Commerce], including single- and multi-source management, stocks, reservations, and more. The [!DNL Inventory Management] modules are disabled by default.

MCOM provides extensive features and services for advanced omnichannel order management, global inventory and multi-sourcing, store to warehouse fulfillment, and centralized customer service. For a complete list of features, see the [MCOM Feature list](https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/).

[!DNL Inventory Management] extends existing [!DNL Commerce] features with additional options to track in-process orders, on-hand inventory, available inventory for a stock, and APIs for extension development.

## [!DNL Inventory Management] modules

You may want to disable [!DNL Inventory Management] modules to:

- Speed up upgrade of merchants currently on Adobe Commerce or Magento Open Source 2.0/2.1/2.2/2.3 and migrating to 2.4.x.

- Use custom or third-party inventory and order management modules.

- Use [!DNL Order Management System] for inventory management. The current connector does not support [!DNL Inventory Management] interfaces. For OMS merchants upgrading to Adobe Commerce 2.4.0, they must disable these modules.

For complete details, see [Install and Update](install-update.md).
