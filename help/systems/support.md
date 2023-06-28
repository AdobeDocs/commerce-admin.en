---
title: Support tools
description: Learn about the provided support tools that you can use to identify issues in your system.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
---
# Support tools

{{ee-feature}}

The support tools are designed to identify known issues in your system. They can be used as a resource during the development and optimization processes, and as a diagnostic tool to help our support team identify and resolve issues.

## Data collector

The data collector gathers the information about your system that is needed by our Support team to troubleshoot issues with your Adobe Commerce installation. The backup that is created takes several minutes to complete, and includes both a code and database dump. The data can be exported to a CSV or Excel XML file.

![System - Data Collector](./assets/data-collector.png){width="600" zoomable="yes"}

### Run the data collector

1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Support]_ > **[!UICONTROL Data Collector]**.

1. In the upper-right corner, click **[!UICONTROL New Backup]**.

   It takes a few minutes to generate the backup. You can monitor the results of processing by clicking **[!UICONTROL Refresh Status]**. When complete, the backup appears in the _[!UICONTROL Data Collector]_ grid.

1. To view a log with the backup details, do the following:

   - In the _[!UICONTROL Action]_ column, select **[!UICONTROL Show Log]**.

   - Click **[!UICONTROL Back]** to return to the grid.

   ![data collector log](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Export backup data

1. In the first column, select the checkbox of the backup to be exported.

1. Use the **[!UICONTROL Export]** menu to choose the format of the export data.

   ![Export Format](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Access the file from the web browser download location and **[!UICONTROL Save]** it.

### Download backup data

After the backup is generated, you can download the copy of Code and DB data.

1. Find the needed backup entity in the grid.

1. Make sure it has a `Complete` status.

1. Click the entity name in _[!UICONTROL Code Dump]_ or _[!UICONTROL DB Dump]_ columns.

The download process should start automatically.

## Delete backup data

1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Support]_ > **[!UICONTROL Data Collector]**.

1. Find and select the backup data to be deleted.

1. In the _[!UICONTROL Action]_ column, click **[!UICONTROL Delete]**.

1. To confirm the action, click **[!UICONTROL OK]**.

## System reports

The system reporting tool gives you the ability take periodic full, or partial, snapshots of the system, and save them for future reference. You can compare performance settings before and after code development cycles, or changes to server settings. The system reporting tool can dramatically reduce the time spent preparing and submitting the information required by Support to begin an investigation.

From the System Reports grid, you can view and download existing reports, delete reports, and create reports.

### Access system reports

On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Support]_ > **[!UICONTROL System Report]**.

![Admin - system reports](./assets/reports.png){width="600" zoomable="yes"}

### Generate a report

1. Click **[!UICONTROL New Report]**.

1. In the **[!UICONTROL Groups]** list, select each set of information that you want to include in the report. By default, all groups are selected.

   ![System report - select groups](./assets/report-create.png){width="600" zoomable="yes"}

1. In the upper-right corner, click **[!UICONTROL Create]**.

   It might take a few minutes for the report to generate, depending on the number of report types selected. When the report is ready, it appears at the top of the grid with the date and time generated.

### View module information

You can find useful information about installed modules.

**_To view report info for each installed module:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Support]_ > **[!UICONTROL System Report]**.
1. Click **[!UICONTROL New Report]**.
1. Select `Modules` from the **[!UICONTROL Groups]** list.
1. Click **[!UICONTROL Create]**.
1. After the report generates, click **[!UICONTROL Select]** and then **[!UICONTROL View]** to see all module versions.
1. Click **[!UICONTROL Download]** to download the report.

### Manage system reports

In the **[!UICONTROL Action]** column of the grid, select one of the following:

- `View` - Use this function to view the details of the report.
- `Delete` - Use this function to delete the generated report from the list.
- `Download` - Use this function to save the report as an HTML file.

### View system report details

1. For the report you need, select **[!UICONTROL View]** in the _[!UICONTROL Actions]_ column.

1. In the left panel, expand ![Expansion selector](../assets/icon-display-expand.png) each section of the report to view the detail.

   ![General system report information](./assets/report-information.png){width="600" zoomable="yes"}

### Available system reports

| Report group | Information included |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce Version<br>Data Count<br>Cache Status<br>Index Status |
| [!UICONTROL Environment] | Environment Information<br>MySQL Status |
| [!UICONTROL Data] | Duplicate Categories By URL Key<br>Duplicate Products By URL Key<br>Duplicate Products By SKU<br>Duplicate Orders By Increment Id<br>Duplicate Users By Email<br>Corrupted Categories Data |
| [!UICONTROL Modules] | Custom Modules List<br>Disabled Modules List<br>All Modules List |
| [!UICONTROL Configuration] | Configuration<br>Data from `app/etc/env.php`<br>Shipping Methods<br>Payment Methods<br>Payments Functionality Matrix |
| [!UICONTROL Logs] | Log Files<br>Top System Messages<br>Today's Top System Messages<br>Top Debug Messages<br>Today's Top Debug Messages<br>Top Exception Messages<br>Today's Top Exception Messages |
| [!UICONTROL Attributes] | User Defined EAV Attributes<br>New EAV Attributes<br>Entity Types<br>All EAV Attributes<br>Category EAV Attributes<br>Product EAV Attributes<br>Customer EAV Attributes<br>Customer Address EAV Attribute<br>RMA Item EAV Attributes |
| [!UICONTROL Events] | Custom Global Events<br>Custom Admin Events<br>Custom Frontend Events<br>Custom Doc Events<br>Custom Crontab Events<br>Custom REST Events<br>Custom SOAP Events<br>Core Global Events<br>Core Admin Events<br>Core Frontend Events<br>Core Doc Events<br>Core Crontab Events<br>Core REST Events<br>Core SOAP Events<br>All Global Events<br>All Admin Events<br>All Frontend Events<br>All Doc Events<br>All REST Events<br>All SOAP Events<br>All Crontab Events |
| [!UICONTROL Cron] | Cron Schedules by status code<br>Cron Schedules by job code<br>Errors in Cron Schedules Queue<br>Cron Schedules List<br>Custom Global Cron Jobs<br>Custom Configurable Cron Jobs<br>Core Global Cron Jobs<br>Core Configurable Cron Jobs<br>All Global Cron Jobs<br>All Configurable Cron Jobs |
| [!UICONTROL Design] | Adminhtml Themes List<br>Frontend Themes List |
| [!UICONTROL Stores] | Website Tree<br>Websites List<br>Stores List<br>Store Views List |
OMS Connector<br>_(visible with OMS integration)_ | Connector Version<br>Connector monitoring<br>Message Processing Results |

{style="table-layout:auto"}
