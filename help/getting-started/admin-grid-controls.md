---
title: Admin Grid Controls
description: Learn how to work in Admin pages that manage data display a collection of records in a grid.
---
# Admin Grid Controls

Admin pages that manage data display a collection of records in a grid. The controls at the top of each column can be used to sort the data. The current sort order is indicated by an ascending or descending arrow in the column header. You can specify which columns appear in the grid, and drag them into different positions. You can also save different column arrangements as views that can be used later. The **Action** column lists operations that can be applied to an individual record. In addition, date from the current view of most grids can be exported to a [CSV](https://docs.magento.com/user-guide/system/data-csv.html) or XML file.

![Orders page - grid display](./assets/admin-workspace-grid.png)<!-- zoom -->

## Sort the list

1. Click any column header.

   The arrow indicates the current order as either ascending or descending.

1. Use the pagination controls to view additional pages in the collection.

## Paginate the list

1. Set the **Pagination** control to the number of records that you want to view per page.

1. Click **Next** and **Previous** to page through the list, or enter a specific **Page Number**.

    ![Grid display - page controls](./assets/pagination-controls.png )<!-- zoom -->

## Filter the list

1. Click **Filters**.

1. Complete as many filters as necessary to describe the record you want to find.

1. Click **Apply Filters**.

    ![Orders list - filter controls](./assets/admin-workspace-filters.png)<!-- zoom -->

## Export data

1. Select the records that you want to export.

   >[!NOTE]
   >
   >Product data cannot be exported from the grid. To learn more, see [Export](https://docs.magento.com/user-guide/system/data-export.html).

1. On the **Export** (![Menu selector](../assets/icon-export.png)) menu in the upper-right corner, choose one of the following file formats:

   - CSV
   - Excel XML

   ![Orders list - export options](./assets/customers-grid-export.png)<!-- zoom -->

1. Click **Export**.

1. Look for the downloaded file of exported data at the location used for downloads by your browser.

## Grid Layout

The selection of columns and their order in the grid can be changed according to your preference, and saved as a _view_. You can control which attributes show in the grid under the individual attribute configuration. Having many attributes displayed in the product grid may affect admin load time and performance.

![Order Grid Columns](./assets/admin-grid-columns.png)<!-- zoom -->

### Change the selection of columns

1. In the upper-right corner, click the **Columns** (![Columns control](../assets/icon-columns.png)) control.

1. Change the column selections:

   - Select the checkbox of any column that you want to add to the grid.
   - Clear the checkbox of any column that you want to remove from the grid.
   - To return the default grid view, click **Reset**.

  Make sure to scroll down to see all available columns.

### Move a column

1. Click the header of the column and hold.

1. Drag the column to the new position and release.

### Save a grid view

1. Click the **View** (![View control](../assets/icon-view-eye.png)) control.

1. Click **Save Current View**.

1. Enter a **name** for the view.

1. To save all changes, click the **arrow** (![Save all changes](../assets/icon-arrow-save.png)).

   The name of the view now appears as the current view.

### Change the grid view

1. Click the **View** (![View icon](../assets/icon-view-eye.png)) control.

1. Do one of the following:

   - To use a different view, click the name of the view.
   - To change the name of a view, click the **Edit** (![Edit icon](../assets/icon-edit-pencil.png)) icon and update the name.
   - To delete a view, click the **Edit** (![Edit icon](../assets/icon-edit-pencil.png)) icon and then click the **Delete** (![Delete icon](../assets/icon-delete-trashcan-solid.png)) icon.
