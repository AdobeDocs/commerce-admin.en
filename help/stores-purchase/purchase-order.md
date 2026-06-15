---
title: Purchase orders
description: Learn how to set up purchase orders as an offline method of payment on your store.
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
TQID: https://experienceleague.adobe.com/Oc2vdP-OTXwo-6cjKWFj5zPf-QJVvU8aK6OUMPko4eY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
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
# Purchase orders

A _purchase order_ (PO) allows commercial customers to pay for authorized purchases by referencing the PO number. The purchase order is authorized and issued in advance by the company that is making the purchase. During checkout, the customer chooses Purchase Order as the method of payment. Upon receipt of your invoice, the company processes the payment in their accounts payable system, and pays for the purchase.

Before accepting payment by purchase order, always establish the credit worthiness of the commercial customer.

**_To configure payment by purchase order:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Payment Methods]**.

1. Under _[!UICONTROL Other Payment Methods]_, expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Purchase Order]** section.

   ![Purchase Order](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   For a detailed description of each of these configuration settings, see [Purchase Order](../configuration-reference/sales/payment-methods.md#purchase-order) in the _Configuration Reference Guide_.

   >[!NOTE]
   >
   >If necessary, first clear the **[!UICONTROL Use system value]** checkbox to change these settings.

1. To activate this payment method, set **[!UICONTROL Enabled]** to `Yes`.

1. For **[!UICONTROL Title]**, enter a title that identifies this payment method during checkout.

1. Set **[!UICONTROL New Order Status]** to `Pending` until payment is authorized.

1. Set **[!UICONTROL Payment from Applicable Countries]** to one of the following:

   - `All Allowed Countries` - Customers from all [countries](../getting-started/store-details.md#country-options) specified in your store configuration can use this payment method.
   - `Specific Countries` - After you choose this option, the _[!UICONTROL Payment from Specific Countries]_ list appears. To select multiple countries, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

1. Set **[!UICONTROL Minimum Order Total]** and **[!UICONTROL Maximum Order Total]** to the amounts required to qualify for this payment method.

   >[!NOTE]
   >
   >An order qualifies if the total falls between, or exactly matches, the minimum or maximum total values.

1. For **[!UICONTROL Sort Order]**, enter a number that determine the position of this item in the list of payment methods that is displayed during checkout.

   This number is relative to the other payment methods. (`0` = first, `1` = second, `2` = third, and so on.)

1. When complete, click **[!UICONTROL Save Config]**.
