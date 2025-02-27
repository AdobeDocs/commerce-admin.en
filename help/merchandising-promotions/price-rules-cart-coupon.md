---
title: Coupon codes
description: Learn how to use coupons codes with cart price rules to apply a discount when a set of conditions is met.
exl-id: 4f2e6203-0de2-44eb-a5f7-edd7b5f714d1
feature: Merchandising, Price Rules, Shopping Cart
---
# Coupon codes

Coupons codes are used with [cart price rules](price-rules-cart.md) to apply a discount when a set of conditions is met. For example, a coupon code can be created for a specific customer group, or for anyone who makes a purchase over a certain amount. To apply the coupon to a purchase, the customer can enter the coupon code in the cart, or possibly at the cash register of your _brick and mortar_ store. Here are a few ways that you can use coupons in your store:

- Email coupons to customers
- Produce printed coupons
- Create in-store coupons for mobile users

Coupon codes can be sent by email, or included in newsletters, catalogs, and advertisements. The list of coupon codes can be exported and sent to a commercial printer. You can also create in-store coupons with a quick response code that shoppers can scan with their smart phones. The QR code can link to a page on your site with more information about the promotion.

As of Commerce 2.4.7, shoppers can apply multiple coupons to a cart. Merchants can also apply multiple coupons using shopping assistance.

>[!NOTE]
>
>Cart price rules that have the same priority do not result in a combined discount. Each rule (coupon) is applied to matching products separately, one-by-one, according to the cart price rule ID in the database. To control the order in which discounts are applied, Adobe recommends setting a different priority for each added cart price rule.

## Configure coupon codes

The length and format of automatically generated coupon codes is controlled by the configuration. The characters can be set to all numbers, all letters, or a combination. You can insert a dash at set intervals to make it easy to read, and add a prefix and suffix to associate the code with a specific campaign or initiative.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Customers]** and choose **[!UICONTROL Promotions]**.

   ![Customers configuration - auto-generated specific coupon codes](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Expand the **[!UICONTROL Auto Generated Specific Coupon Codes]** section.

   ![Customers configuration - auto-generated specific coupon codes](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Enter the **[!UICONTROL Code Length]**, including prefix, suffix, and separators.

1. Set the **[!UICONTROL Code Format]** to one of the following:

   - `Alphanumeric`
   - `Alphabetical`
   - `Numeric`

1. For **[!UICONTROL Code Prefix]**, enter the value that you want to appear at the beginning of all coupon codes.

1. For **[!UICONTROL Code Suffix]**, enter the value that you want to appear at the end of all coupon codes.

1. For **[!UICONTROL Dash Every X Characters]**, enter the number of characters between each dash.

   Coupon codes with different dash patterns are considered to be different codes, even if the numbers are the same.

1. When complete, click **[!UICONTROL Save Config]**.

## Create coupons

>[!NOTE]
>
>Before you create coupons, use the `bin/magento cron:run` command to verify that cron is running. See [Run cron from the command line](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html#run-cron-from-the-command-line) in the _Configuration Guide_ for more information.

### Method 1: Create a specific coupon

1. Follow the instructions to create a [cart price rule](price-rules-cart.md).

1. In the **[!UICONTROL Rule Information]** section, set **[!UICONTROL Coupon]** to `Specific Coupon`.

1. Enter a **[!UICONTROL Coupon Code]** to be used with the promotion.

   The format of the code (numeric, alphanumeric, or alphabetical) is determined by the [configuration](#configure-coupon-codes).

1. To limit the number of times the coupon can be used, do the following:

   - Enter the number of **[!UICONTROL Uses per Coupon]**.
   - Enter the number of **[!UICONTROL Uses per Customer]**.

   For unlimited use, leave these fields blank.

   ![Cart price rule - coupon information](./assets/coupon-info.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >If there is simultaneous use of the same coupon by multiple customers at the same time, it is possible that the usage limit that is set could be exceeded due to delayed coupon processing.

1. To make the coupon valid for a time period, do the following:

   - ![Magento Open Source](../assets/open-source.svg) (Magento Open Source only) Complete the **From** and **To** dates. To select the date, click the **Calendar** (![Calendar icon](../assets/icon-calendar.png)) icon next to each field. If you leave the date range empty, the rule does not expire.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) Do one of the following:

      **Option 1:** Schedule a new update

      - Click **[!UICONTROL Schedule New Update]** in the upper-right corner of the page.

        ![Schedule Update](./assets/coupon-schedule-new-update.png){width="600" zoomable="yes"}

      - Enter the **[!UICONTROL Update Name]** and **[!UICONTROL Description]**.

      - Choose the **Start Date** and **[!UICONTROL End Date]** from the Calendar ( ![Calendar icon](../assets/icon-calendar.png) ). If you leave the date range empty, the rule does not expire.

      - When complete, click **[!UICONTROL Save]**.

        ![Cart price rule - scheduled change](./assets/coupon-scheduled-change.png){width="600" zoomable="yes"}

      **Option 2:** Assign to an existing update:

      - Select **[!UICONTROL Assign to Another Update]**.

      - Find the update in the list, and click **[!UICONTROL Select]**.

1. Complete the [cart price rule](price-rules-cart.md) as needed.

### Method 2: Generate a batch of coupons

The generation of discount coupons is an asynchronous operation, which executes in the background so that you can continue working in the Admin without waiting for the operation to finish. The system displays a message when the task is complete.

1. Follow the instructions to create a [cart price rule](price-rules-cart.md).

1. Under **[!UICONTROL Coupon Code]**, select the **[!UICONTROL Use Auto Generation]** checkbox.

1. To limit the number of times each customer can use the coupon, enter the number of **[!UICONTROL Uses per Customer]**.

   ![Cart price rule - generate auto-numbered coupons](./assets/coupon-auto.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >If there is simultaneous use of the same coupon by multiple customers at the same time, it is possible that the usage limit that is set could be exceeded due to delayed coupon processing.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Manage Coupon Codes]** section and do the following:

   ![Cart price rule - manage coupon codes](./assets/manage-coupon-codes.png){width="600" zoomable="yes"}

   - For **[!UICONTROL Coupons Qty]**, enter the number of coupons that you want to generate.

   - Enter the **[!UICONTROL Code Length]**, not including the prefix, suffix, or separators.

   - Set the **[!UICONTROL Code Format]** to one of the following:

      - `Alphanumeric`
      - `Alphabetical`
      - `Numeric`

   - (Optional) Enter a **[!UICONTROL Code Prefix]** to be added to the beginning of the code.

   - (Optional) Enter a **[!UICONTROL Code Suffix]** to be added to the end of the code.

   - (Optional) For **[!UICONTROL Dash Every X Characters]**, enter the number of characters between each dash. For example, if the code is 12 characters long, and there is a dash every four characters, it looks like `xxxx-xxxx-xxxx`. Dashes make codes easier to read and enter.

1. When complete, click **[!UICONTROL Generate]**.

   The system displays `Message is added to queue, wait to get your coupons soon`.

   After the cron job completes, the list of generated codes is displayed.

   | Field       | Description |
   |-------------|-------------|
   | [!UICONTROL Coupon Code] | A unique code of coupon that was created and can be used for receiving special conditions. |
   | [!UICONTROL Created]     | The date when the coupon code was created.|
   | [!UICONTROL Used]        | Indicates if the coupon was used. |
   | [!UICONTROL Times Used]  | Indicates how many times that the coupon code was used. |

   {style="table-layout:auto"}

You can export coupon codes to a CSV or Excel XML file by selecting the file format and clicking **[!UICONTROL Export]**.

To delete coupon codes, select one or more codes from the list. Select `Delete` from the **[!UICONTROL Actions]**  selector, and then click **[!UICONTROL Submit]**.

>[!NOTE]
>
>Although Commerce allows configuring multiple coupon codes, a customer can use only one coupon code in the cart. To allow the use of more than one coupon code in the cart simultaneously, you could consider using a corresponding extension from [Commerce Marketplace](https://marketplace.magento.com/).

## Coupons report

The _Coupons_ report aggregates data from each coupon that is used during a specific date range. Because coupons are applied from the shopping cart, the report includes data from all redeemed coupons, regardless of [order status](../stores-purchase/order-status.md). As a result, the report might include both projected and actual totals. The report can be filtered for a specific store view, time period, order status, and cart price rule.

In the following example, the coupon code "H20" was used by two customers. One of the orders is invoiced, but the other is still _pending_. The projected Sales Subtotal, Sales Discount, and Sales Total columns show the aggregated amounts from both orders, but only the actual invoiced order appears in the Subtotal, Discount, and Total columns. Each row in the report represents a single coupon promotion.

![Coupons report](./assets/reports-coupons.png){width="600" zoomable="yes"}

### Run the report

1. On the _Admin_ sidebar, go to **[!UICONTROL Reports]** > _[!UICONTROL Sales]_ > **[!UICONTROL Coupons]**.

1. If you have multiple store views, set **[!DNL Store View]** in the upper-left corner to establish the scope of the report.

1. To refresh the sales [statistics](../getting-started/sales-reports.md#refresh-statistics) for the day, click the _Last Updated_ message at the top of the workspace.
   
   Next, click to select the **[!UICONTROL Coupons]** checkbox and click **[!UICONTROL Refresh]**.

   ![Coupons report - refresh statistics](./assets/reports-coupons-refresh-statistics.png){width="600" zoomable="yes"}

1. To filter the data, do the following:

   ![Coupon report - filters](./assets/reports-coupons-filters.png){width="600" zoomable="yes"}

   - Set **[!UICONTROL Date Used]** to one of the following:

      - `Order Created`
      - `Order Updated`

      The _Order Updated_ report is created in real time and does not require a refresh.

   - To define the time period covered by the report, set **[!UICONTROL Period]** to one of the following:

      - `Day`
      - `Month`
      - `Year`

   - To define the date range of the report, enter the **From** and **To** dates in M/D/YY format.

   - To print a report for a specific [order status](../stores-purchase/order-status.md), set **[!UICONTROL Order Status]** to `Specified` and choose the order status from the list.

   - To omit rows without data from the report, set **[!UICONTROL Empty Rows]** to `No`.

   - To define coupon activity included in the report, do one of the following:

      - To include all coupon activity from all price rules, set **[!UICONTROL Cart Price Rule]** to `Any`.
      - To include only activity related to a specific price rule, set **[!UICONTROL Cart Price Rule]** to `Specified` and select the cart price rule in the list.

1. When ready to run the report, click **[!UICONTROL Show Report]**.

   The report appears at the bottom of the page.

### Filter options

|Field|Description|
|--- |--- |
|[!UICONTROL Date Used] |Identifies the date field that is used as the basis of the report. Options:<br/>**[!UICONTROL Order Created]**: Generates the report based on the date that the order was placed by the customer. To ensure that the most current data is included, click the link in the message to refresh statistics. <br/>**[!UICONTROL Order Updated]**: Generates the report based on the date orders were last updated. This report uses real-time data and does not require statistics to be refreshed.|
|[!UICONTROL Period]|Determines the type of date range that is used for the report. Options: `Day` / `Month` / `Year`|
|[!UICONTROL From]|Indicates the first date in the range of order data that is included in the report.|
|[!UICONTROL To]|Indicates the last date in the range of order data that is included in the report.|
|[!UICONTROL Order Status]|Filters the report by order status. The report can be generated for all orders or can be limited to a specific order status. Options: <br/>**[!UICONTROL Any]**: Includes all orders regardless of status. <br/>**[!UICONTROL Specified]**: Includes only orders with the specified status. Canceled orders are not included in the report.|
|[!UICONTROL Empty Rows]|Determines if the report includes any rows of empty data that might be retrieved. Options: `Yes` / `No`|
|[!UICONTROL Cart Price Rules]|Determines which coupon promotions are included in the report. Options:<br/>**[!UICONTROL Any]**: Includes order information for any coupon promotion that was used during the specified date range.<br/>**[!UICONTROL Specified]**: Includes only order information for the selected coupon promotion during the specified date range.|

{style="table-layout:auto"}

### Report columns

|Column|Description|
|--- |--- |
|[!UICONTROL Interval]|Indicates the date range of coupon usage to be included in the report. The interval can be a specific day, month, or year, or range of dates. The interval date is formatted as in the following examples, according to the value set in **[!UICONTROL Period]** setting:<br/>`Day`: 6/21/19<br/>`Month`: 6/2019<br/>`Year`: 2019|
|[!UICONTROL Coupon Code]|The Discount Code that is entered by customers in the shopping cart to receive the discount.|
|[!UICONTROL Price Rule]|The name of the price rule that is associated with the coupon.|
|[!UICONTROL Uses]|The number of times the coupon has been used during the date range specified for the report.|
|[!UICONTROL Sales Subtotal]|The projected Subtotal from all orders that were placed with the coupon. <br/>The Sales Subtotal represents the aggregated Subtotal from all qualifying orders and includes `Pending` sales orders that are not yet invoiced.|
|[!UICONTROL Sales Discount]|The projected Discount amount from all orders that were placed with the coupon. <br/>The Discount represents the aggregated discount amount from all qualifying orders and includes `Pending` sales orders that are not yet invoiced.|
|[!UICONTROL Sales Total]|The projected Grand Total from all orders that were placed with the coupon. The Sales Total includes any shipping and handling fees, less the discount amount. <br/>The Sales Total represents the aggregated Grand Total amount from all qualifying orders and includes `Pending` sales orders that are not yet invoiced. The value includes the Subtotal plus Shipping and Handling, less the Discount, plus Tax. <br/> Calculated by: `((Subtotal + Shipping & Handling) - Discount) + Tax` |
|[!UICONTROL Subtotal]|The aggregated Subtotal from all invoiced orders that used the coupon.|
|[!UICONTROL Discount]|The aggregated Discount from all invoiced orders that used the coupon.|
|[!UICONTROL Total]|The aggregated Order Total from all invoiced orders that used the coupon.|

{style="table-layout:auto"}
