---
title: Scheduled import and export
description: Placeholder
---
# Scheduled import and export

{{ee-feature}}

Scheduled imports and exports can be run on a daily, weekly or monthly basis. The files to be imported or exported can be located on local Adobe Commerce servers, or on remote FTP servers. Scheduled Import/Export is implemented by default, and does not require additional configuration. All scheduled imports and exports are managed by the Cron job scheduler.

## Access scheduled import/export

1. On the _Admin_ sidebar, go to **System** > _Data Transfer_ > **Scheduled Imports/Exports**.

   ![Scheduled data import/export](./assets/data-scheduled-import-export.png)<!-- zoom -->

1. To create a new scheduled import or export job, click the appropriate button and follow the instructions for the type of scheduled job.

    - [Add Scheduled Export](#schedule-an-export)
    - [Add Scheduled Import](#schedule-an-import)

1. When the record is saved, the job appears in the _Scheduled Import/Export_ grid.

   >[!NOTE]
   >
   >Scheduled import/export makes changes to the system configuration. After saving, make sure you address the cache invalidation notice that appears at the top of the Admin page and flush the cache in order to apply the new or updated schedule.

1. After each scheduled job, a copy of the file is placed in the `var/log/import_export` directory on the Adobe Commerce local server.

   The details of each operation are not written to the log. If an error occurs, notification is sent of the failed import/export job, with a description of the error.

## Schedule an import

The Scheduled Import process is similar to the manual Import process, with respect to the available import file format and types of import entities:

- The import file should be in .CSV format
- You can import product and customer data

The advantage of using Scheduled Import is that you can automatically import a data file multiple times after specifying the import parameters and schedule only once.

![Scheduled data import](./assets/data-transfer-scheduled-import-add.png)<!-- zoom -->

The details of each import operation are not written to a log, but in case of failure you will receive an Import Failed email, with a description of the error. The result of the last scheduled import job is shown in the Last Outcome column on the Scheduled Import/Export page.

After each import operation, a copy of the import file is placed in the `var/log/import_export` directory on the server where Adobe Commerce or Magento Open Source is deployed. The timestamp, the marker of the imported entity (products or customers), and the type of the operation (in this case, import) are added to the import file name.

After each scheduled import job, a reindex operation is performed automatically. On the frontend, changes in the descriptions and other text information are reflected after the updated data goes to the database, and the changes in prices are reflected only after the reindex operation.

### Step 1: Complete the import settings

1. On the _Admin_ sidebar, go to **System** > _Data Transfer_ > **Scheduled Import/Export**.

1. In the upper-right corner, click **Add Scheduled Import** and do the following:

   - **Name** — Enter a name for the scheduled import.

   - **Description** — Enter a brief description that explains the purpose of the import and how it is to be used.

   - **Entity Type** — Set to one of the following: `Products` or `Customers`

      >[!NOTE]
      >
      >For the _Advanced Pricing_, _Products_, _Customers and Addresses (single file)_, and _Stock Sources_ entity types, these additional import behaviors displayed: Add/Update, Replace, and Delete. For the _Customer Finances_, _Customers Main File_, and _Customers and Addresses_ entity types, these additional import behaviors displayed: Add/Update Complex Data, Delete Entities, and Custom Action.

   - **Import Behavior** — Set to one of the following:

      - `Add/Update Complex Data` — Adds or updates new complex data to the existing complex data for existing entries in the database. This is the default value.
      - `Replace` — Writes over existing complex for existing entities in the database.
      - `Delete Entities` — Deletes existing entries in the database.
      - `Custom Action` - Customizes existing entities in the database.

   - **Start Time** — Set to the hour, minute, and second that the import is scheduled to begin.

   - **Frequency** — Set to one of the following: `Daily`, `Weekly`, or `Monthly`

   - **On Error** - Set to one of the following: `Stop Import` or `Continue Processing`

   - **Field Separator** — Enter the character that is used to separate fields in the import file. The default character is a comma.

   - **Multiple Value Separator** — Enter the character that is used to separate multiple values within a field.

   - **Status** — To activate the scheduled import, set to `Enabled`.

   ![Data import - scheduled import settings](./assets/data-transfer-scheduled-import-settings.png)<!-- zoom -->

### Step 2: Complete the import file information

1. Set **Server Type** to one of the following:

   - `Local Server` - Imports the data from the same server where Adobe Commerce is installed.
   - `Remote FTP` - Imports the data from a remote server.

   ![Data import - scheduled import file information](./assets/data-transfer-scheduled-import-file-information.png)<!-- zoom -->

   >[!NOTE]
   >
   >When the Remote storage module is enabled, `Local Server` **Server Type** automatically switches to `Remote Storage`.

1. Enter the **File Directory** where the import file originates.

   - `Local Server` - Enter a relative path in the Commerce installation. For example, `var/import`. If the Remote storage module is configured, use `import_export/import`.
   - `Remote FTP server` - Enter the full URL and path to the import folder on the remote server.

1. Enter the **File Name** to be imported.

1. For **Images File Directory**, enter the path to the directory where product images are stored. 

   On a local server, enter a relative path such as: `var/import`. On a remote storage, enter a relative path such as: `import_export/import` or `import_export/import/some/dir`.

## Step 3: Configure the import failed emails

1. Set **Failed Email Receiver** to the store contact who is to receive notification if an error occurs during the import.

1. Set **Failed Email Sender** to the store contact that appears as the sender of the notification.

1. Set **Failed Email Template** to the template that is used for the notification.

1. For **Send Failed Email Copy To**, enter the email address of anyone who is to receive a copy of the notification.

   Separate multiple email addresses with a comma.

1. Set **Failed Email Copy Method** to one of the following:

   - `Bcc` - Sends a blind courtesy copy of the failed import notification. The name and address of the recipient is included in the original email distribution, but hidden from view.
   - `Separate Email` - Sends a copy of the failed import notification as a separate email.

   ![Data import - failed import email copy method](./assets/data-transfer-scheduled-import-email-fail.png)<!-- zoom -->

1. When complete, click **Save**.

   The new scheduled import job is added to the list on the _Scheduled Import/Export_ page. From this page it can be run immediately for testing and edited. The import file is validated before the execution of each import job.

>[!NOTE]
>
>Scheduled import makes changes to the system configuration. After saving, make sure you address the cache invalidation notice that appears at the top of the Admin page and flush the cache in order to apply the new or updated schedule.

### Field descriptions

#### Import Settings

| Field | Description | 
| ----- | ----------- | 
| Name | The name of the import. Helps you to distinguish it if many different scheduled imports are created.| 
Description | (Optional) You can enter an additional description.| 
Entity Type | Defines the data to be imported. Options: Products / Customers.| 
| Import Behavior | Defines how complex data is handled if the entities being imported already exist in the database. Complex data for products include categories, websites, custom options, tier prices, related products, up-sells, cross-sells, and associated products data. Complex data for customers include addresses. Options:<br>**Add/Update Complex Data** - The new complex data are added or updated to the existing complex data for existing entries in the database. This is the default value.<br>**Add/Update** - New data is added to the existing entries in the database. All fields except `sku` can be updated for products. Any multiple field values that are not listed in the CSV file, such as categories or websites, remain in the database after the import.<br>**Replace** - The existing complex data for the existing entities are replaced.<br>**Delete Entities** - If imported entities already exist in the database, they are deleted from the database.<br>**Custom Action** - The existing complex entities are customized during the import process.
Start Time | Set the start hour, minutes, and seconds of the import.
Frequency | Define how often the import will be run. Options: Daily / Weekly / Monthly.
| On Error | Define the system behavior in case errors are found during file validation. Options:<br>**Stop Import** — The file is not imported if any errors are found during validation. This is the default value.<br>**Continue Processing** - In case errors are found during validation, but importing is possible, the file is imported.| 
| Status | The import is enabled by default. You can suspend it by setting the Status to `Disabled`.| 
| Field Separator | Determines the character that is used to separate fields. Default value: `,` (comma)| 
Multiple Value Separator| Determines the character that is used to separate multiple values within a field. Default value: `,` (comma)| 

{style="table-layout:auto"}

#### Import File Information

| Field | Description | 
| ----- | ----------- | 
| Server Type | You can import from a file located on the same server where Commerce is deployed (select Local Server) or from the remote FTP server (select Remote FTP). If you select Remote FTP, additional options for credentials and file transfer settings appear. If the Remote storage module is enabled, Local Server type is automatically switched to Remote Storage.
| File Directory | Specify the directory where the import file is located. If Server Type is set to Local Server, specify the path relative to the Commerce installation directory. For example: `var/import` or `import_export/import` for remote storage. |
| File Name | Specify the name of the import file. |
| Images File Directory | Enter the path to the directory where product images are stored. For a local server, enter a relative path. For example: `var/import` or `import_export/import` for remote storage. |

{style="table-layout:auto"}

#### Import Failed Emails

| Field | Description | 
| ----- | ----------- | 
| Failed Email Receiver | Specify the email address to which an email notification (failed import email) is sent if the import fails. |
| Failed Email Sender | Specify the email address that is used as the sender for the import failed email. |
| Failed Email Template | Select a template for the import failed email. By default, only the Import Failed (Default Template from Locale option is available. Custom templates can be created under **System** > **Transactional Emails**. |
| Send Failed Email Copy To | The email address to which a copy of import failed email is sent. |
| Send Failed Email Copy Method | Select the copy sending method for the import failed email. |

{style="table-layout:auto"}

## Schedule an export

Scheduled Export is similar to manual [Export](data-export.md), with respect to the available export file format and types of entities that can be exported:

- You can export to CSV format
- You can export product and customer data

The advantage of using Scheduled Export is that you can export data multiple times automatically, after specifying the export parameters, and schedule only once.

![Data transfer scheduled export](./assets/data-transfer-scheduled-export-add.png)<!-- zoom -->

The details of each export are not written to a log, but in case of failure you will receive an Export Failed email, which contains the error description. The result of the last export job appears in the Last Outcome column on the Scheduled Import/Export page.

After each export, the export file is placed in the user-defined location, and a copy of the file is placed in the `var/log/import_export`directory on the server where Adobe Commerce or Magento Open Source is deployed. The timestamp and the marker of the exported entity (products or customers) and type of the operation (in this case, export) are added to the export file name.

### Step 1: Complete the Export Settings

1. On the _Admin_ sidebar, go to **System** > _Data Transfer_ > **Scheduled Import/Export**.

1. In the upper-right corner, click **Add Scheduled Export** and do the following:

   - Enter a **Name** for the scheduled export.

   - Enter a brief **Description** that explains the purpose of the export, and how it is to be used.

   - Set **Entity Type** to one of the following:

      - `Advanced Pricing`
      - `Products`
      - `Customer Financing`
      - `Customers Main File`
      - `Customer Addresses`
      - `Stock Sources`

      The _Entity Attributes_ section at the bottom of the page is updated to reflect the selected Entity Type.

   - Set **Start Time** to the hour, minute, and second that the export is scheduled to begin.

   - Set **Frequency** to one of the following:

      - `Daily`
      - `Weekly`
      - `Monthly`

1. To activate the scheduled export, set **Status** to `Enabled`.

1. Accept `CSV` as the default **File Format**.

   ![Scheduled export settings](./assets/data-transfer-scheduled-export-settings.png)<!-- zoom -->

### Step 2: Complete the Export File Information

1. Set **Server Type** to one of the following:

   - `Local Server` - To save the export file on the same server where Commerce is installed.
   - `Remote FTP` — To save the export file on a remote server.

   ![Scheduled export file information](./assets/data-transfer-scheduled-export-file-information.png)<!-- zoom -->

   >[!NOTE]
   >
   >When the Remote storage module is enabled, the `Local Server` **Server Type** automatically switches to `Remote Storage`.

1. Enter the **File Directory** where the export file is to be saved as follows:

   - For **Local Server**, enter a relative path within the Commerce installation, such as `var/export`. If the Remote storage module is configured, use `import_export/export`.
   - For **Remote FTP server**, enter the full URL and path to the target folder on the destination server.

1. If the **Remote FTP** server is selected, enter connection credentials to the server and select additional settings:

   - For **FTP Host[:Port]**, enter remote FTP host address.
   - For **User Name**, enter the username used to access the remote server.
   - For **Password**, enter the password of the provided username account.
   - For **File Mode**, choose `Binary` or `ASCII`.
   - For **Passive Mode**, choose `No` or `Yes`.

### Step 3: Configure the Export Failed Emails

1. Set **Failed Email Receiver** to the store contact who is to receive notification if an error occurs during the export.

1. Set **Failed Email Sender** to the store contact that appears as the sender of the notification.

1. Set **Failed Email Template** to the template that is used for the notification.

1. For **Send Failed Email Copy To**, enter the email address of anyone who is to receive a copy of the notification.

   For multiple email addresses, separate with a comma.

1. Set **Failed Email Copy Method** to one of the following:

   - `Bcc` - Sends a blind courtesy copy. The name and address of the recipient is included in the original email distribution, but is hidden from view.
   - `Separate Email` — Sends the copy as a separate email.

   ![Scheduled export failed email](./assets/data-transfer-scheduled-export-email-fail.png)<!-- zoom -->

### Step 4: Choose the Entity Attributes

1. In the _Entity Attributes_ section, choose the attributes that you want to include in the export data.

   - To filter export data by attributes value, enter the attribute value in the Filter column.
   - To exclude products or customers with certain attribute values, enter the values of the attributes that you want to exclude, and select the checkbox in the Skip column.

1. When complete, click **Save**.

   The new scheduled export job is added to the list on the _Scheduled Import/Export_ page. From this page it can be run immediately, for testing, and edited.

>[!NOTE]
>
>Scheduled export makes changes to the system configuration. After saving, make sure you address the cache invalidation notice that appears at the top of the Admin page and flush the cache in order to apply the new or updated schedule.

### Field Descriptions

#### Export Settings

| Field | Description | 
| ----- | ----------- | 
| Name | The name of the export. Helps you to distinguish it if many different scheduled exports are created. |
| Description | (Optional) A description of the scheduled export.
| Entity Type | Identifies the data to be exported. After the selection is made, the Entity Attributes appear below. Options: Advanced Pricing / Products / Customer Finances/ Customers Main File / Customer Addresses / Stock Sources. |
| Start Time | Set the start hour, minutes, and seconds of the export.
Frequency | Define how often the export job will be executed. Options: Daily / Weekly / Monthly. |
| Status | A new scheduled export is enabled by default. You can suspend it by setting Status to Disabled. Options: Enabled / Disabled. |
File Format | Select the format of the export file. Currently only the `.CSV` option is available. |

{style="table-layout:auto"}

#### Export Settings Information

| Field | Description | 
| ----- | ----------- | 
| Server Type | Determines the location of the export file. Options:<br>**Local Server** — Places the export file on the same server where Commerce is deployed. If the Remote storage module is enabled, `Local Server` is switched to `Remote Storage`.<br>**Remote FTP** — Places the export file on a remote server. Additional options for credentials and file transfer settings appear. |
| File Directory| Specify the directory where the export file is placed. In case Server Type is set to Local Server, specify the path relative to the Commerce installation path. For example, `var/export`, or `import_export/export` for remote storage. |

{style="table-layout:auto"}

#### Export Failed Emails

| Field | Description | 
| ----- | ----------- | 
| Failed Email Receiver | Specify the email address to which an email notification (export failed email) is sent if the export fails. |
| Failed Email Sender | Specify the email address that is used as export failed email sender. |
| Failed Email Template | Select a template for the failed export email. By default, only the Export Failed (Default Template from Locale) option is available. |
| Send Failed Email Copy To | The email address to which a copy of the failed export email is sent. |
| Send Failed Email Copy Method | Specify the copy sending method for the export failed email. |

{style="table-layout:auto"}
