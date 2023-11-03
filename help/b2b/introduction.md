---
title: Introduction to [!DNL B2B for Adobe Commerce]
description: Learn how to use integrated B2B features to meet your needs for customers that are companies.
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
---
# Introduction to [!DNL B2B for Adobe Commerce]

Unlike the standard business-to-consumer model, integrated B2B (Business to Business) features are designed to meet the needs of sellers (Adobe Commerce merchants) who have customers that are companies. It accommodates companies with complex organizational structures and multiple users with various roles and levels of purchasing permission. A typical B2B customer might be the manager of a retail store, or a buyer that makes purchases on behalf of a company. In both cases, the transaction takes place between your business and theirs. You might also sell products direct to the consumer. [!DNL B2B for Adobe Commerce] is an integrated solution that provides support for both B2B and B2C models.

With the [installation](install.md) and [enablement](enable-basic-features.md) of the B2B extension in your Adobe Commerce store, the buying experience can be personalized with customer-specific catalogs and pricing, and targeted content and promotions.

## Company accounts

The Company account feature is a key entity within B2B on which all other features are in some way dependent. It allows joining multiple buyers that belong within a single company into a single company account (or corporate account). The company administrator is able to build this hierarchical company structure (divisions, subdivisions, and users) in the appropriate hierarchy and provide different user roles and permissions to the company members. This hierarchy allows the company administrator to control user activity for the company account: ordering, quoting, purchasing, access to company credit information or profile, and so on. A seller can configure how the buying company operates on the website, including the payment methods, pricing levels, the ability to negotiate prices, and the ability to create requisition lists.

This company structure is an excellent opportunity to improve the performance of a company.

For more information, see [Company Accounts](account-companies.md).

>[!NOTE]
>
>When enabled, your store can give companies the option to _Pay on Account_, which means to make purchases on a company credit line. As the merchant, you can allocate credit for a company account and manage credit settings for a company, and credit reimbursement.

## Company management

Company management helps companies with complex organizational structures to set a [!UICONTROL Company Hierarchy].

**[!UICONTROL Company Hierarchy]** allows Commerce B2B admin users with the appropriate permissions to create a parent company and assign companies, then this parent company administrator can manage the company accounts for the parent and all assigned companies.

For more information, see [Company Management](manage-companies.md).

## Services for Adobe Commerce

Services for Adobe Commerce are hosted services that provide extended capabilities to Adobe Commerce and Magento Open Source. Services that support B2B workflows are:

* [Catalog Service](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html)
* [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)
* [Product Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)

## Shared catalogs

Shared catalogs are the pricing levels that allow setting custom prices per product for different companies on one or multiple websites. By using shared catalogs, you can sell products by applying different pricing levels for different customer groups. Support for Shared catalogs is available only for Commerce stores configured to support Company accounts.

For more information, see [Working with Shared Catalogs](catalog-shared.md).

## Quick Order

Configure Quick Order to reduce the order process to several clicks for logged in customers when they know the product name or SKU of the products they want to order.

For more information, see [Quick Orders](quick-order.md).

## Negotiable Quotes

Use the Quotes feature to initiate price negotiation between a company buyer and seller.

* An authorized buyer can initiate a quote from the shopping cart.

* A seller can initiate a quote for a buyer from Admin.

Buyers and sellers use the quote to manage the negotiation process–such as adding items, updating quantities, requesting and applying discounts—until they reach an agreement. The _Quotes_ grid in the Admin lists each quote received, and maintains a history of the communication between buyer and seller.

Support for Negotiable Quotes is available only for Commerce stores configured to support Company accounts.

For more information, see [Negotiable Quotes](quotes.md).

## Purchase order approvals

When Purchase Orders are activated for a company account, all orders are automatically created as Purchase Orders (PO). Company users with the required permissions can create, edit, and delete POs that they create and POs created by subordinate users. Depending on their role, and the order, company users could be subjected to several approval rules.

For more information, see [Purchase Orders for Companies](purchase-order-flow.md).

## Requisition lists

Customers can use requisition list to save time when purchasing frequently ordered products because they can add items to the shopping cart directly from the list. They can maintain multiple lists that focus on products from different vendors, buyers, teams, campaigns, or anything else that streamlines their workflow.

For more information, see [Requisition Lists](requisition-lists.md).
