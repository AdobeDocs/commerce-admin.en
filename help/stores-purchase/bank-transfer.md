---
title: Bank transfers
description: Learn how to set up bank transfers as an offline method of payment on your store.
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
TQID: https://experienceleague.adobe.com/uIYk-S9M8nsKxo3O71N1z25Y-K5WaYOOAM26k9HLVoQ
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Bank transfers

Adobe Commerce and Magento Open Source allow you to accept payment that is transferred from a customer bank account and deposited into your merchant bank account.

**_To configure bank transfer payments:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Payment Methods]**.

1. Under _Other Payment Methods_, expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Bank Transfer Payment]** section.

   ![Bank Transfer Payment](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >If necessary, first clear the **[!UICONTROL Use system value]** checkbox to change these settings.

1. To activate bank transfers, set **[!UICONTROL Enabled]** to `Yes`.

1. For **[!UICONTROL Title]**, enter a title that identifies the bank transfer payment method during checkout.

1. Set **[!UICONTROL New Order Status]** to `Pending` until payment is authorized.

1. Set **[!UICONTROL Payment from Applicable Countries]** to one of the following:

   - `All Allowed Countries` - Customers from all [countries](../getting-started/store-details.md#country-options) specified in your store configuration can use this payment method.

   - `Specific Countries` - After you choose this option, the _[!UICONTROL Payment from Specific Countries]_ list appears. To select multiple countries, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

1. Enter the **[!UICONTROL Instructions]** that your customers must follow to set up a bank transfer.

   Depending on the country where your bank is located and the requirements of the bank, you can include the following information:

   - Bank account name
   - Bank account number
   - Bank routing code
   - Bank name
   - Bank address

1. Set **[!UICONTROL Minimum Order Total]** and **[!UICONTROL Maximum Order Total]** to the amounts required to qualify to use this payment method.

   >[!NOTE]
   >
   >An order qualifies if the total falls between, or exactly matches, the minimum or maximum total values.

1. For **[!UICONTROL Sort Order]**, enter a number that determines the position of this item in the list of payment methods that is displayed during checkout.

   This number is relative to the other payment methods. (`0` = first, `1` = second, `2` = third, and so on.)

1. When complete, click **[!UICONTROL Save Config]**.
