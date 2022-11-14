---
title: Cash on delivery (COD)
description: Learn how to set up cash on delivery as an offline method of payment on your store.
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
---
# Cash on delivery (COD)

Adobe Commerce and Magento Open Source allow you to accept _cash on delivery_ (COD) payments for purchases. You can accept COD payment only from specific countries, and you can fine-tune the configuration with minimum and maximum order total limits.

The shipping carrier receives payment from the customer at the time of delivery, which is then transferred to you. You can make an adjustment for any fee charged by the carrier service in your shipping and handling charges.

**_To set up cash on delivery payments:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Payment Methods]**.

1. Under _Other Payment Methods_, expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Cash On Delivery Payment]** section.

   ![Cash on Delivery Payment](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

   For a detailed description of each of these configuration settings, see [Cash On Delivery Payment](https://docs.magento.com/user-guide/configuration/sales/payment-methods.html#cash-on-delivery-payment) in the _Configuration Reference Guide_.

   >[!NOTE]
   >
   >If necessary, first clear the **[!UICONTROL Use system value]** checkbox to change these settings.

1. To activate cash on delivery payment, set **[!UICONTROL Enabled]** to `Yes`.

1. Enter a **[!UICONTROL Title]** to identify the COD payment method during checkout.

1. Set **[!UICONTROL New Order Status]** to `Pending` until receipt of payment is confirmed.

   If you prefer, you can use the `Processing` or `Suspected Fraud` status for new orders with this payment method.

1. Set **[!UICONTROL Payment from Applicable Countries]** to one of the following:

   - `All Allowed Countries` - Customers from all [countries](../getting-started/store-details.md#country-options) specified in your store configuration can use this payment method.
   - `Specific Countries` - After you choose this option, the _[!UICONTROL Payment from Specific Countries]_ list appears. To select multiple countries, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

1. Enter the **[!UICONTROL Instructions]** for accepting delivery of a COD order.

1. Set **[!UICONTROL Minimum Order Total]** and **[!UICONTROL Maximum Order Total]** to the order amounts that are required to qualify for COD payment.

   >[!NOTE]
   >
   >An order qualifies if the total is between, or matches, the minimum or maximum order total.

1. Enter a **[!UICONTROL Sort Order]** number to determine the position of this item in the list of payment methods that is displayed during checkout.

   This is relative to the other payment methods. (`0` = first, `1` = second, `2` = third, and so on.)

1. When complete, click **[!UICONTROL Save Config]**.
