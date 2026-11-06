---
title: Get Started
description: Learn how to get started with [!DNL Adobe Commerce Optimizer].
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="SaaS only" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service and [!DNL Adobe Commerce Optimizer] projects only (Adobe-managed SaaS infrastructure)."
TQID: 'https://experienceleague.adobe.com/0PmobUkdEWspxuRSaIPL8vS1ojDDZ3gw-L-3SfPmJAg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
  - id: d3b92bef-63fa-5031-a925-d04d9362d616
    internal-label: Saas
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

# Get started with Merchandising Services

Merchandisers optimize and personalize the shopping experience through product discovery and recommendations. They also use shopper data and analytics to make strategic decisions about product placement, pricing, and promotions on the storefront.

Developers handle technical implementation and data integration, including platform architecture tasks. For Adobe Commerce as a Cloud Service with the composable catalog data model, the catalog setup tasks are done in Adobe Commerce.

| Task | Description | Link |
| --- | --- | --- |
| **Configure products and prices** | Configure products and prices in Adobe Commerce. Pricing data is mapped to price books when data is synced to Merchandising Services. See [Base catalog mapping](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview#base-catalog-mapping{target=_blank}) to understand how catalog data is mapped. | Manage products: [Products list](../catalog/products-list.md), [Product workspace](../catalog/product-workspace.md), and [Create a product](../catalog/product-create.md). Manage pricing: [Price scope](../catalog/catalog-price-scope.md), [Advanced pricing](../catalog/pricing-advanced.md), [Group pricing](../catalog/product-price-group.md), [Special prices](../catalog/product-price-special.md), and [Tier pricing](../catalog/product-price-tier.md). Sync: [Adobe Commerce Optimizer Connector](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview) |
| **Configure catalogs** | Configure store views in Adobe Commerce. Store views are mapped to catalog sources when data is synced to Merchandising Services, and each catalog source includes the localized product attributes and any store-view-specific data. | [Catalog sources](./setup/catalog-sources.md) |
| **Configure catalog views** | Create catalog views that combine catalog sources, policies, and price books for each brand, region, business unit, or channel. From the catalog view, define the catalog layers that modify product data without changing the source data. Optionally, restrict a catalog view to make it private. | [Catalog views](./setup/catalog-view.md), [Catalog layers](./setup/catalog-layer.md), and [Private catalog views](./setup/private-catalog-view.md) |
| **Configure policies** | Define the data access filters that control which products each catalog view delivers | [Policies](./setup/policies.md) |
| **Set up B2B catalogs and accounts** | For B2B, set up shared catalogs and configure companies and company accounts | [Shared catalogs](../b2b/catalog-shared.md) and [Companies](../b2b/account-companies.md) |
| **Set Up the Storefront** | Configure Edge Delivery Services storefront | [Storefront Setup](./storefront.md) |

| Task | Description | Link |
| --- | --- | --- |
| **Product Discovery** | Configure search and filtering | [Merchandising Overview](./merchandising/overview.md) |
| **Search settings** | Manage semantic search (enabled by default) and optional tuning | [Settings — Advanced search](./settings.md#advanced-search) and [Semantic search](./setup/semantic-search.md) |
| **Recommendations** | Set up AI-powered product recommendations | [Product Recommendations](./merchandising/recommendations/overview.md) |
| **Performance Tracking** | Monitor success metrics and search performance | [Success Metrics](./manage-results/success-metrics.md) and [Search Performance](./manage-results/search-performance.md) |

