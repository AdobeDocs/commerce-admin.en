---
title: '[!DNL New Relic] reporting'
description: Learn about the [!DNL New Relic] reporting available for accounts for Adobe Commerce on cloud infrastructure, which includes the software for the New Relic APM service.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
---
# [!DNL New Relic] reporting

[New Relic][1] is a software analytics service that helps you analyze and improve application interactions. Accounts for Adobe Commerce on cloud infrastructure include the software for the [!DNL New Relic APM] service. For more information, see [New Relic services][4] in the _Commerce on Cloud Infrastructure Guide_.

## Step 1: Sign Up for a [!DNL New Relic] account

1. Go to the [[!DNL New Relic]][1] website and sign up for an account.

   You can also sign up for a free trial account.

1. Follow the instructions on the site. When prompted, choose the product that you want to install first.

1. While you are in your account, locate the following credentials that are required to complete the Commerce configuration:

    | Option | Description |
    | ------ | ----------- |
    | Account ID | From your [!DNL New Relic] account dashboard, the Account ID is the number in the URL after: `/accounts` |
    | Application ID | From your [!DNL New Relic] account dashboard, click **[!UICONTROL New Relic APM]**. In the menu, choose **[!UICONTROL Applications]**. Then, choose your application. The Application ID is the number in the URL after: `/applications/` |
    | New Relic API Key | From your [!DNL New Relic] account dashboard, click **[!UICONTROL Account Settings]**. In the menu on the left under Integrations, choose **[!UICONTROL Data Sharing]**. You can create, regenerate, or delete your API key from this page. |
    | Insights API Key | From your [!DNL New Relic] account dashboard, click **[!UICONTROL Insights]**. In the menu on the left under Administration, choose **[!UICONTROL API Keys]**. Your Insights API Keys appear on this page. If necessary, click the plus sign (**+**) next to Insert Keys to generate a key. |

    {style="table-layout:auto"}

## Step 2: Install the [!DNL New Relic] agent on your server

To use [!DNL New Relic APM Pro] to gather and transmit data, the PHP agent must be installed on your server.

1. When prompted to choose a web agent, click **PHP**.

1. To set up the PHP agent on your server, follow the instructions.

   If you need help, see [New Relic for PHP][3].

1. Make sure that cron is running on your server.

   To learn more, see [Configure and run cron][5] in the developer documentation.

## Step 3: Configure your store

>[!NOTE]
>These configuration options do not apply to Adobe Commerce on Cloud Infrastructure. 
>
>If you are on the Pro plan, New Relic is already [preconfigured and enabled by default](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). If you are on the Starter plan, you must complete the [New Relic configuration steps](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) that are part of the setup process.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left navigation panel where **[!UICONTROL General]** is expanded, choose **[!UICONTROL New Relic Reporting]** and do the following:

   ![New Relic Reporting configuration](./assets/new-relic-reporting-general.png){width="600"}

    * Set **[!UICONTROL Enable New Relic Integration]** to `Yes`.

    * In the **[!UICONTROL Insights API URL]**, replace the percent (`%`) symbol with your New Relic Account ID.

    * Enter your **[!UICONTROL New Relic Account ID]**.

    * Enter your **[!UICONTROL New Relic Application ID]**.

    * Enter your **[!UICONTROL New Relic API Key]**.

    * Enter you **[!UICONTROL Insights API Key]**.

1. For **[!UICONTROL New Relic Application Name]**, enter a name to identify the configuration for internal reference.

1. (Optional) For **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**, select `Yes` to send collected data for the storefront and Admin as separate apps to New Relic.

   This option requires a name entered for the **[!UICONTROL New Relic Application Name]**.

   >[!NOTE]
   >
   >Enabling this feature reduces the number of false positive [!DNL New Relic] alerts and allows for configured monitoring and alerts strictly for frontend performance. New Relic receives separate app data files with names of Application Name appended to `Adminhtml` and frontend. For example: `MyStore_Adminhtml`

1. When complete, click **[!UICONTROL Save Config]**.

## Step 4: Enable Cron for [!DNL New Relic] reporting

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Cron]** section.

    ![New Relic Cron configuration](./assets/new-relic-reporting-cron.png){width="600"}

1. Set **[!UICONTROL Enable Cron]** to `Yes`.

1. When complete, click **[!UICONTROL Save Config]**.

## [!DNL New Relic] queries

[!DNL New Relic Insights] data is based on statements that are written in [!DNL New Relic Query Language] (NRQL), and any custom parameters that you might include. Data can be returned from adhoc queries, or by queries saved to your dashboard. To learn more, see the [NRQL Reference][6] in the [!DNL New Relic] documentation.

### Admin events

#### Active Admin users

Returns the number of active Admin users.

      SELECT uniqueCount(AdminId)
      FROM Transaction
      WHERE appName='<your_app_name>' SINCE 15 minutes ago

#### Currently active Admin users

Returns the names of active Admin users.

      SELECT uniques(AdminName)
      FROM Transaction
      WHERE appName='<your_app_name>' SINCE 15 minutes ago

#### Recent Admin activity

Returns the number of recent Admin actions.

      SELECT count(AdminId)
      FROM Transaction
      WHERE appName ='<your_app_name>' FACET AdminName SINCE 1 day ago

#### Latest Admin activity

Returns detail information about recent admin actions, including the Admin username, duration, and application name.

      SELECT AdminName, duration, name
      FROM Transaction
      WHERE appName='<your_app_name>' AND AdminName IS NOT NULL
      AND AdminName != 'N/A' LIMIT 50

### Cron events

#### Category count

Returns the number of application events by category during the specified time period.

      SELECT average(CatalogCategoryCount)
      FROM Cron
      WHERE CatalogCategoryCount IS NOT NULL
      AND appName = '<your_app_name>' TIMESERIES 2 minutes

#### Current catalog count

Returns the average number of application events in the catalog by category during the specified time period.

      SELECT average(CatalogCategoryCount)
      FROM Cron
      WHERE CatalogCategoryCount IS NOT NULL
      AND CatalogCategoryCount > 0
      AND appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Active products

Returns the number of application events by product during the specified time period.

      SELECT average(CatalogProductActiveCount)
      FROM Cron
      WHERE CatalogProductActiveCount IS NOT NULL
      AND appName = '<your_app_name>' TIMESERIES 2 minutes

#### Active product count

Returns the average number of active application events by product during the specified time period.

      SELECT average(CatalogProductActiveCount)
      FROM Cron
      WHERE CatalogProductActiveCount IS NOT NULL
      AND CatalogProductActiveCount > 0
      AND appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Configurable products

Returns the average number of application events for configurable products during the specified time period.

      SELECT average(CatalogProductConfigurableCount)
      FROM Cron
      WHERE CatalogProductConfigurableCount IS NOT NULL
      AND appName = '<your_app_name>' TIMESERIES 2 minutes

#### Configurable product count

Returns the average number of application events by configurable product during the specified time period.

      SELECT average(CatalogProductConfigurableCount)
      FROM Cron
      WHERE CatalogProductConfigurableCount IS NOT NULL
      AND CatalogProductConfigurableCount > 0
      AND appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Product count (all)

Returns the total number of application events for all products.

      SELECT average(CatalogProductCount)
      FROM Cron
      WHERE CatalogProductCount IS NOT NULL
      AND appName = '<your_app_name>' TIMESERIES 2 minutes

#### Current product count (all)

Returns the average number of application events for all products during the specified time period.

      SELECT average(CatalogProductCount)
      FROM Cron
      WHERE CatalogProductCount IS NOT NULL
      AND CatalogProductCount > 0
      AND appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Customer count

Returns the average number of application events by customer.

      SELECT average(CustomerCount)
      FROM Cron
      WHERE CustomerCount IS NOT NULL
      AND CustomerCount > 0<
      AND appName = '<your_app_name>' TIMESERIES 2 minutes

#### Current customer count

Returns the average number of customers during the specified time period.

      SELECT average(CustomerCount)
      FROM Cron
      WHERE CustomerCount IS NOT NULL
      AND CustomerCount > 0
      AND appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Module status

Returns the average number of times application modules are enabled, disabled, or installed during the specified time period.

      SELECT average(ModulesDisabled), average(ModulesEnabled), average
      (ModulesInstalled)
      FROM Cron<
      WHERE appName = '<your_app_name>' TIMESERIES 2 minutes

#### Current module status

Returns the average number of times modules were enabled, disabled, or installed during the specified time period.

      SELECT average(ModulesDisabled), average(ModulesEnabled), average
      (ModulesInstalled)
      FROM Cron
      WHERE appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Website and store counts

Returns the average number of application events by website and store during the specified time period.

      SELECT average(StoreViewCount), average(WebsiteCount)
      FROM Cron
      WHERE appName = '&lt;your_app_name&gt;' TIMESERIES 2 minutes

#### Current website and store counts

Returns the average number of current application events during the specified time period.

      SELECT average(StoreViewCount), average(WebsiteCount)
      FROM Cron
      WHERE appName = '<your_app_name>' SINCE 2 minutes ago LIMIT 1

#### Cron - all data from event

Returns all application event data.

      SELECT *
      FROM Cron
      WHERE appName = '<your_app_name>'

### Customers

#### Active customer count

Returns the number of active customers during the specified time period.

      SELECT uniqueCount(CustomerId)
      FROM Transaction
      WHERE appName = '<your_app_name>' SINCE 15 minutes ago

#### Active customers

Returns the names of active customers during the specified time period.

      SELECT uniques(CustomerName)
      FROM Transaction
      WHERE appName='<your_app_name>' SINCE 15 minutes ago

#### Top customers

Returns the top customers during the specified time period.

      SELECT count(CustomerId)
      FROM Transaction
      WHERE appName = '<your_app_name>' FACET CustomerName SINCE 1 day ago

#### Recent Admin activity

Returns a defined number of records of recent activity, that include the customer name and duration of visit.

      SELECT CustomerName, duration, name
      FROM Transaction
      WHERE appName='<your_app_name>'
      AND CustomerName IS NOT NULL
      AND CustomerName != 'N/A' LIMIT 50

### Orders

#### Number of orders placed

Returns the number of orders placed during the specified time period.

      SELECT count(Order)
      FROM Transaction SINCE 1 day ago

#### Total order value

Returns the total number of line items ordered during the specified time period.

      SELECT sum(orderValue)
      FROM Transaction SINCE 1 day ago

#### Total line items ordered

Returns the total number of line items ordered during the specified time period.

      SELECT sum(lineItemCount)
      FROM Transaction SINCE 1 day ago


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
