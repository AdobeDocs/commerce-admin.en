---
title: Add an inventory tock
description: Learn how to add a stock and map sources to sales channels (websites), providing a direct link to salable quantities and product inventories.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
---
# Add a stock

Stocks map your sources to sales channels (or websites), providing a direct link to salable quantities and product inventories.

When creating a custom stock, you assign websites and sources. Sources can include enabled and disabled sources. For example, you might add a warehouse to your stock, preparing to open the location for managing inventory and completing shipments.

After adding sources, you must prioritize the order for the sources from top (first) to bottom (last). This order affects recommendations during order shipment.

![New Stock](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## Add the inventory stock

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_ > **[!UICONTROL Stock]**.

1. Click **[!UICONTROL Add New Stock]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL General]** section and enter a unique **[!UICONTROL Name]** to identify the new stock.

   ![General stock options](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Sales Channels]** section and select the **[!UICONTROL Websites]** where this stock is available.

   For a multisite installation, hold down the Ctrl key (PC) or the Command key (Mac) and click each website.

   >[!NOTE]
   >
   >If you select a website or sales channel assigned to another stock, it is unassigned from that stock. Any Sales Channels not assigned to a custom stock are assigned to the Default Stock.

   ![Sales Channels options for  stocks](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Sources]** section and do the following for any stock other than the default:

    - Click **[!UICONTROL Assign Sources]**.

    ![Assigned Sources](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

    - Select checkboxes for all sources that you want to assign to the stock.

   >[!IMPORTANT]
   >
   >If you assign the same source to multiple stocks, it could result in overselling of the products assigned to that source.

    - Click **[!UICONTROL Done]**.

      The added sources display in Assigned Sources.

      ![Assign Sources to Stock](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. Use ![Sort icon](assets/icon-sort.png) to drag and drop the sources into a priority from top (first) to bottom (last).

   The source order is important when shipping orders.

   ![Assigned Sources Example](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. On the _[!UICONTROL Save]_ (![Menu arrow](../assets/icon-menu-down-arrow-red.png)) menu, choose **[!UICONTROL Save & Close]**.

## Field descriptions

|Field|Description|
|--|--|
|**[!UICONTROL General]**| |
|[!UICONTROL Name]|Name for the stock. For example: `UK Stock`, `US Stock`|
|**[!UICONTROL Sales Channels]**| |
|[!UICONTROL Websites]|Defines the [scope](../getting-started/websites-stores-views.md#scope-settings) of the stock by assigning the stock to specific websites as _sales channels_. Select one or more websites per stock. Each website can only be assigned to one stock.|
|**[!UICONTROL Sources]**| |
|[!UICONTROL Assign Sources]|Assigns inventory sources to this stock. Custom sources cannot be assigned to Default Stock.|
|[!UICONTROL Assigned Sources]|List of assigned sources. Drag and drop the sources using ![Sort icon](assets/icon-sort.png) into a prioritized order for order fulfillment and shipping.<br/><br/>**[!UICONTROL Code]** - Unique code ID for the source.<br/>**[!UICONTROL Name]** - Name description for the source.<br/>**[!UICONTROL Unassign]** - Remove the assigned source from the stock using ![Trash icon](../assets/icon-delete-trashcan-solid.png).|
