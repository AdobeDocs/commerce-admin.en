---
title: Introduction to Inventory Management
description: Learn how to use [!DNL Inventory Management] features to manage stock in multiple locations so that your [!DNL Commerce] store accurately reflects the physical inventory.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
TQID: https://experienceleague.adobe.com/7v-G-DZEki7y-4HSmq-rJxsmu6vih26jRYYCRRUF-XY
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
# Introduction to Inventory Management

[!DNL Inventory Management] for [!DNL Commerce] gives you the tools to manage your product inventory. Merchants with a single store to multiple warehouses, stores, pickup locations, drop shippers, and more can use these features to maintain quantities for sales and handle shipments to complete orders. You can track your inventory quantities, provide accurate salable stock amounts to customers for all of your websites, and ship according to recommendations based on distance or priority. You can also configure your preferred product configurations globally (for all stores and products), per source, and per product. These features grow with your business, allowing you to work from a single warehouse or a complex shipping network with a few additional settings.

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

[!UICONTROL **Sources**] represent physical locations that store and ship available products. These locations can include warehouses, brick-and-mortar stores, distribution centers, and drop shippers. (Any location can be designated as a source for virtual products.)

[!UICONTROL **Stocks**] map a sales channel (currently limited to websites) to source locations and on-hand inventory. A stock can map to multiple sales channels, but a sales channel can be assigned to only one stock.

[!UICONTROL **Aggregate Salable Quantity**] is the total virtual inventory that can be sold through a sales channel. The amount is calculated across all sources assigned to a stock.

[!UICONTROL **Reservations**] track deductions from the salable quantity as customers add products to carts and complete checkout. When an order ships, the reservation clears and deducts the shipped amounts from specific source inventory quantities.
