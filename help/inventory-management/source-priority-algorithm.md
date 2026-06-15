---
title: Configure the Source Priority Algorithm
description: Learn how to configure the source priority used for the order of assigned sources in your stock to make recommendations.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
TQID: https://experienceleague.adobe.com/TB4THYjkzbNvEbsjNzOewNtYS6JoRvLDiQQCovSMkbI
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
# Configure the Source Priority Algorithm

Custom stocks include an assigned list of sources to sell and ship available product inventory through your storefront. This algorithm uses the order of assigned sources in your stock to make recommendations.

When run, the algorithm:

- Works through the configured order of sources at the stock level starting at the top

- Recommends a quantity to ship and source per product based on the order in the list, available quantity, and quantity ordered

- Continues down the list until the order shipment is filled

- Skips disabled sources if found in the list

To configure, arrange those sources from top to bottom in priority for fulfilling orders. The Source Selection Algorithm (SSA) provides an algorithm Priority using this order when determining shipment and inventory deductions. See [Prioritizing Sources for a Stock](stocks-prioritize-sources.md).

## Configure the priority of sources

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. Open a stock in edit mode and navigate to the _[!UICONTROL Sources]_ area.

1. Click **[!UICONTROL Assign Sources]**.

1. In the _[!UICONTROL Assign Sources]_ view, select the checkbox for the required source, and then click **[!UICONTROL Done]** to assign a source to the stock.

>[!NOTE]
>
>When using the [Distance Priority](distance-priority-algorithm.md) algorithm for shipping, if routes and data do not return for the selected [Computation mode](distance-priority-algorithm.md) (driving, bicycling, or walking) for a shipment, the SSA defaults to using the Source Priority.

![Source order after prioritization](assets/inventory-stock-priority-after.png)

| Icons                                        | Description                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| ![drag and drop the icon to set priority](assets/icon-drag-and-drop-action.png) | Use to drag and drop sources according to priority. |
| ![click icon to unassign a source](assets/icon-delete-action.png) | Unassigning a source to a stock. |
