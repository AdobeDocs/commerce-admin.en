---
title: Stored payment methods
description: Learn how customers can use stored payment methods on your Commerce storefront.
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
TQID: https://experienceleague.adobe.com/dYEYXgEIp83AKhHepfDQVNR9YBUQGbJ7B2zu8UTM-I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
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
# Stored payment methods

Customers with access to a secure vault for storing payment information can speed through checkout without entering their credit card information each time. If [Instant Purchase](checkout-instant-purchase.md) is enabled, customers can bypass the two-step checkout process and place the order from the product page.

A payment method that supports a secure vault, such as [Braintree](braintree.md), is required. When a secure vault is enabled in the payment method configuration, customers have the option during checkout to save their credit card information as a stored payment method. Customers can manage stored payment methods from their account dashboard.

![Stored Payment Methods](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## Add stored payment method at checkout

1. From the storefront, the customer goes to the detail page of the product.

1. Adds product to the cart.

1. Proceeds to the checkout page.

1. Completes the _Shipping_ step.

1. Selects the **[!UICONTROL Braintree Credit Card]** payment method.

1. Fills in credit card data.

1. Selects the **[!UICONTROL Save for later use]** checkbox.

1. Clicks **[!UICONTROL Place Order]**.

The saved payment method is then displayed in the _[!UICONTROL Stored Payment Methods]_ tab of the customer dashboard.

## Delete a stored payment method

Any previously added, stored payment methods cannot be edited by the customer, they can only be deleted. This action cannot be undone.

1. In the sidebar of their account, the customer selects **[!UICONTROL Stored Payment Methods]**.

1. Finds the payment method entry to be deleted.

1. Clicks **[!UICONTROL Delete]**.

1. To confirm the action, clicks **[!UICONTROL OK]**.
