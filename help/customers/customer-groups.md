---
title: Customer Groups
description: Customer groups determine which discounts are available and the tax class that is associated with the group.
---

# Customer groups

Customer groups determine which discounts are available and the tax class that is associated with the group. The default customer groups are General, Not Logged In, and Wholesale.

![Customer Groups](assets/customer-groups.png))<!-- zoom -->

## Filter the [!UICONTROL Customer Groups] list

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Click **[!UICONTROL Filters]**.

1. Enter criteria for searching groups, including a range of IDs, group, or tax class.

   ![Filtering Options](assets/groups-filters.png)<!-- zoom -->

1. When complete, click **[!UICONTROL Apply Filters]**.

## Create a customer group

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Click **[!UICONTROL Add New Customer Group]**.

1. Enter a unique [!DNL **Group Name]** less than 32 characters to identify the group.

1. Select the **[!UICONTROL Tax Class]** that applies to the group.

1. Select the **[!UICONTROL Excluded Website(s)]** that you want to [exclude from the group](https://developer.adobe.com/commerce/php/development/components/indexing/optimization/).

   >[!NOTE]
   >
   > No websites are excluded by default. To select multiple values, hold down the _Ctrl key_ (PC) or the _Command key_ (Mac) and click each option.

   ![Group Information](assets/group-information.png)<!-- zoom -->

1. When complete, click **[!UICONTROL Save Customer Group]**.

## Edit a customer group

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Open the record in edit mode.

1. Make the necessary changes.

1. When complete, click **[!UICONTROL Save Customer Group]**.

## Assign a customer to a different group

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Find the customer in the list and select the checkbox in the first column.

1. Set the **Actions** control to `Assign a Customer Group`.

1. Set the **Group** control to the new group.

1. When prompted to confirm, click **OK**.

   ![Assign a Customer Group](assets/group-assign.png)<!-- zoom -->

## Associate a group of customers with specific discounts

1. On the _Admin_ sidebar, go to **[!UICONTROL Marketing]** > _Promotions_ > **[!UICONTROL Cart Price Rules]**.

1. Select the cart price rule with the discount to apply, or [create a new price rule](../merchandising-promotions/price-rules-catalog.md).

1. Select the customer groups the rule will apply to.

   ![Customer Group to Specific Discounts](assets/group-discount.png)<!-- zoom -->

1. Click **[!UICONTROL Save]**.

>[!NOTE]
>
> You can also use Advance pricing to apply product discounts to customer groups. See [Advanced pricing](../catalog/product-price-group.md).

## Delete a customer group

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Open the record in edit mode.

1. In the button bar, click **[!UICONTROL Delete Customer Group]**.

1. When prompted to confirm, click **OK**.

## Customer groups demo

Watch this video to learn about creating customer groups:

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12)
