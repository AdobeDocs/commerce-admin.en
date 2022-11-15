---
title: Sales > Checkout
description: Placeholder
---
# Sales > Checkout

{{config}}

## Checkout Options

![Checkout Options](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://docs.magento.com/user-guide/sales/checkout-options.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Enable Onepage Checkout|Store View|Determines if [Onepage checkout](https://docs.magento.com/user-guide/sales/checkout-onepage.html) is the default checkout format. Options: `Yes` / `No`|
|Allow Guest Checkout|Store View|Determines if guests can go through [checkout without registering](https://docs.magento.com/user-guide/sales/checkout-guest.html) for an account with your store. Options: `Yes` / `No`|
|Enable Terms and Conditions|Store View|Determines if customers are required to agree to the [Terms and Conditions](https://docs.magento.com/user-guide/sales/terms-and-conditions.html) of the sale before making a purchase. Options: `Yes` / `No`|
|Display Billing Address On|Store View|Determines the location of the Billing Address during checkout. Options: `Payment Method` / `Payment Page`|
|Maximum Number of Items to Display in Order Summary|Store View|Determines the maximum number of items that can  appear in the _Order Summary_ during checkout. The default is `10`.|
|Enable Address Search|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only) Determines if customers can use [address search](https://docs.magento.com/user-guide/sales/checkout-address-search.html) functionality for Shipping, and Review & Payments steps. When this is enabled, use Number of Customer Addresses Limit to set the number of saved addresses required to activate this functionality during checkout. Options: `Yes` / `No`|
|Number of Customer Addresses Limit|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only) When address search is enabled, determines the number of saved addresses required to activate this functionality during checkout. When the customer's number of saved addresses meets or exceeds this number, only the default address is rendered on the _Shipping_ and _Review & Payments_ steps. The customer can use a search function to change the selected address. The default is `10`.|

## Shopping Cart

![Shopping Cart](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://docs.magento.com/user-guide/sales/cart-configuration.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Quote Lifetime (days)|Website|Determines the [lifetime of a quoted price](https://docs.magento.com/user-guide/sales/cart-quote-lifetime.html), in days.|
|After Adding a Product Redirect to Shopping Cart|Store View|Determines if the [shopping cart page appears](https://docs.magento.com/user-guide/sales/cart-redirect.html) immediately after a product is added to the cart. Options: `Yes` / `No`|
|Number of Items to Display Pager|Store View|Determines the number of items in the shopping cart before the pager is triggered. Default value: `20`|
|Show Cross-sell Items in the Shopping Cart|Store View|Indicates if [cross-sell items](https://docs.magento.com/user-guide/catalog/settings-advanced-cross-sells.html) are displayed in the shopping cart, providing additional sale options to customers. Options: `Yes` (default) / `No`|
|Grouped Product Image|Store View|Determines the [thumbnail](https://docs.magento.com/user-guide/sales/cart-thumbnails.html) image that appears for a [grouped product](https://docs.magento.com/user-guide/catalog/product-create-grouped.html) in the shopping cart. Options: `Product Thumbnail Itself` / `Parent Product Thumbnail`|
|Configurable Product Image|Store View|Determines the [thumbnail](https://docs.magento.com/user-guide/sales/cart-thumbnails.html) image that appears for a configurable product in the shopping cart. Options: `Product Thumbnail Itself` / `Parent Product Thumbnail`|
|Preview Quote Lifetime (minutes)|Store View|Determines the maximum age of the quote in minutes when previewed from the shopping cart.|
|Enable Clear Shopping Cart|Website|Determines if the shopping cart displays the option for users to clear the contents of the cart in a single action. Options: `Yes` / `No`|

## My Cart Link

![My Cart Link](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Display Cart Summary|Website|Determines the value that appears in parentheses after the My Cart link. Options: `Display number of items in cart` / `Display item quantities`|

## Mini Cart

![Mini Cart](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Display Mini Cart|Store View|Determines if the mini cart appears on store pages when the cart icon in the header is clicked. The display of the mini cart depends upon the theme. Options: `Yes` / `No`|
|Number of Items to Display Scrollbar|Store View|Determines the number of items that can appear in the mini cart before the scrollbar is triggered. Default: `5`|
|Maximum Number of Items to Display|Store View|Determines the maximum number of items that can appear in the mini cart. Default: `10`|

## Payment Failed Emails

![Payment Failed Emails](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://docs.magento.com/user-guide/sales/checkout-payment-failed-emails.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Payment Failed Email Receiver|Store View|Identifies the store contact who receives Payment Failed emails. Default receiver: `General Contact`|
|Payment Failed Email Sender|Store View|Identifies the store contact that appears as the message sender of Payment Failed emails. Default sender: `General Contact`|
|Payment Failed Template|Store View|Identifies the template that is used for Payment Failed emails. Default template: `Payment Failed`|
|Send Payment Failed Copy To|Store View|Provides the email address of anyone to receive a copy of a Payment Failed email. Separate multiple addresses with a comma.|
|Send Payment Failed Copy Method|Store View|Indicates the email method used to send the copy. Options: <br />**Bcc** - Sends a blind courtesy copy by including the recipient in the header of the same email that is sent to the customer. The BCC recipient is not visible to the customer. <br />**Separate Email** - Sends the copy as a separate email.|
