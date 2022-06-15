---
title: Merchant sourcing types
description: Learn about the two sourcing types based on the number of locations, or sources, in your business.
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
---
# Merchant sourcing types

[!DNL Commerce] supports [!DNL Inventory Management] for all sizes of businesses, including a single store with one website to an international network of websites, stores, warehouses, and drop shippers. All merchants using Adobe Commerce or Magento Open Source fall into two types based on the number of locations, or sources, in your business.

- Single-source merchants ship products from one location. You are considered a single-source merchant/mode until you start adding custom sources and stocks to your installation.

- Multi-source merchants ship products from more than one location such as brick-and-mortar stores, warehouses, drop shippers, and distribution centers. After adding custom sources per location, you automatically become a multi-source merchant.

## Single-source merchants

Single-source merchants have a single location that manages on-hand inventory and fulfills orders. Typically, you have multiple websites (or sales channels) selling products from the same catalog, inventory, and location.

For example, you have one website or a multi-site implementation with sites for United States, Germany, France, and Brazil all pulling products from one large warehouse. This single source manages all inventory quantities, shipments, and returns regardless of which sales channel receives the order.

To get started:

- Configure [global and product settings](configuration.md) for your store's inventory as needed.

- Update the [Default Source](sources-manage.md) with information for your single inventory location. Creating additional sources is not required.

- Update the [Default Stock](stocks-manage.md). Ensure all of your websites are selected as sales channels. As you add new websites, [!DNL Commerce] automatically adds them to the Default Stock. Creating additional stocks is not required.

>[!NOTE]
>
>As your business expands, add additional sources and stocks and update your [!DNL Inventory Management] configuration to become a multi-source merchant. See [Expand and Restructure Inventory](expand-restructure.md) for all details.

## Multi-source merchants

Multi-source merchants have one website or a multi-site implementation and manage on-hand inventory and fulfilling orders through multiple locations.

For example, you have a multi-site implementation with websites for United States, Germany, France, and Brazil. Your business includes multiple warehouses and stores in these countries and drop shipper services that manage all inventory stock and fulfill orders. These locations and websites become sources and stocks in [!DNL Commerce]. You may create a stock for the Americas and another for Europe, assigning websites and sources based on locales and locations. Customers shopping each website only have access to salable inventories from the assigned sources.

To get started:

- Configure global settings for your store's inventory as needed.

- Add [custom sources](sources-add.md) for your inventory locations: warehouses, stores, distribution centers, and drop shippers.

- Add [custom stocks](stocks-add.md) for each region to map your websites with multiple sources. Reorder the sources in each stock in priority of location, helpful when fulfilling your orders.

- Assign sources to products, adding quantities per location.

- Complete any further configurations per product for quantity thresholds, backorders, and so on.
