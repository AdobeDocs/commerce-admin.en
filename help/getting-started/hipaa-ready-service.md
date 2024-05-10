---
title: HIPAA readiness on Adobe Commerce
description: Learn how you can add the Adobe Commerce HIPAA-Ready module and get additional features and functionalities that allow you to comply with your HIPAA obligations.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
---
# HIPAA readiness on Adobe Commerce

>[!IMPORTANT]
>
>**Legal Disclaimer**<br/>
>This information is intended to help Adobe customers answer their questions regarding Adobe's HIPAA-Ready Services. It does not constitute legal advice. Merchants should consult with their own legal counsel to understand their obligations under HIPAA and the appropriate use and configuration of Adobe's products.

>[!BEGINSHADEBOX]

**Health Insurance Portability and Accountability Act (HIPAA)**

The Health Insurance Portability and Accountability Act (HIPAA) is the key federal healthcare privacy law in the United States and is enforced by the U.S. Department of Health and Human Services (HHS). HIPAA applies to _Covered Entities_ (such as healthcare providers, insurers, and clearinghouses) and _Business Associates_ (such as those entities that provide services to covered entities). HIPAA requirements are set across three separate rules: Privacy Rule, Security Rule, and Breach Notification Rule. Adobe acts as a Business Associate for certain products, which Adobe classifies as "HIPAA-Ready Services." Data regulated under HIPAA is referred to as _Protected Health Information_ or PHI. PHI is a subset of health information that (1) is created or received by a healthcare provider, health plan, or healthcare clearinghouse, (2) relates to the past, present, or future physical or mental health or condition of an individual, the provision of healthcare to an individual, or the past, present, or future payment for the provision of healthcare to an individual, and (3) identifies the individual or with respect to which there is a reasonable basis to believe that the information can be used to identify the individual. The HIPAA Privacy and Security Rules require that a Covered Entity obtain written assurances from a Business Associate in the form of a Business Associate Agreement, or BAA, requiring the Business Associate to safeguard the privacy and security of the Covered Entityʼs PHI. For more information, see [HIPAA and Adobe Products and Services](https://www.adobe.com/trust/compliance/hipaa-ready.html) in the Adobe Trust Center.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA-Ready

Adobe Commerce HIPAA-Ready has additional features and functionalities that allow merchants to comply with their respective HIPAA obligations.

You can install the Adobe Commerce HIPAA-Ready (`magento/hipaa-ee`) extension on Adobe Commerce on cloud infrastructure or Adobe Managed Services projects. Some services and features must be disabled to comply with HIPAA requirements. See [Disabled services and features](#disabled-services-and-features).

*These materials are intended for informational purposes only. Provision of this information does not entitle the recipient to any contractual or other rights. While efforts have been made to assure the accuracy of the information as of the date it has been provided, no representation is made that such information is accurate and complete. Adobe undertakes no obligation to update this information as the law or Adobe's products change. Also, this document is not to be distributed to any party other than the intended recipient without written consent from Adobe.*

## System requirements

Adobe Commerce must be deployed on either Adobe Commerce on cloud infrastructure or Adobe Commerce Managed Services with version 2.4.6-p3 or later—no beta versions).

## Installation

Install the latest version of Adobe's HIPAA-Ready Services extension (`magento/hipaa-ee`) on an instance that is running Adobe Commerce version 2.4.6-p3 or later—no beta versions. The extension is delivered as a composer metapackage from the [repo.magento.com](https://repo.magento.com) repository.

>[!BEGINSHADEBOX]

**Prerequisite**

You must have access to [repo.magento.com](https://repo.magento.com) to install the extension. For key generation and obtaining the necessary rights, see [Get your authentication keys](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

1. On your local workstation, change to the project directory for your Adobe Commerce on cloud infrastructure project.

1. Check out the environment branch to install the extension.

1. Add the metapackage `magento/hipaa-ee` to the composer configuration using the composer CLI.

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. Update package dependencies.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. Add, commit, and push the updated code to the cloud environment.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

### Verify installation

After the updates are deployed, verify that the `Hipaa*` relevant modules have been included.

1. Use SSH to log in to the remote cloud environment.

   ```shell
   magento-cloud ssh
   ```

1. From the command line, use the Adobe Commerce CLI to check the module status.

   ```shell
   bin/magento module:status
   ```

1. Verify that the HIPAA modules are included in the list of enabled modules:

   ```text
   List of enabled modules:
   <truncated for brevity>
   Magento_HipaaAnalytics
   Magento_HipaaCheckout
   Magento_HipaaLogging
   Magento_HipaaScheduledImportExport
   Magento_HipaaAdminLogging
   Magento_HipaaCustomerLogging
   Magento_HipaaNewsletter
   Magento_HipaaImportExport
   Magento_HipaaApiLogging
   <truncated for brevity>
   ```

   All modules prefixed with `Magento_Hipaa` must be in the enabled modules section.

## Feature enhancements for HIPAA-readiness

The `magento/hipaa-ee` package introduces some changes and enhancements to the base Commerce product. The following sections provide details about these changes and how they alter the base product.

### Action Logs

Audit Logging is a HIPAA requirement. In Adobe Commerce, the [Action Logs](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) feature records every change made by an Admin user who works in your store. To meet HIPAA requirements for the Audit Log, the feature has been updated to record all Admin user and customer actions performed through the Admin UI and through API calls.

#### Action Logs report

The _Action Logs_ report grid (**[!UICONTROL System]** > Action Logs > Report) is modified to accommodate customer actions performed through the Admin UI and API.

1. Two additional columns:
   - ***Source***: Displays where the action was performed.
      Values: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Client Type***: Displays the client type.
      Values: Customer | Admin | Integration

2. Rename ***Username*** to ***Client Identifier***
   - ***Client Identifier***: Displays the login ID for the user who performed the action.
      Values:
      - an email if Client Type is Customer
      - a username if Client Type is Admin
      - a name if Client Type is Integration

3. Rename ***Full Action Name*** to ***Target***
   - ***Target***: Displays the action name.
         Values:
       - an endpoint if Source is a REST API or SOAP API
       - a query or mutation name if a GraphQL API
       - an action name if an Admin UI or Customer UI.

#### Configure Admin actions for logging

This feature is not available because all actions must be recorded by default.

### Import and export features

Enhancements to import and export features are focused on improving the administrative experience and providing better visibility into user actions.

>[!NOTE]
>
>These ***enhancements do not alter the Import and Export core logic***; rather, they extend the functionality to offer more comprehensive logging and improved data attribution. The fundamental functionality of import and export remains unchanged. Users can continue to use the existing features and workflows without any disruption.

#### Administrative action logging

One of the key improvements within the import and export features is the enhanced logging of administrative actions. This enhancement introduces the capability to delve deeper into activities associated with data import and export, contributing to improved tracking and auditability. The following actions are now logged and reflected in the **[!UICONTROL System] > _[!UICONTROL Action Logs]_ > [!UICONTROL Report]** grid:

| Type | Actions |
| ---- | ------- |
| Import | <ul><li>An Admin user executes an import<li>An Admin user downloads an imported file<li>An Admin user downloads an error file<ul/> |
| Export | <ul><li>An Admin user requests<li>An Admin user downloads an exported file<ul/> |
| Scheduled imports/exports | <ul><li>An Admin user schedules export<li>An Admin user edits a scheduled export<li>An Admin user runs a scheduled export<li>An Admin user deletes a scheduled export<li>An Admin user schedules an import<li>An Admin user edits a scheduled import<li>An Admin user runs a scheduled import<li>An Admin user deletes a scheduled import<li>An Admin user executes a bulk delete of import/export operations<ul/> |

### Display enhancements and improved filtering and sorting

To empower Admin users with more informative grids, there are several enhancements to the display of data and to the filtering and sorting capabilities:

#### Import history ([!UICONTROL System] > _[!UICONTROL Data Transfer]_ > [!UICONTROL Import History])

- Enabled filtering for all columns except for **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]**, and **[!UICONTROL Summary]**.

#### Export ([!UICONTROL System] > _[!UICONTROL Data Transfer]_ > [!UICONTROL Export])

- Added an **[!UICONTROL ID]** column.
- Added a **[!UICONTROL Requested At]** column (_date and time when export was requested_).
- Added a **[!UICONTROL User]** column (_username of an admin who did the request_).
- Removed an **[!UICONTROL Action]** column.
- Moved the **[!UICONTROL Download]** link to a **[!UICONTROL File name]** column (_like the Import History grid_).
- Disabled the action responsible for deletion of an exported file (_to improve tracking_).
- Enabled sorting for all columns except **[!UICONTROL File name]**.
- Enabled filtering for all columns.

#### Scheduled imports and exports ([!UICONTROL System] > _[!UICONTROL Data Transfer]_ > [!UICONTROL Scheduled Import/Export])

- Added an **[!UICONTROL ID]** column.
- Added a **[!UICONTROL Scheduled At]** column (the _date and time when the import or export was scheduled_).
- Added a **[!UICONTROL User]** column (the _username of an Admin user who scheduled the import or export_).

## Disabled services and features

To comply with HIPAA requirements, some services and features supported by Adobe Commerce are either not available or disabled by default. Merchants have the option to re-enable or use these services and features at their own risk.

### Services

- **SaaS services from Adobe Commerce**—None of the SaaS services offered for Adobe Commerce are available under the HIPAA-readiness offering. These services include, but are not limited to:

  - Live Search
  - API Mesh
  - App Builder
  - Catalog Service

- **[SendGrid service](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)**—This service is disabled by default because the application is non-HIPAA-compliant. Merchants can submit a support request to enable Sendgrid, but they must acknowledge that they assume the risk of using the service.

### Features disabled by default

The following features are disabled by default in the the HIPAA-readiness module. Merchants can enable any of these features at their own risk.

- **[Guest checkout](../stores-purchase/checkout-guest.md)**—This feature presents a potential risk for various aspects of HIPAA including logging, access control, PHI hygiene and lineage, and potentially more.

- **[Newsletter feature](../merchandising-promotions/newsletters.md)**—This feature is disabled to prevent PHI being used in a marketing context.

- **[Advanced Reporting service setting](../getting-started/business-intelligence.md)**— This configuration setting is disabled to prevent PHI from being used for analysis and reporting.
