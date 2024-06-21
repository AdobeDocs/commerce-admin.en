---
title: Cart persistence
description: Learn how a persistent shopping cart tracks unpurchased cart items and saves the information for the customer's next visit.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
---
# Cart persistence

A persistent shopping cart tracks unpurchased items that are left in the cart and saves the information for the customer's next visit when the logged-in session expires. Customers who are _remembered_ can have the contents of their shopping carts restored the next time they sign in to your store.

Using a persistent shopping cart can help reduce the number of abandoned shopping carts and increase sales. The persistent shopping cart **does not** expose sensitive account information at any time.

To manage the use of cart persistence for your site or within specific store views, you can [configure persistent shopping cart](#configure-a-persistent-cart) settings. For more information about how these settings affect the shopper experience in your storefront, see [Persistent cart workflow](#persistent-cart-workflow).

>[!NOTE]
>
>The persistent shopping cart capability is available only to customers that are registered and signed-in. Guest shoppers can not use the persistent shopping cart feature.

To use the persistent shopping cart, the customer's browser must be set to allow cookies. There are two types of cookies used for shopping cart operations:

- **Session cookie** – A short-term session cookie exists during a single visit to your site, and expires when the customer leaves, or after a set time period.

- **Persistent Cookie** – A long-term, persistent cookie continues in existence after the end of the session and saves a record of the customer's shopping cart contents for future reference.

## Persistent cart workflow

When the persistent shopping cart is [enabled](#configure-a-persistent-cart), the workflow depends on:

- The values of the _Enable Remember Me_ and _Clear Persistence on Log Out_ settings
- The customer's decision to select or clear the _Remember Me_ checkbox
- When the persistent cookie is cleared

When a persistent cookie is applied, a `Not Jane Smith?` link appears in the page header. This prompt gives the customer the ability to terminate the persistent session and start working as a guest, or to log in as a different customer. The system retains a record of the shopping cart contents, even if the registered customer logs in later on different devices to shop in your store. For example, a customer can add an item to the cart from a laptop computer, add more items from a mobile device, and complete the checkout process from a tablet.

If the customer checked the _[!UICONTROL Enable Remember Me]_ checkbox when logging in, there is a separate independent persistent cookie for each browser. Your store creates and maintains a separate persistent cookie for each browser that is used by a customer to log in or create an account. If the customer uses multiple browsers while visiting your store during a single, persistent session, changes made in one browser are reflected in any other browser sessions upon page refresh.

>[!NOTE]
>
>To ensure cart synchronization across multiple devices, customers must log in on each new device they use for shopping. This login process activates the persistent cookie specific to that device, enabling seamless cart updates and synchronization.

### Example: An open session on a shared computer

Jane is finishing her holiday shopping with a persistent session. She adds a present for John to her cart, and something for her mother. Then, she goes to the kitchen for a snack and her login session expires.

John sits down at the computer to do some quick shopping while Jane is in the kitchen. Without noticing the `Not Jane Smith?` link at the top of the page, he finds a nice present for Jane and adds it to the cart. When he goes to check out and logs in as himself, both items in Jane's cart are added to his cart. John is in such a hurry that he does not notice the additional items during _Order Review_, and submits the order. Jane's cart is now empty, and John bought all the gifts.

### Remember Me

Customers can select the _[!UICONTROL Remember Me]_ checkbox on the login page to save the contents of their shopping carts when the log-in session expires.

| Remember Me? |  Result |
| ------------ |  ------ |
| Selected |Creates a persistent cookie and saves the contents of the shopping cart for the customer's next logged-in session. |
| Not selected | Does not create a persistent cookie and does not save the cart information for the customer's next logged-in session. |

{style="table-layout:auto"}

### Continue persistence on logout - no

| Action | Result |
| ------ | ------ |
| Customer logs in | Invokes the persistent cookie in addition to the session cookie, which is already in use. |
| Customer logs out | Deletes the session cookie but the persistent cookie remains in effect. The next time the customer logs in, it restores the cart items or adds them to any new items placed in the cart. |
| Customer does not log out and the session cookie expires | The persistent cookie remains in effect.|

{style="table-layout:auto"}

### Clear persistence on logout

| Action | Result |
| ------ | ------ |
| Customer logs in | Invokes the persistent cookie in addition to the session cookie, which is already in use. |
| Customer logs out | Deletes both cookies. |
| Customer does not log out but the session cookie expires | The persistent cookie remains in effect. |

{style="table-layout:auto"}

## Persistent cart settings and effects

| Settings | Effect |
|----------|--------|
| **[!UICONTROL Enable Remember Me]** is set to `No`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]** has any value.<br/><br/>The **Remember Me** checkbox is not available on the login and registration page. | The persistent cookie is not used for new log in sessions. |
| **[!UICONTROL Enable Remember Me]** is set to `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]** has any value.<br/><br/>**Remember Me** is not selected. | The session cookie is applied as usual; the persistent cookie is not used. |
| **[!UICONTROL Enable Remember Me]** is set to `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]** is set to `Yes`.<br/><br/>**Remember Me** is set to `Yes`. | When a customer logs in, both cookies are applied. When a customer logs out, both cookies are deleted. If a customer does not log in but the session cookie expires, the persistent cookie is still used. Apart from logging out, the persistent cookie is deleted when its lifetime runs out or when the customer clicks the `Not Jane Smith` link. |
| **[!UICONTROL Enable Remember Me]** is set to `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]** is set to `No`.<br/><br/>**Remember Me** is set to `Yes` | When a customer logs in, both cookies are applied. When a customer logs out, the session cookie is deleted, the persistent session continues. The persistent cookie is deleted when its lifetime runs out or when the customer clicks the `Not Jane Smith` link.|

{style="table-layout:auto"}

## Configure a persistent cart

During the setup of a persistent shopping cart, you can specify the lifetime of the cookies, and which options you want to make available for various customer activities.

For more information about how the customer workflow is determined by these settings, see [Persistent cart workflow](#persistent-cart-workflow).

>[!NOTE]
>
>If the session cookie expires while the customer is logged in, the persistent cookie remains active.

{{$include /help/_includes/persistent-cart-configuration.md}}
