---
title: Product Types
description: Learn how [!DNL Inventory Management] supports inventory and order management for all Adobe Commerce and Magento Open Source product types.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
---
# Product Types

[!DNL Inventory Management] supports inventory and order management for all product types in Adobe Commerce and Magento Open Source: simple, configurable, virtual, downloadable, bundle, and grouped. Options and requirements may differ per product type for sources, stocks, and shipping.

- Single-source merchants create and update product settings and quantities without requiring additional updates. All created and newly imported products automatically assign to the Default Source and Default Stock, immediately available to customers if enabled and In-Stock.

- Multi-source merchants assign sources, quantities per source, and settings during or after product creation. [!DNL Commerce] assigns all newly imported products to the Default Source, requiring additional edits to assign sources and quantities.

|Product Type|Shipping and Source Selection Algorithm|
|--|--|
|[Simple](https://docs.magento.com/user-guide/catalog/product-create-simple.html){target="_blank"}|Supports SSA recommendations and overrides at shipping.|
|[Configurable](https://docs.magento.com/user-guide/catalog/product-create-configurable.html){target="_blank"}|Supports SSA recommendations and overrides at shipping.|
|[Virtual](https://docs.magento.com/user-guide/catalog/product-create-virtual.html){target="_blank"}|Always uses the SSA recommendation. The system runs the algorithm implicitly when it creates invoices, and always uses the suggested results.<br/>You cannot adjust these results.|
|[Downloadable](https://docs.magento.com/user-guide/catalog/product-create-downloadable.html){target="_blank"}|Always uses the SSA recommendation. The system runs the algorithm implicitly when it creates invoices, and always uses the suggested results. <br/>You cannot adjust these results.|
|[Bundle](https://docs.magento.com/user-guide/catalog/product-create-bundle.html){target="_blank"}|Supports SSA recommendations and overrides at shipping.|
|[Grouped](https://docs.magento.com/user-guide/catalog/product-create-grouped.html){target="_blank"}|Supports SSA recommendations and overrides at shipping.|
