---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Express Checkout]'
description: Review the configurations settings in the [!UICONTROL PayPal Express Checkout] section on the [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] page of the Commerce Admin.
exl-id: aae5b1d9-f47e-447a-b40c-924f8d2ee824
---
# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Express Checkout]

>[!IMPORTANT]
>
>**PSD2 Requirements:** <br/>
>As of September 14, 2019, European banks might decline payments that do not meet [PSD2](../../getting-started/compliance-payment-services-directive.md) requirements. No action is needed for PayPal Express Checkout to comply with PSD2 because all requirements are handled by PayPal.

{{config}}

## [!UICONTROL Required PayPal Settings]

![PayPal Express Checkout Required Settings](./assets/paypal-express-required-settings.png)<!-- zoom -->

<!-- [PayPal Express Checkout Required Settings](../../stores-purchase/paypal-express-checkout.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable this Solution]|Website|Activates [!DNL PayPal Express Checkout] as a payment method that is available to your customers. Options: `Yes` / `No`|
|[!UICONTROL Enable In-Context Checkout Experience]|Website|Activates streamlined PayPal In-Context Checkout as a payment method available to your customers. Options: `Yes` / `No`|
|[!UICONTROL Enable PayPal Credit]|Website|Activates PayPal Credit to allow customers to buy now, but pay later. You get paid up front, but customers have more time to pay. Options: `Yes` / `No`|

{:style="table-layout:auto"}

### [!UICONTROL Express Checkout]

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Email Associated with PayPal Merchant Account]|Website|Specifies the email address that you specified when your PayPal merchant account was established. The email address is case-sensitive, and must exactly match your email address in the PayPal system.|
|[!UICONTROL API Authentication Methods]|Website|Determines the method used for API authentication. Options: <br/>**`API Signature`** - Displays the _[!UICONTROL API Signature]_ field in the form. <br/>**`API Certificate`** - Displays the _[!UICONTROL API Certificate]_ field in the form.|
|[!UICONTROL API Username]|Website|The API user name that is associated with your PayPal merchant account.|
|[!UICONTROL API Password]|Website|The API password that is associated with your PayPal merchant account.|
|[!UICONTROL API Signature]|Website|The API signature that is associated with your PayPal merchant account.|
|[!UICONTROL API Certificate]|Website|Browse to upload your API certificate.|
|[!UICONTROL Get Credentials from PayPal]||Fetches your API credentials from PayPal.|
|[!UICONTROL Sandbox Credentials]||Fetches your sandbox credentials from PayPal.|
|[!UICONTROL Sandbox Mode]|Website|To run PayPal Express Checkout in a test environment, enter your sandbox API credentials, and set this to `Yes`. Options: `Yes` / `No`|
|[!UICONTROL API Uses Proxy]|Website|If your system uses a proxy server to establish the connection between Commerce and the PayPal system, set this to `Yes`. Options: `Yes` / `No`|
|[!UICONTROL Proxy Host]|Website|If the API uses proxy, this specifies the IP address of the proxy host.|
|[!UICONTROL Proxy Port]|Website|If the API uses proxy, this specifies the port used by the proxy host.|

{:style="table-layout:auto"}

### [!UICONTROL Advertise PayPal Credit]

![Advertise PayPal Credit](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Publisher ID]|Website|The Publisher ID associated with your PayPal Credit account.|
|[!UICONTROL Get Publisher ID from PayPal]||Fetches your Publisher ID from PayPal.|
|[!UICONTROL Home Page]|Website|Determines the position and size of the [!DNL PayPal Credit] banner on the home page. Options: <br/>**Display** - Displays a[!DNL PayPal Credit] banner on the home page of your store. Options: `Yes` / `No` <br/>**Position** - Determines the position of the [!DNL PayPal Credit] banner on the home page. Options: Header (center) / Sidebar (right) <br/>**Size** - Determines the size of the [!DNL PayPal Credit] banner on the home page. Options: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66`|
|[!UICONTROL Catalog Category Page]|Website|Determines the position and size of the [!DNL PayPal Credit] banner on category pages. Options: (same as for [!UICONTROL Home Page])|
|[!UICONTROL Catalog Product Page]|Website|Determines the position and size of the [!DNL PayPal Credit] banner on product pages. Options: (same as for [!UICONTROL Home Page])|
|[!UICONTROL Checkout Cart Page]|Website|Determines the position and size of the [!DNL PayPal Credit] banner on cart page. Options: (same as for [!UICONTROL Home Page])|

{:style="table-layout:auto"}

## [!UICONTROL Basic Settings]

![Basic Settings](./assets/payment-methods-paypal-express-checkout-basic-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Title]|Store View|A name that identifies the PayPal Express Checkout payment method during checkout.|
|[!UICONTROL Sort Order]|Store View|A number that determines the order that PayPal Express Checkout appears when listed with other payment methods during checkout. Enter `0` for the top of the list.|
|[!UICONTROL Payment Action]|Website|Determines the action taken by PayPal  when it receives an order. Options: <br/>**`Authorization`** - Approves the purchase, but puts a hold on the funds. The amount is not withdrawn until it is "captured" by the merchant. <br/>**`Sale`** - The amount of the purchase is authorized and immediately withdrawn from the customer's account. <br/>**`Order`** - Represents an agreement with PayPal that allows the merchant to capture one or more amounts up to the ordered total from the customer's buyer account, within a defined time period. This can be up to 29 days. One or more invoices must be generated from the Commerce Admin to capture the funds.|
|[!UICONTROL Display on Product Details Page]|Store View|Determines if the "Checkout with PayPal" button appears on product pages. Options include: `Yes` / `No`|

{:style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![Advanced Settings](./assets/payment-methods-paypal-express-checkout-advanced-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Display on Shopping Cart]|Store View|Determines if PayPal Express Checkout appears as a payment option in the shopping cart. Options: `Yes` (PayPal recommended)  / `No`|
|[!UICONTROL Payment Action Applicable From]|Website|Determines the range of the applicable country selection. Options: `All Allowed Countries` / `Specific Countries`|
|[!UICONTROL Countries Payment Applicable From]|Website|Identifies each country from which payment is accepted. Only customers with a billing address in a selected country can make purchases with this payment method.|
|[!UICONTROL Debug Mode]|Website|Records messages sent between your store and the payment system in a log file. Options: `Yes` / `No` <br/><br/>**_Note:_** The log file is stored on the server and is accessible only to developers. In accordance with PCI Data Security Standards, credit card information is not recorded in the log file.|
|[!UICONTROL Enable SSL Verification]|Website|Enables verification of the host security certificate. Options: `Yes` / `No`|
|[!UICONTROL Transfer Cart Line Items]|Website|Displays a full summary of the line items from the customer's shopping cart on the PayPal site. Options: `Yes` / `No`|
|[!UICONTROL Transfer Shipping Options]|Website|Includes up to ten shipping options on the PayPal site. Options: `Yes` / `No`|
|[!UICONTROL Shortcut Buttons Flavor]|Store View|Determines the type of image used for the PayPal acceptance button. Options: <br/>**`Dynamic`** - (Recommended) Displays an image that can be dynamically changed from the PayPal server. <br/>**`Static`** - Displays a static image that cannot be changed dynamically.|
|[!UICONTROL Enable PayPal Guest Checkout]|Website|Allows customers who do not have PayPal accounts to make purchases with PayPal Express Checkout. Options: `Yes` / `No`|
|[!UICONTROL Require Customer's Billing Address]|Website|Determines if the customer billing address is required. Options: `Yes` / `No` / `For Virtual Quotes Only`|
|[!UICONTROL Billing Agreement Signup]|Website|Determines if customers are able to enter into a [billing agreement](../../stores-purchase/paypal-billing-agreements.md) with your store. Options: <br/>**`Auto`** - Customer can sign up for a billing agreement during Express Checkout. <br/>**`Ask Customer`** - Customer are asked if they want to sign up for a billing agreement. <br/>**`Never`** - Customers are not offered the option to  sign up for a billing agreement.|
|[!UICONTROL Skip Order Review Step]|Website|Determines if customers can complete the transaction from the PayPal site, or are required to return to your store and complete the Order Review step before submitting the order. Options: `Yes` / `No`|

{:style="table-layout:auto"}

### [!UICONTROL Billing Agreement Settings]

![Billing Agreement Settings](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled]|Website|When enabled, billing agreements appear to customers as a payment option during checkout. Options: `Yes` / `No`|
|[!UICONTROL Title]|Store View|The label for the PayPal billing agreement option that appears as a payment option during checkout.|
|[!UICONTROL Sort Order]|Store View|Determines the order in which billing agreements are listed with other payment methods during checkout.|
|[!UICONTROL Payment Action]|Website|Determines how PayPal manages the transaction: Options: <br/>**Authorization** - Approves the purchase, but puts a hold on the funds. The amount is not withdrawn until it is "captured" by the merchant. <br/>**Sale** - The amount of the purchase is authorized and immediately withdrawn from the customer's account.|
|[!UICONTROL Payment Applicable From]|Website|Determines the range of the applicable country selection. Options: All Allowed Countries / Specific Countries|
|[!UICONTROL Countries Payment Applicable From]|Website|Identifies each country from which payment is accepted. Only customers with a billing address in a selected country can make purchases with this payment method.|
|[!UICONTROL Debug Mode]|Website|Records communication with the payment system in a log file. Options: `Yes` / `No` <br/><br/>**_Note:_** The log file is stored on the server and is accessible only to developers. In accordance with PCI Data Security Standards, credit card information is not recorded in the log file.|
|[!UICONTROL Enable SSL Verification]|Website|Enables a verification step to that ensures the transaction takes place over an encrypted SSL channel. Options: `Yes` / `No`|
|[!UICONTROL Transfer Cart Line Items]|Website|When enabled, displays a summary of line items from the shopping cart on your PayPal payments page. Options: `Yes` / `No`|
|[!UICONTROL Allow in Billing Agreement Wizard]|Website|When enabled, customers can initiate a billing agreement from the dashboard of their customer account.|

{:style="table-layout:auto"}

### [!UICONTROL Settlement Report Settings]

![Settlement Report Settings](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|**[!UICONTROL SFTP Credentials]**|||
|[!UICONTROL Login]|Website|Your user name that is required to log in to PayPal's Secure FTP Server.|
|[!UICONTROL Password]|Website|Your password that is required to log in to PayPal's Secure FTP Server.|
|[!UICONTROL Sandbox Mode]|Website|When enabled, runs reports in a test environment before "going live" in the production environment. Options: `Yes` / `No`|
|[!UICONTROL Custom Endpoint Hostname or IP-Address]|Website|The URL where settlement reports are managed. Default value: `reports.paypal.com`|
|[!UICONTROL Custom Path]|Website|The path where settlement reports are saved on your server. Default value: `/ppreports/outgoing`|
|**[!UICONTROL Scheduled Fetching]**|||
|[!UICONTROL Enable Automatic Fetching]|Website|When enabled, fetches settlement reports automatically on schedule. Options: `Yes` / `No`|
|[!UICONTROL Schedule]|Website|Determines how often settlement reports are generated by PayPal. Options: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days`|
|[!UICONTROL Time of Day]|Website|Determines the hour,  minute, and second that settlement reports are generated.|

{:style="table-layout:auto"}

### [!UICONTROL Frontend Experience Settings]

![Frontend Experience Settings - PayPal Merchant Pages Style](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL PayPal Product Logo]|Store View|Determines the PayPal logo that appears in your store. There are four basic styles in two sizes. Options: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)`|
|**[!UICONTROL PayPal Merchant Pages Style]**|||
|[!UICONTROL Page Style]|Store View|Determines the appearance of your PayPal merchant page. Permitted values: **`paypal`** - Uses the PayPal page style. <br/>**`primary`** - Uses the page style that you identified as the "primary" style in your account profile. <br/>**`your_custom_value`** - Uses a custom payment page style, which is specified in your account profile.|
|[!UICONTROL Header Image URL]|Store View|The URL of the image that appears in the upper-left corner of the checkout page. The maximum size is 750 x 90 pixels. <br/><br/>**_Note:_** PayPal recommends that the image is stored on a secure (https) server. Otherwise, the customer's browser may warn that "the page contains both secure and nonsecure items."|
|[!UICONTROL Header Image Background Color]|Store View|The six-character [hexadecimal color](https://en.wikipedia.org/wiki/Web_colors) code for the background color of the header on the checkout page. You can enter the code in either upper- and lowercase characters.|
|[!UICONTROL Header Image Border Color]|Store View|The six-character [hexadecimal color](https://en.wikipedia.org/wiki/Web_colors) code for the two-pixel border around the header.|
|[!UICONTROL Page Background Color]|Store View|The six-character [hexadecimal color](https://en.wikipedia.org/wiki/Web_colors) code for the background color of the checkout page that appears behind the header and payment form.|

{:style="table-layout:auto"}

#### [!UICONTROL Customize Smart Buttons (Basic)]

![Frontend Experience Settings - Customize Smart Buttons](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Customize Button]|Store view|Determines whether the PayPal Smart Buttons can be customized to match the layout and theme of your store. You can apply these changes independently on the Checkout page, on Product pages, on the Cart page, and in the Mini Cart.|
|[!UICONTROL Label]|Store view|The text that PayPal displays on the Smart Payment Button. Options: <br/>**`Checkout`** (displays as "PayPal Checkout") <br/>**`Pay`** (displays as "Pay with PayPal") <br/>**`Buy Now`** (displays as "Buy Now with PayPal") <br/>**`PayPal`** (displays as "PayPal") <br/>**`Installment`** (displays as "PayPal") <br/>**`Credit`** (displays as "PayPal CREDIT")|
|[!UICONTROL Layout]|Store view|Determines whether to display PayPal Smart Buttons vertically or horizontally. Options: <br/>**`Vertical`** - The buyer must either log in to PayPal or create a PayPal account regardless of whether "Enable Guest Checkout" is selected. <br/>**`Horizontal`** - When "Enable Guest Checkout" is selected, displays the **`Pay with Debit Card or Credit Card`** button on the PayPal popup window. Otherwise, the buyer must either log in to PayPal or create a PayPal account.|
|[!UICONTROL Size]|Store view|Sets the size of the Smart Payment Button. Options: <br/>**`Medium`** - 250 pixels by 35 pixels <br/>**`Large`** - 350 pixels by 40 pixels <br/>**`Responsive`** - (Default) Adjusts to the width of the container. The minimum width is 100 pixels, and the maximum width is 500 pixels. The height dynamically adjusts based on the width.|
|[!UICONTROL Shape]|Store view|Sets the shape of the Smart Payment Button. Options: `Pill` (default) / `Rectangle`|
|[!UICONTROL Color]|Store view|Set the color of the Smart Payment Button. Options: `Gold` (default) / `Blue` / `Silver` / `Black`|

{:style="table-layout:auto"}

#### [!UICONTROL Customize Smart Buttons (Features)]

![Frontend Experience Settings - Customize Smart Buttons (Features)](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Disable Funding Options]|Store view|Determines which other PayPal funding options are displayed on the Checkout page. The selected options are never displayed on the Checkout page. Unselected options are displayed only if PayPal supports the store's currency and the buyer's location. Options: `PayPal Credit` / `PayPal Guest Checkout` `Credit Card Icons` / `Elektronisches Lastschriftverfahren - German ELV`|

{:style="table-layout:auto"}
