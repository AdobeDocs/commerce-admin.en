---
title: Create a catalog price rule
description: <placeholder>
---
# Create a catalog price rule

Follow these instructions to apply a discount to specific products whenever a set of conditions is met. Catalog price rule discounts go into effect before the product is placed into the shopping cart.

## Step 1: Add a new rule

1. On the _Admin_ sidebar, go to **Marketing** > _Promotions_ > **Catalog Price Rule**.

1. In the upper-right corner, click **Add New Rule**.

   The **Rule Information** section includes expandable sections for **Conditions** and **Actions**.

   ![Catalog price rule - information](./assets/price-rule-catalog-new-ee.png)<!-- zoom -->

1. Complete the **Rule Name** and **Description** fields. These fields are for your internal reference only.

1. Set the **Status** of the price rule as needed. By default, the status is `Inactive`.

   >[!NOTE]
   >
   >After the rule is created, its status can be updated by changing the status to `Active` or `Inactive` as needed.

1. Select the **Websites** where the rule is to be available.

1. Select the **Customer Groups** to which this rule applies.

   To choose multiple groups, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

   >[!NOTE]
   >
   >The options in this list is dependent on the customer groups created and managed in _Customers_ > _Customer Groups_.

1. ![Magento Open Source](../assets/open-source.svg) (Magento Open Source only) Enter the **From** and **To** dates to determine when the price rule is in effect.

   You can enter the dates or use the **Calendar** (![Calendar icon](../assets/icon-calendar.png)) to choose the dates. If you leave the dates blank, the rule is enabled as soon as the price rule is saved.

1. Enter a number to establish the **Priority** of this rule in relation to other rules.

   >[!NOTE]
   >
   >The Priority setting is important when the same catalog product meet the conditions set for more than one price rule. The rule with the highest Priority setting (1 being the highest) will become active for the product.

## Step 2: Define the conditions

Most of the available conditions are based on existing attribute values. To apply the rule to all products, leave the conditions blank.

>[!NOTE]
>
>To apply a `Category` product attribute condition to any [bundle](../catalog/product-create-bundle.md) or [grouped](../catalog/product-create-grouped.md) product, all child products must be assigned to the same category for the rule to apply correctly. If this is not the case, you can use a [Cart Price Rule](price-rules-cart-create.md) promotion instead.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **Conditions** section.

   The first condition appears by default, and states:

         If **ALL** of these conditions are **TRUE**:

   ![Catalog price rule - condition line 1](./assets/catalog-condition1.png)<!-- zoom -->

   The statement has two bold links that you can click to display the selection of options for that part of the statement. You can create different conditions by changing the combination of these values. 
   
1. Change the statement in any of the following ways:

   - Click **ALL** and select `ALL` or `ANY`.
   - Click **TRUE** and select `TRUE` or `FALSE`.
   - Leave the condition unchanged to apply the rule to all products.

   You can create different conditions by changing the combination of these values. For this example, the default condition is used.

1. Click the **Add** (![Add icon](../assets/icon-add-green-circle.png)) icon at the beginning of the next line and select an option for the condition, such as a product attribute or combination.

1. In the list under **Product Attribute**, choose the attribute that you want to use as the basis of the condition. For this example, the condition is `Attribute Set`.

   ![Catalog price rule - condition line 2](./assets/catalog-condition2.png)<!-- zoom -->

   >[!NOTE]
   >
   >For an attribute to appear in the list, it must be configured to be used in promo rule conditions. To learn more, see [Product Attributes](../catalog/product-attributes.md).

   The selected condition appears in the statement, followed by two more bold links. The options differ depending on the condition attribute you select. The statement now says:

       If **ALL** of these conditions are **TRUE**: <br/>Attribute Set **is** …

1. Click **is** and choose the comparison operator that describes the condition to be met.

   These options may include an option for different comparisons, such as matching values, not including or including at least one of a value, and greater than, equal to, and less than a numerical amount. In this example, the options are `is` and `is not`.

1. Select or enter values for the condition. Depending on the condition, you may select products from a grid or list, enter a numerical value, and so on.

   For this example, click the (**...**) more link and choose the attribute set upon which the condition is based.

   ![Catalog price rule - condition line 2](./assets/catalog-condition3.png)<!-- zoom -->

   The selected item appears in the statement to complete the condition.

      If **ALL** of these conditions are **TRUE**: <br/> Attribute Set **is Default**

1. To add another condition line to the statement, click the **Add** (![Add icon](../assets/icon-add-green-circle.png)) icon and choose one of the following:

   - `Conditions Combination`
   - `Product Attribute`

   Repeat the process until all desired conditions are complete.

   If at any time you want to delete part of the condition statement, click the **Delete** (![Delete icon](../assets/icon-delete-red-circle.png) icon at the end of the line.

## Step 3: Define the actions

1. Expand ![Expansion selector](../assets/icon-display-expand.png)the **Actions** section and do the following:

   ![Catalog price rule - actions](./assets/price-rule-catalog-actions.png)<!-- zoom -->

1. Under **Pricing Structure Rules**, set **Apply** to one of the following:

   - `Apply as percentage of original` - Discounts item by subtracting a percentage of the regular price. For example: Enter 10 in Discount Amount for a final price that is marked down 10% from the regular price.
   - `Apply as fixed amount` - Discounts item by subtracting a fixed amount from the regular price. For example: Enter 10 in Discount Amount for a final price that is $10 less than the regular price.
   - `Adjust final price to this percentage` - Adjusts the final price by a percentage of the regular price. For example: Enter 25 in Discount Amount for a final price that is marked down 75% from the regular price.
   - `Adjust final price to discount value` - Sets the final price to a fixed, discounted amount. For example: Enter 20 in Discount Amount for a final price of $20.00.

   >[!NOTE]
   >
   >_Regular price_ refers to the base product price without any advanced pricing (special/tier/group) or promotional discounts. _Final price_ refers to the discounted price that appears in the shopping cart. <br/>The **_final_** product price is calculated as the **_minimum_** relevant price, using the following formula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

1. Enter the **Discount Amount**.

1. To stop processing other rules after this rule is applied, set **Discard Subsequent Rules** to `Yes`.

   >[!NOTE]
   >
   >Setting this to `Yes` is a safeguard to prevent the system from applying multiple discounts (rules) to the same product.

## Step 4: Add related dynamic blocks

{{#ee-feature}}

[Dynamic blocks](../content-design/dynamic-blocks.md) that are associated with a catalog price rule appear in the storefront whenever the conditions are met. This is an optional step.

1. Expand ![Expansion selector](../assets/icon-display-expand.png)the **Related Dynamic Blocks** section.

1. Use the [search filters](../getting-started/admin-workspace.md) to locate the dynamic block(s) that you want to associate with the rule.

1. Select the checkbox in the first column to associate the dynamic block with the rule.

   ![Catalog price rule - related dynamic blocks](./assets/price-rule-catalog-related-dynamic-blocks.png)<!-- zoom -->

## Step 5: Schedule the rule

{{#ee-feature}}

>[!NOTE]
>
>Setting the rule to active must be added as a scheduled update. To learn more, see [Scheduled Changes](price-rule-catalog-scheduled-changes.md).

1. Click **Save and Continue Edit**.

   ![Catalog price rules - scheduled changes](./assets/price-rule-scheduled-changes-new.png)<!-- zoom -->

1. In the _Scheduled Changes_ box, click **View/Edit** to the right of the listed change (or you can click **Schedule New Update** at the top of the box).

   You can either edit the existing update or assign the catalog price rule to another campaign. The **Edit Existing Update** option is selected by default.

1. To schedule the rule, enter the **Start Date** and **End Date** that the price rule is to be active.

   You can either enter the dates or choose the dates from the **Calendar** (![Calendar icon](../assets/icon-calendar.png)).

   ![Catalog price rule - update schedule](./assets/price-rule-catalog-schedule-update.png)<!-- zoom -->

1. Scroll to the _Rule Information_ section and set the **Status** to `active`.

## Step 6: Save and test the rule

1. When complete, save the rule.

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source only) Click **Save and Apply**.

      ![Catalog price rules - pricing structures](./assets/price-rule-catalog-saved.png)<!-- zoom -->

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) Click **Save**.

      The Rule Information page displays an updated timeline in the Scheduled Changes for the rule.

      ![Catalog price rules - scheduled changes](./assets/price-rule-scheduled-changes-updated.png)<!-- zoom -->

1. Update properties for a rule:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) Click **Edit** to display the Rule Information page.

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source only) Click the rule in the list to display the Rule Information page.

1. Test the rule to make sure that it works correctly.

   Price rules are automatically processed with other system rules each night. When you create a new price rule, allow enough time for it to get into the system before you test the rule to make sure that it works correctly. As new rules are added, Commerce recalculates the prices and the priorities accordingly.

## Catalog price rule demo

Watch this video to learn about creating catalog price rules:

>[!VIDEO](https://video.tv.adobe.com/v/343834?quality=12)

## Field descriptions

### Rule Information

|Field|Description|
|-----|-----------|
|Rule name|(Required) The name of the rule is for internal reference.|
|Description|A description of the rule should include the purpose of the rule and explain how it is used.|
|Websites|(Required) Identifies the websites where the rule can be used.|
|Customer Groups|(Required) Identifies the customer groups to which the rule applies.|
|Priority|A number that indicates the priority of this rule in relation to others. The highest priority is number 1.|
|Status|![Magento Open Source](../assets/open-source.svg) (Magento Open Source only) Determines if the rule is currently active in the store. Options: Yes / No|
|From|![Magento Open Source](../assets/open-source.svg) (Magento Open Source only) Specifies the first day the price rule is in effect. If left blank, the price rule goes into effect as soon as it is saved.|
|To|![Magento Open Source](../assets/open-source.svg) (Magento Open Source only) Specifies the last day the price rule is in effect. If left blank, the price rule continues indefinitely.|

### Conditions

Specifies the conditions that must be met before the catalog price rule goes into action. If left blank, the rule applies to all products.

### Actions

|Field|Description|
|-----|-----------|
|Apply|Determines the type of calculation that is applied to the purchase. Options: <br/>**Apply as percentage of original** - Discounts item by subtracting a percentage of the regular price. <br/>**Apply as fixed amount** - Discounts item by subtracting a fixed amount from the regular price. <br/>**Adjust final price to this percentage** - Adjusts the final price by a percentage of the regular price. <br/>**Adjust final price to discount value** - Sets the final price to a fixed, discounted amount. <br/><br/>**_Note:_** Regular price refers to the base product price without any advanced pricing (special/tier/group) or promotional discounts. Final price refers to the discounted price that appears in the shopping cart. <br/>The **_final_** product price is calculated as the **_minimum_** relevant price, using the following formula: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`|
|Discount Amount|(Required) The amount of discount that is offered.|
|Discard Subsequent Rules|Determines if additional rules can be applied to this purchase. To prevent multiple discounts from being applied to the same purchase, select `Yes`. Options: Yes / No|

### Related Dynamic Blocks

{{#ee-feature}}

Identifies any dynamic block(s) that are associated with the rule.
