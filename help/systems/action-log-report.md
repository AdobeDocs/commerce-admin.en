---
title: Action Logs report
description: Placeholder
---
# Action Logs report

{{ee-feature}}

The Action Logs report displays a detailed record of all admin actions that are enabled for logging. Each record is time stamped, and records the IP address and name of the user. The log detail includes admin user data and related changes that were made during the action.

Actions that you want to display in the report must be enabled in the [Admin Actions Logging](action-log.md) screen in the store settings. If the action type is checked (enabled), those types of admin actions will display in the Action Logs Report.

The report can be filtered using the options in each column. You may set a single filter option or set filter options for multiple columns to narrow the report to list specific actions. You can also export report data in either CSV or Excel XML format.

The Action Logs Report includes the following information:

- **Time** - The date and time the action occurred
- **Action Group** - Displays the action type, correlates to the actions enabled on _Admin Actions Logging_ screen in your store settings
- **Action** - Displays the action that was logged
- **IP Address** - Displays the IP address for the machine on which the action was performed
- **Username** - Displays the login ID for the user who performed the action
- **Result** - Displays the success or failure of the user's action
- **Full Action Name** - Displays the backend action name
- **Details** - Displays the backend action category
- **Full Details** - Displays all logged details of the admin action

## View the Action Logs Report

1. On the _Admin_ sidebar, go to **System** > _Actions Logs_ > **Report**.

   ![Action logs](./assets/action-log-report.png)<!-- zoom -->

1. To view the full details of a listed admin action, click **View**.

   ![Action log entry details](./assets/action-log-report-view.png)<!-- zoom -->

## Filter the Action Logs Report

You can define the filter options fields and then click **Search** to narrow the actions displayed.

To clear the filter options and return to the full report, click **Reset Filter**.

![Action log report filters](./assets/action-log-report-filters.png)<!-- zoom -->

### Filter by field

|Field|description|
|--- |--- |
|Time|In **From**, click to select a date from the dynamic calendar to define the beginning date for the filter. Then in **To**, click to select a date from the dynamic calendar to define the ending date for the filter.|
|Action Group|Choose an action group.|
|Action|Choose an action.|
|IP Address|Enter the IP address of the machine used for an action.|
|Username|Choose an username. Default is All Users.|
|Result|Choose Success or Failure.|
|Full Action Name|Enter text for the search to match in the field.|
|Details|Enter text for the search to match in the field.|

{style="table-layout:auto"}

## Export the Action Logs report

1. For **Export to**, choose an export format:

   - **CSV** - A comma-separated value file containing plain text data
   - **Excel XML** - An XML-based, spreadsheet data format

1. Click **Export**.

   The generated file is automatically saved to your designated folder for downloads.

   ![Action logs report export](./assets/action-log-report-export.png)<!-- zoom -->
