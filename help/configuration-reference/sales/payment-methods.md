---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods]'
description: Review the configurations settings on the [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] page of the Commerce Admin.
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
---
# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Payment Services for Adobe Commerce and Magento Open Source provides a turnkey self-service solution, including sandbox testing and a simple setup, for providing robust and secure payment processing. To learn more about this powerful tool set and how it can give you the insight and control you need to create the best experience for your buyers, see the [_Payment Services User Guide_](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

{{config}}

## [!UICONTROL Merchant Location]

![Merchant Location](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://docs.magento.com/user-guide/payment/merchant-location.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Merchant Country]|Website|Identifies the country where the merchant is registered to conduct business.|

{:style="table-layout:auto"}

## Recommended solutions

The following payment solutions are recommended as an easy way for merchants who are just starting out to accept online payment by PayPal account or credit card. As your business grows, you can combine these with additional PayPal payment solutions.

- [PayPal Express Checkout](paypal-express-checkout.md)
- [Braintree](braintree.md)
- [Payment Services](payment-services.md)

>[!NOTE]
>
>Some payment integrations and bundled extensions have been removed in 2.4.x releases and moved to Commerce Marketplace. You can find the latest official payment integration extensions in [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.
><br/>
>**Amazon Pay** and **Klarna**: Adobe Commerce and Magento Open Source releases 2.4.0 through 2.4.3 included these vendor-developed extensions. Starting with the 2.4.4 release, these extensions are no longer bundled with the core release and must be installed and updated from the Commerce Marketplace. The Marketplace also provides access to current documentation provided by the extension developer.
><br/>
>   If you have either of these bundled extension enabled and configured, you must update your `composer.json` file as part of the 2.4.4 upgrade process and to manage extension updates going forward. See [Upgrade modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) in the _Upgrade Guide_ for more information.
><br/><br/>
>**Worldpay**, **Eway**, **CyberSource**, and **Authorize.Net**: For details about making a secure transition from these payment integrations, see the [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Other PayPal methods

PayPal offers various payment solutions that meet the needs of businesses of every size, and that are engaged in business all over the world. PayPal gives you the ability to accept payments from all major debit and credit cards. PayPal offers additional convenience without extra effort, because even customers who don't have a PayPal account can pay for their purchases with PayPal.

### PayPal all-in-one methods

- [PayPal Payment Advanced](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

### PayPal payment gateways

- [PayPal Payflow Pro](paypal-payflow-pro.md) (Includes Express Checkout)
- [PayPal Payflow Link](paypal-payflow-link.md) (Includes Express Checkout)

## Basic payment methods

The following payment methods are built into Commerce and do not use a third-party payment provider to process the transaction. Many of the basic payment methods managed offline, rather than online.

### [!UICONTROL Check / Money Order]

![Check / Money Order](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://docs.magento.com/user-guide/payment/check-money-order.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled]|Website|Determines if customers can pay by check or money order. Options: `Yes` / `No`|
|[!UICONTROL Title]|Store View|The name for this payment method that appears to customers during checkout.|
|[!UICONTROL New Order Status]|Website|Determines the initial [order status](../../stores-purchase/order-status.md) assigned to orders paid by a check or money order. Default value: `Pending`|
|[!UICONTROL Payment from Applicable Countries]|Website|Determines the countries from which you accept payment by check or money order. Options: `All Allowed Countries` / `Specific Countries`|
|[!UICONTROL Payment from Specific Countries]|Website|Identifies the specific countries from which you accept payment by check or money order.|
|[!UICONTROL Make Check Payable to]|Store View|The name of the entity to whom checks and money orders should be made payable.|
|[!UICONTROL Send Check to]|Store View|The street address or PO Box where checks and money orders should be sent.|
|[!UICONTROL Minimum Order Total]|Website|The smallest order amount that can be paid by check or money order.|
|[!UICONTROL Maximum Order Total]|Website|The largest order amount that can be paid by check or money order. <br/><br/>**_Note:_** An order qualifies if the total is between, or matches, the minimum or maximum order total.|
|[!UICONTROL Sort Order]|Website|A number that determines the order that payment by check or money order appears when listed with other payment methods during checkout. Enter `0` to place it at the top of the list.|

{:style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![Bank Transfer Payment](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://docs.magento.com/user-guide/payment/bank-transfer.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled]|Website|Determines if customers can pay by  transferring payment directly from their bank to your merchant account. Options: `Yes` / `No`|
|[!UICONTROL Title]|Store View|The name for this payment method that appears to customers during checkout.|
|[!UICONTROL New Order Status]|Website|Determines the initial order status assigned to orders paid by bank transfer. Default value: `Pending`|
|[!UICONTROL Payment from Applicable Countries]|Website|Determines the countries from which you accept payment by bank transfer. Options: `All Allowed Countries` / `Specific Countries` |
|[!UICONTROL Payment from Specific Countries]|Website|Identifies the specific countries from which you accept payment by bank transfer.|
|[!UICONTROL Minimum Order Total]|Website|The smallest order amount that can be paid by bank transfer.|
|[!UICONTROL Maximum Order Total]|Website|The largest order amount that can be paid by bank transfer. <br/><br/>**_Note:_** An order qualifies if the total is between, or matches, the minimum or maximum order total.|
|[!UICONTROL Sort Order]|Website|A number that determines the order that payment by bank transfer appears when listed with other payment methods during checkout. Enter `0` to place it at the top of the list.|

{:style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![Payment on Account](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://docs.magento.com/user-guide/payment/payment-on-account.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled]|Website|Determines if companies can use company credit to make purchases. Options: `Yes` / `No`|
|[!UICONTROL Title]|Store View|The name for this payment method that appears to customers during checkout.|
|[!UICONTROL New Order Status]|Website|Determines the status of new orders charged to a company account. Options: `Pending (default)` / `Processing` / `Suspected Fraud` |
|[!UICONTROL Payment from Applicable Countries]|Website|Determines the countries where you allow companies to charge purchases to their accounts. Options: `All Allowed Countries` / `Specific Countries` |
|[!UICONTROL Payment from Specific Countries]|Website|Identifies the specific countries where companies can charge purchases to their accounts.|
|[!UICONTROL Minimum Order Total]|Website|Specifies the smallest order amount that can be charged to a company account.|
|[!UICONTROL Maximum Order Total]|Website|The largest order amount that can be charged to a company account. <br/><br/>**_Note:_** An order qualifies if the total is between, or matches, the minimum or maximum order total.|
|[!UICONTROL Sort Order]|Website|A number that determines the order that payment on account appears when listed with other payment methods during checkout. Enter `0` to place it at the top of the list.|

{:style="table-layout:auto"}

>[!NOTE]
>
>Payment on Account is not supported for orders with [multiple shipping addresses](../../stores-purchase/shipping-settings.md#multiple-addresses) and does not appear among the payment options.

### [!UICONTROL Cash On Delivery Payment]

![Cash On Delivery Payment](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled]|Website|Determines if customers can pay by transferring payment directly from their bank to your merchant account. Options: `Yes` / `No`|
|[!UICONTROL Title]|Store View|The name for this payment method that appears to customers during checkout.|
|[!UICONTROL New Order Status]|Website|Determines the initial order status assigned to orders paid by bank transfer. Default value: `Pending` |
|[!UICONTROL Payment from Applicable Countries]|Website|Determines the countries from which you accept payment by bank transfer. Options: `All Allowed Countries` / `Specific Countries` |
|[!UICONTROL Payment from Specific Countries]|Website|Identifies the specific countries from which you accept payment by bank transfer.|
|[!UICONTROL Minimum Order Total]|Website|Specifies the smallest order amount that can be paid by bank transfer.|
|[!UICONTROL Maximum Order Total]|Website|The largest order amount that can be paid by bank transfer. <br/><br/>**_Note:_** An order qualifies if the total is between, or matches, the minimum or maximum order total.|
|[!UICONTROL Sort Order]|Website|A number that determines the order that payment by bank transfer appears when listed with other payment methods during checkout. Enter `0` to place it at the top of the list.|

{:style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![Zero Subtotal Checkout](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Title]|Store View|The name that is used for this payment method during checkout. Default value: No Payment Information Required|
|[!UICONTROL Enabled]|Website|Determines if Zero Subtotal Checkout is available for the store administrator to manage orders that have a subtotal of zero, such as one that has been taxed, but a discount has reduced the amount to zero. Options: `Yes` / `No`|
|[!UICONTROL New Order Status]|Website|Determines the initial order status assigned to orders processed as Zero Subtotal Checkout. Default value: `Pending` |
|[!UICONTROL Payment from Applicable Countries]|Website|Determines the countries from which Zero Subtotal Checkout can be applied. Options: `All Allowed Countries` / `Specific Countries` |
|[!UICONTROL Payment from Specific Countries]|Website|Identifies the specific countries for which Zero Subtotal Checkout can be applied.|
|[!UICONTROL Sort Order]|Website|A number that determines the order that the title, such as "No Payment Information is Required", appears when listed with other payment methods during checkout. Enter `0` to place it at the top of the list.|

{:style="table-layout:auto"}

## [!UICONTROL Payment actions]

Payment actions are configured _per payment method_. The payment action determines when the funds are captured and when invoices are created for your sales orders.

See the Basic settings section of each individual payment method topic for a comprehensive list of individual configuration options.

|Payment Action |Description|
|--- |---|
|[!UICONTROL Authorization] |Approves the purchase, but puts hold on the funds. The amount is not withdrawn until is captured by the merchant.|
|[!UICONTROL Authorize] |Authorizes the buyer's account for the order total but does not capture the payment. Capture payment by creating an invoice. Authorized orders can be voided or canceled.|
|[!UICONTROL Authorize and Capture] |Authorizes the buyer's account for the order total and captures the payment. An invoice is automatically created. You can refund captured funds via credit memo. You cannot cancel an order once payment has been captured.|
|[!UICONTROL Charge on shipment] |Amazon receives a capture request and charges the customer when an invoice is created in Commerce.|
|[!UICONTROL Charge on order] |Amazon creates the invoice and charges the customer when the order is placed.|
|[!UICONTROL Not Capture] |When the invoice is submitted, the system does not capture the payment. It is assumed that you capture the payment through Commerce later. There is a Capture button in the completed invoice. Before capturing, you can cancel the invoice. After capturing, you can create a credit memo and void the invoice.|
|[!UICONTROL Order] |Represents an agreement with PayPal that allows the merchant to capture one or more amounts up to the order total from the customer's buyer account, within a defined time period (up to 29 days).|
|[!UICONTROL Sale] |Amount of the purchase is authorized and immediately withdrawn from the customer's account.|

{:style="table-layout:auto"}

>[!NOTE]
>
>Do not select the _[!UICONTROL Not Capture]_ option unless you are certain that you are going to capture the payment through Commerce later. You cannot create a credit memo until the payment has been captured using the Capture button.

## [!UICONTROL Purchase Order]

![Purchase Order](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled]|Website|Determines if customers can pay by purchase order (PO). Options: `Yes` / `No`|
|[!UICONTROL Title]|Store View|The name of this payment method that appears to customers during checkout.|
|[!UICONTROL New Order Status]|Website|Determines the initial [order status](../../stores-purchase/order-status.md) assigned to orders paid by PO. Default value: Pending|
|[!UICONTROL Payment from Applicable Countries]|Website|Determines the countries from which you accept payment by PO. Options: `All Allowed Countries` / `Specific Countries` |
|[!UICONTROL Payment from Specific Countries]|Website|Identifies the specific countries from which you accept payment by PO.|
|[!UICONTROL Minimum Order Total]|Website|The smallest order amount that can be paid by PO.|
|[!UICONTROL Maximum Order Total]|Website|The largest order amount that can be paid by PO. <br/><br/>**_Note:_** An order qualifies if the total is between, or matches, the minimum or maximum order total.|
|[!UICONTROL Sort Order]|Website|A number that determines the order that payment by PO appears when listed with other payment methods during checkout. Enter `0` to place it at the top of the list.|

{:style="table-layout:auto"}
