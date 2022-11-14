---
title: Shipments
description: Learn how to create shipment records for invoices and to cancel shipments.
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
---
# Shipments

The _[!UICONTROL Shipments]_ grid lists the shipment record of all invoices that have been prepared for shipping. A shipment record can be generated when an order is [invoiced](invoices.md) or later.

Adobe Commerce and Magento Open Source support partial and complete order shipment, with additional options available from [Inventory Management](../inventory-management/introduction.md) and third-party extensions.

![Shipments grid](./assets/shipments.png)<!-- zoom -->

## Column descriptions

|Column or control|Description|
|--- |--- |
|[!UICONTROL Select]|Select the checkbox for each quote to be subject to an action, or use the selection control in the column header. Options: `Select All` / `Deselect All`|
|[!UICONTROL Shipment]|A unique, sequential number that is assigned when a new shipment is saved for the first time|
|[!UICONTROL Ship Date]|Shipping date|
|[!UICONTROL Order]|Unique number of the order|
|[!UICONTROL Order Date]|The date and time the order was placed|
|[!UICONTROL Ship-to Name]|The name of the person to whom the order is shipped|
|[!UICONTROL Total Quantity]|Total quantity of items to ship|
|[!UICONTROL Action]|View opens the shipment in edit mode|

{style="table-layout:auto"}

Additional columns:

|Column|Description|
|--- |--- |
|[!UICONTROL Order Status]|Indicates the order status|
|[!UICONTROL Purchased From]|Indicates the website, store, and store view where the order was placed|
|[!UICONTROL Customer Name]|The name of the customer or buyer who placed the order|
|[!UICONTROL Email]|The email address of a registered customer|
|[!UICONTROL Customer Group]|The name of the customer group or shared catalog to which the customer is assigned|
|[!UICONTROL Billing Address]|The name of the customer or buyer who placed the order|
|[!UICONTROL Shipping Address]|The name of the person to whom the order is shipped|
|[!UICONTROL Payment Method]|The method of payment to be used for the order|
|[!UICONTROL Shipping Information]|The method that is to be used to ship the order|

{style="table-layout:auto"}

## Create a shipment

The following instructions walk you through the process to create a shipment in Adobe Commerce or Magento Open Source. If you have Inventory Management enabled, you may want to review [Create Multi-Source Shipments](../inventory-management/shipments-create.md) and select a source (or location) and a quantity to send per line item. 

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Find the order in the grid and open it.

1. If the order is paid, invoiced, and ready to ship, click **[!UICONTROL Ship]**.

   The sections at the top of the shipment contain name, address, and payment information from the sales order.

1. Complete each section of the shipment form using the instructions in the following sections.

### [!UICONTROL Items to Ship]

For each line item in the order, modify the **[!UICONTROL Qty to Ship]** as needed.

### [!UICONTROL Shipping Information]

**Method 1:** Using the order page

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. In the **[!UICONTROL Action]** column for the selected order, click **[!UICONTROL View]**.

1. Click **[!UICONTROL Ship]**.

1. Scroll down to the _[!UICONTROL Payment & Shipping Method]_ block and click **[!UICONTROL Add Tracking Number]**.

1. Set **[!UICONTROL Carrier]**:

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. Enter **[!UICONTROL Title]** and **[!UICONTROL Number]** to track the shipment.

**Method 2:** Using the shipment page

This method is only allowed if the order shipment has already been created from the order page.
You can modify shipping and tracking information as needed using the direct shipment page:

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Find and open the shipment in edit mode.

1. Scroll down to the _[!UICONTROL Payment & Shipping Method]_ block.

1. Select the **[!UICONTROL Carrier]**.

1. Enter a **[!UICONTROL Title]** for the package.

1. Enter the tracking **[!UICONTROL Number]**.

1. Click **[!UICONTROL Add]**.

1. To send an email with tracking information to customer, click **[!UICONTROL Send Tracking Information]**, and confirm the action.

   To track the location of any shipment, open the required shipment in edit mode and click **[!UICONTROL Track this shipment]**.

   ![Shipping and Tracking Information](./assets/tracking-information.png)<!-- zoom -->

### Buttons

|Button|Description|
|--- |--- |
|**[!UICONTROL Back]**|Closes the New Shipment form, and returns to the order|
|**[!UICONTROL Submit Shipment]**|Adds the shipment for the order.|
|**[!UICONTROL Reset]**|Restores all fields to original values.|

{style="table-layout:auto"}

### Shipping comments

1. Enter **Comments** for the shipment, if needed.

1. When the shipment is ready, click **Submit Shipment**.

## Set up comments for shipments

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. Under _[!UICONTROL Sales]_, select **[!UICONTROL Sales Email]**.

1. Expand the **Shipment Comments** section and modify the settings as needed:

   ![Shipment comment configuration](./assets/shipment-comments.png)<!-- zoom -->

   - The **[!UICONTROL Enabled]** option is set to `Yes` by default, which means that the email is sent to a customer when a shipping comment is entered.

   - For **[!UICONTROL Shipment Comment Email Sender]**, select the person from whom the shipment comment email is sent. The default offers five email addresses.

   - For **[!UICONTROL Shipment Comment Email Template]**, select the template based on your requirement or select the default option.

   - For **[!UICONTROL Shipment Comment Email Template for Guests]**, choose the template used for customers who do not have an account in your store.

   - For **[!UICONTROL Shipment Comment Email Copy To]**, enter the email addresses to send a shipment comment email copy. Separate multiple email addresses with a comma.

   - For **[!UICONTROL Shipment Comment Email Copy Method]**, select `bcc` (blind carbon copy) or `separate email copy` method based on your preference.

1. Click **[!UICONTROL Save Config]**.

## Cancel a shipment

Before a shipment is dispatched to a carrier, it can be canceled by opening the order and navigating to the shipment, provided the carrier supports cancellations. Some carriers restrict or limit cancellations after a booking. For example, UPS allows cancellations, but requires that you wait 24 hours after the shipment is booked. If a shipment is canceled, the cancellation cannot be reversed. The only recourse is to recreate the order.

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Find the order in the grid.

1. In the _Action_ column, choose **[!UICONTROL View]**.

1. In the left panel, choose **[!UICONTROL Shipments]**.

   If the shipment can be canceled, _[!UICONTROL Cancel Shipment]_ appears as an option in the top button bar.

1. Click **[!UICONTROL Cancel Shipment]**.

1. When prompted to confirm, click **[!UICONTROL OK]**.

The status of the shipment changes to `Canceled`. If the carrier does not support cancellations, an error message appears and explains why the shipment could not be canceled.

## Shipment field descriptions

### [!UICONTROL Shipping Information]

|Field|Description|
|-----|-----------|
|[!UICONTROL Carrier]|The name of the selected carrier|
|[!UICONTROL Title]|A descriptive name assigned to the package by the carrier.|
|[!UICONTROL Number]|The linked tracking number that is assigned to the package.|
|[!UICONTROL Action]|![Trashcan icon](../assets/icon-delete-trashcan-solid.png) - Deletes the package information from the shipment record.|
|[!UICONTROL Add]|Add another package to the shipment.|

{style="table-layout:auto"}

### [!UICONTROL Route Information]

|Field|Description|
|-----|-----------|
|[!UICONTROL Origin Location]|Displays a list of available locations.|
|[!UICONTROL International]|If checked, identifies the shipment as an international shipment.|

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

|Field|Description|
|-----|-----------|
|[!UICONTROL Description]|The description of the item.|
|[!UICONTROL SKU]|The Stock Keeping Unit of the item.|
|[!UICONTROL Weight]|The weight of the item.|
|[!UICONTROL Qty Ordered]|The quantity of the item that was ordered.|
|[!UICONTROL Qty Shipped]|The quantity of items that have been shipped.|
|[!UICONTROL Qty Packed]|The number of items included in this package.|

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

|Field|Description|
|-----|-----------|
|[!UICONTROL Comments]|Comments about the shipment are for internal use.|

{style="table-layout:auto"}

### [!UICONTROL Documentation]

|Field|Description|
|-----|-----------|
|[!UICONTROL Package Label]|**PNG** - Download the shipment package label. Size: A6 (105 x 148mm; 4.1 x 5.6 in.)|

{style="table-layout:auto"}
