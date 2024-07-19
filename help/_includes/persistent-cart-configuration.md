---
title: Configuration  Reference of the Persistent Shopping Cart
description: Reusable content for the configuration reference of the Persistent Shopping Cart.
---

# [!UICONTROL General Options]

![General Options](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

|Field| [Scope](/help/getting-started/websites-stores-views.md#scope-settings) |Description|
|--- |------------------------------------------------------------------------|--- |
|[!UICONTROL Enable Persistence]| Website                                                                |Determines if the persistence option is enabled.|
|[!UICONTROL Persistence Lifetime (seconds)]| Website                                                                |Defines the lifetime of the persistent cookie in seconds. The maximum allowed value is 34560000 seconds (400 days). This is a limitation of the maximum recommended cookie life.|
|[!UICONTROL Enable "Remember Me"]| Website                                                                |Defines whether the _Remember Me_ checkbox appears on the login and registration pages of the store. Options: <br/>**`Yes`** - Displays the _Remember Me_ checkbox. <br/>**`No`** - Does not display the _Remember Me_ checkbox, and the persistent cookie is used only for customers who already have it.|
|[!UICONTROL "Remember Me" Default Value]| Website                                                                |Defines the default state for the _Remember Me_ checkbox.|
|[!UICONTROL Clear Persistence on Log Out]| Website                                                                |Defines whether the persistent cookie is deleted when a store customer logs out. No matter how this option is configured, if a customer does not log out, but the session cookie expires, the persistent cookie is still used.|
|[!UICONTROL Persist Shopping Cart]| Website                                                                |Defines whether using the persistent cookie gives access to the shopping cart data of the correspondent account. Options: <br/>**`Yes`** - The shopping cart contents are saved after the session ends. <br/>**`No`** - The shopping cart contents are not saved after the session ends.|
|[!UICONTROL Persist Wish List]| Website                                                                |![Adobe Commerce](/help/assets/adobe-logo.svg) (Adobe Commerce only) Determines if the state of customer wish lists is retained when the session ends. Options: <br/>**`Yes`** - The wish list contents are saved when the session ends. <br/>**`No`** - The wish list is not saved when the session ends.|
|[!UICONTROL Persist Recently Ordered Items]| Website                                                                |![Adobe Commerce](/help/assets/adobe-logo.svg) (Adobe Commerce only) Determines if the state of recently ordered items is retained when the session ends. Options: <br/>**`Yes`** - The state of Recently Ordered Items is saved when the session ends. <br/>**`No`** - The state of Recently Ordered Items is not saved when the session ends.|
|[!UICONTROL Persist Currently Compared Products]| Website                                                                |![Adobe Commerce](/help/assets/adobe-logo.svg) (Adobe Commerce only) Determines if the state of currently compared products is retained when the session ends. Options: <br/>**`Yes`** - The state of currently compared products is saved when the session ends. <br/>**`No`** - The state of currently compared products is not saved when the session ends.|
|[!UICONTROL Persist Comparison History]| Website                                                                |![Adobe Commerce](/help/assets/adobe-logo.svg) (Adobe Commerce only) Determines if the state of comparison history is retained when the session ends. Options: <br/>**`Yes`** - The state of comparison history is saved when the session ends. <br/>**`No`** - The state of comparison history is not saved when the session ends.|
|[!UICONTROL Persist Recently Viewed Products]| Website                                                                |![Adobe Commerce](/help/assets/adobe-logo.svg) (Adobe Commerce only) Determines if the state of recently viewed products is retained when the session ends. Options: <br/>**`Yes`** - The state of recently viewed products is saved when the session ends. <br/>**`No`** - The state of recently viewed products is not saved when the session ends.|
|[!UICONTROL Persist Customer Group Membership and Segmentation]| Website                                                                |![Adobe Commerce](/help/assets/adobe-logo.svg) (Adobe Commerce only) Determines if the state of customers' group membership and segmentation criteria are retained when the session ends. Options: <br/>**`Yes`** - The state of the customer's group membership and segmentation data is saved when the session ends. <br/>**`No`** - The state of the customer's group membership and segmentation data are not saved when the session ends.|

{style="table-layout:auto"}
