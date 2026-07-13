---
title: "[!UICONTROL Sales] menu"
description: The Commerce Admin includes the [!UICONTROL Sales] menu, which provides access to tools for working with orders according to where they are in the workflow.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
TQID: https://experienceleague.adobe.com/mliJ1Q1-DEkR5rAoIRLQ9qBxQopBytjicPiqzWTg7ac
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
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# [!UICONTROL Sales] menu

The Sales menu lists transactions according to where they are in the order workflow. You might think of each of option as a different stage in the lifetime of an order.

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."}

![Sales menu](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE SaaS only]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service and Adobe Commerce Optimizer projects only (Adobe-managed SaaS infrastructure)."}

![Sales menu](./assets/admin-menu-sales-accs.png){width="450" zoomable="yes"}

>[!ENDTABS]

## Display the [!UICONTROL Sales] menu

On the _Admin_ sidebar, click **[!UICONTROL Sales]**.

## Menu options

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (Available with Adobe Commerce B2B)

Authorized buyers can [negotiate the price](../b2b/quotes.md) with the seller by sending a [request](../b2b/quote-request.md) from the shopping cart.

### [!UICONTROL Quote Templates]

![Adobe Commerce B2B](../assets/b2b.svg) (Available with Adobe Commerce B2B)

Allows buyers and sellers to streamline the quote process by creating reusable and customizable [quote templates](../b2b/quote-templates-overview.md).

### [!UICONTROL Orders]

When an [order](orders.md) is placed, a sales order is created as a temporary record of the transaction. Payment has not been processed, and the order can still be canceled.

### [!UICONTROL Invoices]

An [invoice](invoices.md) is a record of the receipt of payment for an order. Multiple invoices can be created for a single order, each with as many, or as few of the purchased products that you specify. Depending on the payment action, payment can be automatically captured when the invoice is generated.

### [!UICONTROL Shipments]

A [shipment](shipments.md) is a record of the products in an order that have been shipped. As with invoices, multiple shipments can be associated with a single order, until all products in the order are shipped.

### [!UICONTROL Credit Memos]

A [credit memo](credit-memos.md) is a document that shows the amount that is due the customer for a full or partial refund. The amount can be applied toward a purchase or refunded to the customer.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)

A [returned merchandise authorization](returns.md) (RMA) can be granted to customers who request to return an item for replacement or refund. RMAs can be issued for Simple, Grouped, Configurable, and Bundle product types. However, RMAs are not available for virtual and downloadable products, or gift cards.

### [!UICONTROL Billing Agreements]

[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."}

A [billing agreement](paypal-billing-agreements.md) is similar to a purchase order, except that it isn't limited to a single purchase. During checkout, the customer chooses Billing Agreement as the payment method. A billing agreement streamlines the checkout process because the customer doesn't have to enter payment information for each purchase.

### [!UICONTROL Transactions]

The [Transactions](transactions.md) page lists all payment activity that has taken place between your store and all payment systems, and provides access to more detailed information.

### [!UICONTROL Braintree Virtual Terminal]

[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."}

On the Braintree Virtual Terminal page, an Admin user can accept the payment for the selected amount. To make the terminal feature available, a merchant should configure basic [Braintree settings](braintree.md). Braintree offers a fully customizable checkout experience with fraud detection and PayPal integration.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)

(Archive option must be enabled) [Archiving orders](order-archive.md) and other sales documents regularly improves performance and keeps your workspace free of unnecessary information.
