---
title: Bank transfers
description: Learn how to set up bank transfers as an offline method of payment on your store.
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
---
# Bank transfers

Adobe Commerce and Magento Open Source allow you to accept payment that is transferred from a customer bank account and deposited into your merchant bank account.

**_To configure bank transfer payments:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Payment Methods]**.

1. Under _Other Payment Methods_, expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Bank Transfer Payment]** section.

   ![Bank Transfer Payment](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

   >[!NOTE]
   >
   >If necessary, first clear the **[!UICONTROL Use system value]** checkbox to change these settings.

1. To activate bank transfers, set **[!UICONTROL Enabled]** to `Yes`.

1. Enter a **[!UICONTROL Title]** to identify the Bank Transfer Payment method during checkout.

1. Set **[!UICONTROL New Order Status]** to `Pending` until payment is authorized.

1. Set **[!UICONTROL Payment from Applicable Countries]** to one of the following:

   - `All Allowed Countries` - Customers from all [countries](../getting-started/store-details.md#country-options) specified in your store configuration can use this payment method.

   - `Specific Countries` - After you choose this option, the _[!UICONTROL Payment from Specific Countries]_ list appears. To select multiple countries, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

1. Enter the **[!UICONTROL Instructions]** that your customers must follow to set up a bank transfer.

   Depending on the country where your bank is located and the requirements of the bank, you might need to include the following information:

   - Bank account name
   - Bank account number
   - Bank routing code
   - Bank name
   - Bank address

1. Set **[!UICONTROL Minimum Order Total]** and **[!UICONTROL Maximum Order Total]** to the amounts required to qualify to use this payment method.

   >[!NOTE]
   >
   >An order qualifies if the total falls between, or exactly matches, the minimum or maximum total values.

1. Enter a **[!UICONTROL Sort Order]** number to determine the position of this item in the list of payment methods that is displayed during checkout.

   This is relative to the other payment methods. (`0` = first, `1` = second, `2` = third, and so on.)

1. When complete, click **[!UICONTROL Save Config]**.
