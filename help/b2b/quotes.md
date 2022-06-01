---
title: Negotiated Quotes
description: Learn about quote workflows and how you can provide this service to your company accounts.
---
# Negotiated Quotes

If quotes are [enabled in the configuration](configure-quotes.md), an authorized buyer from a company can initiate the price negotiation process by submitting a [request to negotiate](quote-price-negotiation.md) the price from the shopping cart. The _Quotes_ grid lists each quote received and maintains a history of the communication between buyer and seller. The standard [workplace controls](https://docs.magento.com/user-guide/stores/admin-workspace.html) can be used to filter the list, change the column layout, save views, and export data.

## Quote workflow

All quotes are initiated by the buyer from the shopping cart and follow the same basic workflow:

Step 1: Buyer requests quote - The buyer [requests a quote](quote-request.md) from the shopping cart. The request appears in the _My Quotes_ list in the account dashboard of the buyer and email notification is sent to the sales representative who is assigned to the company account. In the Admin, the request appears in the _Quotes_ grid, with a status of `New`. A request for a quote can be modified by the buyer until it is opened by the seller.

Step 2: Seller views request and sends response - The seller views the request for a quote. The status of the quote changes to `Pending`, and the buyer cannot make any changes. The [seller responds](quote-price-negotiation.md) by offering discounted pricing for the products in the quote, enters a comment, and sends the quote back to the buyer. The buyer and sales representative are notified by email that the seller has responded.

Step 3: Buyer receives response from seller - The buyer clicks the link in the email to open the quote, or opens the quote from the _My Quotes_ page of the account dashboard. The buyer and seller can continue the negotiation process until an agreement is reached, or the buyer declines the quote to end the negotiation.

Step 4: Buyer accepts quote - The buyer accepts the proposed price and continues to checkout. Additional discounts cannot be added to the negotiated quote.

## B2B role resources for store quotes

Configuration options for quotes are controlled using the [Role Resources](https://docs.magento.com/user-guide/system/permissions-role-resources.html). These role resources must be set for the Admin [User Role](https://docs.magento.com/user-guide/system/permissions-user-roles.html) that is assigned to the store administrator.

To grant access to quote functions in the Admin, go to **System** > _Permissions_ > **User Roles**, select the role, and navigate to Sales > Operations > Quotes in the _Role Resources_ tree.

## Apply an action

![Quotes](./assets/quotes-grid.png)<!-- zoom -->

The following actions can be applied to either single or multiple records.

1. On the _Admin_ sidebar, go to **[!UICONTROL Sales]** > _[!UICONTROL Operations]_ > **[!UICONTROL Quotes]**.

1. In the first column of the grid, select the checkbox for each record that you want to update.

1. Follow the instructions for the action that you want to apply.

### View a quote

1. In the **[!UICONTROL Actions]** column for a record, click **[!UICONTROL View]**.

1. To respond to the customer request, follow the instructions and begin the [price negotiation](quote-price-negotiation.md) process.

### Decline a request for a quote

Only quote requests with an `Open` status can be declined.

1. Select each open quote request that you want to decline.

1. Set the _[!UICONTROL Actions]_ control to `Declined`.

1. When prompted, enter the reason the quote was declined and click **[!UICONTROL Confirm]**.

   ![Decline Quote?](./assets/quote-decline-confirm.png)<!-- zoom -->

## Column descriptions

|Column|Description|
|--- |--- |
|[!UICONTROL Select]|To select the quotes to be subject to an action, select the checkbox or use the selection control in the column header. Options: Select All / Deselect All|
|[!UICONTROL ID]|A unique numeric identifier that is assigned when a request for a quote is submitted from the shopping cart of a buyer. When viewing the quote detail the ID appears at the top of the page, instead of the quote name.|
|[!UICONTROL Name]|The name assigned to a quote request by the buyer.|
|[!UICONTROL Created Date]|The date and time the buyer first submitted the request for a quote.|
|[!UICONTROL Company]|The name of the company on behalf of which a buyer submits a request for a quote.|
|[!UICONTROL Submitted By]|The first and last name of the company buyer who submits a request for a quote.|
|[!UICONTROL Last Updated]|The date and time of the last communication between buyer and seller regarding the quote.|
|[!UICONTROL Sales Rep]|The first and last name of the sales representative who manages the buyer’s account.|
|[!UICONTROL Quote Total (Base)]|The total price of products to be purchased based on the original quote. The total amount appears in the base currency of the website and in the currency of the storefront.|
|[!UICONTROL Quote Total (Negotiated)]|The total price of products to be purchased based on the negotiated quote. The total amount appears in the base currency of the website and in the currency of the storefront.|
|[!UICONTROL Status]|Indicates the current state of a quote request. The status of a quote can be changed only by action on the part of either the buyer or seller. See also the Status settings from the [buyer’s account](account-dashboard-my-quotes.md). <br/>**[!UICONTROL New]** - The buyer submitted a request for a quote, but it has not been viewed by the seller. The request can be updated by the buyer until it is opened by the seller. <br/>**[!UICONTROL Open]** - The seller opened the request and is in the process of reviewing it and preparing a response. <br/>**[!UICONTROL Submitted]** - The seller sent a response to the buyer. The quote record cannot be edited during the negotiation process. <br/>**[!UICONTROL Client Reviewed]** - The buyer viewed the response from the seller and is in the process of preparing a reply. <br/>**[!UICONTROL Updated]** - The buyer submitted a response, but it has not been viewed by the seller. <br/>**[!UICONTROL Ordered]** - The buyer submitted the order based on the negotiated quote. <br/>**[!UICONTROL Closed]** - The buyer canceled the quote request. <br/>**[!UICONTROL Declined]** - The seller declined the request for a quote. Any custom pricing is removed from the quote and the record is locked from further edits. <br/>**[!UICONTROL Expired]** - The buyer did not respond to the seller’s reply within the designated time period and the quote is no longer valid.|
|[!UICONTROL Actions]|**[!UICONTROL View]** - Opens the request for a quote and maintains a record of the negotiation between buyer and seller.|

{style="table-layout:auto"}

## Button bar

| Button | Description |
| ------ | ----------- |
| [!UICONTROL Send ]| Sends the updated quote as a reply to the buyer’s inquiry. This button is disabled if the seller is waiting for a reply from the buyer. |
| [!UICONTROL Back] | Returns to the _Quotes_ page without saving changes. |
| [!UICONTROL Print] | Sends the quote to a printer or saves it as a PDF file. |
| [!UICONTROL Save as Draft] |Saves any changes made to the quote, but does not send it back to the buyer.|
| [!UICONTROL Decline] | Declines the request to negotiate prices, either on the initial inquiry, or during ongoing negotiations. When a quote is declined, the seller should add a comment to explain the decision. When a quote is declined, all negotiated prices are reset to the original values. This button is disabled while the seller is waiting for a reply from the buyer.|

{style="table-layout:auto"}

## Example Quote

The following figure shows an example quote with some settings configured.

![Example quote](./assets/quote-full.png)
