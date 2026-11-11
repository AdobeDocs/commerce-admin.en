---
title: Merchandising Services Limits and Boundaries
description: Learn about Adobe Commerce Optimizer license limits and system boundaries. Plan capacity, track usage, and avoid latency and throttling when limits are exceeded.
role: Admin, Developer
badgeSaas: label="SaaS only" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service and [!DNL Adobe Commerce Optimizer] projects only (Adobe-managed SaaS infrastructure)."
autotag-review: '2026-11-02T18:48:38.168Z'
TQID: 'https://experienceleague.adobe.com/KoRp--G2sMvv-Hr7KiHriZrFmtEm0BhGoGWVQQK-ofE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: d3b92bef-63fa-5031-a925-d04d9362d616
    internal-label: Saas
---

# Merchandising Services limits and boundaries with the composable catalog data model (CCDM)

Adobe Commerce Merchandising Services with CCDM applies license limits and system boundaries that define how much capacity your project can use:

- **License limits**—Based on your purchased capacity; can be expanded by purchasing additional packages.
- **System boundaries**—Fixed limits that protect system resources and ensure reliable performance for all users.

Your usage must stay within these limits. Exceeding them can cause increased latency and request throttling.

## Request additional capacity

License limits can be increased by purchasing the license packages described in the [License limits and system boundaries](#license-limits-and-system-boundaries) section, or by negotiating custom licensing for unique use cases. Contact your Adobe Account representative to discuss your requirements.

For questions about system boundaries, contact [Adobe Support](https://experienceleague.adobe.com/home?lang=en#support).

## Prevent performance issues

Follow these best practices to stay within limits and avoid operational issues:

- **Review your limits**—Understand your [capacity limits](#license-limits-and-system-boundaries) before launching new storefronts or campaigns.
- **Track your usage**—Use built-in metrics dashboards or CDN logs.

## License limits and system boundaries

The following tables summarize the license limits and system boundaries by capability area and include information about adding additional licenses to expand capacity where applicable.


### Catalog

| **Capability** | **Description** | **Base allocation** | **Expandable?** |
| --- | --- | --- | --- |
| Product ingestion rate | The number of products created or updated | 1K updates per minute<p>A maximum of 100K updates per day</p> | Yes<p>Add one license pack:</p><ul><li>5K updates per minute<br>A maximum of 500K updates per day</li> <li>10K updates per minute<br>A maximum of 1M updates per day</li></ul><p>The maximum capacity for data ingestion is 1M updates per day.</p> |
| Product payload size | The maximum amount of data allowed when creating, updating, or ingesting product information using the API | 200 KB | No |
| Catalog variations | The number of views of a catalog that are available to storefront users,<p>which are counted as (*Number of Catalog Views × Number of Price Books*)</p> | 100 variations | Yes<p>Add 100 catalog variations license pack</p> |
| Products in a single catalog source | SKUs supported in the catalog | 250K SKUs | Yes<p>Add 100K SKU license pack</p> |
| Variants per product | The number of product variants (size, color combinations) allowed per product | 10K | No |
| Catalog sources | The number of catalog data contexts (for example, locales or data sources like PIMs and ERPs) | 50 | No |

{style="table-layout:auto"}

### Price books

| **Capability** | **Description** | **Base allocation** | **Expandable?** |
| --- | --- | --- | --- |
| Price books | The number of price books allowed per instance | Based on the number of [Catalog variations](#catalog) | Yes<br>Increase catalog variations |
| Discounts per price record | The number of discounts that can be applied to a product price within a single price book | 10 | No |

{style="table-layout:auto"}

### Catalog views and policies

| **Capability** | **Description** | **Base allocation** | **Expandable?** |
| --- | --- | --- | --- |
| Catalog views | Number of configurable subsets of your master catalog | Based on the number of [Catalog variations](#catalog) | Yes<br>Increase catalog variations |
| Policies per catalog view | Number of data filters allowed | 10 | No |
| Attribute values in a policy | Number of product characteristics that can be configured for filtering | 100 | No |
| [Restricted access key assignment](setup/private-catalog-view.md) | Number of restricted access keys that can be assigned to a single catalog view | 3 | No |
| RSA key size (restricted access keys) | Minimum and maximum key strength accepted for a restricted access key | 2048-bit minimum, 8192-bit maximum | No |
| Restricted access keys | Key revocation propagation delay | Up to 5 minutes, due to caching. Tokens signed by a removed key are denied once the delay elapses. | Not applicable |

{style="table-layout:auto"}

### Catalog storefront

The base allocation for catalog storefront capabilities is determined based on GMV (gross merchandise value) tier. The table indicates the minimum allocation for each capability.

| **Capability** | **Description** | **Base allocation** | **Expandable?** |
| --- | --- | --- | --- |
| Catalog retrieval rate | Number of times a catalog API is called per month by a system (storefront, transaction system, ERP, or other) to retrieve data from the catalog | Based on GMV tier<p>Minimum allocation: 10M/month</p> | Yes<p>Add 1M requests per month license packs</p> |
| Content requests | Requests to the storefront for HTML page views or JSON API calls. Counted as 1 page view or 5 API calls. | Based on GMV tier<p>Minimum allocation: 2M/month</p> | Yes<p>Add 1M per month license pack</p> |
| Storefront GenAI variations | Allowance for text-based content generation | Based on GMV tier<p>Minimum allocation: 1K variations/month</p> | Yes<p>Purchase Generative AI credits separately</p> |

{style="table-layout:auto"}

>[!NOTE]
>
>Image generation requires an [!DNL Adobe Firefly] license provisioned to the same IMS org as [!DNL Adobe Commerce Optimizer].


### Product discovery

The following limits apply to storefront product search, listing, and merchandising configuration.

| **Capability** | **Description** | **Base allocation** | **Expandable?** |
| --- | --- | --- | --- |
| Product retrieval | Maximum SKUs per [!DNL Catalog Service] GraphQL request when fetching product data with `products`, `productSearch`, `refineProduct`, and `variants`. Split larger requests across multiple calls. | 100 | No |
| Filterable attributes | The number of product characteristics (like color, size, brand, or material) that can be enabled for layered navigation and facets | 200 | No |
| Searchable attributes | The number of product characteristics that can be indexed for catalog search | 200 | No |
| Sortable attributes | The number of product characteristics available as sort options on search and category pages. | 50 | No |
| Search pagination depth | Maximum products reachable through search pagination (for example, page 100 × 100 products/page) | 10K | No |
| Facets | The number of filterable product attributes (like Brand, Color, Size, Price) that can be configured to help shoppers refine search results and browse categories | 100<p>Must be filterable attributes</p> | No |
| Options per facet | The number of filterable product attribute values shoppers can select within a facet (for example, "Red," "Blue" for Color; "Small," "Medium" for Size) | 100 | Yes<p>Can increase via support request</p> |

{style="table-layout:auto"}

### Recommendations

The following capabilities are available for product recommendations. Some features available in other Adobe Commerce products are not supported in [!DNL Adobe Commerce Optimizer].

| **Capability** | **Description** | **Base allocation** | **Expandable?** |
| --- | --- | --- | --- |
| Active recommendation units | Number of live recommendation components on your storefront (like "Customers also viewed" or "You might also like") | 50 | No |
| Category or attribute inclusions/exclusions | Filter products to a specific set that qualifies for recommendations | Not supported | — |

{style="table-layout:auto"}
