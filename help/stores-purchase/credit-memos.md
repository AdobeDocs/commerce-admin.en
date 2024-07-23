---
title: Credit memos
description: Learn about credit memos and how they are used to issue a partial or full refund.
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
---
# Credit memos

A _credit memo_ is a document that shows the amount that is due the customer for a full or partial refund. The amount can be applied toward a purchase or refunded to the customer. You can print a credit memo for a single order, or for multiple orders as a batch. Before a credit memo can be printed, it must first be generated for the order. The _Credit Memos_ page lists the credit memos that have been issued to customers.

![Credit Memos](./assets/credit-memos.png){width="700" zoomable="yes"}

## Refund method

The [payment method](payments.md) for the order determines, to an extent, the method by which you refund an order.

You can refund orders in three ways:

- Account credit---Orders paid using a credit account can be refunded as an account credit:
    - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) [Store Credit](../customers/store-credit-using.md)
    - ![Adobe Commerce B2B](../assets/b2b.svg) (Available with Adobe Commerce B2B) [Payment on Account](../b2b/enable-basic-features.md#configure-payment-on-account) (offline method)
    - ![Adobe Commerce B2B](../assets/b2b.svg) (Available with Adobe Commerce B2B) [Company Credit](../b2b/credit-company.md)
- [Online refund](payments.md#online-payment-methods)---Orders paid by credit card through a payment gateway, such as PayPal or Braintree, are refunded online via the payment processor.
- [Offline refund](payments.md#offline-payment-methods)---Orders that are paid by Cash on Delivery ([COD](cash-on-delivery.md)) or by [check or money order](check-money-order.md) are refunded offline.

You can issue an offline refund or account credit (if enabled) for any payment method.

An order that was paid by Cash on Delivery ([COD](cash-on-delivery.md)) or by [check or money order](check-money-order.md) is refunded offline.

## Refund workflow

1. **Payment action** - If the [Payment Action](credit-memo-create.md#payment-action-setting) configuration is set to `Authorize`, you must generate an invoice before creating a credit memo---proceed to step 2. If set to `Authorize and Capture`, an invoice has already been generated---proceed to step 3.

1. **Generate invoice** - [Create an invoice](invoices.md#create-an-invoice) for the order, so that you can send a refund to the customer via credit memo.

1. **Create credit memo** - [Issue a credit memo](credit-memo-create.md) in the Admin for a [credit purchase](credit-memo-create.md#issue-a-refund-for-a-credit-purchase), or a [check or money order](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order).

## Column descriptions

|Column|Description|
|--- |--- |
|[!UICONTROL Select]|Select the checkboxes for the credit memo items to be subject to an action, or use the selection control in the column header. Options: `Select All` / `Deselect All`|
|[!UICONTROL Credit Memo]|A unique numeric identifier that is assigned when a request for a credit memo is submitted.|
|[!UICONTROL Created]|The date and time the buyer first submitted the request for a credit memo.|
|[!UICONTROL Order#]|Order ID of the order whose products are being returned.|
|[!UICONTROL Order Date]|The date and time the buyer placed an order.|
|[!UICONTROL Bill-to Name]|The name of the person who is responsible to pay for the order.|
|[!UICONTROL Status]|Indicates the current state of a credit memo request.|
|[!UICONTROL Refunded]|The total amount refunded from the order.|
|[!UICONTROL Actions]|**[!UICONTROL View]** - Opens the request for a credit memo and maintains a record of the negotiation between buyer and seller.|
|[!UICONTROL Order Status]|Indicates the order status.|
|[!UICONTROL Purchased From]|Indicates the website, store, and store view where the order was placed.|
|[!UICONTROL Billing Address]|The billing address of the customer who placed the order.|
|[!UICONTROL Shipping Address]|The address where the order is to be shipped.|
|[!UICONTROL Customer Name]|The first and last name of the customer who placed the order.|
|[!UICONTROL Email]|The email address of the person who placed the order.|
|[!UICONTROL Customer Group]|The customer group to which the customer is assigned.|
|[!UICONTROL Payment Method]|The method of payment to be used for the payment.|
|[!UICONTROL Shipping Information]|The method to be used to ship the order.|
|[!UICONTROL Subtotal]|The order subtotal, without shipping and handling, and tax.|
|[!UICONTROL Shipping & Handling]|The amount charged for shipping and handling.|
|[!UICONTROL Adjustment Refund]|The amount that is added to the total amount refunded as an extra refund.|
|[!UICONTROL Adjustment Fee]|The amount that is subtracted from the total amount refunded.|
|[!UICONTROL Grand Total]|The order total.|

{style="table-layout:auto"}
