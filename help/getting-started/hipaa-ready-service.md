---
title: HIPAA readiness on Adobe Commerce
description: TBD
feature: Security, Roles/Permissions
---

# HIPAA readiness on Adobe Commerce

### *Legal Disclaimer*
*This document is intended to help Adobe customers answer their questions regarding Adobe’s HIPAA-Ready Services. It does not
constitute legal advice. Each customer should consult with their own legal counsel to understand their obligations under HIPAA
and the appropriate use and configuration of Adobe’s products.*

## Health Insurance Portability and Accountability Act (HIPAA)

The Administrative Simplification subtitle of the Health Insurance Portability and Accountability Act of 1996 (“HIPAA”) provides for the U.S. Department of Health and Human Services to promulgate standards governing the privacy and security of certain individually identifiable health information.  HIPAA was most significantly amended by the Health Information Technology Act for Economic and Clinical Health Act of 2009 (the “HITECH Act”), which added breach notification requirements and expanded the scope of who is governed by HIPAA.  The HIPAA Privacy, Security, and Breach Notification Rules establish important protections for individually identifiable health information called protected health information or “PHI” when created, received, maintained, or transmitted by a HIPAA covered entity or business associate.  A “Covered Entity” is a health care provider, health plan, or a health care clearinghouse.  A “Business Associate” is an entity or person, other than a member of the workforce of a covered entity, who performs functions or activities on behalf of, or provides certain services to, a Covered Entity that involves creating, receiving, maintaining, or transmitting PHI.
The HIPAA Privacy and Security Rules require that a Covered Entity obtain written assurances from a Business Associate in the form of a Business Associate Agreement, or BAA, requiring the Business Associate to safeguard the privacy and security of the Covered Entity’s PHI.

## Adobe Commerce HIPAA-Ready

Adobe Commerce HIPAA-Ready has additional features and functionalities that allow merchants to comply with their respective HIPAA obligations. You can install the Adobe Commerce Hipaa Ready (magento/hipaa-ee) module to your Adobe Commerce on cloud infrastructure. There are some features that also have to be disabled to be compliant with HIPAA.

*These materials are intended for informational purposes only. Provision of this information does not entitle the recipient to
any contractual or other rights. Furthermore, while efforts have been made to assure the accuracy of the information as of the
date it has been provided, no representation is made that such information is accurate and complete, and Adobe undertakes no
obligation to update this information as the law or Adobe’s products change. Additionally, this document is not to be distributed to
any party other than the intended recipient without written consent from Adobe.*

## System Requirements

HIPAA readiness on Adobe Commerce shares the same system requirements as Adobe Commerce with the additional requirements:
- Adobe Commerce version 2.4.6-p3 or newer.
- Adobe Commerce cloud infrastructure.
- Latest version of **magento/hipaa-ee** extension.

## Installation instructions

Adobe’s HIPAA-Ready Services is technically a composer's metapackage `magento/hipaa-ee` that contains links to special modules. The metapackage `magento/hipaa-ee` located in the repository [repo.magento.com](https://repo.magento.com). 

In order to be able to install `magento/hipaa-ee` metapackage, you need to have access to it. For key generation and obtaining the necessary rights, please refer to this topic "[Get your authentication keys](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en)".

Before installing the `magento/hipaa-ee` metapackage, you should also check the environment where the package will be installed meets the [system requirements](#system-requirements).

So, having the necessary rights to the repository where the metapackage `magento/hipaa-ee` is located, and making sure that your environment meets the system requirements, you can start the installation.

To install, you only need to add the metapackage `magento/hipaa-ee` to the composer configuration.

```shell
composer require magento/hipaa-ee
```

If Adobe Commerce has not been installed, then you can start the installation. Follow this [Installation instructions](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en).
If Adobe Commerce was already installed, then after downloading modules, you need to run `bin/magento setup:upgrade` command and then follow the recommendations.

```shell
bin/magento setup:upgrade
```

In fact, when this command is running, the newly downloaded modules will be enabled, and the scripts to install them will be launched. You can learn more about module management in this topic "[Enable or disable modules](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en)".

After the installation or updating process is finished, you should check whether the Hipaa relevant modules have been included.
Run the command:

```shell
bin/magento module:status
```
Output:

```shell
List of enabled modules:
Magento_Store
...
Magento_HipaaAnalytics
Magento_HipaaCheckout
Magento_HipaaLogging
Magento_HipaaScheduledImportExport
Magento_HipaaAdminLogging
Magento_HipaaCustomerLogging
Magento_HipaaNewsletter
Magento_HipaaImportExport
Magento_HipaaApiLogging
...
Temando_ShippingRemover

List of disabled modules:
```
Or this command

```shell
php bin/magento module:status --enabled | grep Hipaa
```

Output:

```shell
Magento_HipaaAnalytics
Magento_HipaaCheckout
Magento_HipaaLogging
Magento_HipaaScheduledImportExport
Magento_HipaaAdminLogging
Magento_HipaaCustomerLogging
Magento_HipaaNewsletter
Magento_HipaaImportExport
Magento_HipaaApiLogging
```

The result of this command is a list of modules. All modules prefixed with `Magento_Hipaa` must be in the enabled modules section.

## HIPAA Readiness Changes

The `magento/hipaa-ee` package introduces some changes and enhancements to the base Commerce product. The sections below detail those changes and how they alter the base product.


### [Action Logs](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en)

Audit Log is one of the HIPAA requirements. In Adobe Commerce, we already have an Action Logs feature to record every change made by an Admin user who works in your store. But to meet HIPAA requirements about Audit Log, we made some changes with the feature to record all Admin user and customer actions performed via both the UI and API calls.

#### Action logs report (System > Action Logs > Report)  

We modified the Action Logs report grid to accommodate customer actions perform via UI and API. 
1. Add 2 new columns ***Source*** & ***Client Type***.
   - ***Source***: Displays where the action was performed.  
      Values: Admin UI | Customer UI | REST API | SOAP API | GraphQL API
   - ***Client Type***: Display the client type.   
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

This feature is not available anymore since all actions have to be recorded by default.

### Import / Export Features

Enhancements to Import/Export Features focus on improving the administrative experience and providing better visibility into user actions. It's important to note that these enhancements do not alter Import/Export core logic; rather, they extend the functionality to offer more comprehensive logging and improved data attribution.

#### Core Logic

The fundamental functionality of Import/Export remains unchanged. Users can continue to leverage the existing features and workflows without any disruption.

### Administrative Action Logging

One of the key improvements within the Import/Export features is the enhanced logging of administrative actions. This introduces the capability to delve deeper into activities associated with data import/export, contributing to improved tracking and auditability. The following actions are now logged and reflected in the **System > Action Logs > Report** grid:

#### Import

- an Admin does import
- an Admin downloads an imported file
- an Admin downloads an error file

#### Export

- an Admin requests export
- an Admin downloads exported file

#### Scheduled Imports/Exports

- an Admin schedules export
- an Admin edits scheduled export
- an Admin runs scheduled export
- an Admin deletes scheduled export
- an Admin schedules import
- an Admin edits scheduled import
- an Admin runs scheduled import
- an Admin deletes scheduled import
- an Admin mass deletes import/export operations

### Grid Display Enhancements & Improved Filtering and Sorting

To empower administrators with more informative grids, several enhancements have been made to the display of data as well as filtering and sorting capabilities:

#### Import History Grid (System > Data Transfer > Import History)

- Enabled filtering for all columns except **Imported File**, **Error File**, **Execution Time** and **Summary**.

#### Export Grid (System > Data Transfer > Export)

- Added an **ID** column.
- Added a **Requested At** column (_date and time when export was requested_).
- Added a **User** column (_username of an admin who did the request_).
- Removed an **Action** column.
- Moved the **Download** link to a **File name** column (_just like in Import History Grid_).
- Disabled the action responsible for deletion of an exported file (_to improve tracking_).
- Enabled sorting for all columns except **File name**.
- Enabled filtering for all columns.

#### Scheduled Imports/Exports Grid

- Added an **ID** column.
- Added a **Scheduled At** column (_date and time when import/export was scheduled_).
- Added a **User** column (_username of an admin who scheduled import/export_).

### Disabled Guest Checkout by default
- Guest checkout presents a potential risk for various aspects of HIPAA including logging, access control, PHI hygiene and lineage, and potentially more.
- Guest Checkout has been disabled by default in the HIPAA product but can be enabled my merchants at their own risk.

### Disabled Newsletter feature by default
- The newsletter feature has been disabled by default to prevent PHI being used in a market context but can be enabled by the merchant at their own risk.

### Disabled Advanced Reporting Service setting by default
The Advanced Reporting Service setting has been disabled by default to prevent PHI from being used for analysis and reporting but can be enabled by the merchant at their own risk.
