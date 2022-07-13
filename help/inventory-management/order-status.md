---
title: Order Status and Reservations
description: Learn about automatic reservation entry or changes that update the salable quantity for a stock (or sales channel) and the on-hand inventory quantity per source.
exl-id: d264cb49-5aa8-4949-ae87-5efcd463d38c
---
# Order Status and Reservations

[!DNL Inventory Management] supports partial and full invoicing, payments, shipping, and cancellations per order. As you manage an order through processing, invoicing, shipment, and potentially refunds, [!DNL Commerce] automatically enters or changes reservations to update the salable quantity for a stock (or sales channel) and the on-hand inventory quantity per source. You do not have to actively access or enter reservations. Completing actions to fulfill, cancel, or refund an order does it for you.

These reservations always add to your salable quantity, with positive or negative amounts to increase or decrease quantities. These reservations are compensations, updating your on-hand inventory and salable quantities for up-to-date amounts for your store.

For specifics on orders and shipments, see [Managing Orders and Shipments](shipments.md).

## Order management options

Depending on inventory status and customer requests, you can update orders with partial payments and cancellations, partial shipments from multiple sources or for back orders, or credit memos to refund returned products.

### Shipments

After invoicing orders, send partial or full shipments until you fulfill the entire order. Each shipment converts reservation, deducting the amount from the product quantity per source. Reservation compensations enter to update the salable quantity for your stock. If you send partial shipments, each shipment deducts that amount from your product quantity and reservations. Any unshipped product reservations remain in place until they are also shipped, so that your salable amount is current and to give you control over product inventory and support multiple source shipments and backorders.

### Canceled orders

If a customer cancels their order before shipment (partial or in full), a new reservation is entered to return the inventory amount to the salable quantity. The reservations effectively cancel each other out, not deducting the quantity from any sources. Other customers can actively purchase those product quantities through the associated stocks and sales channels.

### Refunded orders

If a customer requests a refund, issue the credit memo for the partial or full product amounts. When you receive the returned products, enter a credit memo to provide the funds and update product amounts. When selecting the Return to Stock option, [!DNL Commerce] adds quantities back to the products and sources that shipped the orders and reservation compensations to update salable quantities for the associated stock.

## Order types

Simple orders begin with a shopping cart, continue to payment, and end with a satisfied delivery. In these orders, [!DNL Inventory Management] easily processes reservations against the availability (or salable quantity) in the cart and checkout, and deducts from the on-hand inventory at shipment.

![Process for a simple order](assets/diagram-simple-order-flow.png)

A more complicated order may have partial cancellations, partial shipments, and refunds. In these situations, reservations affect the available inventory to add quantities for cancellations and refunds and decrease quantities when ordered and shipped.

![Process for a complicated order](assets/diagram-complicated-order-flow.png)

Availability reservations and inventory changes occur based on the order status.

## Status and reservations

The following tables detail order and credit memo status with reservation changes entered by [!DNL Commerce] to manage your inventory.

|Order Status|Description|Reservation for Salable Quantity|
|--|--|--|
|[!UICONTROL Open]|New and recently submitted, no processing|Reservation is saved when order is submitted for the stock.|
|[!UICONTROL Canceled]|Canceled in partial or full before payment|Reservation compensation is entered to return partial or full quantity back to the stock salable quantity.|
|[!UICONTROL On Hold]|Payment and shipping not processed or invoiced|Reservation stays in place.|
|[!UICONTROL Suspected Fraud]|Not processed due to fraud|If approved or in review, the reservation stays in place.<br/>If declined, the reservation stays in place until the merchant makes a decision.<br/>If canceled, the reservation compensation is entered to return full quantity back to the stock salable quantity.|
|[!UICONTROL Pending]|Waiting for payment|The reservation stays in place.|
|[!UICONTROL Processing]|Payment processing, not received|The reservation stays in place.|
|[!UICONTROL Pending Payment]|Payment not received|The reservation stays in place.|
|[!UICONTROL Payment Review]|Payment being reviewed for processing and completion|The reservation stays in place.|
|[!UICONTROL Complete]|Paid and shipped in full|The reservation amount is deducted from the product quantity for the selected source when invoiced partial or in full. The reservation compensation is entered to update the total salable quantity.|
|[!UICONTROL Closed]|Refunded or archived|If archived, there is no change in quantities. If refunded in partial or full, the reservation compensation is entered and converted to add back product quantities per source and salable quantity per stock.|

|Credit Memo Status|Description|Reservation for Salable Quantity|
|--|--|--|
|[!UICONTROL Open]|The refund is due, not completed|There is no change in reservations.|
|[!UICONTROL Refunded]|Completed, funds returned|If refunded in partial or full, the reservation compensation is entered and converted to add back product quantities per source and salable quantity per stock.|

## Example complex order

Jenny Sanders orders bikes and clothing for her family vacation and fun. She sees some great sales on your Biking Adventures store with stock and sources spanning the United States, Canada, and Europe.

She buys two great park bikes for her daughters, a BMX bike for her son, a nice mountain bike for herself, and a modern German cross-country bike for her husband. The store had a sale on cute shirts, so she bought some for the whole family to match. See the list of vacation purchases below, the matching SKUs, and the reservations entered against the stock salable quantities.

![Complex order](assets/diagram-order-complex.png)

She shows her family what she found, but makes some changes. Before payment completes, she cancels two of the 33-BikeFun SKUs (her daughters did not like them). This is a partial cancellation due to payment pending, so no credit memo needed. To update, [!DNL Commerce] adds back to the salable quantity stock for Canada. The order is paid, and all products ship, arriving in time for vacation. [!DNL Commerce] updates the salable quantity and source quantities for the shipping warehouses for the shipped products.

But the shirt didn't quite fit her husband. Jenny requests a refund and sends back his shirt. The creation of the credit memo adds one 54-BikeLife shirt back to the Canada stock and shipping warehouse.

- **Shipped products** - With products purchased and shipped, [!DNL Commerce] updates the inventory. Reservation compensations convert to on-hand inventory quantity deductions from the shipped source. The available salable quantity updates for the stock.

- **Canceled products** - By canceling stock, [!DNL Commerce] removes the reservation for that product. Reservation compensation is entered to the stock level to add back salable quantities for the partial cancellation of two shirts. This does not affect the inventory quantity at the source level.

- **Credit Memo/Refunded product** - By returning stock, it must be added back to the quantities. When issuing the credit memo, you can select to return to stock. [!DNL Commerce] adds back inventory quantity to the shipped source for the product. Reservation compensations enter to clear any remaining reservations. The salable quantity recalculates against the updated quantity.

![Order refund quantity updates](assets/diagram-order-refund.png)
