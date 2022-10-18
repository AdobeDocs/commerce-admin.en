---
title: PayPal payment solutions
description: Learn about the PayPal payment solution integrations that are available for your store.
---
# PayPal payment solutions

PayPal is a global leader in online payments and a fast and secure way for your customers to pay online. The selection of available PayPal solutions varies by merchant location. PayPal Express Checkout and PayPal Payments Standard can be used in all parts of the world. To learn more, see [PayPal solutions by country](#paypal-solutions-by-country).

>[!IMPORTANT]
>
>**PSD2 Requirements:** <br/>
>Beginning September 14, 2019, European banks may decline payments that do not meet [PSD2](../getting-started/compliance-payment-services-directive.md) requirements. For most PayPal solutions, no action is needed to comply with PSD2 because these requirements are handled by PayPal.

## PayPal business account

To offer PayPal as a payment method in your store, you must have a PayPal [business account][1] and/or a [PayPal Payflow account][2]. The account requirements are specified in the description of each PayPal solution. Your PayPal merchant account is also used to manage any [fraud filters](#paypal-fraud-management-filters) that are applied to purchases made from your store.

Customers who use PayPal Express Checkout or Express Checkout for Payflow Pro must have a PayPal buyer account. PayPal Payments Standard (Website Payments Standard in some countries) can be used directly or through a buyer account when that the merchant enables _PayPal Account Optional_. By default, this parameter is enabled so that customers can choose to enter their credit card information or create a buyer account with PayPal. When disabled, customers must first create a PayPal buyer account before making a purchase.

Website Payments Pro, Website Payments Pro Payflow Edition, Payflow Pro Gateway, and Payflow Link require customers to enter credit card information during checkout.

## PayPal Credit and Pay Later

PayPal Pay Later offers your customers quick access to financing, so they can buy now and pay over time, at no additional cost to you. You are not charged when customers choose PayPal Credit options, and you pay only your normal PayPal transaction fee. To learn more, see the [PayPal website][3].

Give your sales a boost when you advertise financing. PayPal helps turn browsers into buyers with financing with PayPal Pay Later. Your customers can pay over time, while you get paid up front---at no additional cost to you. Use PayPal free banner ads to advertise PayPal financing as a payment option when your customers check out with PayPal. The PayPal Advertising Program has been shown to generate additional purchases and increase average purchase sizes by 15% or more.

You can easily add free, ready-made banner ads to pages of your site and the _PayPal Credit_ button to your shopping cart during checkout to remind your customers that financing is readily available.

>[!NOTE]
>
>Starting with the 2.4.3 release, PayPal Pay Later is supported in deployments that include PayPal. This feature allows shoppers to pay for an order in bi-weekly installments instead of paying the full amount at time of purchase. The PayPal Credit experience is deprecated.

For US merchants, PayPal Credit is enabled by default for the [PayPal Express Checkout](paypal-express-checkout.md) payment option. To disable it for this payment method, see the _Features_ section of [PayPal Express Checkout configuration](paypal-express-checkout.md#features).

PayPal Credit is disabled by default for the other PayPal payment solutions, but can be enabled in the payment method configuration for supporting solutions:

- [Payments Advanced](paypal-payments-advanced.md)
- [Payments Pro](paypal-payments-pro.md)
- [Payments Standard](paypal-payments-standard.md)
- [Payflow Pro](paypal-payflow-pro.md)
- [Payflow Link](paypal-payflow-link.md)

>[!IMPORTANT]
>
>Before you configure PayPal Credit or PayPay Pay Later for your store, make sure it is enabled in your PayPal merchant account.

## Integrated PayPal solutions

With PayPal and Adobe Commerce and Magento Open Source, you can accept payments from all major debit and credit cards. PayPal offers additional convenience without extra effort, because even your customers who don't have a PayPal account can pay for their purchases with PayPal.

>[!NOTE]
>
>You cannot have more than one PayPal method enabled in your store at a time, except for PayPal Express Checkout. PayPal Express Checkout can be used with other PayPal payment methods, except for PayPal Payments Standard. If you change payment solutions, the previous method is disabled.

### PayPal Express Checkout

[PayPal Express Checkout](paypal-express-checkout.md)

### PayPal All-in-one payment solutions

In the United States, PayPal offers the following PCI-compliant solutions to meet the needs of your growing business.

- [PayPal Payments Advanced](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

![PayPal all-in-one payment Solutions](./assets/paypal-all-in-one.png)<!-- zoom -->

### PayPal payment gateways

A payment gateway is a merchant service provided by an e-commerce application service provider that authorizes credit card or direct payments processing. They work as intermediaries between customers and banks.

Payment gateways are available in online and offline environments. Payments can be accepted by phone, online, or through a mobile app. The transaction is sent to the service provider's processing system and then sent to the customer's bank for verification and confirmation. If verified, the merchant receives the payment without having direct contact with the customer's bank account.

There are two types of payment gateways---direct and hosted.

- Direct payment gateways allow users to enter their card details on the store website.
- Hosted payment gateways redirect users to a hosted payment page, outside of the store website.

The payment gateway provides security and protection for all parties involved in a transaction.

PayPal offers a choice of two payment gateway solutions for your business. You can let PayPal host your checkout on its secure payment site, or you can take control of the entire payment experience with a customizable solution.

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal Payflow Link](paypal-payflow-link.md)

![Set up PayPal payment gateways](./assets/paypal-payment-gateway.png)<!-- zoom -->

## PayPal fraud management filters

PayPal fraud management filters make it easier to detect and respond to fraudulent transactions, and can be configured to flag, hold for review, or deny riskier payments. Actions related to Commerce [order status](order-status.md) values changed according to the fraud filter settings:

| Action | Result|
| --- | --- |
| Review | The suspected order receives the status _Payment Review_ when the order is placed. You can review the order and approve, or cancel the payment in the Admin, or on the PayPal side. When you click **Accept Payment** or **Deny Payment**, no new transactions for the order are created. <br/><br/>If you change the status of the transaction on the PayPal site, you must click **Get Payment Update** in the Order page of the Admin to apply the changes. If you click **Accept Payment** or **Deny Payment**, the changes made at the PayPal site are applied. |
| Deny | The suspected order cannot be placed by the customer, because the corresponding transaction is rejected by PayPal. <br/><br/>To deny the payment from the Admin, click **Deny Payment** in the upper-right corner of the page. The order status changes to _Canceled_, the transaction is reverted, and funds are released on the customer account. The corresponding information is added in the _Comments History_ section of the order view. |
| Flag | The suspected order gets the status _Processing_ when it is placed. The corresponding transaction is marked with a flag in the list of the merchant account transactions. |

{style="table-layout:auto"}

## PayPal solutions by country

|Country|PayPal payment solution|
|--- |--- |
|Australia|PayPal Website Payments Standard<br/>[PayPal Payflow Pro](paypal-payflow-pro.md)<br/>PayPal Website Payments Pro Hosted Solution<br/>[PayPal Express Checkout](paypal-express-checkout.md)|
|Canada|PayPal Website Payments Standard<br/>PayPal Website Payments Pro<br/>[PayPal Payflow Pro](paypal-payflow-pro.md)<br/>[PayPal Payflow Link](paypal-payflow-link.md) (includes Express Checkout)<br/>[PayPal Express Checkout](paypal-express-checkout.md)|
|France|PayPal Integral Evolution<br/>PayPal Website Payments Standard<br/>[PayPal Express Checkout](paypal-express-checkout.md)|
|Germany|[PayPal Express Checkout](paypal-express-checkout.md)|
|Hong Kong SAR China|PayPal Website Payments Pro Hosted Solution<br/>PayPal Website Payments Standard<br/>[PayPal Express Checkout](paypal-express-checkout.md)|
|Italy|PayPal ProPay<br/>[Pal Payments Standard](paypal-payments-standard.md)<br/>[PayPal Express Checkout](paypal-express-checkout.md)|
|Japan|PayPal Website Payments Plus<br/>PayPal Website Payments Standard<br/>[PayPal Express Checkout](paypal-express-checkout.md)|
|New Zealand|[PayPal Payflow Pro](paypal-payflow-pro.md)<br/>PayPal Website Payments Standard<br/>[PayPal Express Checkout](paypal-express-checkout.md)|
|Spain|PayPal Pasarela Integral<br/>PayPal Website Payments Standard<br/>[PayPal Express Checkout](paypal-express-checkout.md)|
|United Kingdom|PayPal Payments Pro Hosted Solution (includes Express Checkout)<br/>[PayPal Payments Standard](paypal-payments-standard.md)<br/>[PayPal Express Checkout](paypal-express-checkout.md)|
|United States|[PayPal Payments Advanced](paypal-payments-advanced.md) (Includes Express Checkout)<br/>[PayPal Payments Pro](paypal-payments-pro.md) (Includes Express Checkout)<br/>[PayPal Payments Standard+](paypal-payments-standard.md)<br/>[PayPal Payflow Pro](paypal-payflow-pro.md) (Includes Express Checkout)<br/>[PayPal Payflow Link](paypal-payflow-link.md) (Includes Express Checkout)<br/>[PayPal Express Checkout](paypal-express-checkout.md)|

{style="table-layout:auto"}

### Other countries

PayPal Express Checkout and PayPal Website Payments Standard are available in the following countries:

- Argentina
- Austria
- Belgium
- Brazil
- Bulgaria
- Chile
- Costa Rica
- Cyprus
- Czech Republic
- Denmark
- Dominican Republic
- Ecuador
- Estonia
- Finland
- French Guiana
- Gibraltar
- Greece
- Guadeloupe
- Hungary
- Iceland
- India
- Indonesia
- Ireland
- Israel
- Jamaica
- Latvia
- Liechtenstein
- Lithuania
- Luxembourg
- Malaysia
- Malta
- Martinique
- Mexico
- Netherlands
- Norway
- Philippines
- Poland
- Portugal
- Réunion
- Romania
- San Marino
- Singapore
- Slovakia
- Slovenia
- South Africa
- South Korea
- Sweden
- Switzerland
- Taiwan
- Thailand
- Turkey
- United Arab Emirates
- Uruguay
- Venezuela
- Vietnam


[1]: https://manager.paypal.com/0
[2]: https://developer.paypal.com/docs/payflow/payflow-gateway/
[3]: https://www.paypal.com/us/business/buy-now-pay-later
