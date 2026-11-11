---
title: Merchandising Services Overview
description: Learn about catalog configuration, merchandising, reporting, and monitoring tools for Adobe Commerce as a Cloud Service instances provisioned with CCDM.
recommendations: noCatalog
badgeSaas: label="SaaS only" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service instances provisioned with CCDM only (Adobe-managed SaaS infrastructure)."
exl-id: f9516d4c-fbae-4db2-a1a9-cda3684a8122
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Merchandising Services overview

Adobe Commerce as a Cloud Service instances provisioned with the Composable Catalog Data Model (CCDM) provide catalog configuration, merchandising, reporting, and monitoring tools in [Commerce Admin in Adobe Unified Experience](../getting-started/admin-unified-experience.md). CCDM is the same catalog foundation that powers Adobe Commerce Optimizer.

With Merchandising Services, you can:

- Use catalog data from your Adobe Commerce as a Cloud Service instance to support storefront experiences.
- Configure catalog views and policies to define storefront product assortments.
- Apply merchandising rules across all catalog views or tailor them to a specific view.
- Configure product recommendations, search facets, and synonyms.
- Review storefront performance through Success Metrics and search performance reporting.
- Monitor catalog synchronization and captured storefront events.

Commerce Foundation remains the source of truth for products and prices and continues to manage cart, checkout, and other transactional operations.

## Quick tour

>[!BEGINTABS]

>[!TAB Catalog configuration]

Configure the catalog context available to a storefront.

- **Catalog views**—Combine catalog sources, policies, and price books to define the products and pricing a storefront can retrieve. See [Catalog views](./setup/catalog-view.md).
- **Catalog layers**—Override selected product attributes without changing source data. When using AEM Assets for product images, the AEM-Assets layer is applied through Product Visuals. See [Catalog layers](./setup/catalog-layer.md).
- **Private catalog views**—Enable Catalog Protection to require a valid signed token when retrieving a catalog view's data. See [Private catalog views](./setup/private-catalog-view.md).

>[!TAB Policies]

Policies filter the products available through a catalog view based on product attributes. For example, a policy can limit an assortment to a particular brand or product category.

Policies determine the available product assortment. They do not replace Catalog Protection, which controls access to a private catalog view.

>[!TAB Merchandising]

Configure how shoppers discover products and how products are promoted within the available assortment.

- **Opportunities**—Review product performance, shopper behavior, and search trends to identify areas for merchandising improvements.
- **Recommendations**—Create and manage recommendation units in Commerce Admin. Recommendations use catalog data and aggregated shopper behavior to suggest relevant products, such as "Customers who viewed this product also viewed."
- **Merchandising rules**—Control how products are promoted and ranked. Rules can apply across all catalog views or be tailored to a specific view. See [Create a merchandising rule](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#create-a-rule).
- **Facets**—Configure the filters shoppers use to narrow product results by attributes such as brand, size, or price.
- **Synonyms**—Associate equivalent search terms to help shoppers find products using different words for the same concept.
- **Settings**—Configure search and merchandising options, including price facets, language, and advanced search.

Policies determine which products are available through a catalog view. Merchandising rules control how products within that assortment are promoted and ranked.

For details about how search results are matched and ranked, see [Search matching and ranking](./manage-results/search-relevance-matching.md).

>[!TAB Reports]

Use reports to review storefront activity and inform merchandising decisions.

- **Success Metrics**—Review revenue, conversion, engagement, acquisition, and bounce rate based on storefront activity.
- **Search performance**—Review the search terms shoppers use and their performance to identify areas for refining product discovery.

Reporting depends on the storefront activity data collected by the implementation.

>[!TAB System configuration]

Monitor catalog synchronization and storefront event collection to investigate data availability and implementation issues.

- **Catalog sync**—Review synchronization status for catalog data transferred from Commerce Foundation.
- **Events**—Review captured storefront events used by product discovery, recommendations, and reporting. Use the Events page to help verify behavioral-data collection and investigate missing or unexpected events.

>[!ENDTABS]
<!--
Watch the following video for a high-level overview of [!DNL Adobe Commerce Optimizer]:

>[!VIDEO](https://video.tv.adobe.com/v/3450226)
-->

## Confirm that an instance uses CCDM

1. Sign in to Commerce Admin through Unified Shell, and select the intended Adobe Commerce as a Cloud Service instance.
1. Confirm that CCDM merchandising pages, such as Catalog Views and Policies, are available in the instance's navigation.
1. If those pages are not available, confirm that you selected the correct instance and are using Unified Shell.

   Contact Adobe Support or the Commerce provisioning team to verify the instance's CCDM provisioning status.

The instance's Ready status confirms that it is provisioned, but does not by itself confirm that it uses CCDM.

