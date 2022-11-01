---
title: Email templates
description: Placeholder
---
# Email templates

Email templates define the layout, content, and formatting of automated messages sent from your store. They are called transactional emails because each one is associated with a specific type of transaction, or event.

Commerce includes a set of responsive email templates that are triggered by a variety of events that take place during the operation of your store. Each template is optimized for any screen size, and can be viewed from the desktop, as well as on tablets and mobile devices. You will find a variety of prepared email templates related to customer activities, sales, product alerts, admin actions, and system messages that you can [customize](email-template-custom.md) to reflect your brand.

Commerce emails can be rendered by HTML and plain text email clients. There might be some variation between clients in the way email are rendered.

## Prepare your email logo

Logos can be saved as any of the following file types. Logos with transparent backgrounds can be saved as either .GIF or .PNG files.

- JPG/JPEG
- GIF
- PNG

To ensure that your logo renders well on high-resolution devices, the uploaded image should be three times the size of the dimensions that are specified in the header template. Typically, original logo artwork is created as a vector image, so it can be scaled up without losing resolution. The image can then be saved in one of the supported bitmap image formats.

![Logo 3X display size](./assets/email-logo-third-size.png)<!-- zoom -->

To take advantage of the limited vertical space in the header, make sure to crop the image to eliminate any wasted space at the top or bottom. When editing the image, be careful to preserve the aspect ratio of the logo, so the height and width resize proportionally.

As a general rule, you can make an image smaller than the original, but not larger without losing resolution. Taking a small image and scaling it up in a photo editor lowers the resolution of the image. For example, if the display dimensions of the logo are 168 pixels wide by 48 pixels high in the header template, the uploaded image should be 504 pixels wide by 144 pixels high.

| Logo Dimensions | 1 x (display size) | 3 x (image size) |
|----------|----|----|
| Width: | 168 px | 504 px |
| Height: | 48 px | 144 px |

{style="table-layout:auto"}

## Configure email templates

The configuration determines the logo that appears in the default header template, as well as any custom [header](email-template-custom.md#header-template) and [footer](email-template-custom.md#footer-template) templates that you want to use for transactional email messages sent from your stores.

![Transactional email design](./assets/design-configuration-transactional-emails.png)<!-- zoom -->

[_Transactional Emails_](../content-design/configuration.md)

## Step 1. Upload Your Logo

1. On the _Admin_ sidebar, go to **Content** > _Design_ > **Configuration**.

1. Find the store view that you want to configure and click **Edit** in the _Action_ column.

1. Under _Other Settings_, expand ![Expansion selector](../assets/icon-display-expand.png) the **Transactional Emails** section.

1. To upload your prepared **Logo Image**, click **Upload** and select the file from your system.

1. For **Logo Image Alt**, enter alternate text to identify the image.

1. Enter the **Logo Width** and **Logo Height** in pixels.

   Enter each value as a number, without the `px` abbreviation. These values refer to the display dimensions of the logo in the header, and not to the actual size of the image.

## Step 2. Choose the header and footer templates

If you have custom header and footer templates for your store, or for different stores, you can specify which templates are used for each, according to the [scope](https://docs.magento.com/user-guide/configuration/scope.html) of the configuration. Otherwise, the default templates are used. To learn more, see [Customizing Email Templates](email-template-custom.md).

1. Choose the **Header Template** to be used for all transactional email messages.

1. Choose the **Footer Template** to be used for all transactional email messages.

1. When complete, click **Save Config**.

## Email template list

The list of email templates is organized alphabetically by module.

### Amazon_Payment

|Template|Configuration path|
|--- |--- |
|Hard-declined Authorization| n/a |
|Soft-declined Authorization| n/a |

{style="table-layout:auto"}

### Magento_Checkout

|Template|Configuration path|
|--- |--- |
| Payment Failed | **Page:** Sales > [Checkout](https://docs.magento.com/user-guide/configuration/sales/checkout.html)<br/>**Section:** Payment Failed Emails<br/>**Field:** Payment Failed Template|

{style="table-layout:auto"}

### Magento_Company

![B2B for Adobe Commerce](../assets/b2b.svg) (Available with B2B for Adobe Commerce only)

|Template|Configuration path|
|--- |--- |
| Assign Company Admin | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:**Customer-Related Emails<br/>**Field:** Default 'Assign Company Admin' Email|
| Assign Company to Customer | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:**Customer-Related Emails <br/>**Field:** Default 'Assign Company to Customer' Email|
| Company Admin Changed to Member | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:**Customer-Related Emails<br/>**Field:** Default 'Company Admin Changed To Member' Email|
| Company Admin Set Inactive | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:**Customer-Related Emails<br/>**Field:** Default 'Customer Status Inactive' Email|
| Company Invite | n/a |
| Company Registration Request | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:** Email Options - Company Registration<br/>**Field:** Default Company Registration Email|
| Company Status Active1 | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:**Company Status Change<br/>**Field:** Default 'Company Status Change To Active 1" Emai|
| Company Status Active2 | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:**Company Status Change<br/>**Field:** Default 'Company Status Change To Active 2" Emai|
| Company Status Blocked | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:**Company Status Change<br/>**Field:** Default 'Company Status Change To Blocked" Email|
| Company Status Pending Approval | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:**Company Status Change<br/>**Field:** Default 'Company Status Change To Pending Approval" Email|
| Company Status Rejected | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:**Company Status Change<br/>**Field:** Default 'Company Status Change To Rejected" Emai|
| Customer Status Active | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:**Customer-Related Emails<br/>**Field:** Default 'Customer Status Active' Email|
| Customer Status Inactive | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:**Customer-Related Emails<br/>**Field:** Default 'Company Admin Inactive' Email|
| Sales Representative Assigned to Company | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:**Customer-Related Emails<br/>**Field:** Default 'Sales Rep Assigned' Email|

{style="table-layout:auto"}

### Magento_CompanyCredit

![B2B for Adobe Commerce](../assets/b2b.svg) (Available with B2B for Adobe Commerce only)

|Template|Configuration path|
|--- |--- |
| Credit Limit Allocated | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:** Company Credit<br/>**Field:** Allocated Email Template|
| Credit Limit Updated | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:** Company Credit<br/>**Field:** Updated Email Template|
| Credit Reimbursed | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:** Company Credit<br/>**Field:** Reimbursed Email Template|
| Order Refunded to Company Credit |**Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:** Company Credit<br/>**Field:** Refunded Email Template|
| Order Reverted to Company Credit | **Page:** Customers > [Company Configuration](https://docs.magento.com/user-guide/configuration/customers/company-configuration.html)<br/>**Section:** Company Credit<br/>**Field:** Reverted Email Template|

{style="table-layout:auto"}

### Magento_Contact

|Template|Configuration path|
|--- |--- |
| Contact Form | **Page:** General > [Contacts](https://docs.magento.com/user-guide/configuration/general/contacts.html)<br/>**Section:** Email Options<br/>**Field:** Email Template |

{style="table-layout:auto"}

### Magento_Customer

|Template|Configuration path|
|--- |--- |
| Change Email |  **Page:** Customers > [Customer Configuration](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html)<br/>**Section:** Account Information Options<br/>**Field:** Change Email Template|
| Change Email and Password | **Page:** Customers > [Customer Configuration](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html)<br/>**Section:** Account Information Options<br/>**Field:** Change Email and Password Template|
| Forgot Password | **Page:** Customers > [Customer Configuration](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html)<br/>**Section:** Password Options<br/>**Field:** Forgot Email Template|
| New Account | **Page:** Customers > [Customer Configuration](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html)<br/>**Section:** Create New Account Options<br/>**Field:** Default Welcome Email|
| New Account (Magento/luma) | **Page:** Customers > [Customer Configuration](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html)<br/>**Section:** Create New Account Options<br/>**Field:** Default Welcome Email |
| New Account Confirmation Key | **Page:** Customers > [Customer Configuration](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html)<br/>**Section:** Create New Account Options<br/>**Field:** Confirmation Link Email |
| New Account Confirmed | **Page:** Customers > [Customer Configuration](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html)<br/>**Section:** Create New Account Options<br/>**Field:** Welcome Email |
| New Account Without Password | **Page:** Customers > [Customer Configuration](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html)<br/>**Section:** Create New Account Options<br/>**Field:** Default Welcome Email Without Password |
| Remind Password | **Page:** Customers > [Customer Configuration](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html)<br/>**Section:** Password Options<br/>**Field:** Remind Email Template |
| Reset Password | **Page:** Customers > [Customer Configuration](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html)<br/>**Section:** Password Options <br/>**Field:** Reset Password Template |

{style="table-layout:auto"}

### Magento_CustomerBalance

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)

|Template|Configuration path|
|--- |--- |
| Store Credit Update | **Page:** Customers > [Customer Configuration](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html)<br/>**Section:** Store Credit Options<br/>**Field:** Store Credit Update Email Template |

{style="table-layout:auto"}

### Magento_Directory

|Template|Configuration path|
|--- |--- |
| Currency Update Warnings | **Page:** General > [Currency Setup](https://docs.magento.com/user-guide/configuration/general/currency-setup.html)<br/>**Section:** Scheduled Import Settings<br/>**Field:** Error Email Template |

{style="table-layout:auto"}

### Magento_Email

|Template|Configuration path|
|--- |--- |
| Footer | n/a |
| Footer (Magento/luma) | n/a |
| Header | n/a |

{style="table-layout:auto"}

### Magento_GiftCard

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)

|Template|Configuration path|
|--- |--- |
| Gift Card(s) Purchase | **Page:** Sales > [Gift Cards](../catalog/product-gift-card-create.md)<br/>**Section:** Gift Card Email Settings<br/>**Field:** Gift Card Notification Email Template |

{style="table-layout:auto"}

### Magento_GiftCardAccount

|Template|Configuration path|
|--- |--- |
| Gift Card Code/Balance | **Page:** Sales > [Gift Cards](../catalog/product-gift-card-create.md)<br/>**Section:** Email Sent from Gift Card Account Management<br/>**Field:** Gift Card Template |

{style="table-layout:auto"}

### Magento_GiftRegistry

|Template|Configuration path|
|--- |--- |
| New Registry | **Page:** Customers > [Gift Registry](https://docs.magento.com/user-guide/configuration/customers/gift-registry.html) <br/>**Section:** Owner Notification<br/>**Field:** Email Template |
| Registry Sharing | **Page:** Customers > [Gift Registry](https://docs.magento.com/user-guide/configuration/customers/gift-registry.html) <br/>**Section:** Gift Registry Sharing<br/>**Field:** Email Template |
| Registry Update | **Page:** Customers > [Gift Registry](https://docs.magento.com/user-guide/configuration/customers/gift-registry.html) <br/>**Section:** Gift Registry Update<br/>**Field:** Email Template |

{style="table-layout:auto"}

### Magento_InventoryInStorePickupSales

|Template|Configuration path|
|--- |--- |
| Order is Ready for Pickup | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Order Ready For Pickup in Store<br/>**Field:** Order Ready For Pickup Email Template |
| Order is Ready for Pickup For Guest | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Order Ready For Pickup in Store<br/>**Field:** Order Ready For Pickup Email Template for Guest|

{style="table-layout:auto"}

### Magento_Invitation

|Template|Configuration path|
|--- |--- |
| Customer Invitation | **Page:** Customers > [Invitation](https://docs.magento.com/user-guide/configuration/customers/invitations.html)<br/>**Section:** Email<br/>**Field:** Customer Invitation Email Template |

{style="table-layout:auto"}

### Magento_NegotiableQuote

![B2B for Adobe Commerce](../assets/b2b.svg) (Available with B2B for Adobe Commerce only)

|Template|Configuration path|
|--- |--- |
| Declined Quote | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Quote<br/>**Field:** Declined Quote Template (to Buyer) |
| Expiration Date Reset | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Quote<br/>**Field:** Expiration Date Reset| **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Quote<br/>**Field:** Order Ready For Pickup Email Template |
| Expiration Warning | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Quote<br/>**Field:** Quote Expiration (in 48 hrs) |
| Expiration Warning1 | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Quote<br/>**Field:** Quote Expiration (in 24 hrs) |
| New Quote | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Quote<br/>**Field:** New Quote Template (to Seller) |
| Updated Quote | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Quote<br/>**Field:** Updated Quote Template (to Seller) |

{style="table-layout:auto"}

### Magento_Newsletter

|Template|Configuration path|
|--- |--- |
| Subscription Confirmation | **Page:** Customers > [Newsletter](https://docs.magento.com/user-guide/configuration/customers/newsletter.html)<br/>**Section:** Subscription Options<br/>**Field:** Confirmation Email Template |
| Subscription Success | **Page:** Customers > [Newsletter](https://docs.magento.com/user-guide/configuration/customers/newsletter.html)<br/>**Section:** Subscription Options<br/>**Field:** Success Email Template |
| Unsubscription Success | **Page:** Customers > [Newsletter](https://docs.magento.com/user-guide/configuration/customers/newsletter.html)<br/>**Section:** Subscription Options<br/>**Field:** Unsubscription Email Template |

{style="table-layout:auto"}

### Magento_ProductAlert

|Template|Configuration path|
|--- |--- |
| Cron Error Warning | **Page:** Catalog > [Catalog](https://docs.magento.com/user-guide/configuration/catalog/catalog.html)<br/>**Section:** Product Alerts Run Settings<br/>**Field:** Error Email Template |
| Price Alert | **Page:** Catalog > [Catalog](https://docs.magento.com/user-guide/configuration/catalog/catalog.html)<br/>**Section:** Product Alerts<br/>**Field:** Price Alert Email Template |
| Stock Alert | **Page:** Catalog > [Catalog](https://docs.magento.com/user-guide/configuration/catalog/catalog.html)<br/>**Section:** Product Alerts<br/>**Field:** Stock Alert Email Template |

{style="table-layout:auto"}

### Magento_PurchaseOrder

|Template|Configuration path|
|--- |--- |
|Approved Purchase Order|**Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Purchase Order Approval<br/>**Field:** Approved Purchase Order |
|Approved, requires payment|**Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Purchase Order Approval<br/>**Field:** Approved, requires payment details (to Buyer) |
|Comment added to Purchase Order|**Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Purchase Order Approval<br/>**Field:** Comment added to Purchase Order |
|Created and Auto-approved Purchase Order|**Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Purchase Order Approval<br/>**Field:** Created and Automatically approved Purchase Order (to Buyer) |
|Created and automatically approved, requires payment details|**Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Purchase Order Approval<br/>**Field:** Created and automatically approved, requires payment details (to Buyer) |
|Created and requires Approval Purchase Order|**Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Purchase Order Approval<br/>**Field:** Created and requires Approval Purchase Order (to Buyer) |
|Error creating Order from Purchase Order|**Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Purchase Order Approval<br/>**Field:** Error creating Order from Purchase Order (to Buyer) |
|Purchase Order requires Approval|**Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Purchase Order Approval<br/>**Field:** Purchase Order requires Approval (to Approver) |
|Rejected Purchase Order|**Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** Purchase Order Approval<br/>**Field:** Rejected Purchase Order (to Buyer) |

{style="table-layout:auto"}

### Magento_Reminder

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)

|Template|Configuration path|
|--- |--- |
| Promotion Notification/Reminder | **Page:** Customers > [Promotions](https://docs.magento.com/user-guide/configuration/customers/promotions.html)<br/>**Section:** Automated Email Reminder Rules<br/>**Field:** Reminder Email Sender|

{style="table-layout:auto"}

### Magento_Reward

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)

|Template|Configuration path|
|--- |--- |
| Balance Update | **Page:** Customers > [Reward Points](https://docs.magento.com/user-guide/configuration/customers/reward-points.html)<br/>**Section:** Email Notification Settings<br/>**Field:** Balance Update Email |
| Points Expiry Warning | **Page:** Customers > [Reward Points](https://docs.magento.com/user-guide/configuration/customers/reward-points.html)<br/>**Section:** Email Notification Settings<br/>**Field:** Reward Points Expiry Warning Email |

{style="table-layout:auto"}

### Magento_Rma

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)

|Template|Configuration path|
|--- |--- |
| New RMA | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** RMA<br/>**Field:** RMA Email Template |
| New RMA for Guest | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** RMA<br/>**Field:** RMA Email Template for Guest |
| RMA Admin Comments | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** RMA Admin Comments<br/>**Field:** RMA Comment Email Template |
| RMA Admin Comments for Guest | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** RMA Admin Comments<br/>**Field:** RMA Comment Email Template for Guest |
| RMA Authorization | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** RMA Authorization<br/>**Field:** RMA Authorization Email Template |
| RMA Authorization for Guest | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** RMA Authorization<br/>**Field:** RMA Authorization Email Template for Guest |
| RMA Customer Comments | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) <br/>**Section:** RMA Customer Comments<br/>**Field:** RMA Comment Email Template |

{style="table-layout:auto"}

### Magento_Sales

|Template|Configuration path|
|--- |--- |
| Credit Memo Update | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Credit Memo Contents<br/>**Field:** Credit Memo Comment Email Template |
| Credit Memo Update (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Credit Memo Comments<br/>**Field:** Credit Memo Comment Email Template |
| Credit Memo Update for Guest | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Credit Memo Comments<br/>**Field:** Credit Memo Comment Email Template for Guest |
| Credit Memo Update for Guest (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Credit Memo Comments<br/>**Field:** Credit Memo Comment Email Template for Guest |
| Invoice Update | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Invoice Comments<br/>**Field:** Invoice Comment Email Template |
| Invoice Update (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Invoice Comments<br/>**Field:** Invoice Comment Email Template |
| Invoice Update for Guest | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Invoice Comments<br/>**Field:** Invoice Comment Email Template for Guest |
| Invoice Update for Guest (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Invoice Comments<br/>**Field:** Invoice Comment Email Template for Guest |
| New Credit Memo | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Credit Memo<br/>**Field:** Credit Memo Email Template |
| New Credit Memo (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Credit Memo<br/>**Field:** Credit Memo Email Template |
| New Credit Memo for Guest | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Credit Memo<br/>**Field:** Credit Memo Email Template for Guest |
| New Credit Memo for Guest (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Credit Memo<br/>**Field:** Credit Memo Email Template for Guest |
| New Invoice | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Invoice<br/>**Field:** Invoice Email Template |
| New Invoice (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Invoice<br/>**Field:** Invoice Email Template |
| New Invoice for Guest | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Invoice<br/>**Field:** Invoice Email Template for Guest |
| New Invoice for Guest (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Invoice<br/>**Field:** Invoice Email Template for Guest |
| New Order | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Order<br/>**Field:** New Order Confirmation Template |
| New Order (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Order<br/>**Field:** New Order Confirmation Template |
| New Order for Guest | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Order<br/>**Field:** New Order Confirmation Template for Guest |
| New Order for Guest (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Order<br/>**Field:** New Order Confirmation Template for Guest |
| New Shipment | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Shipment<br/>**Field:** Shipment Email Template |
| New Shipment (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Shipment<br/>**Field:** Shipment Email Template |
| New Shipment for Guest | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Shipment<br/>**Field:** Shipment Email Template for Guest |
| New Shipment for Guest (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Shipment<br/>**Field:** Shipment Email Template for Guest |
| Order Update | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Order Comments<br/>**Field:** Order Comment Email Template |
| Order Update (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Order Comments<br/>**Field:** Order Comment Email Template |
| Order Update for Guest | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Order Comments<br/>**Field:** Order Comment Email Template for Guest |
| Order Update for Guest (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Order Comments<br/>**Field:** Order Comment Email Template for Guest |
| Shipment Update | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Shipment Comments<br/>**Field:** Shipment Comment Email Template |
| Shipment Update (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Shipment Comments<br/>**Field:** Shipment Comment Email Template |
| Shipment Update for Guest | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Shipment Comments<br/>**Field:** Shipment Comment Email Template for Guest |
| Shipment Update for Guest (Magento/luma) | **Page:** Sales > [Sales Emails](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)<br/>**Section:** Shipment Comments<br/>**Field:** Shipment Comment Email Template for Guest |

{style="table-layout:auto"}

### Magento_ScheduledImportExport

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)

|Template|Configuration path|
|--- |--- |
| Export Failed | **Page:** Advanced > [System](https://docs.magento.com/user-guide/configuration/advanced/system.html)<br/>**Section:** Scheduled Import/Export File History Cleaning<br/>**Field:** Export Failed Template |
| File History Clean Failed | **Page:** Advanced > [System](https://docs.magento.com/user-guide/configuration/advanced/system.html)<br/>**Section:** Scheduled Import/Export File History Cleaning<br/>**Field:** Error Email Template |
| Import Failed | **Page:** Advanced > [System](https://docs.magento.com/user-guide/configuration/advanced/system.html)<br/>**Section:** Scheduled Import/Export File History Cleaning<br/>**Field:** Import Failed Template |

{style="table-layout:auto"}

### Magento_SendFriend

|Template|Configuration path|
|--- |--- |
| Send Product Link to Friend | **Page:** Catalog > [Email to a Friend](https://docs.magento.com/user-guide/configuration/catalog/email-to-a-friend.html)<br/>**Section:** Email Templates<br/>**Field:** Select Email Template |

{style="table-layout:auto"}

### Magento_Sitemap

|Template|Configuration path|
|--- |--- |
| Sitemap Generation  Settings | **Page:** Catalog > [XML Sitemap](https://docs.magento.com/user-guide/configuration/catalog/xml-sitemap.html)<br/>**Section:** Generation Settings<br/>**Field:** Error Email Template |

{style="table-layout:auto"}

### Magento_TwoFactorAuth

|Template|Configuration path|
|--- |--- |
|2FA Configuration Required by User| n/a |
|2FA Configuration Required for the Application| n/a |

{style="table-layout:auto"}

### Magento_User

|Template|Configuration path|
|--- |--- |
| Forgot Admin Password | **Page:** Advanced > [Admin](https://docs.magento.com/user-guide/configuration/advanced/admin.html)<br/>**Section:** Admin User Emails<br/>**Field:** Forgot Password Email Template |
| User Notification | **Page:** Advanced > [Admin](https://docs.magento.com/user-guide/configuration/advanced/admin.html)<br/>**Section:** Admin User Emails<br/>**Field:** User Notification Template |
| New User Notification | **Page:** Advanced > [Admin](https://docs.magento.com/user-guide/configuration/advanced/admin.html)<br/>**Section:** Admin User Emails<br/>**Field:** New User Notification Template |

{style="table-layout:auto"}

### Magento_Wishlist

|Template|Configuration path|
|--- |--- |
| Magento Wish List Sharing | **Page:** Customers > [Wish List](https://docs.magento.com/user-guide/configuration/customers/wishlist.html)<br/>**Section:** Share Options<br/>**Field:** Email Template |

{style="table-layout:auto"}
