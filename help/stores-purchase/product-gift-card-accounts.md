---
title: Gift card accounts
description: Learn about gift card accounts and how to configure the default settings for code pool management. 
---
# Gift card accounts

A gift card account is automatically created for each Gift Card that is purchased. The value of the gift card can then be applied toward the purchase of a product in your store. You can also create gift card accounts from the Admin as a promotion or service for customers. The gift card account number corresponds to the gift card code.

![Gift Card Accounts](./assets/marketing-gift-card-accounts-grid.png)<!-- zoom -->

## Configure gift card accounts

The Gift Card configuration establishes the default settings for all gift cards for the store view and manages the code pool. The code pool is a set of unique gift card codes in a specific format. Codes from the pool are used each time a gift card account is created. It is the responsibility of the store administrator to ensure that there are enough codes available for gift card sales. Make sure to generate a code pool before offering gift cards for sale. By default, Adobe Commerce generates 1,000 codes. A new code pool is not generated until there are no more codes available in the current pool.

### Step 1: Configure email notifications

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Sales** and choose **Gift Cards**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the _Gift Card Email Settings_ section and do the following:

   - Set **Gift Card Notification Email Sender** to the store identity that appears as the sender of gift card notifications.

   - Set **Gift Card Notification Email Template** to the template that is used for the notification.

    ![Gift Card Email Settings](../configuration-reference/sales/assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the _Email Sent from Gift Card Account Management_ section and do the following:

   - Set **Gift Card Email Sender** to the store identity to appear as the sender of the gift cards.

   - Set **Gift Card Template** to the template you want to use for the gift card.

See [Store Email Addresses](https://docs.magento.com/user-guide/configuration/general/store-email-addresses.html) for specific configuration fields and options.

### Step 2: Complete the general settings

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the _Gift Card General Settings_ section.

1. To allow the customer to redeem the value on the card for cash, set **Redeemable** to `Yes`.

1. For **Lifetime (days)**, enter the number of days before the card expires.

   If there is no expiration date, leave the field blank.

   >[!NOTE]
   >
   >Depending on your location, it may be illegal for gift cards to expire. Check your local laws before setting a lifetime for your gift cards.

1. To give customers the option to enter a message to accompany the gift card, set **Allow Gift Message** to `Yes` and enter the number of characters available for the message for **Gift Message Maximum Length**.

1. Set **Generate Gift Card Account when Orders Item is** to one of the following:

   - `Ordered` - The gift card account is created when the order is placed.
   - `Invoiced` - The gift card account is created after payment is captured and the order is invoiced.

   ![Gift Card General Settings](../configuration-reference/sales/assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

### Step 3: Establish the gift card code pool

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the _Gift Card Account General Settings_ section and do the following:

   ![Gift Card Account General Settings](../configuration-reference/sales/assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

   - To customize the code, complete the following according to your preference:

      - Code Length
      - Code Format
      - Code Prefix
      - Code Suffix
      - Dash Every X Characters

   - To determine the number of codes to generate, enter the **New Pool Size**.

   - To specify when you receive notification to restock the code pool, enter the **Low Code Pool Threshold**.

1. Before you generate the code pool, click **Save Config**.

1. Click **Generate**.

1. When complete, click **Save Config**.

## Review an existing gift card account

1. If you need to find the number of the gift card account for a current order, do the following:

    - On the _Admin_ sidebar, go to **Sales** > _Operations_ > **Orders**.

    - Find the order in the list and click **View** in the _Action_ column.

    - Scroll down to the _Items Ordered_ section.

    The number is in the _Product_ column, under **Gift Card Accounts**.

1. On the _Admin_ sidebar, go to **Marketing** > _Promotions_ > **Gift Card Accounts**.

1. Find the gift card account in the grid and open it in edit mode.

   The gift card code appears at the top of the _Information_ section.

   ![Gift Card Account Information](./assets/gift-card-account-information.png)<!-- zoom -->

## Create a gift card account

1. On the _Admin_ sidebar, go to **Marketing** > _Promotions_ > **Gift Card Accounts**.

1. At the upper-right corner, click **Add Gift Card Account**.

   ![New Account](./assets/gift-card-account-add-new.png)<!-- zoom -->

1. In the _Information_ section, set **Active** to `Yes` and do the following:

    - To make the card balance redeemable at checkout or transferred to the customer's store credit, set **Redeemable** to `Yes`.

    - Choose the **Website** where the gift card account can be used.

    - Enter the initial **Balance** on the gift card.

    - To set an **Expiration Date** for the gift card, select the date from the calendar ![Calendar icon](../assets/icon-calendar.png).

      If left blank, the gift card account does not expire.

    ![Gift Card Information](./assets/marketing-gift-card-accounts-new-information.png)<!-- zoom -->

1. In the left panel, choose **Send Gift Card** and do the following:

    - Enter the **Recipient Email** address.

    - Enter the **Recipient Name**.

    - Set **Send Email from the Following Store View** to the store view that appears as the sender of the gift card notification.

    ![Send Gift Card Settings](./assets/marketing-gift-card-accounts-new-send.png)<!-- zoom -->

1. Do one of the following to save the new account:

    - If you are not ready to send the gift card, click **Save**.

    - To save the changes and send the gift card by email to the recipient, click **Save & Send Email**.

## View gift card account history

1. Go to **Marketing** > **Gift Card Accounts**.

1. Open the gift card in Edit mode.

1. The **History** of the gift card is displayed.

   ![Gift Card History](./assets/gift-card-history.png)<!-- zoom -->

|Column|Description|
|--- |--- |
|ID|A unique numeric of action with gift card.|
|Date|Date of action.|
|Action|Determines all possible actions with a gift card. Options: Created / Updated / Sent / Used / Redeemed / Expired|
|Balance Change|Displays the amount by which the balance of the gift card has changed.|
|Balance|Indicates the available balance.|
|More Information|Displays information about who changed the balance of the gift card.|

{style="table-layout:auto"}

## Delete a gift card account

1. On the _Admin_ sidebar, go to **Marketing** > _Promotions_ > **Gift Card Accounts**.

1. Select the gift card account to be deleted and open it in edit mode.

1. In the menu bar, click **Delete**.

1. To confirm the action, click **OK**.

## Column descriptions

|Column|Description|
|--- |--- |
|ID|A unique numeric identifier that is assigned to gift card account.|
|Code|The code that must be entered to apply a gift card.|
|Website|Indicates the websites where the gift card account is available.|
|Created|Creation date.|
|End|Gift card expiration date, if scheduled.|
|Active|Determines if the gift card is active.|
|Status|Determines if the gift card is redeemed in customer's account or available. Options: Used / Redeemed / Expired|
|Balance|Indicates the available balance.|

{style="table-layout:auto"}
