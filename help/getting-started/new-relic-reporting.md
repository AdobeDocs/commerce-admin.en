---
title: New Relic Reporting
description: Learn about the New Relic reporting available for accounts for Adobe Commerce on cloud infrastructure, which includes the software for the New Relic APM service.
---
# New Relic Reporting

[New Relic][1] is a software analytics service that helps you analyze and improve application interactions. Accounts for Adobe Commerce on cloud infrastructure include the software for the New Relic APM service. For more information, see [New Relic services][4]{:target="_blank"} in the developer documentation.

## Step 1: Sign Up for a New Relic Account

1. Go to the [New Relic][1] website and sign up for an account.

   You can also sign up for a [free trial account][2].

1. Follow the instructions on the site. When prompted, choose the product that you want to install first.

1. While you are in your account, locate the following credentials that are required to complete the configuration:

    | Option | Description |
    | ------ | ----------- |
    | Account ID | From your New Relic account dashboard, the Account ID is the number in the URL after: `/accounts` |
    | Application ID | From your New Relic account dashboard, click **New Relic APM**. In the menu, choose **Applications**. Then, choose your application. The Application ID is the number in the URL after: `/applications/` |
    | New Relic API Key | From your New Relic account dashboard, click **Account Settings**. In the menu on the left under Integrations, choose **Data Sharing**. You can create, regenerate, or delete your API key from this page. |
    | Insights API Key | From your New Relic account dashboard, click **Insights**. In the menu on the left under Administration, choose **API Keys**. Your Insights API Keys appear on this page. If necessary, click the plus sign (**+**) next to Insert Keys to generate a key. |

## Step 2: Install the New Relic Agent on Your Server

To use New Relic APM Pro to gather and transmit data, the PHP agent must be installed on your server.

1. When prompted to choose a web agent, click **PHP**.

1. To set up the PHP agent on your server, follow the instructions.

   If you need help, see [New Relic for PHP][3].

1. Make sure that cron is running on your server.

   To learn more, see [Configure and run cron][5] in the developer documentation.

## Step 3: Configure Your Store

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel where **General** is expanded, choose **New Relic Reporting** and do the following:

   ![New Relic Reporting configuration](./assets/new-relic-reporting-general.png)<!-- zoom -->

    * Set **Enable New Relic Integration** to `Yes`.

    * In the **Insights API URL**, replace the percent (%) symbol with your New Relic Account ID.

    * Enter your **New Relic Account ID**.

    * Enter your **New Relic Application ID**.

    * Enter your **New Relic API Key**.

    * Enter you **Insights API Key**.

1. In the **New Relic Application Name** field, enter a name to identify the configuration for internal reference.

1. (Optional) For the **Send Adminhtml and Frontend as Separate Apps** field, select `Yes` to send collected data for the storefront and Admin as separate apps to New Relic.

   This option requires a name entered for the **New Relic Application Name**.

   >[!NOTE]
   >
   >Enabling this feature reduces the number of false positive New Relic alerts and allows for configured monitoring and alerts strictly for frontend performance. New Relic receives separate app data files with names of Application Name appended to `Adminhtml` and frontend. For example: `MyStore_Adminhtml`

1. When complete, click **Save Config**.

## Step 4: Enable Cron for New Relic Reporting

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Cron** section.

    ![New Relic Cron configuration](./assets/new-relic-reporting-cron.png)<!-- zoom -->

1. Set **Enable Cron** to `Yes`.

1. When complete, click **Save Config**.

## New Relic Queries

New Relic Insights data is based on statements that are written in New Relic Query Language (NRQL), and any custom parameters that you might include. Data can be returned from adhoc queries, or by queries saved to your dashboard. To learn more, see the [NRQL Reference][6] in the New Relic documentation.

### Admin Events

#### Active Admin Users

Returns the number of active admin users.

      SELECT uniqueCount(AdminId)
      FROM Transaction
      WHERE appName='<your_app_name>' SINCE 15 minutes ago

#### Currently Active Admins

Returns the names of active admin users.

      SELECT uniques(AdminName)
      FROM Transaction
      WHERE appName='<your_app_name>' SINCE 15 minutes ago

#### Recent Admin Activity

Returns the number of recent admin actions.

      SELECT count(AdminId)
      FROM Transaction
      WHERE appName ='<your_app_name>' FACET AdminName SINCE 1 day ago

#### Latest Admin Activity

Returns detail information about recent admin actions, including the admin username, duration, and application name.

      SELECT AdminName, duration, name
      FROM Transaction
      WHERE appName='<your_app_name>' AND AdminName IS NOT NULL
      AND AdminName != 'N/A' LIMIT 50

### Cron Events

#### Category Count

Returns the number of application events by category during the specified time period.

      SELECT average(CatalogCategoryCount)
      FROM Cron
      WHERE CatalogCategoryCount IS NOT NULL
      AND appName = '<your_app_name>' TIMESERIES 2 minutes

#### Current Catalog Count

Returns the average number of application events in the catalog by category during the specified time period.

      SELECT average(CatalogCategoryCount)
      FROM Cron
      WHERE CatalogCategoryCount IS NOT NULL
      AND CatalogCategoryCount > 0
      AND appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Active Products

Returns the number of application events by product during the specified time period.

      SELECT average(CatalogProductActiveCount)
      FROM Cron
      WHERE CatalogProductActiveCount IS NOT NULL
      AND appName = '<your_app_name>' TIMESERIES 2 minutes

#### Active Product Count

Returns the average number of active application events by product during the specified time period.

      SELECT average(CatalogProductActiveCount)
      FROM Cron
      WHERE CatalogProductActiveCount IS NOT NULL
      AND CatalogProductActiveCount > 0
      AND appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Configurable Products

Returns the average number of application events for configurable products during the specified time period.

      SELECT average(CatalogProductConfigurableCount)
      FROM Cron
      WHERE CatalogProductConfigurableCount IS NOT NULL
      AND appName = '<your_app_name>' TIMESERIES 2 minutes

#### Configurable Product Count

Returns the average number of application events by configurable product during the specified time period.

      SELECT average(CatalogProductConfigurableCount)
      FROM Cron
      WHERE CatalogProductConfigurableCount IS NOT NULL
      AND CatalogProductConfigurableCount > 0
      AND appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Product Count (all)

Returns the total number of application events for all products.

      SELECT average(CatalogProductCount)
      FROM Cron
      WHERE CatalogProductCount IS NOT NULL
      AND appName = '<your_app_name>' TIMESERIES 2 minutes

#### Current Product Count (all)

Returns the average number of application events for all products during the specified time period.

      SELECT average(CatalogProductCount)
      FROM Cron
      WHERE CatalogProductCount IS NOT NULL
      AND CatalogProductCount > 0
      AND appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Customer Count

Returns the average number of application events by customer.

      SELECT average(CustomerCount)
      FROM Cron
      WHERE CustomerCount IS NOT NULL
      AND CustomerCount > 0<
      AND appName = '<your_app_name>' TIMESERIES 2 minutes

#### Current Customer Count

Returns the average number of customers during the specified time period.

      SELECT average(CustomerCount)
      FROM Cron
      WHERE CustomerCount IS NOT NULL
      AND CustomerCount > 0
      AND appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Module Status

Returns the average number of times application modules are enabled, disabled, or installed during the specified time period.

      SELECT average(ModulesDisabled), average(ModulesEnabled), average
      (ModulesInstalled)
      FROM Cron<
      WHERE appName = '<your_app_name>' TIMESERIES 2 minutes

#### Current Module Status

Returns the average number of times modules were enabled, disabled, or installed during the specified time period.

      SELECT average(ModulesDisabled), average(ModulesEnabled), average
      (ModulesInstalled)
      FROM Cron
      WHERE appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Website and Store Counts

Returns the average number of application events by website and store during the specified time period.

      SELECT average(StoreViewCount), average(WebsiteCount)
      FROM Cron
      WHERE appName = '&lt;your_app_name&gt;' TIMESERIES 2 minutes

#### Current Website and Store Counts

Returns the average number of current application events during the specified time period.

      SELECT average(StoreViewCount), average(WebsiteCount)
      FROM Cron
      WHERE appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Cron - All Data from Event

Returns all application event data.

      SELECT *
      FROM Cron
      WHERE appName = '<your_app_name>'

### Customers

#### Active Customer Count

Returns the number of active customers during the specified time period.

      SELECT uniqueCount(CustomerId)
      FROM Transaction
      WHERE appName = '<your_app_name>' SINCE 15 minutes ago

#### Active Customers

Returns the names of active customers during the specified time period.

      SELECT uniques(CustomerName)
      FROM Transaction
      WHERE appName='<your_app_name>' SINCE 15 minutes ago

#### Top Customers

Returns the top customers during the specified time period.

      SELECT count(CustomerId)
      FROM Transaction
      WHERE appName = '<your_app_name>' FACET CustomerName SINCE 1 day ago

#### Recent Admin Activity

Returns a defined number of records of recent activity, that include the customer name and duration of visit.

      SELECT CustomerName, duration, name
      FROM Transaction
      WHERE appName='<your_app_name>'
      AND CustomerName IS NOT NULL
      AND CustomerName != 'N/A' LIMIT 50

### Orders

#### Number of Orders Placed

Returns the number of orders placed during the specified time period.

      SELECT count(Order)
      FROM Transaction SINCE 1 day ago

#### Total Order Value

Returns the total number of line items ordered during the specified time period.

      SELECT sum(orderValue)
      FROM Transaction SINCE 1 day ago

#### Total Line Items Ordered

Returns the total number of line items ordered during the specified time period.

      SELECT sum(lineItemCount)
      FROM Transaction SINCE 1 day ago


[1]: http://newrelic.com/
[2]: http://newrelic.com/magento
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://devdocs.magento.com/cloud/project/new-relic.html
[5]: https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-cron.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference