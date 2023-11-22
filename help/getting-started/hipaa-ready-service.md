---
title: HIPAA readiness on Adobe Commerce
description: Learn how you can add the Adobe Commerce HIPAA-Ready module and get additional features and functionalities that allow you to comply with your HIPAA obligations.
feature: Security, Compliance
hide: yes
hidefromtoc: yes
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
---
# HIPAA readiness on Adobe Commerce

>[!IMPORTANT]
>
>**Legal Disclaimer**<br/>
>This information is intended to help Adobe customers answer their questions regarding Adobe's HIPAA-Ready Services. It does not constitute legal advice. Merchants should consult with their own legal counsel to understand their obligations under HIPAA and the appropriate use and configuration of Adobe's products.

## Health Insurance Portability and Accountability Act (HIPAA)

The Health Insurance Portability and Accountability Act (HIPAA) is the key federal healthcare privacy law in the United States and is enforced by the U.S. Department of Health and Human Services (HHS). HIPAA applies to _Covered Entities_ (such as healthcare providers, insurers, and clearinghouses) and _Business Associates_ (such as those entities that provide services to covered entities). HIPAA requirements are set across three separate rules: Privacy Rule, Security Rule, and Breach Notification Rule. Adobe acts as a Business Associate for certain products, which Adobe classifies as "HIPAA-Ready Services." Data regulated under HIPAA is referred to as _Protected Health Information_ or PHI. PHI is a subset of health information that (1) is created or received by a healthcare provider, health plan, or healthcare clearinghouse, (2) relates to the past, present, or future physical or mental health or condition of an individual, the provision of healthcare to an individual, or the past, present, or future payment for the provision of healthcare to an individual, and (3) identifies the individual or with respect to which there is a reasonable basis to believe that the information can be used to identify the individual. The HIPAA Privacy and Security Rules require that a Covered Entity obtain written assurances from a Business Associate in the form of a Business Associate Agreement, or BAA, requiring the Business Associate to safeguard the privacy and security of the Covered Entityʼs PHI.

## Adobe Commerce HIPAA-Ready

Adobe Commerce HIPAA-Ready has additional features and functionalities that allow merchants to comply with their respective HIPAA obligations. You can install the Adobe Commerce HIPAA-Ready (`magento/hipaa-ee`) module to your Adobe Commerce on cloud infrastructure. There are also some features that must be disabled to be compliant with HIPAA.

*These materials are intended for informational purposes only. Provision of this information does not entitle the recipient to
any contractual or other rights. While efforts have been made to assure the accuracy of the information as of the
date it has been provided, no representation is made that such information is accurate and complete, and Adobe undertakes no
obligation to update this information as the law or Adobe's products change. Also, this document is not to be distributed to
any party other than the intended recipient without written consent from Adobe.*

## System requirements

HIPAA-readiness on Adobe Commerce has the same system requirements as Adobe Commerce with the additional requirements:

- Adobe Commerce version 2.4.6-p3 or newer (non-beta)
- Adobe Commerce on cloud infrastructure or Adobe Commerce on Managed Services
- Latest version of the `magento/hipaa-ee` extension

## Installation

Adobe's HIPAA-Ready Services is technically a composer metapackage `magento/hipaa-ee` that contains links to special modules. This metapackage resides in the repository [repo.magento.com](https://repo.magento.com). 

1. To be able to install `magento/hipaa-ee` metapackage, you must have access to it. For key generation and obtaining the necessary rights, refer to [Get your authentication keys](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en).

1. Check the environment where you will install the package and make sure that it meets the general [system requirements](#system-requirements).

1. Add the metapackage `magento/hipaa-ee` to the composer configuration. 

   The simplest way is by using the composer CLI. For example:

   ```shell
   composer require magento/hipaa-ee
   ```

1. If Adobe Commerce is not yet installed, you can start the installation (follow the [Installation instructions](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en)).

   If Adobe Commerce is already installed, then after downloading modules, run `bin/magento setup:upgrade` command and then follow the recommendations.

   ```shell
   bin/magento setup:upgrade
   ```

   When this command is running, the newly downloaded modules are enabled, and the scripts to install them are launched. To learn more about module management, see [Enable or disable modules](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en).

1. After the installation or updating process is finished, you should check whether the `Hipaa*` relevant modules have been included.

   Run the command:

   ```shell
   bin/magento module:status
   ```

   If the HIPAA composer package was added correctly, you see the HIPAA modules in the output of the command. For example:

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

Audit Logging is a HIPAA requirement. In Adobe Commerce, the [Action Logs](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) feature records every change made by an Admin user who works in your store. To meet HIPAA requirements about Audit Log, there are changes to the feature to record all Admin user and customer actions performed through the Admin UI and through API calls.

#### Action Logs report  

The _Action Logs_ report grid (**[!UICONTROL System]** > Action Logs > Report) is modified to accommodate customer actions performed through the Admin UI and API. 

1. Two additional columns:
   - ***Source***: Displays where the action was performed.  
      Values: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Client Type***: Displays the client type.   
      Values: Customer | Admin | Integration
   

2. Rename ***Username*** to ***Client Identifier***
   - ***Client Identifier***: Displays the login ID for the user who performed the action  
      Values:
      - an email if Client Type is Customer
      - a username if Client Type is Admin
      - a name if Client Type is Integration

3. Rename ***Full Action Name*** to ***Target***
   - ***Target***:  Displays the action name  
         Values:
       - an endpoint if Source is REST API or SOAP API
       - a query/mutation name if GraphQL API
       - an action name if Admin UI or Customer UI.

#### Configure Admin actions for logging

This feature is not available because all actions must be recorded by default.

### Import / export features

Enhancements to import/export features are focused on improving the administrative experience and providing better visibility into user actions. 

>[!NOTE]
>
>These ***enhancements do not alter Import/Export core logic***; rather, they extend the functionality to offer more comprehensive logging and improved data attribution. The fundamental functionality of import/export remains unchanged. Users can continue to use the existing features and workflows without any disruption.

#### Administrative action logging

One of the key improvements within the import/export features is the enhanced logging of administrative actions. This introduces the capability to delve deeper into activities associated with data import/export, contributing to improved tracking and auditability. The following actions are now logged and reflected in the **[!UICONTROL System] > _[!UICONTROL Action Logs]_ > [!UICONTROL Report]** grid:

| Type | Actions |
| ---- | ------- |
| Import | <ul><li>An Admin user executes an import<li>An Admin user downloads an imported file<li>An Admin user downloads an error file<ul/> |
| Export | <ul><li>An Admin user requests<li>An Admin user downloads an exported file<ul/> |
| Scheduled imports/exports | <ul><li>An Admin user schedules export<li>An Admin user edits a scheduled export<li>An Admin user runs a scheduled export<li>An Admin user deletes a scheduled export<li>An Admin user schedules an import<li>An Admin user edits a scheduled import<li>An Admin user runs a scheduled import<li>An Admin user deletes a scheduled import<li>An Admin user executes a bulk delete of import/export operations<ul/> |

### Display enhancements and improved filtering/sorting

To empower Admin users with more informative grids, there are several enhancements to the display of data and filtering and sorting capabilities:

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

#### Scheduled imports/exports ([!UICONTROL System] > _[!UICONTROL Data Transfer]_ > [!UICONTROL Scheduled Import/Export])

- Added an **[!UICONTROL ID]** column.
- Added a **[!UICONTROL Scheduled At]** column (_date and time when the import or export was scheduled_).
- Added a **[!UICONTROL User]** column (_username of an Admin user who scheduled the import/export_).

## Disabled features for HIPAA-readiness

### SaaS Services

None of the SaaS services offered for Adobe Commerce are available under the HIPAA-readiness offering. This includes, but is not limited to:

- Live Search
- API Mesh
- App Builder
- Catalog Service

### Disabled guest checkout by default

- Guest checkout presents a potential risk for various aspects of HIPAA including logging, access control, PHI hygiene and lineage, and potentially more.
- Guest Checkout is disabled by default in the HIPAA-readiness module, but can be enabled my merchants at their own risk.

### Disabled newsletter feature by default

- The newsletter feature is disabled by default to prevent PHI being used in a marketing context, but can be enabled by the merchant at their own risk.

### Disabled the Advanced Reporting service setting by default

The Advanced Reporting service setting is disabled by default to prevent PHI from being used for analysis and reporting, but can be enabled by the merchant at their own risk.
