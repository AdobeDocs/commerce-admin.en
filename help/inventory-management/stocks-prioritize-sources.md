---
title: Prioritize inventory sources for a stock
description: Learn how to arrange sources from top to bottom in priority, which is used when determining shipment and inventory deductions.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/oPgeuN3-Il-yf3zpG2r4PNAmNbf-4gmz5-GFngM3-Ng
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
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
# Prioritize sources for a stock

After adding [sources](sources-manage.md) to the [stock](stocks-manage.md), arrange those sources from top to bottom in priority for fulfilling orders. The Source Selection Algorithm (SSA) provides an algorithm Priority using this order when determining shipment and inventory deductions.

The source priority on stocks does not influence assigned sources when editing product inventories.

In this example, the UK Stock has sources assigned out of order for a store and two warehouses in London and a warehouse in Berlin.

![Source order before prioritization](assets/inventory-priority-before.png){width="350" zoomable="yes"}

The merchant prefers to have shipments prioritized from the larger Berlin warehouse, then the London warehouse, the London overflow location, and finally the storefront in London. To change the order, entries are dragged and dropped into the desired order.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_ > **[!UICONTROL Stocks]**.

1. Open the stock in the _Edit_ mode.

1. Expand the _[!UICONTROL Sources]_ tab, if needed.

1. Use ![Sort icon](assets/icon-sort.png) to drag and drop the sources into a priority from top (first) to bottom (last).

   This order is important when shipping orders. SSA recommends shipments based on the order of sources

1. Click **[!UICONTROL Save & Continue]** to save the changes.

![Source order after prioritization](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
