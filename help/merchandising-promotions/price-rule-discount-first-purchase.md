---
title: Cart price rule example - discount with first purchase
description: <placeholder>
---
# Cart price rule example - discount with first purchase

{{#ee-feature}}

Cart price rules can be used to automatically offer a discount to customers on their first purchase, with no coupon needed.

To offer a discount that is targeted to first-time customers, you can:

- Create a customer segment that is defined as _buyers with no orders_, and then
- Create a cart price rule that targets the new customer segment.

>[!NOTE]
>
>Ensure that the Customer Segments feature is enabled. Refer to [Creating a Customer Segment](https://docs.magento.com/user-guide/marketing/customer-segment-create.html).

## Step 1. Create a customer segment

1. On the _Admin_ sidebar, go to **Customers** > **Segments**.

1. In the upper-right corner, click **Add Segment**.

1. Define the **General Properties**.

   - Enter a **Segment Name** to identify the customer segment (Example: _First-time customer_).

   - For **Assigned to Website**, select the website where the customer segment can be used.

   - For **Status**, select `Active`.

   - For **Apply to**, select `Visitors and Registered Customers`.

   - When complete, click **Save and Continue Edit**.

       Additional options become available in the panel on the left.

    ![Customer segment properties](./assets/customer-segment-first-time.png)<!-- zoom -->

1. Define the **Conditions**.

    For this example, the condition targets customers for whom _Total Number of Orders is less than 1_ is True.

   - In the panel on the left, choose **Conditions**.

       The default condition begins, "If ALL of these conditions are TRUE:"

   - Click **Add** (![Add icon](../assets/icon-add-green-circle.png)) and select `Number of Orders`.

   - Click **is** and select `less than`.

   - Click **...** and enter `1` in the field.

   - Click the green checkmark ( ![Green checkmark](../assets/icon-checkmark-green-circle.png) ) to save the condition setting.

   - Click **Save**.

   ![Customer segment condition](./assets/customer-segment-first-time-condition.png)<!-- zoom -->

Your customer segment is created and displayed in the Customer Segment list.

![Customer segments list](./assets/customer-segment-list-first-time.png)<!-- zoom -->

>[!TIP]
>
>Make note of the segment ID. You use this ID number to create the cart price rule.

## Step 2. Create the cart price rule

1. On the _Admin_ sidebar, go to **Marketing** > _Promotions_ > **Cart Price Rule**.

1. In the upper-right corner, click **Add New Rule**.

      The **Rule Information** section displays by default, with expandable sections for **Conditions** and **Actions**.

1. Define the **Rule Information**.

   - Complete the **Rule Name** and **Description** fields. These fields are for your internal reference only.

   - For **Websites**, select the website where the rule is to be available.

   - For **Customer Groups**, select the customer group to which this rule applies.

       To select multiple groups, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

      >[!NOTE]
      >
      >The options in this list are dependent on the customer groups created and managed in **Customers** > **Customer Groups**.

   - For **Coupon**, select `No Coupon`.

   - For **Uses per Customer**, enter `1`.

   - For **Priority**, enter a number to establish the priority of this rule in relation to other rules.

      >[!NOTE]
      >
      >The Priority setting is important when the same catalog product meets the conditions set for more than one price rule. The rule with the highest Priority setting becomes active for the customer. The highest priority is 1. For this example, entering `1` means that this rule is applied before any other price rule. This value will be used by the **Discard Subsequent Rules** setting in the **Action** section.

   - When complete, click **Save and Continue Edit**.

      Additional options become available in the panel on the left.

   ![Cart price rule information](./assets/rule-information-first-time.png)<!-- zoom -->

1. Define the **Conditions**.

   - Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **Conditions** section.

      The default rule begins, "If ALL of these conditions are TRUE:".

   - Click **Add** (![Add icon](../assets/icon-add-green-circle.png)) and select `Customer Segment`.

       The qualifier field defaults to `matches`.

   - Click **...** and enter the segment ID of the customer segment you want to target.

      For this example, the segment ID for the new segment created in Step 1 is `2`.

      >[!NOTE]
      >
      >If you don't know the segment ID, click the chooser icon ( ![List icon](../assets/icon-list-chooser.png) ) to display the Customer Segment list. You can manually enter the ID in the field or select the checkbox for the desired segment to auto-populate the field.

   - Click the green checkmark ( ![Green checkmark](../assets/icon-checkmark-green-circle.png) ) to save the condition setting.

   - When complete, click **Save and Continue Edit**.

       This line of the rule applies to all customers who match customer segment ID 2.

   ![Customer segment condition](./assets/customer-segment-matches.png)<!-- zoom -->

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png)the **Actions** section and define the actions for the rule.

   In this section, you define the type of discount and value/amount of the discount you want to apply for first-time customers. This example defines a 10% discount for all customers who meet the defined condition. For information on other available options, see [Creating a Cart Price Rule](price-rules-cart-create.md).

   - For **Apply**, select Percent of product price discount.

   - For **Discount Amount**, enter `10`.

   - To apply this price rule only to product amounts, set **Apply to Shipping Amount** to `No`.

   - To prevent the system from applying multiple price rules to the same product, set **Discard Subsequent Rules** to `Yes`.

   - When complete, click **Save**.

   ![Cart price rule actions](./assets/actions-first-time.png)<!-- zoom -->

The new rule is normally available within the hour. You should test the rule to ensure that it works as you defined it.

## Step 3: Save and test the rule

{{#new-price-rule}}

1. When your rule is complete, click **Save Rule**.

1. Test the rule to make sure that it works correctly.
