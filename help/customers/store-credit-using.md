---
title: Apply store credit
description: Store administrators can apply store credit to a purchase.
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/O2EJMZscownPnhjPeFROdwikhYmHuDYdCx4N7NpXlho
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
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
# Apply store credit

{{ee-feature}}

Store administrators can view the credit balance and history from the customer account, and also apply store credit to a purchase.

![Customer credit balance and history](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## View the credit balance

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Find the customer in the grid.

1. In the _Action_ column, click **[!UICONTROL Edit]**.

1. Scroll _[!UICONTROL Customer View]_ page and view the **[!UICONTROL Store Credit Balance]** at the bottom.

![Store Credit Balance](assets/store-credit-balance.png){width="600" zoomable="yes"}

## Update store credit balance

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > _Operations_ > **[!UICONTROL All Customers]**.

1. Find the customer in the grid.

1. In the _Action_ column, click **[!UICONTROL Edit]**.

1. In the left panel, choose **[!UICONTROL Store Credit]**.

1. Choose the website (storefront) that you want to associate with the balance.

1. For **[!UICONTROL Update Balance]**, enter the new value.

1. To notify the customer about the balance update, select the **[!UICONTROL Notify Customer by Email]** checkbox and choose the store view from **[!UICONTROL Send Email Notification From the Following Store View]**.

1. Enter a **[!UICONTROL Comment]** about the change.

1. When updates are complete, click **[!UICONTROL Save and Continue Edit]** or **[!UICONTROL Save Customer]**.

The updated balance should be displayed in **[!UICONTROL Balance History]**.

## Apply a credit balance to an order as a store administrator

As a store administrator, you can do various things on behalf of a customer, including submitting orders. When you [create an order](../stores-purchase/customer-account-create-order.md), you can apply a Store Credit balance that is due to the customer. The available balance is displayed in the _Payment & Shipping Information_ section. Select the **[!UICONTROL Use Store Credit]** checkbox to apply the balance, or a portion of the balance if the order total is less.

![Apply the store credit balance to the order](assets/store-credit-apply.png){width="500" zoomable="yes"}

## Apply store credit during checkout

If there is a credit balance for the site, the customer can apply store credit to the order balance before placing the order on the storefront.

1. The customer views the amount of available store credit.

   During the _Review & Payments_ step, the available amount appears under _[!UICONTROL Store Credit]_.

1. To apply the amount to the order, clicks **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >The order total is recalculated and the amount of store credit that is applied appears in the _[!UICONTROL Order Summary]_.

   ![Store credit balance applied to the order](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. When ready, clicks **[!UICONTROL Place Order]**.
