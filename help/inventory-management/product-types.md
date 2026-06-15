---
title: Product types
description: Learn how [!DNL Inventory Management] supports inventory and order management for all Adobe Commerce and Magento Open Source product types.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/3F5vZOseQC7ILpL0j-ksjWP-GW7c0gUN9Zy7hylzzHU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
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
