---
title: Introduction to [!DNL Inventory Management]
description: Learn how [!DNL Inventory Management] uses the Admin and command-line interface to manage stock so your [!DNL Commerce] store matches physical inventory.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
---
# Introduction to [!DNL Inventory Management]

[!DNL Inventory Management] covers two main tools. The Admin lets you set options and generate reports. The command-line interface helps with setup and background changes. Merchants with a single store to multiple warehouses, stores, pickup locations, drop shippers, and more can use these features to maintain quantities for sales and handle shipments to complete orders. You can track your inventory quantities, provide accurate salable stock amounts to customers for all of your websites, and ship according to recommendations based on distance or priority. You can also configure your preferred product configurations globally (for all stores and products), per source, and per product. These features grow with your business, allowing you to work from a single warehouse or a complex shipping network with a few additional settings.

[!DNL Inventory Management] features include:

- Different configurations for merchants whose inventory originates from a single source and from multiple sources
- Stocks for tracking available aggregated quantities through assigned sources
- Concurrent checkout protection
- Shipment matching algorithms

>[!NOTE]
>
>These features were developed as part of the [Inventory Management](https://github.com/magento/inventory) (formerly MSI) project through the Community Engineering program.<br/>
>
>The [!DNL Inventory Management] module is installed with Magento Open Source and Adobe Commerce, with all features enabled by default. For information about changes included in module releases, see the [Release Notes](release-notes.md). 

## Basic terminology

It is important to understand the following terms as you work with [!DNL Inventory Management]:

[!UICONTROL Sources] represent physical or virtual locations that store and ship available products. See [Stocks and sources](sources-stocks.md) for examples and diagrams. (Any location can be designated as a source for virtual products.)

[!UICONTROL Stocks] map a sales channel (currently limited to websites) to source locations and on-hand inventory. A stock can map to multiple sales channels, but a sales channel can be assigned to only one stock.

[!UICONTROL Aggregate Salable Quantity] is the total virtual inventory that can be sold through a sales channel. The amount is calculated across all sources assigned to a stock.

[!UICONTROL Reservations] track deductions from the salable quantity as customers add products to carts and complete checkout. When an order ships, the reservation clears and deducts the shipped amounts from specific source inventory quantities.
