---
title: Purchase orders
description: Learn how to set up purchase orders as an offline method of payment on your store.
---
# Purchase orders

A _purchase order_ (PO) allows commercial customers to pay for authorized purchases by referencing the PO number. The purchase order is authorized and issued in advance by the company that is making the purchase. During checkout, the customer chooses Purchase Order as the method of payment. Upon receipt of your invoice, the company processes the payment in their accounts payable system, and pays for the purchase.

Before accepting payment by purchase order, always establish the credit worthiness of the commercial customer.

**_To configure payment by purchase order:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Payment Methods]**.

1. Under _[!UICONTROL Other Payment Methods]_, expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Purchase Order]** section.

   ![Purchase Order](../configuration-reference/sales/assets/payment-methods-purchase-order.png)
   )<!-- zoom -->

   For a detailed description of each of these configuration settings, see [Purchase Order](https://docs.magento.com/user-guide/configuration/sales/payment-methods.html#purchase-order) in the _Configuration Reference Guide_.

   >[!NOTE]
   >
   >If necessary, first clear the **[!UICONTROL Use system value]** checkbox to change these settings.

1. To activate this payment method, set **[!UICONTROL Enabled]** to `Yes`.

1. Enter a **[!UICONTROL Title]** to identify this payment method during checkout.

1. Set **[!UICONTROL New Order Status]** to `Pending` until payment is authorized.

1. Set **[!UICONTROL Payment from Applicable Countries]** to one of the following:

   - `All Allowed Countries` - Customers from all [countries](../getting-started/store-details.md#country-options) specified in your store configuration can use this payment method.
   - `Specific Countries` - After you choose this option, the _[!UICONTROL Payment from Specific Countries]_ list appears. To select multiple countries, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

1. Set **[!UICONTROL Minimum Order Total]** and **[!UICONTROL Maximum Order Total]** to the amounts required to qualify for this payment method.

   >[!NOTE]
   >
   >An order qualifies if the total falls between, or exactly matches, the minimum or maximum total values.

1. Enter a **[!UICONTROL Sort Order]** number to determine the position of this item in the list of payment methods that is displayed during checkout.

   This is relative to the other payment methods. (`0` = first, `1` = second, `2` = third, and so on.)

1. When complete, click **[!UICONTROL Save Config]**.
