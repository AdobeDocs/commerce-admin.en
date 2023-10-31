---
title: Product types
description: Learn how [!DNL Inventory Management] supports inventory and order management for all Adobe Commerce and Magento Open Source product types.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
---
# Product types

[!DNL Inventory Management] supports inventory and order management for all product types in Adobe Commerce and Magento Open Source: simple, configurable, virtual, downloadable, bundle, and grouped. Options and requirements may differ per product type for sources, stocks, and shipping.

- [Single-source merchants](merchant-sourcing.md#single-source-merchants) create and update product settings and quantities without requiring additional updates. All created and newly imported products automatically assign to the Default Source and Default Stock, immediately available to customers if enabled and In-Stock.

- [Multi-source merchants](merchant-sourcing.md#multi-source-merchants) assign sources, quantities per source, and settings during or after product creation. [!DNL Commerce] assigns all newly imported products to the Default Source, requiring additional edits to assign sources and quantities.

|Product Type|Shipping and Source Selection Algorithm|
|--|--|
|[[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"}|Supports SSA recommendations and overrides at shipping.|
|[[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"}|Supports SSA recommendations and overrides at shipping.|
|[[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"}|Always uses the SSA recommendation. The system runs the algorithm implicitly when it creates invoices, and always uses the suggested results.<br/>You cannot adjust these results.|
|[[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"}|Always uses the SSA recommendation. The system runs the algorithm implicitly when it creates invoices, and always uses the suggested results. <br/>You cannot adjust these results.|
|[[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"}|Supports SSA recommendations and overrides at shipping.|
|[[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"}|Supports SSA recommendations and overrides at shipping.|
