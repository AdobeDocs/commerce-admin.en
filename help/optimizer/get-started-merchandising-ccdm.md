---
title: Merchandising Services Tasks by Role
description: Find task guidance for administrators, developers, and merchandisers working with Adobe Commerce as a Cloud Service instances provisioned with CCDM.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="SaaS only" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service instances provisioned with CCDM only (Adobe-managed SaaS infrastructure)."
TQID: 'https://experienceleague.adobe.com/0PmobUkdEWspxuRSaIPL8vS1ojDDZ3gw-L-3SfPmJAg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
  - id: dec06508-d41f-555a-87e8-29e8bcdfa95a
    internal-label: Recommendations
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
  - id: f37757d8-3174-5335-b977-1161792f965d
    internal-label: Personalization
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
    internal-label: Data and analytics
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---

# Merchandising Services tasks by role

Use this task reference to find guidance for configuring catalog data, integrating the storefront, managing merchandising, and reviewing performance in Adobe Commerce as a Cloud Service instances provisioned with the Composable Catalog Data Model (CCDM).

Responsibilities vary by implementation. The following sections group tasks by the roles that typically perform them.

- Administrators manage products, prices, and B2B configuration in Commerce Foundation.
- Developers configure the storefront integration and verify catalog requests and behavioral-data collection.
- Merchandisers configure product discovery and recommendations and use reporting to inform merchandising decisions.

Product and price data synchronize to CCDM through native Adobe Commerce as a Cloud Service integration. No separate connector installation or App Builder app is required.

## Prepare the catalog and storefront

Complete the tasks that apply to your implementation. B2C catalog views can be created manually. B2B catalog views, policies, and price books are generated from the B2B configuration in Commerce Foundation.

| Task | Description | Resources |
| --- | --- | --- |
| **Configure products and prices** | Manage products and prices in Commerce Foundation. Pricing data synchronizes to CCDM as price books; do not independently author prices in CCDM. | [Products list](../catalog/products-list.md), [Create a product](../catalog/product-create.md), [Price scope](../catalog/catalog-price-scope.md), and [Advanced pricing](../catalog/pricing-advanced.md) |
| **Configure store views** | Configure the store views and localized product data required for your storefront in Commerce Foundation. | [Store views](../stores-purchase/store-views.md) |
| **Set up B2B shared catalogs and companies** | For B2B implementations, configure shared catalogs and company relationships in Commerce Foundation before reviewing the generated catalog configuration. | [Shared catalogs](../b2b/catalog-shared.md) and [Companies](../b2b/account-companies.md) |
| **Configure B2C catalog views and policies** | Create catalog views and select the policies that define the available product assortment. Associate the applicable synchronized price books with each view. | [Catalog views](./setup/catalog-view.md) |
| **Review B2B catalog views** | Confirm that native synchronization has generated the expected catalog views, policies, and price books. Manage the underlying B2B configuration in Commerce Foundation rather than creating duplicate structures manually. | [B2B catalog views](./setup/catalog-view.md#b2b-catalog-views) |
| **Configure the storefront** | Configure the storefront to request the intended catalog context. For custom or other storefront integrations, review the applicable catalog request headers. | [Storefront configuration](https://experienceleague.adobe.com/en/tools/commerce-storefront/setup/configuration/commerce-configuration/) |

Before configuring merchandising, confirm that the storefront returns the expected products and prices. Test add-to-cart, cart, and checkout to verify that transaction pricing matches the intended Commerce Foundation configuration.

## Configure merchandising and review performance

| Task | Description | Resources |
| --- | --- | --- |
| **Configure product discovery** | Set up merchandising rules, facets, and synonyms. Rules can apply across all catalog views or be tailored to a specific view. | [Merchandising overview](./merchandising/overview.md) |
| **Review search settings** | Review the search configuration and available semantic-search options for your implementation. | [Merchandising settings](./settings.md) and [Semantic search](./setup/semantic-search.md) |
| **Configure recommendations** | Create recommendation units and verify that the storefront collects the behavioral data required by the implementation. | [Recommendations overview](./merchandising/recommendations/overview.md) |
| **Review performance** | Use Success Metrics and search performance reporting to evaluate storefront activity and inform merchandising decisions. | [Success Metrics](./manage-results/success-metrics.md) and [Search performance](./manage-results/search-performance.md) |

## Next steps

After configuring merchandising and reviewing performance, continue to monitor and adjust your rules, facets, and recommendations as needed to optimize the storefront experience.
