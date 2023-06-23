---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Payments Pro]'
description: Review the configurations settings in the [!UICONTROL PayPal Payments Pro] section on the [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] page of the Commerce Admin.
exl-id: 08363002-e1e6-4d5e-9303-44f5ee53ee0a
---
# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Pro]

>[!IMPORTANT]
>
>**PSD2 Requirements:** <br/>
>As of September 14, 2019, European banks might decline payments that do not meet [PSD2](../../getting-started/compliance-payment-services-directive.md) requirements. To comply with PSD2, [!DNL PayPal Payments Pro] must be integrated with [!DNL Cardinal Commerce]. To learn more, see [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![Required Settings](./assets/payment-methods-paypal-payments-pro-required.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Email Associated with PayPal Merchant Account]|Website|(Optional) Any email addresses that are associated with your PayPal merchant account. Email addresses are case-sensitive, and must exactly match the addresses that are in your account.|
|[!UICONTROL Partner]|Website|Your PayPal Partner ID, if applicable.|
|[!UICONTROL Vendor]|Website|Your PayPal user login name.|
|User|Website|The ID of another user on your PayPal account.|
|[!UICONTROL Password]|Website|The password that is associated with your PayPal merchant account.|
|[!UICONTROL Test Mode]|Website|When enabled, runs PayPal Payments Pro in a testing environment. Turn off test mode when you are ready to "go live" in production mode. Options: `Yes` / `No`|
|[!UICONTROL Use Proxy]|Website|A proxy can be used to redirect traffic when the server firewall prevents direct access to the PayPal server. If applicable, identifies the proxy server that is used to establish connection with the PayPal server. Options: `Yes` / `No` <br/><br/>If enabled, set the options: <br/>**Proxy Host** - The IP address of the proxy host. <br/>**Proxy Port** - The number of the proxy port.|
|[!UICONTROL Enable this Solution]|Website|Determines if PayPal Payments Pro is available your customers as a payment method.|
|[!UICONTROL Enable PayPal Credit]|Website|Determines if PayPal Credit is available to your customers as a payment option.|

{:style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![Advertise PayPal Credit](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Publisher ID]|Website|The Publisher ID associated with your PayPal Credit account.|
|[!UICONTROL Get Publisher ID from PayPal]||Fetches your Publisher ID from PayPal.|
|[!UICONTROL Home Page]|Website|Determines the position and size of the [!DNL PayPal Credit] banner on the home page. Options: <br/>**`Display`** - Determines if a[!DNL PayPal Credit] banner is displayed on the home page of your store. Options: `Yes` / `No` <br/>**`Position`** - Determines the position of the [!DNL PayPal Credit] banner on the home page. Options: Header (center) / Sidebar (right) <br/>**`Size`** - Determines the size of the [!DNL PayPal Credit] banner on the home page. Options: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66`|
|[!UICONTROL Catalog Category Page]|Website|Determines the position and size of the [!DNL PayPal Credit] banner on category pages. Options: (same as for [!UICONTROL Home Page])|
|[!UICONTROL Catalog Product Page]|Website|Determines the position and size of the [!DNL PayPal Credit] banner on product pages. Options: (same as for [!UICONTROL Home Page])|
|[!UICONTROL Checkout Cart Page]|Website|Determines the position and size of the [!DNL PayPal Credit] banner on cart page. Options: (same as for [!UICONTROL Home Page])|

{:style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Payments Pro]

![Basic Settings](./assets/payment-methods-paypal-payments-pro-basic-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Title]|Store View|A name that identifies PayPal Payments Pro as a payment method during checkout.|
|[!UICONTROL Sort Order]|Store View|A number that determines the order in which PayPal Payments Pro appears when listed with other payment methods during checkout.|
|[!UICONTROL Payment Action]|Website|Determines the action taken by PayPal when an order is submitted. Options: <br/>**`Authorization`** - Approves the purchase, but puts a hold on the funds. The amount is not withdrawn until it is "captured" by the merchant. <br/>**`Sale`** - The amount of the purchase is authorized and immediately withdrawn from the customer's account.|
|[!UICONTROL Credit Card Settings]|||
|[!UICONTROL Allowed Credit Cart Types]|Website|Determines the credit cards that are available to customers during checkout. Select each supported card. Options: `American Express` (requires an extra agreement) / `Visa` / `MasterCard` / `Discover` / `JCB`|

{:style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![Advanced Settings](./assets/paypal-advanced-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Payment Applicable From]|Website|Determines the applicable country selection. Options: `All Allowed Countries` / `Specific Countries`|
|[!UICONTROL Countries Payment Applicable From]|Website|Identifies each country from which payment is accepted. Only customers with a billing address in a selected country can make purchases with this payment method.|
|[!UICONTROL Debug Mode]|Website|Records messages sent between your store and the payment system in a log file. Options: `Yes` / `No` <br/><br/>**_Note:_** The log file is stored on the server and is accessible only to developers. In accordance with PCI Data Security Standards, credit card information is not recorded in the log file.|
|[!UICONTROL Enable SSL Verification]|Website|Determines if the secure channel on the host is verified before a transaction takes place. Options: `Yes` / `No`|
|[!UICONTROL Require CVV Entry]|Website|Determines if customers are required to enter the CVV code from the back of their credit card. Options: `Yes` / `No`|
|**[!UICONTROL CVV and AVS Settings]**|||
|_[!UICONTROL Reject Transaction if:]_|||
|[!UICONTROL AVS Street Does Not Match]|Website|Determines the action taken if the Address Verification Service determines that the street address does not match the information in the system. Options: `Yes` / `No`|
|[!UICONTROL AVS Zip Does Not Match]|Website|Determines the action taken if  the Address Verification Service determines that the ZIP code does not match the information in the system. Options: `Yes` / `No`|
|[!UICONTROL International AVS Indicator Does Not Match]|Website|Determines the action taken if the Address Verification Service determines that the international indicator does not match the information in the system. Options: `Yes` / `No`|
|[!UICONTROL Card Security Code Does Not Match]|Website|Determines the action taken if the CVV security code entered by the customer does not match the information in the system. Options: `Yes` / `No`|

{:style="table-layout:auto"}

## [!UICONTROL Settlement Report Settings]

![Settlement Report Settings](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Login]|Website|Your user name that is required to log in to PayPal's Secure FTP Server.|
|[!UICONTROL Password]|Website|Your password that is required to log in to PayPal's Secure FTP Server.|
|[!UICONTROL Sandbox Mode]|Website|When enabled, runs reports in a test environment before "going live" in the production environment. Options: `Yes` / `No`|
|[!UICONTROL Custom Endpoint Hostname or IP-Address]|Website|The URL where settlement reports are managed. Default value: `reports.paypal.com`|
|[!UICONTROL Custom Path]|Website|The path where settlement reports are saved on your server. Default value: `/ppreports/outgoing`|
|[!UICONTROL Scheduled Fetching]|||
|[!UICONTROL Enable Automatic Fetching]|Website|When enabled, fetches settlement reports automatically on schedule. Options: `Yes` / `No`|
|[!UICONTROL Schedule]|Global|Determines how often settlement reports are generated by PayPal. Options: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days`|
|[!UICONTROL Time of Day]|Global|Determines the hour, minute, and second that settlement reports are generated.|

{:style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![Frontend Experience Settings](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL PayPal Product Logo]|Store View|Determines the PayPal logo that appears in your store. There are four basic styles in two sizes. Options: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)`|
|**[!UICONTROL PayPal Merchant Pages Style]**|||
|[!UICONTROL Page Style]|Store View|Determines the appearance of your PayPal merchant page. Permitted values: <br/>**`paypal`** - Uses the PayPal page style. <br/>**`primary`** - Uses the page style that you identified as the "primary" style in your account profile. <br/>**`your_custom_value`** - Uses a custom payment page style, which is specified in your account profile.|
|[!UICONTROL Header Image URL]|Store View|The URL of the image that appears in the upper-left corner of the checkout page. The maximum size is 750 x 90 pixels. <br/><br/>**_Note:_** PayPal recommends that the image is stored on a secure (https) server. Otherwise, the customer's browser may warn that "the page contains both secure and nonsecure items."|
|[!UICONTROL Header Image Background Color]|Store View|The six-character [hexadecimal color](https://en.wikipedia.org/wiki/Web_colors) code for the background color of the header on the checkout page. You can enter the code in either upper- and lowercase characters.|
|[!UICONTROL Header Image Border Color]|Store View|The six-character hexadecimal color code for the 2-pixel border around the header.|
|[!UICONTROL Page Background Color]|Store View|The six-character hexadecimal color code for the background color of the checkout page that appears behind the header and payment form.|

{:style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Express Checkout]

![PayPal Express Checkout Basic Settings](./assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Title]|Store View|A name that identifies the PayPal Express Checkout payment method during checkout.|
|[!UICONTROL Sort Order]|Store View|A number that determines the order in which PayPal Express Checkout appears when listed with other payment methods during checkout. Enter 0 for the top of the list.|
|[!UICONTROL Payment Action]|Website|Determines the action taken by PayPal  when it receives an order. Options: <br/>**`Authorization`** - Approves the purchase, but puts a hold on the funds. The amount is not withdrawn until it is "captured" by the merchant. <br/>**`Sale`** - The amount of the purchase is authorized and immediately withdrawn from the customer's account. <br/>**`Order`** - Represents an agreement with PayPal that allows the merchant to capture one or more amounts up to the ordered total from the customer's buyer account, within a defined time period. This can be up to 29 days. One or more invoices must be generated from the Commerce Admin to capture the funds.|
|[!UICONTROL URL Display on Product Details Page]|Store View|Determines if the "Checkout with PayPal" button appears on product pages. Options: `Yes` / `No`|

{:style="table-layout:auto"}

## [!UICONTROL PayPal Express Checkout - Advanced Settings]

![PayPal Express Checkout Advanced Settings](./assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Display on Shopping Cart]|Store View|Determines if PayPal Express Checkout appears as a payment option in the shopping cart. Options: `Yes` (PayPal recommends this option) / `No`|
|[!UICONTROL Payment Action Applicable From]|Website|Determines the range of the applicable country selection. Options: `All Allowed Countries` / `Specific Countries`|
|[!UICONTROL Countries Payment Applicable From]|Website|Identifies each country from which payment is accepted. Only customers with a billing address in a selected country can make purchases with this payment method.|
|[!UICONTROL Debug Mode]|Website|Records messages sent between your store and the PayPal payment system in a log file. Options: `Yes` / `No` <br/><br/>**_Note:_** The log file is stored on the server and is accessible only to developers. In accordance with PCI Data Security Standards, credit card information is not recorded in the log file.|
|[!UICONTROL Enable SSL Verification]|Website|Enables verification of the host security certificate. Options: `Yes` / `No`|
|[!UICONTROL Transfer Cart Line Items]|Website|Displays a full summary of the line items from the customer's shopping cart on the PayPal site. Options: `Yes` / `No`|
|[!UICONTROL Skip Order Review Step]|Website|Determines if customers can complete the transaction from the PayPal site, or are required to return to your store and complete the Order Review step before submitting the order. Options: `Yes` / `No`|

{:style="table-layout:auto"}
