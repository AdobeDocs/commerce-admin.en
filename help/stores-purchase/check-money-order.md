---
title: Checks and money orders
description: Learn how to set up check and money order as an offline method of payment on your store.
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
TQID: https://experienceleague.adobe.com/mmlEdLGANV93nvet3YwYoBGZKcft1qYuA6HboQ0Buvw
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
# Checks and money orders

Adobe Commerce and Magento Open Source allow you to accept payments by check or money order. The _Check / Money Order_ payment method is enabled for your store by default. You can accept checks and money orders only from specific countries, and you can fine-tune the configuration with minimum and maximum order total limits.

**_To configure payment by check or money order:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Payment Methods]**.

1. Under _[!UICONTROL Other Payment Methods]_, expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Check / Money Order]** section.

   ![Check / Money Order](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   For a detailed description of each of these configuration settings, see [Check / Money Order](../configuration-reference/sales/payment-methods.md#check--money-order) in the _Configuration Reference Guide_.

   >[!NOTE]
   >
   >If necessary, first clear the **[!UICONTROL Use system value]** checkbox to change these settings.

1. To accept payment by check or money order, set **[!UICONTROL Enabled]** to `Yes`.

1. For **[!UICONTROL Title]**, enter a title that identifies the check / money order payment method during checkout.

1. If orders typically wait for approval, accept the default **[!UICONTROL New Order Status]** as `Pending"` until it is approved.

   If you prefer, you can use the `Processing` or `Suspected Fraud` status for new orders with this payment method.

1. Set **[!UICONTROL Payment from Applicable Countries]** to one of the following:

   - `All Allowed Countries` - Customers from all [countries](../getting-started/store-details.md#country-options) specified in your store configuration can use this payment method.
   - `Specific Countries` - After you choose this option, the _[!UICONTROL Payment from Specific Countries]_ list appears. To select multiple countries, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

1. For **[!UICONTROL Make Check Payable To]**, enter the name of the party to whom the check must be payable.

1. For **[!UICONTROL Send Check To]**, enter the street address or PO Box where the checks are mailed.

1. Set **[!UICONTROL Minimum Order Total]** and **[!UICONTROL Maximum Order Total]** to the order amounts required to qualify for this payment method.

   >[!NOTE]
   >
   >An order qualifies if the total falls between, or exactly matches, the minimum or maximum total values.

1. For **[!UICONTROL Sort Order]**, enter a number that determines the position of this item in the list of payment methods that is displayed during checkout.

   This number is relative to the other payment methods. (`0` = first, `1` = second, `2` = third, and so on.)

1. When complete, click **[!UICONTROL Save Config]**.
