---
title: Cart persistence
description: Learn how a persistent shopping cart tracks unpurchased cart items and saves the information for the customer's next visit.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
---
# Cart persistence

A persistent shopping cart tracks unpurchased items that are left in the cart and saves the information on the current device to keep it accessible when the logged-in session expires. 

Customers who are _remembered_ can have the contents of their shopping cart accessible on the current device when the logged-in session expires. After the session expires, the customers shopping cart is being accessed with the use of the Persistent Cart session. If the same customer logs in on another device or a browser and add something to their shopping cart, and then go back to the device with an active persistent session, their shopping cart will be updated with the added items.

Using a persistent shopping cart can help reduce the number of abandoned shopping carts and increase sales. The persistent shopping cart **does not** expose sensitive account information at any time.

To manage the use of cart persistence for your site or within specific store views, you can [configure persistent shopping cart](#configure-a-persistent-cart) settings. For more information about how these settings affect the shopper experience in your storefront, see [Persistent cart workflow](#persistent-cart-workflow).

>[!NOTE]
>
>The persistent shopping cart capability is available only to customers that are registered and signed-in. Guest shoppers can not use the persistent shopping cart feature.

## Persistent cart workflow

When the persistent shopping cart is [enabled](#configure-a-persistent-cart), the workflow depends on:

- The values of the _Enable Remember Me_ and _Clear Persistence on Log Out_ settings
- The customer's decision to select or clear the _[!UICONTROL Remember Me]_ checkbox
- When the persistent cookie is cleared

When a persistent cookie is applied and the loggen-in with _[!UICONTROL Remember Me]_ option checked customer session expires or the customer logs out when the system is configured with Clear Persistence on Sign Out set to No, a `Not Jane Smith?` link appears in the page header. The system will retains a record of the shopping cart contents on the current device, even if the logged-in session expiries, and this prompt gives the customer the ability to terminate the persistent session and start working as a guest, or to log in as a different or the same customer. 

If the customer checked the _[!UICONTROL Remember Me]_ checkbox when logging in, your store creates and maintains a separate persistent cookie for each browser or device that is used by a customer to log in or create an account. If the customer uses multiple browsers while visiting your store when a persistent session is active or customer is logged in, changes made in one browser or device are reflected in any other browser sessions upon page refresh.

>[!NOTE]
>
>To ensure cart synchronization across multiple devices or browesers, customers must log in on each new device they use for shopping. For logged in customers, the content of the shopping cart will be syncronizing across multiple devices and browsers as long as they are logged in under the same account, regardless of the Persistent Cart configuration.

### "Remember Me" checkbox behaviour

Customers can select the _[!UICONTROL Remember Me]_ checkbox on the login page or when creating a new account to save the contents of their shopping carts on the current device when the logged-in session expires.

| Remember Me? |  Result |
| ------------ |  ------ |
| Selected |Creates a persistent cookie and saves the contents of the shopping cart on the current device when the customer login session expires. |
| Not selected | Does not create a persistent cookie and does not save the cart information on the current device when the login session expires. Please note that the shopping cart content will still be saved in the customer's account and will be loaded upon the next customer's login. |

{style="table-layout:auto"}

### Clear Persistence on Sign Out behaviour

When the customer logs in or register with _[!UICONTROL Remember Me]_ checked, the Persistent Cart behaviour will be affected by the Clear Persistence on Sign Out configuration.

|  | Clear Persistence on Sign Out set to Yes | Clear Persistence on Sign Out set to No |
| ------ | ------ | ------ |
| _Remembered_ customer logs out | Deletes both session and persistent cookies and the shopping cart content disappears on the current device until the same customer logs back in. | Deletes the session cookie but the persistent cookie remains in effect. The shopping cart content will remain accessible on the current device. |
| _Remembered_ customer does not log out but the session cookie expires | The persistent cookie remains in effect and the shopping cart content is accessible from the current device. | The persistent cookie remains in effect and the shopping cart content is accessible from the current device. |

### An example of an open session on a shared computer

Jane is finishing her holiday shopping as a _Remembered_ logged in customer. She adds a present for John to her cart, and something for her mother. Then, she goes to the kitchen for a snack and her login session expires.

John sits down at the computer to do some quick shopping while Jane is in the kitchen. Without noticing the `Not Jane Smith?` link at the top of the page, he finds a nice present for Jane and adds it to the cart. When he goes to check out, he notices that the shipping and billing addresses are pre-filled and thinks that he is signed in. John is in such a hurry that he does not notice the additional items during _Order Review_, and submits the order. Jane's cart is now empty, and John bought all the gifts.

## Configure a persistent cart

During the setup of a persistent shopping cart, you can specify the lifetime of the cookies, and which options you want to make available for various customer activities.

To use the persistent shopping cart, the customer's browser must be set to allow cookies. There are two types of cookies used for shopping cart operations:

- **Session cookie** – A short-term session cookie exists during a single visit to your site, and expires when the customer logs out, or the session expires after a set time period.

- **Persistent Cookie** – A long-term, persistent cookie continues in existence after the end of the logged-in session and keeps the customer's shopping cart content accessible.

For more information about how the customer workflow is determined by these settings, see [Persistent cart workflow](#persistent-cart-workflow).

{{$include /help/_includes/persistent-cart-configuration.md}}
