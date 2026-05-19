---
title: Customer segments in price rules
description: Learn about associating customer segments with a cart price rule so that you can define targeted promotions for your store.
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
TQID: https://experienceleague.adobe.com/MSMNikJwG2lQuLlQxnK82zjCOeF-u8JEjmabKFJgpZU
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
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Customer segments in price rules

{{ee-feature}}

A customer segment can be used for targeted promotions by associating it with a [cart price rule](../merchandising-promotions/price-rules-cart.md).

![Cart price rule - targeted customer segment](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_**To associate a segment with a cart price rule:**_

1. On the _Admin_ sidebar, go to **[!UICONTROL Marketing]** > _Promotions_ > **[!UICONTROL Cart Price Rules]**.

1. Open a new or existing rule:

   * To use a new rule, click **[!UICONTROL Add New Rule]** in the upper-right corner.
   * To use an existing rule, click the rule in the list to open it in edit mode.

1. Scroll down and expand the **[!UICONTROL Conditions]** section.

1. Add the condition.

   * Click the _Add_ (![List icon](../assets/icon-add-green-circle.png)) icon, which displays the list of conditions. Then, choose **[!UICONTROL Customer Segment]**.

   ![Cart price rule - add customer segment condition](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   By default, the condition is set to find a matching condition. If needed, click the **[!UICONTROL matches]** link and change the operator to one of the following:

      * `does not match`
      * `is one of`
      * `is not one of`

   ![Condition operator](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. To target a specific segment, click the More **…** link to display additional options. Then, click the _Chooser_ (![List icon](../assets/icon-list-chooser.png)) icon to display the list of customer segments.

1. In the list, select the checkbox of each segment that you want to target with the condition.

   ![Cart price rule - condition chooser list](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Select]** to place the selected customer segments into the condition.

1. Complete the rest of the price rule as needed.

1. When complete, click **[!UICONTROL Save]**.
