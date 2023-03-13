---
title: Actions control
description: Learn about using the Actions control to apply an operation to one or more records in the Admin.
exl-id: 03f313a9-bc17-4151-a2c8-8906342f025d
---
# Actions control

When working with a collection of records in the grid, you can use the Actions control to apply an operation to one or more records. The Actions control lists each operation that is available for the specific type of data. For example, you can use the Actions control to update the attributes of selected products, to change the status from `Disabled` to `Enabled`, or to delete records from the database.

You can make as many changes as necessary, and then update the records in a single step. It is much more efficient than changing the settings individually for each product. Applying edits to a batch of records is an asynchronous operation, which executes in the background so that you can continue working in the Admin without waiting for the operation to finish. The system displays a message when the task is complete.

The selection of available actions varies by list, and additional options might appear, depending on the action selected. For example, when changing the status of a group of records, a _[!UICONTROL Status]_ box appears next to the Actions control with additional options.

## Step 1: Select records

The checkbox in the first column of the list identifies each record that is a target for the action. The [filter controls](admin-grid-controls.md) can be used to narrow the list to the records you want to target for the action.

1. If needed, set the filters at the top of each column to show only the records that you want to include.

1. Select the checkbox of each record that is a target for the action, or use the column selector to choose a bulk selection.

  ![Select or deselect all or all on page](./assets/action-change-selection.png){width="350"}

## Step 2: Apply an action to selected records

1. Set the **[!UICONTROL Actions]** control to the operation that you want to apply.

   **_Example:_** Update attributes

   - In the list, select the checkbox of each record to be updated.

   - Set the **[!UICONTROL Actions]** control to `Update Attributes`.

     ![Select the Update Attributes action](./assets/action-select.png){width="400"}

   - Click **[!UICONTROL Submit]**.

      The Update Attributes page lists all the available attributes, organized by group in the panel on the left.

      ![Update Attributes page](./assets/action-update-attributes.png){zoomable="yes"}

   - Select the **[!UICONTROL Change]** checkbox next to each attribute and make the necessary changes.

   - Click **[!UICONTROL Save]** to update the attributes for the group of selected records.

1. When complete, click **[!UICONTROL Submit]**.

## Checkbox actions

|Action|Description|
|--- |--- |
|[!UICONTROL Select All]|Selects the checkbox of all records in the list.|
|[!UICONTROL Unselect All]|Clears the checkbox of all records in the list.|
|[!UICONTROL Select All on This Page]|Selects the checkbox of records displayed on the current page.|
|[!UICONTROL Deselect All on This Page]|Clears the checkbox of records displayed on the current page.|

{style="table-layout:auto"}
