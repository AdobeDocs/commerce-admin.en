---
title: Cart price rule example - free shipping promotion
description: Review an example of using a cart price rule to offer free shipping.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
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
# Cart price rule example - free shipping promotion

Free shipping can be offered as a promotion, either with, or without a [coupon](price-rules-cart-coupon.md). A free shipping coupon, or voucher, can also be applied to customer pick-up orders, so the order can be invoiced and shipped to complete the [workflow](../stores-purchase/order-processing.md#order-workflow-and-processing).

Some shipping carrier configurations give you the ability to offer free shipping based on a minimum order. To expand upon this basic capability, you can use shopping cart price rules to create complex conditions based on multiple product attributes, cart contents, and customer groups.

## Step 1. Enable free shipping

1. Enable [free shipping](../stores-purchase/shipping-free.md) in your store configuration.

1. Complete the free shipping settings for any [carrier service](../stores-purchase/carriers.md) that you want to use for free shipping.

## Step 2. Create a cart price rule

On the _Admin_ sidebar, go to **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_ > **[!UICONTROL Cart Price Rules]**.

Follow the steps below to set up the type of free shipping promotion that you want to offer.

### Example 1: Free shipping for any order

1. Complete the **[!UICONTROL Rule Information]** as follows:

   - Enter a **[!UICONTROL Rule Name]** for internal reference.
   - Enter a brief **[!UICONTROL Description]** to describe the rule.
   - Set **[!UICONTROL Active]** to `Yes`.
   - In the **[!UICONTROL Websites]** box, select each site where the free shipping coupon is to be available.
   - Select the **[!UICONTROL Customer Groups]** to which the rule applies.
   - Set **[!UICONTROL Coupon]** to one of the following:
      - To offer a free shipping promotion without a coupon, accept the default (`No Coupon`) setting.
      - To use a coupon with the price rule, select `Specific Coupon`. If necessary, complete the instructions to set up a [coupon](price-rules-cart-coupon.md).

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Actions]** section and do the following:

   - Set **[!UICONTROL Apply]** to `Percent of product price discount`.
   - Set **[!UICONTROL Apply to Shipping Amount]** to `Yes`.
   - Set **[!UICONTROL Free Shipping]** to `For matching items only`.

   ![Cart price rule - free shipping actions](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### Example 2: Free shipping for orders over $ amount

1. Complete the **[!UICONTROL General Information]** settings as described in the previous example.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Conditions]** section.

1. Click _Add_ (![Add icon](../assets/icon-add-green-circle.png)) to insert a condition and do the following:

   - In the list under **[!UICONTROL Cart Attribute]**, choose `Subtotal`.
   - Click **[!UICONTROL is]** and choose `equals or greater than`.
   - Click **...** and enter a threshold value for the Subtotal, such as `100`, to complete the condition.

   ![Cart price rule - condition](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. If necessary, expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Actions]** section and do the following:

   - Set **[!UICONTROL Apply]** to `Percent of product price discount`.
   - Set **[!UICONTROL Apply to Shipping Amount]** to `Yes`.
   - Set **[!UICONTROL Free Shipping]** to `For matching items only`.

## Step 3. Complete the labels

Complete [Step 4](price-rules-cart.md) of the cart price rule instructions to enter any labels that appear during checkout.

## Step 4. Save and test the rule

{{new-price-rule}}

1. When your rule is complete, click **[!UICONTROL Save Rule]**.

1. Test the rule to make sure that it works correctly.
