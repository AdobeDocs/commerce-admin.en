---
title: Reward and loyalty programs
description: <placeholder>
---
# Reward and loyalty programs

{{#ee-feature}}

The _reward points_ system in Adobe Commerce gives you the ability to implement unique programs that drive customer engagement and promote customer loyalty. Points can be awarded for a wide range of transaction and customer activities, and the configuration can be set to control the point allotment, balance, and expiration. Customers can redeem points toward purchases, based on the conversion rate that you establish between reward points and currency. A few examples:

## Shopping cart price rules

Points can be rewarded to customers on the basis of a [shopping cart rule](price-rules-cart.md). They can be rewarded as the only action of the price rule, or in conjunction with a discount.

## Customer balance

Reward point balances can be managed by Admin users per customer. If enabled in the storefront, customers can also view the details of their points balance.

## Redeeming points

Points can be redeemed by Admin users and customers (if enabled) during checkout. In the Payment Method section, a Use my Reward Points checkbox appears above the enabled payment methods. The available points and monetary exchange rate is included. If the available balance is greater than the order grand total, no additional payment methods is required. The amount of reward points applied to the order appears with the order totals, subtracted from the grand total, similar to a store credit or gift cards. If reward points are used in conjunction with store credit or a gift card, the reward points are deducted first, and the store credit or gift card is deducted if the order total is greater than the redeemable amount of reward points.

>[!NOTE]
>
>Reward points are not recommended for use with COD purchases, because receipt of payment cannot be confirmed until after the order is invoiced.

## Refund to reward points

Orders placed with reward points can be refunded to the reward points balance up to the amount redeemed in the order. On the [_New Credit Memo_ page](https://docs.magento.com/user-guide/sales/credit-memo-create.html), the amount of points to be applied to the customer's balance can be entered. By default, the field contains the full amount of points that were used in the order.

## Configure reward points

The Reward Points configuration determines how reward points are presented in the store and defines the basic operating parameters.

![Customers configuration - reward points](../configuration-reference/customers/assets/reward-points-reward-points.png)<!-- zoom -->

### Step 1. Configure the Reward Points

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Customers** and choose **Reward Points**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Reward Points** section and do the following:

   - To activate reward points, set **Enable Reward Points Functionality** to `Yes`.

   - To allow customers to earn their own reward points, set **Enable Reward Points Functionality on Storefront** to `Yes`.

   - To allow customers to see a detailed history of their rewards, set **Customers May See Reward Point History** to `Yes`.

1. In the **Reward Points Balance Redemption Threshold** field, enter the number of points that must accrue before they can be redeemed (blank for no minimum).

1. Enter the maximum number of points a customer can accrue in the **Cap Reward Points Balance At** field (blank for no limit).

1. Enter the number of days before the reward points expire in the **Reward Points Expire in (days)** field (blank for no expiration).

1. Set **Reward Points Expiry Calculation** to one of the following:

   - `Static` - Determines the remaining lifetime of reward points based on the number of days set in the configuration. If the expiration limit in the configuration changes, the expiration date of existing points does not change.
   
   - `Dynamic` - Calculates the number of days left whenever the reward point balance increases. If the expiration limit in the configuration changes, the expiration of all existing points update accordingly.

1. If you want to refund available reward points automatically, set **Refund Reward Points Automatically** to `Yes`.

1. If you want to automatically deduct reward points from the amount of a refund, set **Deduct Reward Points from Refund Amount Automatically** to `Yes`.

1. Set **Landing Page** to the content page that explains your reward points program.

   Make sure to update the default Rewards Points page with your own information.

1. When complete, click **Save Config**.

### Step 2. Configure Points Earned for Customer Activities

In this step, the number of reward points that can be earned for various customer activities is specified. When customers complete an action that has points assigned, a message appears to the customer that indicates how many points they have earned.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Actions for Acquiring Reward Points by Customer** section.

    ![Customers configuration - actions for acquiring reward points by customer](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png)<!-- zoom -->

1. To display a message in the shopping cart that includes the rewards points earned for the purchase and the customer's current reward point balance, set **Purchase** to `Yes`.

1. For **Registration**, enter the number of points earned for opening a customer account.

1. For **Newsletter Signup**, enter the number of points earned by registered customers who subscribe to a newsletter.

1. For **Converting Invitation to Customer**, enter the number of points earned by a customer who sends an invitation and the recipient then opens a customer account.

   To limit the number of invitation conversions that can be used to earn points for the customer who sends the invitation (blank for no limit), enter a number in the **Invitation to Customer Conversions Quantity Limit** field.

1. For **Converting Invitation to Order**, enter the number of points earned by a customer who sends an invitation to the recipient who then places an order and do the following:

   - In the **Invitation to Order Conversions Quantity Limit** field, enter the number of points earned by the customer sending the invitation when the recipient places an initial order (blank for no limit).

   - In the **Invitation Conversion to Order Reward** dropdown select the `Each` option to earn points for each placed by recipient order, or select the `First` option to earn points only for the first placed order by the recipient.

1. For **Review Submission**, enter the number of points earned by a customer who submits a review that is approved for publication.

1. Then to limit the number of reviews that can be used to earn points per customer, enter the number in the **Rewarded Reviews Submission Quantity Limit** field (blank for no limit).

1. When complete, click **Save Config**.

### Step 3. Complete the Email Notification Settings

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Email Notification Settings** section.

    ![Customers configuration - reward points email notifications](../configuration-reference/customers/assets/reward-points-email-notification-settings.png)<!-- zoom -->

1. Set **Email Sender** to the store contact that appears as the sender of balance updates and expiration notifications.

1. If you want to subscribe customers by default to be notified of balance updates and upcoming expiration dates, set **Subscribe Customers by Default** to `Yes`.

1. Set **Balance Update Email** to the template used for the notification that is sent to customers whenever their point balance is updated.

1. Set **Reward Points Expiry Warning Email** to the template used for the notification that is sent to customers when the expiration limit for a batch of points is reached.

1. For **Expiry Warning Before (days)**, enter the number of days before points expire that notification is sent.

1. When complete, click **Save Config**.

## Update the reward points balance

The reward points balance can be updated from the Admin.

1. On the _Admin_ sidebar, go to **Customers** > **All Customers**.

1. Find the customer in the grid and click **Edit** in the _Action_ column.

1. Under _Customer Information_, choose the **Reward Points** section.

1. Enter the number of **Update Points**:

   - To update the reward points amount, enter the number to increase the total points balance.
   - To subtract the reward points amount, enter the negative number you want to reduce the total points balance.

1. Enter **Comments** related to the reward points adjustment, if needed.

   ![Reward Points Balance](./assets/reward-points-balance.png)<!-- zoom -->

1. Optionally, subscribe the customer to _Reward Points Notifications_:

   - **Subscribe for Balance Updates**
   - **Subscribe for Points Expiration Notifications**

1. Click **Save Customer**.

All actions related to reward points are displayed in the customer's **Reward Points History** block in their account on the storefront.

## Field descriptions

|Field|Description|
|--- |--- |
|Balance|Current balance of reward points for client|
|Amount Balance|The amount of the current cash balance|
|Points|The number of added or subtracted points|
|Amount|Amount of money added or subtracted|
|Rate|[Reward exchange rate](reward-exchange-rates.md)|
|Website|Website to which the reward points history is assigned|
|Reason|Reasons for awarding points:<br>**Making purchases** — Every time the customer makes a purchase they can earn points.<br>**Registering on the site** - Accrued upon registration (once).<br>**Subscribing to a newsletter** - Accrued for the first time subscription (once).<br>**Sending Invitations** — Earn points by inviting their friends to join the site.<br>**Converting Invitations to Customer** — Earn points for every invitation they send out, leading friends registering on the site.<br>**Converting Invitations to Order** — Earn points for each sale resulting from a sent invitation.<br>**Review Submission** — Earn points for submitting product reviews.|
|Created|Date and time of reward points update|
|Expires|Amount of expired reward points|
|Comment|Comments when adding or subtracting points|

## Troubleshooting resources

For help with troubleshooting reward points issues, see the following Commerce Support articles:

- [Loyalty points on partial orders](https://support.magento.com/hc/en-us/articles/360051330832)
- [404 error removing rewards points on multi-shipping checkout](https://support.magento.com/hc/en-us/articles/360046920131)
