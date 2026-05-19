---
title: Refunds in the customer account dashboard
description: Store customers can view the refund information associated with the order in their account dashboard.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/ggaeec6NA2K12-eHl7ESC10nU2u11ihbaxaPlbNAE9I
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
# Refunds in the customer account dashboard

{{ee-feature}}

If a refund has been issued for an order, customers can view the refund information associated with the order in their account dashboard. If you have enabled the [!UICONTROL _Show Store Credit History to Customers_] option for [Store Credit configuration](../customers/credit-configure.md), customers can also access their [Store Credit](../customers/store-credit.md) history.

## View a refund on the storefront

1. From the storefront, the customer logs in to their account.

1. Locates their order using one of the following methods:

   * Finding the order in the list of **Recent Orders** and clicking **[!UICONTROL View]**.
   * In the left panel, choosing **[!UICONTROL My Orders]**. Then, finding the order in the list and clicking **[!UICONTROL View]**.

1. The customer clicks the **[!UICONTROL Refunds]** tab to view the details of the refund.

   ![Refund detail on the storefront](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## View store credit balance and history on the storefront

Method 1: **From the customer account dashboard**

1. From the storefront, the customer logs in to account.

1. If the refund was applied to store credit, chooses **[!UICONTROL Store Credit]** in the left panel.

1. The amount refunded to their store credit appears in the list with the date and time of the action.

   ![Amount refunded to store credit](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >The Store Credit page also provides a link for the customer to redeem a [gift card](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

Method 2: **From the _Review & Payments_ page**

1. The customer adds a product to the cart.

2. Proceeds to the _Checkout_ page.

3. Passes the **[!UICONTROL Shipping]** step.

4. If store credit is available, the customer clicks **[!UICONTROL Use Store Credit]**.

   ![Store Credit from Review & Payments page](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. If the customer changes their mind about using the store credit, clicks **[!UICONTROL Remove]** in the _Order Summary_ section.

## Payment actions in the Admin

You can configure payment actions for your specific [Payment Method](../configuration-reference/sales/payment-methods.md). Each payment method has a different set of payment actions.

|Payment action |Description|
|--- |---|
| [!UICONTROL Capture Online] | When the invoice is submitted, the system captures the payment from the third-party payment gateway. An Admin user can then create a credit memo and void the invoice. |
| [!UICONTROL Capture Offline] | When the invoice is submitted, the system does not capture the payment. It is assumed that the payment is captured directly through the gateway, and the payment cannot be captured through Adobe Commerce. An Admin user can then create a credit memo, but cannot void the invoice. (Even though the order used an online payment, the invoice is essentially an offline invoice.) |
| [!UICONTROL Not Capture] | When the invoice is submitted, the system does not capture the payment. It is assumed that the payment is captured through Adobe Commerce later. There is a [!UICONTROL _Capture_] button in the completed invoice. Before capturing, you are able to cancel the invoice. After capturing, you are able to create a credit memo and void the invoice. |

{style="table-layout:auto"}

>[!WARNING]
>
>Select the [!UICONTROL _Not Capture_] option unless you are certain that you are going to capture the payment through Adobe Commerce later. You cannot create a credit memo until the payment has been captured using the [!UICONTROL _Capture_] button.
