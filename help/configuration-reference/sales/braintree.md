---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Braintree]'
description: Review the configurations settings for the [!UICONTROL Braintree] section on the [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] page of the Commerce Admin.
exl-id: cf08bc4d-8d88-45e7-af71-f1ff90023766
---
# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Braintree]

>[!IMPORTANT]
>
>**Commerce 2.4 Migration:**<br/>
>For versions of Adobe Commerce and Magento Open Source earlier than 2.4.0, it was recommended that merchants install and configure the official Braintree payment integration extension from the [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=braintree) to replace the core integration. As of 2.4.0, the extension is now included in the core release.
><br/><br/>
>When migrating to Commerce 2.4, merchants need to uninstall the extension distributed on the Marketplace (`paypal/module-braintree` or `gene/module-braintree`) and update any code customizations to use the `PayPal_Braintree` namespace instead of `Magento_Braintree`. Configuration settings from the Braintree Payments bundled extension for Commerce and the extension distributed on the Commerce Marketplace are persisted and payments placed with those versions of the extension are captured, voided, or refunded as normal.
><br/><br/>
>If you are upgrading to Commerce 2.4.0 and were not using the recommended Commerce Marketplace extension in your previous 2.3.x version, the multi address feature does not work with the 2.4.0 version of Braintree. When a shopper selects _deliver to multiple addresses_ , the Braintree payment method does not appear. The Commerce Marketplace extension previously recommended for 2.3.x has this multiple address issue.

{{config}}

## [!UICONTROL Basic Braintree Settings]

![Basic Braintree Settings](./assets/payment-methods-braintree-basic-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Title]|Store View|Default value: Credit Card (Braintree)|
|[!UICONTROL Environment]|Store View|Options: `Sandbox` / `Production`|
|[!UICONTROL Payment Action]|Store View|Determines the action taken by Braintree when a payment is processed. Options: <br/>**`Authorize`** - Funds on the customer's credit card are authorized, but not transferred from the account. An order is created in your store Admin. You can later capture the sale and create an invoice. <br/>**`Intent Sale`** (previously `Authorize and Capture` in earlier releases) - Funds on the customer's credit card are authorized and captured by Braintree, and an order and invoice are created in your store Admin.|
|[!UICONTROL Merchant ID]|Website|This is the unique identifier for your entire gateway account, including the multiple merchant accounts that may be in your gateway. As known as the _public ID_ or _production ID_, your merchant ID is different for your production and sandbox gateways.|
|[!UICONTROL Public Key]|Store View|This is your user-specific, public identifier that restricts access to encrypted data. Each user associated with your Braintree gateway has their own public key.|
|[!UICONTROL Private Key]|Store View|This is your user-specific, private identifier that restricts access to encrypted data. Each user associated with your Braintree gateway has their own private key.|
|[!UICONTROL Enable this Solution]|Website|Determines if Braintree is available to your customers as a payment method. Options: `Yes` / `No`|
|[!UICONTROL Enable PayPal through Braintree]|Website|Determines if PayPal is included as a payment method through Braintree. Options: `Yes` / `No`|
|[!UICONTROL Enable PayPal Credit through Braintree]|Website|Determines if PayPal Credit is included as a payment method through Braintree. Options: `Yes` / `No`|
|[!UICONTROL Enable Vault for Card Payments]|Website|When enabled, provides secure storage for customer payment information, so customers don't have to reenter their credit card information for each purchase. Options: `Yes` / `No`|
|[!UICONTROL Enable Vault CVV Re-verification]|Website|When enabled, validation is done for the CVV rules setup in your Braintree Account. Options: `Yes` / `No`|

{:style="table-layout:auto"}

## [!UICONTROL Advanced Braintree Settings]

![Braintree Advanced Settings](./assets/payment-methods-braintree-advanced-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Vault Title]|Website|A descriptive title for your reference that identifies the vault where your customer card information is stored.|
|[!UICONTROL Merchant Account ID]|Website|The Merchant ID that is to be associated with Braintree transactions from this website. If left blank, the default merchant account from your Braintree account is used.|
|[!UICONTROL Advanced Fraud Protection]|Website|Determines if Braintree's Advanced Fraud Protection is applied to transactions. Options: `Yes` / `No` |
|[!UICONTROL Debug]|Website|Determines if communications between the Braintree system and your store are recorded in a log file. Options: `Yes` / `No`|
|[!UICONTROL CVV Verification]|Website|Determines if customers are required to provide the three-digit security code from the back of a credit card. Options: `Yes` / `No`|
|[!UICONTROL Credit Card Types]|Website|Specifies each credit card that you accept as payment through  Braintree. Press and hold `Ctrl` (or `Command` on Mac) to select a combination of cards. Options: `American Express` / `Visa` / `MasterCard` / `Discover` / `JCB` / `Diners` / `Maestro International`|
|[!UICONTROL Sort Order]|Website|Determines the order that Braintree is listed with other payment methods during checkout.|

{:style="table-layout:auto"}

### [!UICONTROL Kount Settings]

When the _[!UICONTROL Advanced Fraud Protection]_ option is enabled, [!UICONTROL Kount Settings] appear.

![Kount Configuration](./assets/payment-methods-braintree-kount-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Bypass Fraud Protection Threshold]|Website|Advanced fraud protection checks are bypassed if this threshold is met or exceeded. Leaving this field blank disables this option.|
|[!UICONTROL ENS URL]|Website|This is your unique URL that you need to add into your website in the [Kount AWC control panel](https://developer.paypal.com/braintree/articles/guides/fraud-tools/advanced/overview). This URL must be publicly accessible for the ENS to function correctly. You must add this ENS URL to the 'OPT-IN' website.|
|[!UICONTROL Merchant ID]|Website|Kount ID must be entered here to integrate with the fraud protection platform. If necessary, contact Braintree to set up your [Kount](https://kount.com/) account. |
|[!UICONTROL Skip Fraud Checks on Admin Orders]|Website|If enabled, orders placed through the Admin are prevented from being sent to Kount for evaluation. Options: `Yes` / `No`|
|[!UICONTROL ENS Allowed IPs]|Website|The IPs that have access to the ENS endpoint must be entered here.|

{:style="table-layout:auto"}

## [!UICONTROL Country Specific Settings]

![Country Specific Settings](./assets/payment-methods-braintree-country-specific-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Payment from Applicable Countries]|Website|Determines if you accept payments processed by Braintree from all countries, or only specific countries. Options: `All Allowed Countries` / `Specific Countries`|
|[!UICONTROL Payment from Specific Countries]|Website|If applicable, identifies the specific countries from which you accept payments processed by Braintree.|
|[!UICONTROL Country Specific Credit Card Types]|Website|Identifies the credit cards that are accepted per country for payments processed by Braintree. A record is saved for each country. Options: <br/>**`Country`** - Choose the country. <br/>**`Allowed Card Types`** - Select each credit card that is accepted from the country as payment through Braintree. <br/>**`Add`** - Add a line to allow credit cards for a different country. <br/>**`Action`** - Deletes the record of allowed credit cards  for the country.|

{:style="table-layout:auto"}

## [!UICONTROL ACH through Braintree]

![ACH through Braintree](./assets/payment-methods-braintree-ach-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled ACH Direct Debit]|Website|Determines if PayPal is included as a payment method through Braintree. Options: `Yes` / `No`|

{:style="table-layout:auto"}

## [!UICONTROL Apple Pay through Braintree]

![Apple Pay through Braintree](./assets/payment-methods-braintree-applepay-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled ApplePay through Braintree]|Website|Determines if ApplePay is included as a payment method through Braintree. Options: `Yes` / `No` <br/><br/> The Domain must be [verified in Braintree Account first](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3).|
|[!UICONTROL Payment Action]|Website|Determines the action taken by Braintree when a payment is processed. Options: <br/>**`Authorize`** - Funds on the customer's card are authorized, but not transferred from the customer's account. An order is created in your store Admin. You can later capture the sale and create an invoice. <br/>**`Intent Sale`** - Funds on the customer's card are authorized and captured by Braintree, and an order and invoice are created in your store Admin. **_Note:_** This was `Authorize and Capture` in 2.3.x and earlier releases.|
|[!UICONTROL Merchant Name]|Store View|Label that is displayed to customers in the ApplePay popup.|

{:style="table-layout:auto"}

## [!UICONTROL Local Payment Methods]

![Local Payment Methods](./assets/payment-methods-braintree-local-payment-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled Local Payment Methods]|Website|Determines if Local Payment Method is included as a payment method through Braintree. Options: `Yes` / `No`|
|[!UICONTROL Title]|Website|Label that appears on the checkout Payment Method section. Default value: Local|
|[!UICONTROL Allowed Payment Method]|Website|Select the local Payment method that needs to be enabled. Options: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit`|

{:style="table-layout:auto"}

## [!UICONTROL GooglePay through Braintree]

![GooglePay through Braintree](./assets/payment-methods-braintree-googlepay-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled GooglePay through Braintree]|Website|Determines if [!DNL Google Pay] payment is included as a payment method through Braintree. Options: `Yes` / `No`|
|[!UICONTROL Payment Action]|Website|Determines the action taken by Braintree when a payment is processed. Options: <br/>**`Authorize`** - Funds on the customer's card are authorized, but not transferred from the customer's account. An order is created in your store Admin. You can later capture the sale and create an invoice. <br/>**`Intent Sale`** - Funds on the customer's card are authorized and captured by Braintree, and an order and invoice are created in your store Admin. **_Note:_** This was `Authorize and Capture` in 2.3.x and earlier releases.|
|[!UICONTROL Button Color]|Website|Determines the color of the [!DNL Google Pay] button. Options: `White` / `Black`|
|[!UICONTROL Merchant ID]|Store View|ID provided by Google must be entered here.|
|[!UICONTROL Accepted Cards]|Website|Select the type of cards that a customer can use to place order using [!DNL Google Pay].|

{:style="table-layout:auto"}

## [!UICONTROL Venmo through Braintree]

![Venmo through Braintree](./assets/payment-methods-braintree-venmo-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled Venmo through Braintree]|Website|Determines if [!DNL Venmo] is included as a payment method through Braintree. Options: `Yes` / `No`|
|[!UICONTROL Payment Action]|Website|Determines the action taken by Braintree when a payment is processed. Options: <br/>**`Authorize`** - Funds on the customer's card are authorized, but not transferred from the customer's account. An order is created in your store Admin. You can later capture the sale and create an invoice. <br/>**`Intent Sale`** - Funds on the customer's card are authorized and captured by Braintree, and an order and invoice are created in your store Admin. **_Note:_** This was  _Authorize and Capture_ in 2.3.x and earlier releases.|

{:style="table-layout:auto"}

## [!UICONTROL PayPal through Braintree]

![PayPal through Braintree](./assets/payment-methods-braintree-paypal-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Title]|Store View|The label that identifies PayPal through Braintree to customers during checkout. Default value: `PayPal (Braintree)`|
|[!UICONTROL Vault Enabled]|Website|When enabled, provides secure storage for customer payment information, so customers don't have to re enter their PayPal information for each purchase. Options: `Yes` / `No`|
|[!UICONTROL Sort Order]|Website|A number that determines the order in which PayPal through Braintree is listed with other payment methods during checkout.|
|[!UICONTROL Override Merchant Name]|Store View|An alternate name that can be used to identify the merchant for each store view.|
|[!UICONTROL Payment Action]|Website|Determines the action taken by PayPal through Braintree when a payment is processed. Options: <br/>**`Authorize`** - Funds on the customer's card are authorized, but not transferred from the customer's account. An order is created in your store Admin. You can later capture the sale and create an invoice. <br/>**`Authorize and Capture`** - Funds on the customer's card are authorized and captured by PayPal through Braintree, and an order and invoice are created in your store Admin.|
|[!UICONTROL Payment from Applicable Countries]|Website|Determines if you accept payments processed by PayPal through Braintree from all countries, or only specific countries. Options: `All Allowed Countries` / `Specific Countries`|
|[!UICONTROL Payment from Specific Countries]|Website|If applicable, identifies the specific countries from which you accept payments processed by Braintree.|
|[!UICONTROL Require Customer's Billing Address]|Website|Determines if the customer's billing address is required to submit an order. Options: `Yes` / `No`|
|[!UICONTROL Debug]|Website|Determines if communications between the PayPal through Braintree system and your store are recorded in a log file. Options: `Yes` / `No`|
|[!UICONTROL Display on Shopping Cart]|Website|Determines if the PayPal button appears in the [mini cart](https://docs.magento.com/user-guide/sales/mini-cart.html) and on the [shopping cart](https://docs.magento.com/user-guide/sales/cart.html) page. Options: `Yes` / `No`|

{:style="table-layout:auto"}

### [!UICONTROL Mini-Cart and Cart Page]

![Mini cart and cart page](./assets/payment-methods-braintree-paypal-minicart-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Disable Funding Option]|Website|Disable certain funding options available on the PayPal Smart Button from displaying in this section.|
|[!UICONTROL Customise Button]|Website|If enabled, an option to customize the shape and color of the PayPal button is available. Options: `Yes` / `No`|
|[!UICONTROL Shape]|Website|Determines the shape of the PayPal button. Options: `Pill` / `Rectangle`|
|[!UICONTROL Size]|Website|Determines the size of the PayPal button. Options: `Medium` / `Large` / `Responsive`|
|[!UICONTROL Color]|Website|Determines the color of the PayPal button. Options: `Blue` / `Black` / `Gold` / `Silver`|

{:style="table-layout:auto"}

### [!UICONTROL Checkout Page]

![Checkout Page](./assets/payment-methods-braintree-paypal-checkout-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Disable Funding Option]|Website|Disable certain funding options available on the PayPal Smart Button from displaying in this section.|
|[!UICONTROL Customise Button]|Website|If enabled, an option to customize the shape and color of the PayPal button is available. Options: `Yes` / `No`|
|[!UICONTROL Shape]|Website|Determines the shape of the PayPal button. Options: `Pill` / `Rectangle`|
|[!UICONTROL Size]|Website|Determines the size of the PayPal button. Options: `Medium` / `Large` / `Responsive`|
|[!UICONTROL Color]|Website|Determines the color of the PayPal button. Options: `Blue` / `Black` / `Gold` / `Silver`|

{:style="table-layout:auto"}

### [!UICONTROL Product Page]

![Product Page](./assets/payment-methods-braintree-paypal-product-page-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable PayPal Buy Now button on the product page]|Website|If enabled, the PayPal button is available on the Product detail page. Options: `Yes` / `No`|
|[!UICONTROL Disable Funding Option]|Website|Disable certain funding options available on the PayPal Smart Button from displaying in this section.|
|[!UICONTROL Customise Button]|Website|If enabled, an option to customize the shape and color of the PayPal button is available. Options: `Yes` / `No`|
|[!UICONTROL Shape]|Website|Determines the shape of the PayPal button. Options: `Pill` / `Rectangle`|
|[!UICONTROL Size]|Website|Determines the size of the PayPal button. Options: `Medium` / `Large` / `Responsive`|
|[!UICONTROL Color]|Website|Determines the color of the PayPal button. Options: `Blue` / `Black` / `Gold` / `Silver`|

{:style="table-layout:auto"}

## 3d Secure Verification Settings

![3D Secure Verification Settings](./assets/payment-methods-braintree-3d-secure-verify-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL 3D Secure Verification]|Website|Determines if a transaction must pass an extra verification process when the customer is enrolled in a program such as "Verified by VISA". Options: `Yes` / `No`|
|[!UICONTROL Threshold Amount]|Website|Determines the maximum order amount that is authorized for processing on a single order. Braintree declines authorization if the order amount exceeds the Threshold Amount.|
|[!UICONTROL Verify for Applicable Countries]|Website|Determines the countries where payment must be verified. Options: `All Allowed Countries` / `Specific Countries`|
|[!UICONTROL Verify for Specific Countries]|Website|If applicable, identifies the specific countries from which payment by Braintree must be verified.|

{:style="table-layout:auto"}

## [!UICONTROL Dynamic Descriptors]

![Dynamic Descriptors](./assets/payment-methods-braintree-dynamic-config.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |
|[!UICONTROL Name]|Store View|There are two parts to the Name descriptor, which are separated by an asterisk (*). The first part of the descriptor identifies the company or DBA and the second part identifies the product. For example: `company*myproduct`  <br/><br/>The length of the Company and Product parts of the descriptor can be allocated in the following ways, for a combined length of up to 22 characters: <br/>**`Option 1`** - Company must be three characters / Product can be up to 18 characters <br/>**`Option 2`** - Company must be seven characters / Product can be up to 14 characters <br/>**`Option 3`** - Company must be 12 characters / Product can be up to nine characters|
|[!UICONTROL Phone]|Store View|The Phone descriptor must be ten to 14 characters in length, and can include only numbers, dashes, parentheses, and periods. For example: `9999999999` `(999) 999-9999` `999.999.9999`|
|[!UICONTROL URL]|Store View|The URL descriptor represents your domain name, and can be up to 13 characters long. For example: `company.com`|

{:style="table-layout:auto"}
