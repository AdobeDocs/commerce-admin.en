---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt;  [!UICONTROL PayPal Payflow Pro]'
description: Review the configurations settings in the [!UICONTROL PayPal Payflow Pro] section on the [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] page of the Commerce Admin.
exl-id: 2aae038b-15c0-452a-98bc-4d97efbb60f6
---
# [!UICONTROL Sales] > [!UICONTROL Payment Methods] >  [!UICONTROL PayPal Payflow Pro]
 
>[!IMPORTANT]
>
>**PSD2 Requirements:** <br/>
>As of September 14, 2019, European banks might decline payments that do not meet [PSD2](../../getting-started/compliance-payment-services-directive.md) requirements. To comply with PSD2, [!DNL PayPal Payflow Pro] must be integrated with [!DNL Cardinal Commerce]. To learn more, see [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![Required Settings](./assets/paypal-payflow-pro-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Email Associated with PayPal Merchant Account]|Website|(Optional) Any email addresses that are associated with your PayPal merchant account. Email addresses are case-sensitive, and must exactly match the addresses that are in your account.|
|[!UICONTROL Partner]|Website|Your PayPal Partner ID, if applicable.|
|[!UICONTROL Vendor]|Website|Your PayPal user login name.|
|User|Website|The ID of another user on your PayPal account.|
|[!UICONTROL Password]|Website|The password that is associated with your PayPal merchant account.|
|[!UICONTROL Test Mode]|Website|When enabled, runs PayPal Payflow Pro in a testing  environment. Turn off test mode when you are ready to "go live" in production mode. Options: `Yes` / `No`|
|[!UICONTROL Use Proxy]|Website|A proxy can be used to redirect traffic when the server firewall prevents direct access to the PayPal server. If applicable, identifies the proxy server that is used to establish connection with the PayPal server. Options: `Yes` / `No` <br/><br/>If enabled, set the proxy options: <br/>**`Proxy Host`** - The IP address of the proxy host. <br/>**`Proxy Port`** - The number of the proxy port.|
|[!UICONTROL Enable this Solution]|Website|Determines if PayPal Payflow Pro is available your customers as a payment method.|
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

## [!UICONTROL Basic Settings - PayPal Payflow Pro]

![Basic Settings](./assets/payment-methods-paypal-payflow-pro-basic-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Title]|Store View|A name that identifies PayPal Payflow Pro as a payment method during checkout.|
|[!UICONTROL Sort Order]|Store View|A number that determines the order in which PayPal Payflow Pro appears when listed with other payment methods during checkout.|
|[!UICONTROL Payment Action]|Website|Determines the action taken by PayPal when an order is submitted. Options: <br/>**`Authorization`** - Approves the purchase, but puts a hold on the funds. The amount is not withdrawn until it is "captured" by the merchant. <br/>**`Sale`** - The amount of the purchase is authorized and immediately withdrawn from the customer's account.|
|**[!UICONTROL Credit Card Settings]**|||
|[!UICONTROL Allowed Credit Cart Types]|Website|Determines the credit cards that are available to customers during checkout. Select each supported card. Options: `American Express` (requires an extra agreement) / `Visa` / `MasterCard` / `Discover` / `JCB`|

{:style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![Advanced Settings](./assets/payment-methods-paypal-payflow-pro-advanced-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Display on Shopping Cart|Store View|Determines if PayPal Express Checkout appears as a payment option in the shopping cart. Options: Yes (Recommended) / No|
|[!UICONTROL Payment Action Applicable From]|Website|Determines the range of the applicable country selection. Options: All Allowed Countries / Specific Countries|
|[!UICONTROL Countries Payment Applicable From]|Website|Identifies each country from which payment is accepted. Only customers with a billing address in a selected country can make purchases with this payment method.|
|[!UICONTROL Debug Mode]|Website|Records messages sent between your store and the PayPal payment system in a log file. Options: `Yes` / `No` <br/><br/>**_Note:_** The log file is stored on the server and is accessible only to developers. In accordance with PCI Data Security Standards, credit card information is not recorded in the log file.|
|[!UICONTROL Enable SSL Verification]|Website|Enables verification of the host security certificate. Options: `Yes` / `No`|
|[!UICONTROL Transfer Cart Line Items]|Website|Displays a full summary of the line items from the customer's shopping cart on the PayPal site. Options: `Yes` / `No`|
|[!UICONTROL Skip Order Review Step]|Website|Determines if customers can complete the  transaction from the PayPal site, or are required to return to your store and complete the Order Review step before submitting the order. Options: `Yes` / `No`|

{:style="table-layout:auto"}
