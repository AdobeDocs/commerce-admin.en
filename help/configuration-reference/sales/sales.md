---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Sales]'
description: Review the configurations settings on the [!UICONTROL Sales] &gt; [!UICONTROL Sales] page of the Commerce Admin.
exl-id: 29091aab-e608-4e68-a6fe-f2808c78581c
feature: Configuration, Orders
---
# [!UICONTROL Sales] > [!UICONTROL Sales]

{{config}}

## [!UICONTROL General]

![General](./assets/sales-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/marketing/sales-documents-ref-id.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Hide Customer IP]|Store View|Determines if the customer IP address appears on orders, invoices, shipments, and credit memos. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL Checkout Totals Sort Order]

![Checkout Totals Sort Order](./assets/sales-checkout-totals-sort-order.png)<!-- zoom -->

<!-- [Checkout Totals Sort Order](https://docs.magento.com/user-guide/sales/checkout-totals-sort-order.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Subtotal]|Website|A number that determines when the subtotal is calculated in relation to other checkout totals. Default value: `10`|
|[!UICONTROL Discount]|Website|A number that determines when the discount is calculated in relation to other checkout totals. Default value: `20`|
|[!UICONTROL Shipping]|Website|A number that determines when the shipping is calculated in relation to other checkout totals. Default value: `30`|
|[!UICONTROL Tax]|Website|A number that determines when tax is calculated in relation to other checkout totals. Default value: `40`|
|[!UICONTROL Fixed Product Tax]|Website|A number that determines when the Fixed Product Tax is calculated in relation to other checkout totals. Default value: `50`|
|[!UICONTROL Grand Total]|Website|A number that determines when the Grand Total is calculated in relation to other checkout totals. Default value: `100`|

{style="table-layout:auto"}

## [!UICONTROL Reorder]

![Reorder](./assets/sales-reorder.png)<!-- zoom -->

<!-- [Reorder](https://docs.magento.com/user-guide/sales/reorders-allow.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Allow Reorder]|Store View|Determines if the customers can reorder from their accounts. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL Allow Zero Grand Total]

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Allow Zero Grand Total for Credit Memo]|Store View|Determines the possibility of creating a Credit Memo with a Zero Grand Total. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL Invoice and Packing Slip Design]

![Invoice and Packing Slip Design](./assets/sales-invoice-packing-slip-design.png)<!-- zoom -->

<!-- [Invoice and Packing Slip Design](https://docs.magento.com/user-guide/marketing/sales-document-pdf-logo.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Logo for PDF Print-outs]|Store View|Identifies the logo file that appears in the header of PDF invoices and packing slips. Allowed file types: <br/>JPG/JPEG <br/>TIF/TIFF <br/>PNG|
|[!UICONTROL Logo for HTML Print View]|Store View|Identifies the logo file that appears in the header of HTML print view of invoices and packing slips. Allowed file types: <br/>JPG /JPEG <br/>GIF <br/>PNG|
|[!UICONTROL Address]|Store View|The store address as you want it to appear on invoices and packing slips.|

{style="table-layout:auto"}

## [!UICONTROL Minimum Order Amount]

![Minimum Order Amount](./assets/sales-minimum-order-amount.png)<!-- zoom -->

<!-- [Minimum Order Amount](https://docs.magento.com/user-guide/sales/cart-minimum-order-amount.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable]|Website|Determines if a minimum order amount is set for the site. Options: `Yes` / `No`|
|[!UICONTROL Minimum Amount]|Website|Specifies the minimum subtotal, order after discounts are applied.|
|[!UICONTROL Include Discount Amount]|Website|Determines if the minimum order amount includes applied discounts. Options: `Yes` / `No`|
|[!UICONTROL Include Tax to Amount]|Website|Determines if the minimum order amount includes tax. Options: `Yes` / `No`|
|[!UICONTROL Description Message]|Store View|Determines the message that appears at the top of the shopping cart when the cart total is less than the minimum order amount. If left blank, the following default message appears: `Minimum order amount is $[minimum_amount]`|
|[!UICONTROL Error to Show in Shopping Cart]|Store View|Determines the message that appears from the mini cart or checkout link when the order amount is less than the minimum order amount required. If left blank, a default message appears.|
|[!UICONTROL Validate Each Address Separately in Multi-address Checkout]|Website|For multi-item orders, determines if order items going to separate addresses much meet the minimum order amount. Options: `Yes` / `No`|
|[!UICONTROL Multi-address Description Message]|Store View|For multi-address orders, determines the message that appears in the shopping cart if the items sent to an address are less than the minimum order amount.|
|[!UICONTROL Multi-address Error to Show in Shopping Cart]|Store View|For multi-address orders, determines the message that appears from the mini cart or checkout link when the order amount is less than the minimum order amount required. If left blank, a default message appears.|

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![Dashboard](./assets/sales-dashboard.png)<!-- zoom -->

<!-- [Dashboard](https://docs.magento.com/user-guide/stores/admin-dashboard.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Use Aggregated Data]|Global|Determines if real-time, aggregated sales data is used to produce dashboard snapshot reports. If you have a large amount of data to process, performance can be improved by turning off the display of real-time data. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL Orders Cron Settings]

![Orders Cron Settings](./assets/sales-orders-cron-settings.png)<!-- zoom -->

<!-- [Orders Cron Settings](https://docs.magento.com/user-guide/system/cron.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Pending Payment Order Lifetime]|Website|Determines the lifetime of pending orders in minutes. Default setting: `480` minutes (8 hours)|

{style="table-layout:auto"}

## [!UICONTROL Gift Options]

![Gift Options](./assets/sales-gift-options.png)<!-- zoom -->

<!-- [Gift Options](https://docs.magento.com/user-guide/sales/gift-options.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Allow Gift Messages on Order Level]|Website|Specify whether a gift message can be added for the entire order.|
|[!UICONTROL Allow Gift Messages on Order Items]|Website|Specify whether a gift message can be added for an individual order item.|
|[!UICONTROL Allow Gift Wrapping on Order Level]|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only) Specify whether gift wrapping can be added for the entire order.|
|[!UICONTROL Allow Gift Wrapping for Order Items]|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only) Specify whether gift wrapping can be added for the individual order item.|
|[!UICONTROL Allow Gift Receipt]|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only) Specify whether a gift receipt can be added for the order.|
|[!UICONTROL Allow Printed Card]|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only) Specify whether a printed card can be added for the order.|
|[!UICONTROL Default Price for Printed Card]|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only) Specify the default price for the printed card.|

{style="table-layout:auto"}

## [!UICONTROL Minimum Advertised Price]

![Minimum Advertised Price](./assets/sales-minimum-advertised-price.png)<!-- zoom -->

<!-- [Minimum Advertised Price](https://docs.magento.com/user-guide/catalog/product-price-minimum-advertised.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable MAP]|Website|Activates Minimum Advertised Price for your store. Options: `Yes` / `No`|
|[!UICONTROL Display Actual Price]|Website|Determines where the actual price of a product is visible to the customer. Options: <br/>**`In Cart`** - Displays the actual product price in the shopping cart. <br/>**`Before Order Confirmation`** - Displays the actual product price at the end of the checkout process, just before the order is confirmed. <br/>**`On Gesture`** - Displays the actual product price in a popup when the customer clicks the "Click for price" or "What's this?" link.|
|[!UICONTROL Default Popup Text Message]|Store View|The text message that appears when the customer selects the "Click for price" link from a category list or product view page.|
|[!UICONTROL Default "What's This" Text Message]|Store View|The text message that appears when the customer clicks the "What's this?" link from the product view page.|
|[!UICONTROL Manufacturer's Suggested Retail Price]|Global|The retail price as suggested by the manufacturer (MSRP).|

{style="table-layout:auto"}

## [!UICONTROL Multicoupon Settings]

{{ee-feature}}

![Multicoupon Settings](./assets/sales-multicoupon-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Maximum number of coupons per order]|Website|Determines the maximum number of coupons allowed per order|

{style="table-layout:auto"}

## [!UICONTROL Order by SKU Settings]

{{ee-feature}}

![Order by SKU Settings](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

<!-- [Order by SKU Settings](https://docs.magento.com/user-guide/customers/account-dashboard-order-by-sku.html) -->

![Order by SKU Settings for Customer Group](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Order by SKU on My Account in Storefront]|Website|Determines if Order by SKU is available in the customer account dashboard. Options: <br/>**`Yes, for Everyone`** - The Order by SKU tab appears in the account dashboard of all customers. <br/>**`Yes, for Specified Customer Groups`** - The Order by SKU tab appears in the account dashboard for members of specified groups or a shared catalog. <br/>**`No`** - The Order by SKU tab is not available in the customer account.|
|[!UICONTROL Customer Groups]|Website|Determines the Customer Groups. Options: `General` / `Retailer` / `Wholesale`|

{style="table-layout:auto"}

## [!UICONTROL Instant Purchase]

![Instant Purchase](./assets/sales-instant-purchase.png)<!-- zoom -->

<!-- [Instant Purchase](https://docs.magento.com/user-guide/sales/checkout-instant-purchase.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled]|Store View|Enables Instant Purchase for the store view, if the payment method, such as Braintree, has vault enabled. Options: `Yes` / `No`|
|[!UICONTROL Button Text]|Store View|Specifies the text that appears on the Instant Purchase button. The default text is `Instant Purchase`.|

{style="table-layout:auto"}

## [!UICONTROL Rate Limiting]

![Rate Limiting](assets/sales-rate-limiting.png)<!-- zoom -->

| Field                                                  |[Scope](../../getting-started/websites-stores-views.md#scope-settings)| Description                                                                                                                                                                        |
|--------------------------------------------------------|--- |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable rate limiting for placing orders]   |Store View| Determines if rate limiting is used for placing orders from the store view (default is `No`). Options: `Yes` / `No`.                                                                                 |
| [!UICONTROL Requests limit per authenticated customer] |Store View| The number of purchase requests that an authenticated customer can make during the period. The default limit is `10`.                                                              |
| [!UICONTROL Requests limit per guest]                  |Store View| The number of purchase requests that an unauthenticated customer can make during the specified period. The default value is `50`.                                                                 |
| [!UICONTROL Counter resets in a ...]                   |Store View| The time period during which an authenticated/unauthenticated customer can make a certain number of purchase requests (default is `Minute`). Options: `Minute` / `Hour` /`Day` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]

{{ee-feature}}

![Orders, Invoices, Shipments, Credit Memos Archiving](./assets/sales-orders-invoices-shipments-credit-memos-archiving.png)<!-- zoom -->

For more information about changing these settings, see [Configure the order archive](../../stores-purchase/order-archive.md#configure-the-order-archive) in the _Stores and Purchase Experience Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Archiving]|Global|Determines if archiving is enabled. Options: `Yes` / `No`|
|[!UICONTROL Archive Orders Purchased]|Global|Determines the number of days that pass before a completed order is archived. Default value: `30`|
|[!UICONTROL Order  Statuses to be Archived]|Global|Determines the [status](../../stores-purchase/order-status.md) of orders to be archived. By default, orders with a status of either Complete or Closed are archived. Options: `Pending` / `Processing` / `Suspected Fraud` / `Complete` / `Closed` / `Canceled` / `On Hold`|

{style="table-layout:auto"}

## [!UICONTROL RMA Settings]

{{ee-feature}}

![RMA Settings](./assets/sales-rma-settings.png)<!-- zoom -->

For more information about changing these settings, see [Configure returns](../../stores-purchase/rma-configure.md) in the _Stores and Purchase Experience Guide_.

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable RMA on Storefront]|Website|Determines if customers can create and view RMA requests from the storefront. RMA can be applied to both new and existing orders. By default, RMA is not enabled for the storefront. Options: `Yes` / `No`|
|[!UICONTROL Enable RMA on Product Level]|Website|Determines the default value for the Enable RMA field in product information.|
|[!UICONTROL Use Store Address]|Website|Determines the contact name and address that is used for shipments of returned merchandise. Options: <br/>**`Yes`** - Uses the [Point of Origin](../../stores-purchase/shipping-settings.md#point-of-origin) address from Shipping Settings. <br/>**`No`** - Opens the address form so you can enter an alternate address.|

{style="table-layout:auto"}
