---
title: Cart price rule example - discount with minimum product price
description: Review an example of using a cart price rule to offer a discount with a minimum product price.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
TQID: https://experienceleague.adobe.com/IRVMCZ8C4uOJ4cBYLEv0YnOsehv0T9XWSIkyjBLhFw4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
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
# Cart price rule example - discount with minimum product price

Cart price rules can be used to offer a percentage discount based on a minimum product price in the cart. In the following example, a 10% discount is applied to all products in the whole cart when at least 1 product with a price over $30.00 from a specified category is added to the cart. The format of the discount is as follows:

   X% whole cart off when at least 1 product is from Y category, and its price is over $Z dollars.

## Step 1. Create a cart rule

Follow the basic [instructions](price-rules-cart.md) to create a cart rule.

## Step 2. Define the conditions

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Conditions]** section.

1. Click _Add_ (![Add icon](../assets/icon-add-green-circle.png)) and choose **[!UICONTROL Product Attribute Combination]**.

    ![Cart price rule condition - product attribute combination](./assets/condition1.png){width="500" zoomable="yes"}

1. Click _Add_ (![Add icon](../assets/icon-add-green-circle.png)) at the beginning of the next line and in the list under **[!UICONTROL Product Attribute]**, choose **[!UICONTROL Category]**.

    - Click the (**…**) _more_ link to display additional options.

      ![Cart price rule condition - category options](./assets/condition3.png){width="600" zoomable="yes"}

    - Click the _Chooser_ (![List icon](../assets/icon-list-chooser.png)) icon to see the available categories. In the category tree, select the checkbox of each category that you want to include. Click the check icon to accept the category selections.

      ![Cart price rule condition - category](./assets/condition4.png){width="600" zoomable="yes"}

1. Click _Add_ (![Add icon](../assets/icon-add-green-circle.png)) at the beginning of the next line and do the following:

    - In the list under **[!UICONTROL Cart Item Attribute]**, choose **[!UICONTROL Price in cart]**.

      ![Cart price rule condition - cart item attribute](./assets/condition5.png){width="500"}

    - Click **is** and choose `equals or greater than`.

    - Click **...** and enter the amount that the Price in Cart must be to meet the condition. For example, enter `30`.

        ![Cart price rule condition - price in cart](./assets/condition6.png){width="500"}

1. Click **[!UICONTROL Save and Continue Edit]**.

## Step 3. Define the actions

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Actions]** section and do the following:

    ![Cart price rule actions](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

    - Set **[!UICONTROL Apply]** to `Percent of product price discount`.

    - Enter the **[!UICONTROL Discount Amount]**. For example, enter `10` for a 10% discount.

    - To prevent additional promotions from being applied to the purchase, set **[!UICONTROL Discard subsequent rules]** to `Yes`.

1. Click **[!UICONTROL Save and Continue Edit]** and complete the rule as needed.

## Step 4. Complete the labels

Complete [Step 4](price-rules-cart.md) of the cart price rule instructions to enter any labels that appear during checkout.

## Step 5: Save and test the rule

{{new-price-rule}}

1. When your rule is complete, click **[!UICONTROL Save Rule]**.
1. Test the rule to make sure that it works correctly.
