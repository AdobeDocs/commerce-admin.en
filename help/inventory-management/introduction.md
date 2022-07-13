---
title: Introduction to Inventory Management
description: Learn how to use [!DNL Inventory Management] features to manage stock in multiple locations so that your [!DNL Commerce] store accurately reflects the physical inventory.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
---
# Introduction to Inventory Management

[!DNL Inventory Management] for [!DNL Commerce] gives you the tools to manage your product inventory. Merchants with a single store to multiple warehouses, stores, pickup locations, drop shippers, and more can use these features to maintain quantities for sales and handle shipments to complete orders. You can track your inventory quantities, provide accurate salable stock amounts to customers for all of your websites, and ship according to recommendations based on distance or priority. You can also configure your preferred product configurations globally (for all stores and products), per source, and per product. These features grow with your business, allowing you to work from a single warehouse or a complex shipping network with a few additional settings.

[!DNL Inventory Management] features include:

- Different configurations for merchants whose inventory originates from a single source and from multiple sources
- Stocks for tracking available aggregated quantities through assigned sources
- Concurrent checkout protection
- Shipment matching algorithms

>[!NOTE]
>
>These features were developed as part of the [Inventory Management](https://github.com/magento/inventory) (formerly MSI) project through the Community Engineering program.

## Basic terminology

It is important to understand the following terms as you work with [!DNL Inventory Management]:

**Sources** represent physical locations that store and ship available products. These locations can include warehouses, brick-and-mortar stores, distribution centers, and drop shippers. (Any location can be designated as a source for virtual products.)

**Stocks** map a sales channel (currently limited to websites) to source locations and on-hand inventory. A stock can map to multiple sales channels, but a sales channel can be assigned to only one stock.

**Aggregate Salable Quantity** is the total virtual inventory that can be sold through a sales channel. The amount is calculated across all sources assigned to a stock.

**Reservations** track deductions from the salable quantity as customers add products to carts and complete checkout. When an order ships, the reservation clears and deducts the shipped amounts from specific source inventory quantities.
