---
title: General > New Relic Reporting
description: Placeholder
---
# General > New Relic Reporting

{{config}}

## General

![General](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Enable New Relic Integration|Store View|Determines if your store can be used with New Relic Reporting. Options: `Yes` / `No`|
|New Relic API URL|Store View|The URL where New Relic APIs are deployed. For example: `https://api.newrelic.com/deployments.xml`|
|Insights API URL|Store View|The URL where Insights APIs are deployed. Use the percent symbol (%) to represent your account ID. For example: `https://insights-collector.newrelic.com/v1/accounts/%s/events`|
|New Relic Account ID|Store View|The account ID assigned to your New Relic account.|
|New Relic Application ID|Store View|The application ID assigned to your New Relic account for the Commerce integration.|
|New Relic API Key|Store View|The key that is assigned to you for gaining access to the New Relic API.|
|Insights API Key|Store View|The key that is assigned to you for gaining access to Insights.|
|New Relic Application Name|Store View|The name that you have assigned to your New Relic integration.|
|Send Adminhtml and Frontend as Separate Apps|Store View|An option to send report data collected for the storefront and Admin as separate apps to New Relic. This option requires a name entered for the New Relic Application Name. The feature appends the application name with an underscore to the collected app data. For example: `MyStore_Adminhtml` `MyStore_frontend`|

## Cron

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Enable Cron|Store View|Determines if New Relic reports can be run on schedule with [Cron](https://docs.magento.com/user-guide/system/cron.html). Options: `Yes` / `No`|
