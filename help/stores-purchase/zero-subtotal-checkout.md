---
title: Zero subtotal checkout
description: Learn how to set up a zero subtotal as an offline method of payment on your store.
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
---
# Zero subtotal checkout

_Zero subtotal checkout_ can be used for orders with a subtotal of zero that are taxed after a discount is applied. For example, zero subtotal checkout might be used in the following situations:

- A discount covers the entire price of the purchase, with no additional charge for shipping.

- The customer adds a [downloadable](../catalog/product-create-downloadable.md) or [virtual](../catalog/product-create-virtual.md) product to the shopping cart, and the price equals zero.

- The price of a [simple](../catalog/product-create-simple.md) product is zero, and the [free shipping](shipping-free.md) method is available.

- A [coupon code](../merchandising-promotions/price-rules-cart-coupon.md) covers the full price of products and shipping.

To save time, zero subtotal orders can be set to automatically invoice.

**_To configure zero subtotal checkout:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Payment Methods]**.

1. Under _[!UICONTROL Other Payment Methods]_, expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Zero Subtotal Checkout]** section.

   ![Zero Subtotal Checkout](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

   >[!NOTE]
   >
   >If necessary, first clear the **[!UICONTROL Use system value]** checkbox to change these settings.

1. To activate zero subtotal checkout, set **[!UICONTROL Enabled]** to `Yes`.

1. Enter a **[!UICONTROL Title]** to identify the Zero Subtotal method during checkout.

1. If orders typically wait for approval, accept the default **[!UICONTROL New Order Status]** as `Pending"` until the order is approved.

   If you prefer, you can use the `Processing` or `Suspected Fraud` status for new orders with this payment method.

1. Set **[!UICONTROL Automatically Invoice All Items]** to `Yes` if you want to automatically invoice all items that have a zero balance.

   This option is available only if the **[!UICONTROL New Order Status]** option is set to `Processing`.

   >[!NOTE]
   >
   >If _[!UICONTROL New Order Status]_ is set to `Processing` and _[!UICONTROL Automatically Invoice All Items]_ is set to `No`, you must also assign **[!UICONTROL Order Status]** = `Processing` for the **[!UICONTROL Order State]** = `Pending` and **[!UICONTROL Default Status]** = `No` mapping on the [Order Status](order-status.md#custom-order-status) page.

1. Set **[!UICONTROL Payment from Applicable Countries]** to one of the following:

   - `All Allowed Countries` - Customers from all [countries](../getting-started/store-details.md#country-options) specified in your store configuration can use this payment method.
   - `Specific Countries` - After you choose this option, the _[!UICONTROL Payment from Specific Countries]_ list appears. To select multiple countries, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

1. Enter a **[!UICONTROL Sort Order]** number to determine the position of this item in the list of payment methods that is displayed during checkout.

   This is relative to the other payment methods. (`0` = first, `1` = second, `2` = third, and so on.)

1. When complete, click **[!UICONTROL Save Config]**.
