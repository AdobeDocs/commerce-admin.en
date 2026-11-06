---
title: Merchandising with composable catalog data model
description: Learn about merchandising features in [!DNL Adobe Commerce Optimizer].
recommendations: noCatalog
badgeSaas: label="SaaS only" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service and [!DNL Adobe Commerce Optimizer] projects only (Adobe-managed SaaS infrastructure)."
autotag-review: '2026-11-02T19:18:09.501Z'
TQID: 'https://experienceleague.adobe.com/LMKEDmMUyq3PHXG-xoCeBrkbN9yX71fE3ZkstDKTHjw'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: d3b92bef-63fa-5031-a925-d04d9362d616
    internal-label: Saas
  - id: dec06508-d41f-555a-87e8-29e8bcdfa95a
    internal-label: Recommendations
  - id: f37757d8-3174-5335-b977-1161792f965d
    internal-label: Personalization
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
---

# Merchandising Services with composable catalog data model

Learn how to create personalized experiences for your shoppers through product discovery and recommendations.

These merchandising services are built on the composable catalog data model (CCDM), which separates *product data* from *product context*. Product data includes SKUs, attributes, metadata, assets, and prices. Product context defines how that data is delivered, including [catalog views](../setup/catalog-view.md), [data access policies](../setup/policies.md), and [catalog sources](../setup/catalog-sources.md) (locales). Because the catalog view and its policies determine which product data is delivered to the storefront, you can compose custom catalogs for different business models, such as B2B, B2C, and D2C, and tailor the shopping experience for each without duplicating the base catalog data.

- **Product discovery**—Equips merchandisers with powerful tools to curate and optimize the shopping experience, ensuring that customers find the right products quickly, at the right time. By fine-tuning search behavior, you can directly influence product visibility, relevance, and conversion.

  With product discovery, you can guide shoppers toward the most relevant products with minimal friction by configuring:

  - [**Merchandising rules**](rules/overview.md)—Boost, bury, pin, or filter products in search results, default product listings, and category pages.
  - [**Facets**](facets/overview.md)—Configure the filters shoppers use to narrow search and category results.
  - [**Synonyms**](synonyms/overview.md)—Map equivalent terms so different search words return the same products.

  [Semantic search](../setup/semantic-search.md), which is enabled by default in [Settings](../settings.md), improves relevance for natural-language and intent-based queries. In Settings, you can also configure price facets, catalog language, and advanced semantic and fuzzy search options.

- [**Recommendations**](recommendations/overview.md)—Use artificial intelligence and machine-learning algorithms to analyze aggregated visitor behavior and product interactions across your storefront. Combined with your catalog, this data delivers highly engaging, relevant, and personalized experiences. Recommendations are surfaced on the storefront as units with labels, such as "Customers who viewed this product also viewed". You can create, manage, and deploy recommendations directly from the Recommendations workspace and place them throughout the shopping journey to support promotional goals, cross-sell strategies, and personalized experiences.
