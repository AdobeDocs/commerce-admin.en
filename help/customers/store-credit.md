---
title: Store credit
description: Store credit is an amount that is restored to a customer account, and can be used to pay for purchases or for cash refunds.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/kG-y-O2Yh-h1ct-oCwqylZFvS2FOCXFPD6qVIkKrpbg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
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
# Store credit

{{ee-feature}}

Store credit is an amount that is restored to a customer account. Customers can use their store credit to pay for purchases, and administrators can use store credit for cash refunds. Gift card balances can be credited to the customer's account, instead of using the gift card code for future purchases.

After an order is paid and invoiced, the order, or a portion of it, can be refunded by [issuing a credit memo](../stores-purchase/credit-memo-create.md). A credit memo differs from a refund because the amount of the credit is restored to the customer's account where it can be used for future purchases. Sometimes, a refund can be given at the same time that a credit memo is issued, and applied to the customer's balance of store credit. The amount of store credit that is available in the customer's account is specified in the configuration.

>[!NOTE]
>
>The [_Zero Subtotal Checkout_](../stores-purchase/zero-subtotal-checkout.md) payment method must be enabled in the case that store credit covers the order total.

## Store credit workflow

1. **Customer login** - Customer logs into account before beginning the checkout process.

1. **Use Store** - Credit During the [!UICONTROL _Review & Payments_] step of the checkout process, the customer selects [!UICONTROL _Use Store Credit_] as a payment option. The available balance is displayed in parentheses. If the available balance is greater than the grand total, the other payment methods are no longer displayed.

1. **Credit applied to order** - The amount of store credit that is applied to the order appears with the order totals, and is subtracted from the grand total.

1. **Customer balance adjusted** - The customer's available balance is adjusted when the order is placed.
