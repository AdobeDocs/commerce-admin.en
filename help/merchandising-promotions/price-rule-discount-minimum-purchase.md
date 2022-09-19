---
title: Cart price rule example - discount with minimum purchase
description: <placeholder>
---
# Cart price rule example - discount with minimum purchase

Cart price rules can be used to offer a percentage discount based on a minimum purchase. In the following example, a 25% discount is applied to all purchases over $200.00 in a specific category. The format of the discount is as follows:

    X% off all Y (category) over $Z dollars

## Step 1. Create a cart rule

Follow the basic [instructions](price-rules-cart.md) to create a cart rule.

## Step 2. Define the conditions

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **Conditions** section.

1. Click **Add** (![Add icon](../assets/icon-add-green-circle.png)) and choose **Product Attribute Combination**.

    ![Cart price rule condition - product attribute combination](./assets/condition1.png)<!-- zoom -->

1. Click **Add** (![Add icon](../assets/icon-add-green-circle.png)) at the beginning of the next line and in the list under **Product Attribute**, choose **Category**.

    ![Cart price rule condition - category](./assets/condition2.png)<!-- zoom -->

    - Click the (**…**) _more_ link to display additional options.

      ![Cart price rule condition - category options](./assets/condition3.png)<!-- zoom -->

    - Click the **Chooser** (![List icon](../assets/icon-list-chooser.png)) icon to see the available categories. In the category tree, select the checkbox of each category that you want to include. Press **Enter** to add the categories to the condition.

      ![Cart price rule condition - category](./assets/condition4.png)<!-- zoom -->

1. Click **Add** (![Add icon](../assets/icon-add-green-circle.png)) at the beginning of the next line and do the following:

    - In the list under **Cart Item Attribute**, choose **Price in cart**.

      ![Cart price rule condition - cart item attribute](./assets/condition5.png)<!-- zoom -->

    - Click **is** and choose `equals or greater than`.

    - Click **...** and enter the amount that the Price in Cart must be to meet the condition. For example, enter `200`.

        ![Cart price rule condition - price in cart](./assets/condition6.png)<!-- zoom -->

1. Click **Save and Continue Edit**.

## Step 3. Define the actions

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Actions** section and do the following:

    ![Cart price rule actions](./assets/minimum-discount-actions.png)<!-- zoom -->

    - Set **Apply** to `Percent of product price discount`.

    - Enter the **Discount Amount**. For example, enter `25` for a twenty-five percent discount.

    - To prevent additional promotions from being applied to the purchase, set **Discard subsequent rules** to `Yes`.

1. Click **Save and Continue Edit** and complete the rule as needed.

## Step 4. Complete the labels

Complete [Step 4](price-rules-cart.md) of the cart price rule instructions to enter any labels that appear during checkout.

## Step 5: Save and test the rule

{{#new-price-rule}}

1. When your rule is complete, click **Save Rule**.

1. Test the rule to make sure that it works correctly.
