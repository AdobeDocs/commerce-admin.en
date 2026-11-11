---
title: Price Books
description:  "Learn how price books are mapped from catalog and pricing data in [!DNL Adobe Commerce]."
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="SaaS only" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service and [!DNL Adobe Commerce Optimizer] projects only (Adobe-managed SaaS infrastructure)."
TQID: 'https://experienceleague.adobe.com/8gpl-l6oQebTnrt-00-n1FEdKnzqhTQi3hRz4lrGQoE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 3033d2ab-c1d2-5b52-b865-72d9e5ad2c37
    internal-label: Currency
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
---
# Price books

Price books define product prices for a catalog source across customer tiers and markets. They support a hierarchy of parent and child price books.

![Price Book Hierarchy](../assets/price-book-hier.png)

## Key concepts

| Term | Description |
| ------ | ------------- |
| **Price Book** | Logical grouping that defines prices for a catalog source; for example, specific region, or customer tier and is used to manage product prices. |
| **Fallback Price Book** | The top-most price book in a hierarchy. It has no parent and is the *only* price book that defines the currency for itself and all its descendant price books.<br/><br/>If no parent is defined during price book creation (through the API), a new fallback price book is created. |
| **Parent Price Book** | A higher-level price book from which a child price book can inherit prices if they are not explicitly set in the child. |
| **Hierarchy Depth** | Maximum of three levels (Fallback -> Child -> Grandchild)<br/><br/>not enforced at ingestion time. |
| **Currency** | Defined for the fallback price book only. Inherited by all child price books.<br/><br/>If currency is not specified during fallback price book creation (through the API) the currency defaults to USD. |
| **Product Price** | The specific price assigned to a product (SKU) within a particular price book. |
| **Discounts** | Discounts are defined in product price. Not inherited. |

## Price book implementation

When using Adobe Commerce as a Cloud Service with the composable catalog data model (CCDM), price books are mapped from catalog and pricing data. They are not manually created.

At a high level, the mapping is:

- **Store view → Catalog source**—Store-view product data, including localized attributes, maps to a catalog source.
- **Website → Price book or price books**—Website pricing maps to the applicable price book or books.
- **Customer-group pricing → Price book entries**—Customer-group pricing maps to the relevant price entries.

Maintain the source catalog, website, and pricing configuration in the Adobe Commerce configuration, then assign the mapped price books in the relevant catalog view by configuring available price books. If no price books are assigned, the catalog view uses the default price book.

A catalog view uses the available price books configuration with its catalog data and policies to determine the merchandising experience, including the prices returned for products.

>[!NOTE]
>
>For Commerce B2B, the system creates and assigns a single price book to each catalog view based on the shared catalog configuration. You do not need to configure price book availability for these views.

## Checkout pricing

Price books support the merchandising and storefront catalog experience. Commerce Core continues to handle cart and checkout. A price available only in CCDM does not automatically become the price used by checkout.

Keep prices consistent with the Commerce Core configuration, and test displayed prices, add-to-cart, promotions, and checkout as part of implementation validation.

## View price books

After the catalog data sync completes, view the available price books and their IDs in the **[!UICONTROL Catalog views]** workspace.

1. Go to _Store setup_, and click **[!UICONTROL Catalog views]**.

1. Click **[!UICONTROL Create catalog view]**.

1. Review the available price books in the **[!UICONTROL Price Books]** section of the catalog view configuration.

   ![Price Book Names and IDs](../assets/price-book-name-ids.png)

## Configure price book availability

Associate mapped price books with catalog views by configuring available price books in the Catalog Views workspace in the Commerce Admin.

>[!NOTE]
>
>A private catalog view (one with [!UICONTROL Catalog Protection] enabled) can reference only one price book.

1. From the **[!UICONTROL Catalog views]** workspace, select the catalog view you want to configure.

1. In the **[!UICONTROL Price Books]** section, select the price books available to stores backed by the catalog view.
