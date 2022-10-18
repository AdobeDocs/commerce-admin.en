---
title: Order status
description: Learn about the predefined order statuses and how to define custom order statuses to align with your operational needs.
---
# Order status

All orders have an order status that is associated with a stage in the order processing [workflow](order-processing.md). The status of each order is shown in the _Status_ column of the _Orders_ grid. Your store has a set of predefined order status and order state settings. The order state describes the position of an order in the workflow.

![Order Status](./assets/stores-order-status-column.png)<!-- zoom -->

>[!TIP]
>
>A partially refunded order remains in `Processing` status until **_all_** ordered items (including refunded items) are shipped. The order status does not change to `Complete` when even one order item is not yet shipped.

## Order status workflow

![Order status workflow](./assets/order-workflow.png)

## Predefined status

|Order Status|Status Code||
|--- |--- |--- |
|Processing|`processing`|When the state of new orders is set to 'Processing', the _Automatically Invoice All Items_ option becomes available in the configuration. Invoices are not created automatically for orders placed by using Gift Card, Store Credit, Reward Points, or other offline payment methods.|
|Suspected Fraud|`fraud`|Sometimes orders paid via PayPal or another payment gateway are marked as Suspected Fraud. This means that the order does not have invoice issued and the confirmation email is also not sent.|
|Pending Payment|`pending_payment`|This is the status used if order is created and PayPal or similar payment method is used. This means that the customer was directed to the payment gateway website, but no return information has been received yet. This status changes when customer pays.|
|Payment Review|`payment_review`|This status appears when PayPal payment review is turned on.|
|Pending|`pending`|This status indicates that no invoice and shipments have been submitted.|
|On Hold|`holded`|This status can only be assigned manually. You can put any order on hold.|
|Open|`STATE_OPEN`|This status means that an order or credit memo is still open and may need further action.|
|Complete|`complete`|This status means that the order is created, paid,  and shipped to customer.|
|Closed|`closed`|This status indicates that an order was assigned a credit memo and the customer has received a refund.|
|Canceled|`canceled`|This status is assigned manually in the Admin or, for some payment gateways, when the customer does not pay within the specified time.|
|PayPal Canceled Reversal|`paypay_canceled_reversal`|This status means that PayPal canceled the reversal.|
|Pending PayPal|`pending_paypal`|This status means that the order was received by PayPal, but payment has not yet been processed.|
|PayPal Reversed|`paypal_reversed`|This status means that PayPal reversed the transaction.|

{style="table-layout:auto"}

## Custom order status

In addition to the preset order status settings, you can create your own custom order status settings, assign them to order states, and set a default order status for order states. The order state indicates the position of the order within the order processing workflow and the order status defines the state of the order. For example, you might need a custom order status such as `packaging"`, `backordered`, or a status that is specific to your needs. You can create a descriptive name for the custom status and assign it to the associated order state in the workflow.

>[!NOTE]
>
>Only default custom order status values are used in the order workflow. Custom status values that are not set as default can be used only in the comments section of the order.

![Order Status Settings](./assets/order-status.png)<!-- zoom -->

### Create a custom order status

1. On the _Admin_ sidebar, click **Stores**.

1. In the _Settings_ section, choose **Order Status**.

1. In the upper-right corner, click **Create New Status**.

   ![Create New Order Status](./assets/order-status-new.png)<!-- zoom -->

1. Update the _Order Status Information_ section:

   - Enter a **Status Code** for internal reference. The first character must be a letter (a-z), and the rest can be any combination of letters and numbers (0-9). Use the underscore character instead of a space.

   - Enter a **Status Label** to identify the status setting in both the Admin and storefront.

1. In the _Store View Specific Labels_ section, enter any labels that are needed for different store views.

1. Click **Save Status**.

### Assign an order status to a state

1. On the _Order Status_ page, click **Assign Status to State**.

   ![Assign Status](./assets/store-status-assign-status.png)<!-- zoom -->

1. Update the **Assignment Information** section, do the following:

   - Choose the **Order Status** that you want to assign. They are listed by status label.

   - Set **Order State** to the place in the workflow where the order status belongs.

   - To make this status the default for the order state, select the **Use Order Status as Default** checkbox.

      >[!NOTE]
      >
      >Only the default order statuses are used in the order workflow. Non-default statuses can only be set in the **Order Comments** section in the Admin.

   - To make this status visible from the storefront, select the **Visible On Storefront** checkbox.

   ![Assign Status to State](./assets/order-status-assign-state.png)<!-- zoom -->

1. Click **Save Status Assignment**.

### Edit an existing order status

1. In the _Order Status_ grid, open the status record in edit mode.

1. Update the status settings as needed.

1. Click **Save Status**.

### Remove an order status from an assigned state

>[!NOTE]
>
>A status setting cannot be unassigned from a state if the status is in use.

1. In the _Order Status_ grid, find the order status record to be unassigned.

1. In the _Action_ column on the far right of the row, click the **Unassign** link.

   A message appears at the top of the workspace that the order status has been unassigned. Although the order status label still appears in the list, it is no longer assigned to a state. Order status settings cannot be deleted.

## Notification

Customers can track the status of their orders by [RSS feed](../merchandising-promotions/social-rss.md) if the Order RSS feed is enabled in the configuration. When enabled, a link to the RSS feed appears on each order.

### Enable order status notification

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Catalog** and choose **RSS Feeds** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Order** section.

1. Set **Customer Order Status Notification** to `Enable`.

   ![Customer Order Status Notification](../configuration-reference/catalog/assets/rss-feeds-order.png)<!-- zoom -->

1. When complete, click **Save Config**.

### Configure new order email notifications

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Sales** and choose **Sales Emails** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Order** section.

   ![Configuration - Order options](../configuration-reference/sales/assets/sales-emails-order.png)<!-- zoom -->

1. Set **New Order Confirmation Email Sender** to one of the following:

    - General Contact
    - Sales Representative
    - Customer Support
    - Custom Email 1
    - Custom Email 2

1. Choose the templates that you want to use for each customer type:

    - **New Order Confirmation Template** - Choose a template to use for customers with a registered store account.
    - **New Order Confirmation Template for Guest** - Choose a template to use for guest customers without a registered store account.

1. To notify another person (such as a business manager) about the new order, enter the email address to **Send Order Email Copy To**.

   You can add multiple email addresses if more than one recipient is required.

1. Set the **Send Order Email Copy Method** to one of the following:

   - `Bcc` - Only one email about the new order is sent to both customer and the additional recipient, but the customer does not see that the email they received was also sent to the additional recipient.
   - `Separate Email` - Two separate emails are sent---one to the recipient and one to the customer.

1. When complete, click **Save Config**.
