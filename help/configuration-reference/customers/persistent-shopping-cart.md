---
title: Customers > Persistent Shopping Cart
description: Placeholder
---
# Customers > Persistent Shopping Cart

{{config}}

>[!NOTE]
>
>A [Persistent Shopping Cart](https://docs.magento.com/user-guide/sales/cart-persistent.html) allows retention of unpurchased items that are left in the cart and saves them for a period configured in _Persistence Lifetime_. Cookies should be allowed in the customer browser to use persistent shopping cart.

## General Options

![General Options](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!--General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Enable Persistence|Website|Determines if  the persistence is enabled.|
|Persistence Lifetime (seconds)|Website|Defines the lifetime of the persistent cookie in seconds. Maximum allowed value is 3153600000 seconds (100 years).|
|Enable "Remember Me"|Website|Defines whether the "Remember Me" checkbox appears on the login and registration pages of the store. Options: <br/>**Yes** - Displays the "Remember Me" checkbox. <br/>**No** - Does not display the "Remember Me" checkbox, and the persistent cookie is used only for customers who already have it.|
|"Remember Me" Default Value|Website|Defines the default state for the "Remember Me" checkbox.|
|Clear Persistence on Log Out|Website|Defines whether the persistent cookie is deleted when a store customer logs out. No matter how Clear Persistence on Log Out is configured, if a customer does not log out, but the session cookie expires, the persistent cookie is still used.|
|Persist Shopping Cart|Website|Defines whether using the persistent cookie gives access to the shopping cart data of the correspondent account. Options: <br/>**Yes** - The shopping cart contents are saved after the session ends. <br/>**No** - The shopping cart contents are not saved after the session ends.|
|Persist Wish List|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only) Determines if the state of customer wish lists is retained when the session ends. Options: <br/>**Yes** - The wish list contents are saved when the session ends. <br/>**No** - The wish list is not saved when the session ends.|
|Persist Recently Ordered Items|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only)Determines if the state of recently ordered items is retained when the session ends. Options: <br/>**Yes** - The state of Recently Ordered Items is saved when the session ends. <br/>**No** - The state of Recently Ordered Items is not saved when the session ends.|
|Persist Currently Compared Products|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only)Determines if the state of currently compared products is retained when the session ends. Options: <br/>**Yes** - The state of currently compared products is saved when the session ends. <br/>**No** - The state of currently compared products is not saved when the session ends.|
|Persist Comparison History|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only) Determines if the state of comparison history is retained when the session ends. Options: <br/>**Yes** - The state of comparison history is saved when the session ends. <br/>**No** - The state of comparison history is not saved when the session ends.|
|Persist Recently Viewed Products|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only) Determines if the state of recently viewed products is retained when the session ends. Options: <br/>**Yes** - The state of recently viewed products is saved when the session ends. <br/>**No** - The state of recently viewed products is not saved when the session ends.|
|Persist Customer Group Membership and Segmentation|Website|![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce only) Determines if the state of customers' group membership and segmentation criteria are retained when the session ends. Options: <br/>**Yes** - The state of the customer's group membership and segmentation data is saved when the session ends. <br/>**No** - The state of the customer's group membership and segmentation data are not saved when the session ends.|
