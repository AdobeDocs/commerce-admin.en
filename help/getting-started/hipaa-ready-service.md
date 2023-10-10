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


## [Action Logs](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en)

Audit Log is one of the HIPAA requirements. In Adobe Commerce, we already have an Action Logs feature to record every change made by an Admin user who works in your store. But to meet HIPAA requirements about Audit Log, we made some changes with the feature to record all Admin user and customer actions performed via both the UI and API calls.

### Action logs report (System > Action Logs > Report)  
We made some changes with the Action Logs report grid.
- Two new columns Source & Client Type are added.
- Existing column Username renamed to Client Identifier
- Existing column Full Action Name renamed to Target

### Configure Admin actions for logging

This feature is not available anymore since all actions have to be recorded by default.

## Import / Export Features

Enhancements to Import/Export Features focus on improving the administrative experience and providing better visibility into user actions. It's important to note that these enhancements do not alter Import/Export core logic; rather, they extend the functionality to offer more comprehensive logging and improved data attribution.

### Core Logic

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

#### Disabled Guest Checkout by default
- Guest checkout presents a potential risk for various aspects of HIPAA including logging, access control, PHI hygiene and lineage, and potentially more.
- Guest Checkout has been disabled by default in the HIPAA product but can be enabled my merchants at their own risk.

### Disabled Newsletter feature by default
- The newsletter feature has been disabled by default to prevent PHI being used in a market context but can be enabled by the merchant at their own risk.

### Disabled Advanced Reporting Service setting by default
The Advanced Reporting Service setting has been disabled by default to prevent PHI from being used for analysis and reporting but can be enabled by the merchant at their own risk.