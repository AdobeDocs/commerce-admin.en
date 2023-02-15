---
title: Orders
description: Learn about the Orders workspace and the search capabilities used to locate orders in the Admin.
exl-id: 6ec8b8c7-97c4-446e-9420-e36e72e90237
---
# Orders

The _Orders_ grid lists all current orders and tracks their progress and [order status](order-status.md) through the [workflow](order-processing.md). An easy way to understand the basic process is that an order becomes an [invoice](invoices.md), and an invoice becomes a [shipment](shipments.md). The grid represents the first stage of the process, and is where you can [update](order-update.md) existing orders and create orders.

Usually, orders are created when customers complete the checkout process from the storefront. However, if a customer needs assistance, you can also access their [shopping cart](shopping-assisted-cart-manage.md) or [create an order](customer-account-create-order.md) either from the _Orders_ grid or directly from their customer account.

## Orders workspace

The Orders workspace lists all current orders, and gives you the ability to edit existing orders and [create](customer-account-create-order.md) orders. Each row in the grid represents a customer order, and each column represents an attribute, or data field. Use the standard [controls](../getting-started/admin-grid-controls.md) to sort and filter the list, find orders, and apply [actions](../getting-started/admin-actions-control.md) to selected orders. Use the tabs above the pagination controls to filter the list, change the default view, change and rearrange columns, and export data.

![Orders grid](./assets/orders-grid.png)<!-- zoom -->

### Grid layout

The selection of columns and their order in the grid can be changed according to your preference. The new layout can be saved as a grid _view_. By default, only nine of 20 available columns are included in the grid.

![Order Grid Columns](./assets/order-grid-columns.png)<!-- zoom -->

#### Change the column selection

In the upper-right corner, click the _Columns_ ( ![Column settings](../assets/icon-columns.png) ) control and do the following:

- Select the checkbox of any column that you want to add to the grid.
- Clear the checkbox of any column that you want to remove from the grid.

#### Reset the column selection

1. Click the _Columns_ ( ![Column settings](../assets/icon-columns.png) ) control.

1. To reset the grid columns, click **[!UICONTROL Reset]**.

   The grid layout changes to display only [default columns](#column-descriptions).
   
#### Move a column

1. Click and hold the header of the column.

1. Drag the column to the new position and release.

#### Save a grid view

1. Click the **[!UICONTROL View]** ( ![Eye icon](../assets/icon-view-eye.png) ) control.

1. Click **[!UICONTROL Save Current View]**.

1. Enter a **[!UICONTROL name]** for the view.

1. Click the arrow ( ![Arrow icon](../assets/icon-arrow-save.png) ) to save all changes.

    The name of the view now appears as the current view.

#### Change the view

Click the **[!UICONTROL View]** ( ![Eye icon](../assets/icon-view-eye.png) ) control. Then, do one of the following:

- To use a different view, click the name of the view.

- To change the name of a view, click the _Edit_ ( ![Pencil icon](../assets/icon-edit-pencil.png) ) icon and update the name.

### Workspace controls

|Control|Description|
|--- |--- |
|[!UICONTROL Create New Order]|Creates an order. See [Creating an Order](customer-account-create-order.md) for more information.|
|[!UICONTROL Go to Archive]|Displays the list of archived orders.|
|[!UICONTROL Search]|Initiates a search for orders based on the current filters.|
|[!UICONTROL Filters]|Defines a set of search parameters used to filter the records that appear in the grid.|
|[!UICONTROL Default View]|Determines the default column layout of the grid.|
|[!UICONTROL Columns]|Determines the selection of columns and their order in the grid. The column layout can be changed and saved as a _view_. By default, only some of the columns are included in the grid.|
|[!UICONTROL Export]|Exports the selected records as a CSV or Excel XML file.|

{style="table-layout:auto"}

### Actions

To apply an action to specific orders, select the checkbox in the first column of each order. To select or deselect all orders, use the control at the top of the column.

![Order Actions](./assets/orders-action.png)<!-- zoom -->

|Control|Description|
|--- |--- |
|[!UICONTROL Actions]|Lists all actions that can be applied to selected orders. To apply an action to an order or group of orders, select the checkbox in the first column of each order. <br/>Order actions: `Cancel` / `Hold` / `Unhold` / `Print Invoices` / `Print Packing Slips` / `Print Credit Memos` / `Print All` / `Print Shipping Labels` / `Move to Archive` ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)|
|[!UICONTROL Mass Actions]|Can be used to select multiple records as the target of action. Select the checkbox in the first column of each record that is subject to the action. Options: `Select All` / `Unselect All` / `Select Visible` / `Unselect Visible`|
|[!UICONTROL Submit]|Applies the current action to the selected order records.|
|[!UICONTROL Edit]|Opens the order in edit mode.|

{style="table-layout:auto"}

### Column descriptions

|Column|Description|
|--- |--- |
|[!UICONTROL Select]|Select the checkbox to select the quotes to be subject to an action, or use the selection control in the column header. Options: Select All / Deselect All|
|[!UICONTROL ID]|A unique, sequential number that is assigned when a new order is saved for the first time.|
|[!UICONTROL Purchase Point]|Identifies the store view where the order was placed.|
|[!UICONTROL Purchase Date]|The date and time when the order was placed. It is always displayed according to the default time zone.|
|[!UICONTROL Bill-to Name]|The name of the person who is responsible to pay for the order.|
|[!UICONTROL Ship-to Name]|The name of the person to whom the order is to be shipped.|
|[!UICONTROL Grand Total (Base)]|The grand total of the order.|
|[!UICONTROL Grand Total (Purchased)]|The grand total of products purchased in the order.|
|[!UICONTROL Status]|The current order status.|
|[!UICONTROL Action]|_[!UICONTROL View]_ opens the order in edit mode.|
|[!UICONTROL Allocated sources]| The sources allocated to that specific order.|

{style="table-layout:auto"}

Additional columns available:

|Column|Description|
|--- |--- |
|[!UICONTROL Billing Address]|The billing address of the customer who placed the order.|
|[!UICONTROL Shipping Address]|The address where the order is to be shipped.|
|[!UICONTROL Shipping Information]|The method that is to be used to ship the order.|
|[!UICONTROL Customer Email]|The email address of the person who placed the order.|
|[!UICONTROL Customer Group]|The customer group to which the person who placed the order is assigned.|
|[!UICONTROL Subtotal]|The order subtotal, without shipping and handling, and tax.|
|[!UICONTROL Shipping and Handling]|The amount charged for shipping and handling.|
|[!UICONTROL Customer Name]|The first and last name of the customer who placed the order.|
|[!UICONTROL Payment Method]|The method of payment to be used for the order.|
|[!UICONTROL Total Refunded]|Any amount from the order that is to be refunded to the customer.|
|[!UICONTROL Refunded to Store Credit]|![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) Any amount from the order that is to be refunded to the customer's store credit.|
|[!UICONTROL Company Name]|![B2B for Adobe Commerce](../assets/b2b.svg) (Available with B2B for Adobe Commerce) The name of the [company](../b2b/account-companies.md) who placed the order.|

{style="table-layout:auto"}

## Order search

The Search box in the upper left of the Orders grid can be used to find specific orders by keyword, or by filtering the order records in the grid.

![Search Results](./assets/order-search.png)<!-- zoom -->

### Search for a match

1. Enter a search term into the page search box.

1. Click _Search_ ( ![Magnifying glass icon](../assets/icon-magnify-search.png) ) to display the results.

### Filter the search

1. Click the _Filters_ ( ![Funnel icon](../assets/icon-filter-search.png) ) tab to display the selection of search filters.

1. Complete as many of the filters as needed to describe the orders that you want to find.

1. Click **[!UICONTROL Apply Filters]** to display the results.

   ![Order Filters](./assets/order-search-filter.png)<!-- zoom -->

### Search filters

|Filter|Description|
|--- |--- |
|[!UICONTROL Purchase Date]|Filters the search based on the date purchased. To find orders within a range of dates, enter both the **[!UICONTROL from]** and **[!UICONTROL to]** dates.|
|[!UICONTROL ID]|Filters the search based on order ID.|
|[!UICONTROL Grand Total (Base)]|Filters the search based on the Grand Total of each order, which includes any credits applied to the order.|
|[!UICONTROL Grand Total (Purchased)]|Filters the search based on Grand Total of items purchased in each order.|
|[!UICONTROL Bill-to Name]|Filters the search according to the name of the person who is responsible to pay for the order.|
|[!UICONTROL Ship-to Name]|Filters the search according to name of the person to whom each order is shipped .|
|[!UICONTROL Purchase Point]|Filters the search by website, store, or store view where the order was placed.|
|[!UICONTROL Status]|Filters the search based on order status. Options: `Canceled` / `Closed` / `Complete` / `Suspected Fraud` / `On Hold` / `Payment Review` / `PayPal Canceled Reversal` /` PayPal Reversed` /` Pending` / `Pending Payment` / `Pending PayPal` / `Processing`|
|[!UICONTROL Braintree Transaction Source]|Filters the search based on transaction source.|

{style="table-layout:auto"}

### Search tools

|Tool|Description|
|--- |--- |
|[!UICONTROL Apply Filters]|Applies all filters to the search results.|
|[!UICONTROL Cancel]|Cancels the current search.|
|[!UICONTROL Clear All]|Clears all search filters.|

{style="table-layout:auto"}

## Troubleshooting resources

For help with troubleshooting order issues, see the following Commerce Support Knowledge Base articles:

- [Orders display error](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-known-issue-orders-display-error.html)
- [PayPal duplicate orders 10415 error](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-6/mdva-31006-magento-patch-paypal-duplicate-orders-10415-error.html)
- [New orders are sent to archive](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/new-orders-are-sent-to-archive.html)
- [Orders not displayed in the Orders grid in the Admin](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/orders-not-displayed-in-the-orders-grid-in-the-admin.html)
- [Order status - incorrect shipment created via REST API](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-7/mdva-30972-magento-patch-order-status-incorrect-shipment-created-via-rest-api.html)
