---
title: Returns
description: <Add description here>
---
# Returns

A _returned merchandise authorization_ (RMA) can be granted to customers who request to return an item for replacement or refund. Typically, the customer contacts the merchant to request a refund. If approved, a unique RMA number is assigned to identify the returned product. In the configuration, you can either enable RMA for all products or allow RMA for only certain products. The _Returns_ grid lists the current returned merchandise requests (RMAs) and is used to enter new return requests.

![Returns grid](./assets/return.png)<!-- zoom -->

RMAs can be issued for simple, grouped, configurable, and bundle product types. However, RMAs are not available for virtual products, downloadable products, and gift cards.

## Column descriptions

|Column|Description|
|--- |--- |
|Select|Select the checkbox to select the returns to be subject to an action, or use the selection control in the column header. Options: Select All / Deselect All / Select Visible / Unselect Visible|
|RMA|A unique numeric identifier that is assigned to each return|
|Requested|Date and time the return was placed|
|Order|A unique number of the original order|
|Ordered|The date and time the order was placed|
|Customer|The name of the customer or buyer who placed the order|
|Status|Return status. Options: Pending / Authorized / Partially Authorized / Approved / Rejected / Processed and Closed / Closed|
|Action|View opens the return in edit mode|

{style="table-layout:auto"}

## RMA and return workflow

1. **Receive request** - Both registered customers and guests can request an RMA. You can also [submit an RMA request] from the Admin.

2. **RMA issued** - After considering the request, you can authorize it partially, completely, or cancel the request. If you authorize the return and agree to pay for the return shipment, you can create a shipment order from the Admin with a supported carrier.

3. **Merchandise received and return processed** -  The following flow chart describes the operational order to complete the return process:

   ![Product Return Workflow](./assets/workflow-customer-returns.png) <!-- {:width="500px"} -->

## RMA status

During its lifecycle, a returned merchandise authorization (RMA) can have many assigned statuses (such as Pending or Authorized). The RMA status indicates the progress of an RMA request raised by the user or the merchant.

|Status|Description|
|--- |--- |
|Pending|This is the initial status assigned to an RMA request when it is raised by a user on the storefront or by the merchant in the Admin.|
|Authorized|This status is assigned to the RMA when all requested items are authorized by the merchant in the Admin for the returns.|
|Partially Authorized|This status is assigned to the RMA if any of the requested items have been denied and other products are authorized.|
|Denied|This status is assigned to the RMA if all the requested items are rejected by the merchant in the Admin for the returns.|
|Return Received|This status is assigned by the merchant to the RMA when the requested items are received from the user.|
|Return Partially Received|This status is assigned by the merchant to the RMA when the requested items are partially returned and some of the items are denied to process.|
|Approved|This status is assigned by the merchant to the RMA when the requested items are approved to process further.|
|Rejected|This status is assigned by the merchant to the RMA when the requested items are rejected to process further.|
|Processed and Closed|This status is assigned by the merchant to the RMA when all the requested items are approved to process further.|
|Closed|This status is assigned by the merchant to the RMA when the requested items are denied to process for return.|

{style="table-layout:auto"}

## Create a return request

A merchant can create a return request on behalf of the customer from the Admin. Customers can [create a return request](rma-customer-experience.md) on the storefront for an Adobe Commerce store.

1. On the _Admin_ sidebar, go to **Sales** > **Returns**.

1. Click **New Return Request**.

1. Click an order with a `Complete` status to create a return request.

1. Under the _Return Information_ section, select the **Return Items** tab.

1. To add items to return, click **Add Items**.

1. Select the checkbox for the required product and click **Add Selected Product to returns**.

1. For **Requested**, enter the number of items to be returned.

1. Set **Return Reason** to one of the following:

    - Wrong Color
    - Wrong Size
    - Out of Service
    - Other

    If the reason for the return is different from those listed, you can enter your own if you select the `Other` option.

1. Set **Item Condition** to one of the following:

    - Unopened
    - Opened
    - Damaged

1. Set **Resolution** to one of the following:

    - Exchange
    - Refund
    - Store Credit

1. To create a return, click **Submit Returns**.

   ![RMA Items Requested](./assets/return-item-request.png)<!-- zoom -->

   The newly submitted RMA request appears on the **Returns** page with a `Pending` status.
