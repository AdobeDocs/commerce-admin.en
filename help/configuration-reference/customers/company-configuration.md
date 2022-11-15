---
title: Company Configuration
description: Placeholder
---
# Customers > Company Configuration

{{b2b-feature}}

{{config}}

>[!TIP]
>
>With the installation and enablement of B2B for Adobe Commerce, the buying experience can be personalized with company-specific features. B2B for Adobe Commerce is an integrated solution that provides support for both B2B and B2C models. For more information about the B2B features, see the [B2B for Adobe Commerce User Guide](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

>[!NOTE]
>
>Access to these configuration options for B2B features are controlled by the [role resources](../systems/permissions-user-roles.md#role-resources). These role resources must be set for the user role assigned to the Admin user.

## General

![General](./assets/company-general.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Allow Company Registration from the Storefront|Website|Determines if visitors to your store have the choice to [register](https://docs.magento.com/user-guide/customers/to.com/user-guide/customers/customer-sign-in.html) for a company account or an individual account. Options: `Yes` / `No`|

## Email Options - Company Registration

![Email Options - Company Registration](./assets/company-email-options-company-registration.png)<!-- zoom -->

<!-- Email Options - Company Registration](https://docs.magento.com/user-guide/customers/to.com/user-guide/customers/customer-sign-in.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Company Registration Email Recipient|Store View|The [store contact](https://docs.magento.com/user-guide/stores/store-email-addresses.html) that is notified when a company registration request is submitted from the storefront. Options: General Contact, [Sales Representative](https://docs.magento.com/user-guide/customers/to.com/user-guide/customers/account-company-sales-representative.html), Customer Support, Custom Email 1, Custom Email 2|
|Send Company Registration Email Copy To|Store View|The email address of each person who is to receive a copy of the registration notification. Separate multiple email addresses with a comma.|
|Send Email Copy Method|Store View|The email method that is used to send the copy of the registration email. Options: Bcc, Separate Email|
|Default Company Registration Email|Store View|The email template that is used by default for the company registration notification. Default template: Company Registration Request|

## Customer-Related Emails

![Customer-Related Emails](./assets/company-email-options-customer-related-emails.png)<!-- zoom -->

<!-- Customer-Related Emails](https://docs.magento.com/user-guide/marketing/email-company-configuration.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Default 'Sales Rep Assigned' Email|Store View|The email template that is used by default when a sales representative is assigned to a company account. This email is sent to the sales representative and to the company administrator. Default template: Sales Representative Assigned to Company|
|Default 'Assign Company to Customer' Email|Store View|The email template that is used by default when an individual customer account is assigned to a company account. This email is sent to the customer only. Default template: Assign Company to Customer|
|Default 'Assign Company Admin' Email|Store View|The email template that is used when a company administrator is assigned to a company. This email is sent to the sales representative and to the company administrator. Default template: Assign Company Admin|
|Default 'Company Admin Inactive' Email|Store View|The email template that is used by default when the status of the person who serves as the company administrator is changed to "Inactive". The system sends email notification of the change to the new and former company administrators. Default template: Company Admin Set Inactive|
|Default 'Company Admin Changed to Member' Email|Store View|The email template that is used by default when the former company administrator becomes a company member. The email is sent to the company member only. Default template: Company Admin Changed to Member|
|Default 'Customer Status Active' Email|Store View|The email template that is used by default when the status of a customer becomes active. This email is sent to the customer only. Default template: Customer Status Active|
|Default 'Customer Status Inactive' Email|Store View|The email template that is used by default when the status of a customer becomes inactive. This email is sent to the customer only. Default template: Customer Status Inactive|

## Company Status Change

![Company Status Change](./assets/company-email-options-company-status-change.png)<!-- zoom -->

<!-- Company Status Change](https://docs.magento.com/user-guide/customers/to.com/user-guide/customers/account-company-manage.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Company Status Change Email Recipient|Store View|The [store contact](https://docs.magento.com/user-guide/stores/store-email-addresses.html) that is notified whenever the status of a company changes. Options: General Contact, [Sales Representative](https://docs.magento.com/user-guide/customers/to.com/user-guide/customers/account-company-sales-representative.html), Customer Support, Custom Email 1, Custom Email 2|
|Send Company Status Change Email Copy To|Store View|The email address of each person who is to receive a copy of the company status change notification. Separate multiple email addresses with a comma.|
|Send Email Copy Method|Store View|The email method that is used to send the copy of the status change notification. Options: Bcc, Separate Email|
|Default "Company Status Change to Active 1' Email|Store View|The email template that is used when the status of a company changes from "Pending Approval" to "Active". Default template: Company Status Active 1|
|Default 'Company Status Change to Active 2' Email|Store View|The email template that is used by default when the status of a company changes from "Rejected" or "Blocked" to "Active". Default template: Company Status Active 2|
|Default 'Company Status Change to Rejected' Email|Store View|The email template that is used by default when the status of a company changes to "Rejected". Default template: Company Status Rejected|
|Default 'Company Status Change to Blocked' Email|Store View|The email template that is used by default when the status of a company changes to "Blocked". Default template: Company Status Blocked|
|Default 'Company Status Change to Pending Approval' Email|Store View|The email template that is used by default when the status of a company changes to "Pending Approval". Default template: Company Status Pending Approval|

## Company Credit

![Company Credit](./assets/company-email-options-company-credit.png)<!-- zoom -->

<!-- Company Credit](https://docs.magento.com/user-guide/customers/to.com/user-guide/customers/account-dashboard-company-credit.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Company Credit Change Email Sender|Store View|The [store contact](https://docs.magento.com/user-guide/stores/store-email-addresses.html) that is notified whenever there is a change to a company's credit. Options: General Contact, [Sales Representative](https://docs.magento.com/user-guide/customers/to.com/user-guide/customers/account-company-sales-representative.html), Customer Support, Custom Email 1, Custom Email 2|
|Send Company Credit Change Email Copy To|Store View|The email address of each person who is to receive a copy of the company credit change notification. Separate multiple email addresses with a comma.|
|Send Email Copy Method|Store View|The email method that is used to send the copy of the credit change notification. Options: Bcc, Separate Email|
|Allocated Email Template|Store View|The email template that is used by default when company credit is allocated. This email is sent to the company administrator. Default template: Credit Limit Allocated|
|Updated Email Template|Store View|The email template that is used by default when a company's credit limit is updated. This email is sent to the company administrator. Default template: Credit Limit Updated|
|Reimbursed Email Template|Store View|The email template that is used by default when a [reimbursement](https://docs.magento.com/user-guide/customers/to.com/user-guide/customers/credit-company-reimburse.html) is made to company's credit. This email is sent to the company administrator. Default template: Credit Reimbursed|
|Refunded Email Template|Store View|The email template that is used by default when an amount from an order is refunded to company credit. This email is sent to the company administrator. Default template: Order Refunded to Company Credit|
|Reverted Email Template|Store View|The email template that is used by default when an order is reverted to company credit. This email is sent to the company administrator. Default template: Order Reverted to Company Credit|
