---
title: Business Intelligence Tools
description: Learn how Adobe Commerce and Magento Open Source merchants can use business intelligence tools to gain the insight used to make sound business decisions.
---
# Business Intelligence Tools

Use business intelligence tools to gain the insight used to make sound business decisions.

## Business Intelligence account

When you activate a Business Intelligence account through Adobe, you get access to five dashboards with approximately 70 reports. These reports are designed to provide insights around your data and answer questions like “How are my orders growing month-over-month?", "Who are my most loyal customers?", and "Is my coupon strategy working?” For detailed information about this tool set, see the [Magento Business Intelligence User Guide][2].

## Advanced Reporting

Advanced Reporting is included with Adobe Commerce and Magento Open Source. This feature gives you access to a suite of dynamic reports that are based on your product, order, and customer data, with a personalized dashboard that is tailored to your business needs. While Advanced Reporting uses Business Intelligence for analytics, you do not need to have a Business Intelligence account to use Advanced Reporting.

For technical information, see the [Advanced Reporting][1]{:target="_blank"} in the developer documentation.

>[!NOTE]
>
>Business Intelligence accounts use built-in reporting, rather than the Advanced Reporting feature.

![Advanced Reporting dashboard](./assets/reporting-advanced.png)<!-- zoom -->

### Requirements

* The website must run on a public web server.

* The domain must have a valid security (SSL) certificate.

* Commerce must have been installed or upgraded successfully without error.

* In the Commerce configuration for [store URLs](https://docs.magento.com/user-guide/stores/store-urls.html), the **Base URL (Secure)** setting for the store view must point to the secure URL. For example: `https://yourdomain.com`.

* In the Commerce configuration for store URLs, **Use Secure URLs on Storefront** and **Use Secure URLs in Admin** must be set to `Yes`.

* Make sure that [Commerce crontab][3]{:target="_blank"} is created and cron jobs are running on the installed server.

>[!NOTE]
>
>Advanced Reporting can be used only with Commerce installations that have continually used a single [base currency](https://docs.magento.com/user-guide/stores/currency-configuration.html).


### Step 1: Enable Advanced Reporting

In the Commerce configuration, [Advanced Reporting](https://docs.magento.com/user-guide/configuration/general/advanced-reporting.html) is enabled by default, and starts automatically if cron is [configured](https://docs.magento.com/user-guide/configuration/advanced/system.html) and running. An attempt to establish the subscription is initiated at the beginning of each hour over the next 24-hours until successful. The subscription status is “pending” until the subscription is successfully established.

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel where **General** is expanded, choose **Advanced Reporting** and do the following:

   * Verify that **Advanced Reporting Service** is set to `Enable` (the default setting).

   * Set the **Time of day to send data** to the hour, minute, and second, according to a 24-hour clock, that you want the service to receive updated data from your store. By default, data is sent at 2:00 AM.

   * Under **Industry Data**, choose the **Industry** that best describes your business.

   ![Advanced Reporting configuration](./assets/advanced-reporting-config.png)<!-- zoom -->

1. When complete, click **Save Config**.

1. When prompted, click the [Cache Management](https://docs.magento.com/user-guide/system/cache-management.html) in the message at the top of the page and refresh any invalid caches.

1. Wait overnight, or until after the time of your next scheduled update. Then, check the status of your subscription. If the status is still _pending_, make sure that your installation meets all requirements.

### Step 2: Access Advanced Reporting

1. Do one of the following:

   * On the _Admin_ sidebar, choose **Dashboard**. Then, click **Go to Advanced Reporting**.
   * On the _Admin_ sidebar, go to **Reports** > _Business Intelligence_ > **Advanced Reporting**.

   The Advanced Reporting dashboard provides a quick summary of your orders, customers, and products. Make sure to scroll down to see the full dashboard.

1. To get a better view of the data, set the **Filters** in the upper-right corner to the time period and store view that you want to include in the report. Then, do the following:

   * Hover over any data point for more information.
   * To see all dashboard reports, click each tab.

   ![Data Point](./assets/reporting-advanced-data-point.png)<!-- zoom -->

### Access your data resources:

In the upper-right corner of the Advanced Reporting dashboard, click **Additional Resources**.

![Advanced Reporting data resources](./assets/advanced-reporting-your-data-resources.png)<!-- zoom -->

### Troubleshooting

If you get a 404 “Page Not Found” message, verify that your store meets the requirements for Advanced Reporting. Then, follow the instructions to verify that the integration is installed.

#### Verify that the Integration is Active

1. On the _Admin_ sidebar, go to **System** > _Extensions_ > **Integration**.

1. Verify that the **Magento Analytics user** integration appears in the list and the **Status** is `Active`.

1. To reestablish the user, click **Reauthorize** and do the following:

   ![Reauthorize](./assets/advanced-reporting-integration-reauthorize.png)<!-- zoom -->

   * When prompted, click **Reauthorize** to approve access to the API resources.

      ![Reauthorize Access to API Resources](./assets/advanced-reporting-integration-api.png)<!-- zoom -->

   * Verify that the list of Integration Tokens for Extensions is complete. Then, click **Done**.

      ![Integration Tokens](./assets/advanced-reporting-integration-tokens-for-extensions.png)<!-- zoom -->

1. Look for the message that indicates the integration `Magento Analytics user` is reauthorized.

1. Wait overnight, or until after the time of your next scheduled update.

#### Verify Single Base Currency

Advanced Reporting can be used only with Commerce installations that have used only a single [base currency](https://docs.magento.com/user-guide/stores/currency-configuration.html) since the time of installation. The result is that in the history, all orders use the same base currency. Advanced Reporting does not work if you have, at any time, changed your base currency and have orders in your history that were processed with different base currencies.

To determine if your store has multiple base currencies, you can query your Commerce database from the command line using the following MySQL example. You might be required to change the table names to match your data structure:

```sql
select distinct base_currency_code from sales_order;
```

#### Data discrepancy

If you notice that the `Data last updated...` caption displays yesterday's date and not today's, there might be a delay of up to a day in the Advanced Reporting updates. This delay is due to a larger than expected queue size.

#### Dashboard Reports

**Orders**

|Field|Description|
|--- |--- |
|Revenue|Shows all revenue received by the store view during the defined time period.|
|Orders|Shows all orders placed through the store view during the defined time period.|
|AOV|Shows the average order value placed through the store view during the defined time period.|
|Refunds|Shows all refunds processed through the store view during the defined time period.|
|Tax Collected|Shows all tax collected through the store view during the defined time period.|
|Shipping Collected|Shows all shipping fees collected through the store view during the defined time period.|
|Orders by Status|Shows the number of orders by status, for the store view during the defined time period.|
|Orders by Status|Lists a summary of  the number of orders by status.|
|Coupon Usage|Lists all coupon codes  and the number of users for each, redeemed through the store view during the defined time period.|
|Orders and Revenue by Billing Region|Lists the number of orders and revenue by region for the store view during the defined time period.|
|Tax Collected by Billing Region|Lists the amount of tax collected by region for the store view during the defined time period.|
|Shipping Fees Collected by Shipping Region|Lists the shipping fees collected by region for the store view during the defined time period.|

**Customers**

|Field|Description|
|--- |--- |
|Unique Customers|Shows the number of unique customer accounts associated with the store view during the defined time period.|
|New Registered Accounts|Shows the number of new customer accounts registered with the store view during the defined time period.|
|Top Coupon Users|Lists the top coupon users by Customer ID, and the number of orders placed with coupons for the store view during the defined time period.|
|Customer KPI Table|Lists  the number of orders, revenue, and average order value by Customer ID for the store view during the defined time period.|

**Products**

|Field|Description|
|--- |--- |
|Quantity of Products Sold|Shows the number of products sold through the store view during the defined time period.|
|Products Added to Wishlists|Lists all products added to wishlists through the store view during the defined time period.|
|Best Selling Products by Quantity|Lists the best-selling products and quantity sold through the store view during the defined time period.|
|Best Selling Products by Revenue|Lists the best-selling products and revenue generated by the sale of the product through the store view during the defined time period.|


[1]: https://docs.magento.com/mbi/
[2]: https://devdocs.magento.com//guides/v2.4/advanced-reporting/overview.html
[3]: https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-cron.html
