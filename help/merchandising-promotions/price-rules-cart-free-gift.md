---
title: Free Gift promotions
description: Learn how to configure a free gift promotion with cart price rules to offer a free gift when a set of conditions is met.
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
TQID: https://experienceleague.adobe.com/FR-q4Qj-ZDDzmfEKSvSj-BlwsM7ro-BqAE1yCppTaXE
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
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---

# Free gift promotion

The *Free Gift* promotion allows you to set a [cart price rule](price-rules-cart.md) that adds a free item to the cart under specific conditions.

>[!NOTE]
>
>This feature is not supported on Luma storefronts. It is accessible through [GraphQL](https://developer.adobe.com/commerce/webapi/graphql/schema/cart/mutations/select-free-gift/) and available on Edge Delivery Services (EDS) storefronts.

## Create a free gift promotion

This section describes how to create a free gift promotion using the following format:

**Buy X product, get Y product free**

1. [Create a cart price rule](price-rules-cart.md#step-1-add-a-rule) with a free gift promotion.

1. [Describe the conditions](price-rules-cart.md#step-2-describe-the-conditions) of the cart instructions to define the conditions for the price rule. This is the first of multiple conditions that can be added to the rule, and determines when the rule is triggered. It can be based on a combination of the following:

   - Product attributes
   - Products
   - Cart attributes
   - Adobe Commerce Customer segments

   If left blank, the rule is triggered for every cart.

   ![Cart price rule - conditions](./assets/conditions.png){width="600" zoomable="yes"}

1. Define the actions for the cart price rule:

   1. Expand ![Expansion selector] (../assets/icon-display-expand.png) the **[!UICONTROL Actions]** section and enter the following information:
   
     - Set **[!UICONTROL Apply]** to `Free Gift`.
     - In **[!UICONTROL Gift SKU(s)]**, select one or more SKUs that the customer can choose as a free gift.
     - Set **[!UICONTROL Free Gift Discount Type]** to **[!UICONTROL Price Based]** or **[!UICONTROL Discount Based]**.
     - In **[!UICONTROL Gift Qty ]**, enter the quantity of the free gift that the customer receives. For example, enter `2` if you want the customer to receive two free items.
     - To prevent other discounts from being applied, set **[!UICONTROL Discard subsequent rules]** to `Yes`.
   
   1. Click **[!UICONTROL Save and Continue Edit]** and complete the rest of the rule as needed.

1. [Complete the label](price-rules-cart.md) of the cart price rule instructions to enter the label that appears during checkout.

  ![Cart price rule - Free Gift Label](./assets/free-gift-promotion-label.png){width="600" zoomable="yes"}

  {{new-price-rule}}

1. When your rule is complete, click **[!UICONTROL Save Rule]**.

## Variations

You can customize cart price rules many different ways. The Free Gift feature can be configured with two different discount types:

  - **Price based** : A gift line item is added at a price of `0`.
  - **Discount Based** : A full discount is applied to the gift line item.
