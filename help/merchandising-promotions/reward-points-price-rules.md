---
title: Reward points in price rules
description: Learn how reward points can be awarded to customers according to a cart price rule.
exl-id: 6e23b56d-64e4-435d-9f4c-ee3f400b0250
feature: Rewards, Promotions/Events, Customers
TQID: https://experienceleague.adobe.com/amQYBXl5evC-BUqmb5SyGR97iOAMIPv5UxqCFfOkGmQ
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
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
# Reward points in price rules

{{ee-feature}}

Reward points can be awarded to customers according to a [cart price rule](price-rules-cart.md). The award of points can be the only action of the price rule, or can be used with a discount.

>[!NOTE]
>
>[Reward Exchange Rates](reward-exchange-rates.md) configuration is required for redemption of reward points by customers and Admin users during checkout.

## Add reward points to a price rule

1. On the _Admin_ sidebar, go to **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_ > **[!UICONTROL Cart Price Rules]**.

1. Click **[!UICONTROL Add New Rule]** to create a cart price rule or click an existing cart price rule to open it.

1. Scroll down, expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Actions]** section, set the conditions, and enter the number of points in the **[!UICONTROL Add Reward Points]** field.

   ![Cart price rule - reward points](./assets/reward-points-price-rule-actions.png){width="600" zoomable="yes"}

1. Follow the standard instructions to complete the [cart price rule](price-rules-cart-create.md).

   When the price rule is activated, a message appears in the cart to let customers know how many points they can earn by placing the order. This applies only to registered users and may vary when a user is logged in.
