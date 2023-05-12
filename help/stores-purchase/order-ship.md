---
title: Ship an order
description: Learn how to complete the shipping information for a processing order, and view shipment and tracking information.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
---
# Ship an order

An order that has been paid, but is awaiting shipment has the `Processing` status. The shipment record contains a detailed history of the fulfillment process associated with the order. Partial shipments can be made until the order is fulfilled.

1. On the _Admin_ sidebar, select **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. In the _[!UICONTROL Orders]_ list, find the order to be shipped and click to open it.

1. In the upper-right corner, click the **[!UICONTROL Ship]** button.

1. If you want to update the billing or shipping address, click the **[!UICONTROL Edit]** link in the upper-right corner of the section. 

   Make the necessary changes, and click **[!UICONTROL Save Order Address]**.

1. To have the carrier generate a shipping label, select the **[!UICONTROL Create Shipping Label]** checkbox and set the options:

   - To add a tracking number, scroll down to the _[!UICONTROL Shipping Information]_ section, and click **[!UICONTROL Add Tracking Number]**.

   - Do one of the following:

      - Select the **[!UICONTROL Carrier]** and enter the tracking **[!UICONTROL Number]**.

      - Set **[!UICONTROL Carrier]** to `Custom Value`, enter a **[!UICONTROL Title]** for the custom carrier, and enter the tracking **[!UICONTROL Number]**.

      - [View tracking information](#track-the-shipment).

1. To make a partial shipment, scroll down to the Items to Ship section, and enter the **[!UICONTROL Qty to Ship]** for each item.

1. To notify customers by email of the shipment, do the following:

   - Enter any comments that you would like to include in the **[!UICONTROL Shipment Comments]** box.

   - To include the comments in the notification email that is sent to the customer, select the **[!UICONTROL Append Comments]** checkbox.

   - To send a copy of the shipment email to yourself, select the **[!UICONTROL Email Copy of Shipment]** checkbox.

      The status of an invoice email appears next to the invoice number of the completed invoice as either sent or not sent.

1. When complete, click **[!UICONTROL Submit Shipment]**.

   The status of the order changes from `Processing` to `Complete`.

>[!NOTE]
>
>If an order is placed as an 'in-store delivery', shipping options are not available. Click **[!UICONTROL Notify Order is Ready for Pickup]** to trigger an email to the customer. The status of the order is then changed to `Complete`.

## View the shipment detail

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Find the shipment in the list, and click to open the record.

1. If you want to add a comment to the order, scroll down to the _[!UICONTROL Comments History]_ section, and enter the comment in the box.

   - To send the comment to the customer by email, select the **[!UICONTROL Notify Customer by Email]** checkbox.

   - To post the comment in the customer's account, select the **[!UICONTROL Visible on Frontend]** checkbox.

1. Click **[!UICONTROL Submit Comment]**.

## Track the shipment

**Method 1:** From order information tab

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Find the shipment order in the grid, and click **[!UICONTROL View]**.

1. Scroll down to the _[!UICONTROL Shipping & Handling Information]_ section and click **[!UICONTROL Track Order]**.

   Any available tracking information appears in a popup window.

1. When ready, click **[!UICONTROL Close Window]**.

**Method 2:** From order shipment tab

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Find the shipment in the list, and click to open the record.

1. Click **[!UICONTROL Track this Shipment]**.

   Any available tracking information appears in a popup window.

1. When ready, click **[!UICONTROL Close Window]**.
