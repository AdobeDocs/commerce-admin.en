---
title: HIPAA readiness on Adobe Commerce
description: TBD
feature: Security, Roles/Permissions
---
# HIPAA readiness on Adobe Commerce

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