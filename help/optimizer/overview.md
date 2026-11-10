---
title: What is Merchandising Services with the Composable Catalog Data Model?
description: Learn about Merchandising Services with the Composable Catalog Data Model (CCDM) and its key features.
recommendations: noCatalog
badgeSaas: label="SaaS only" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service and [!DNL Adobe Commerce Optimizer] projects only (Adobe-managed SaaS infrastructure)."
exl-id: f9516d4c-fbae-4db2-a1a9-cda3684a8122
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# What is Merchandising Services with the Composable Catalog Data Model?

Merchandising Services with the Composable Catalog Data Model (CCDM) enhances your e-commerce experience with a high-performance storefront, boosting organic traffic, customer engagement, and revenue.

With Merchandising Services with the Composable Catalog Data Model (CCDM), you can:

- Use catalog data from your Adobe Commerce as a Cloud Service instance to power your storefront experiences.
- Define business catalog views and policies.
- Create personalized search and recommendations using AI and ML.
- Improve product discovery relevance with ranking that prioritizes **exact and near matches** and same-field matches. See [Search matching and ranking](./manage-results/search-relevance-matching.md).
- View crucial product data availability, including synchronization status and storefront eventing data for accurate implementation and troubleshooting.

<!--
Watch the following video for a high-level overview of [!DNL Adobe Commerce Optimizer]:

>[!VIDEO](https://video.tv.adobe.com/v/3450226)
-->

## What are the benefits of using Merchandising Services with the Composable Catalog Data Model (CCDM)?

Merchandising Services with the Composable Catalog Data Model (CCDM) is for Adobe Commerce as a Cloud Service merchants who want to use their existing backend commerce system to transform storefront experiences.

## Quick tour

>[!BEGINTABS]

>[!TAB Catalog Views and Policies]

Define your catalog views. The catalog contains your product data and helps you define your business structure. Also, you can view valuable insights into the availability of product data for your storefront, ensuring it can be promptly displayed to your shoppers.

- **Catalog views**—Help you define your retail structure into meaningful business groups. For example, dealers for the automobile industry, subsidiaries for multi brand conglomerates, or manufacturing locations for suppliers.
- **Catalog layers**— Modify product data without changing source data. When using AEM Assets for product images, the AEM-Assets layer is applied through Product Visuals. See Catalog layers for details.
- **Private catalog views** - Configure catalog protection to restrict a catalog view so only requests carrying a valid signed token can retrieve its data. See [Private catalog views](./setup/catalog-layer.md#private-catalog-views) for setup.

>[!TAB Policies]

Define your data access filters within catalog views. Policies help to ensure that the right content is sent to the right destination. For example, point of sale physical stores, marketplaces, advertisement pipelines (Google, Facebook, Instagram).


>[!TAB Merchandising]

Create personalized experiences for your shoppers through product discovery and product recommendations.

- **Opportunities**— Helps identify potential areas for growth and optimization within your store's merchandising strategy. This includes analyzing product performance, shopper behavior, and search trends to make informed decisions that drive sales and engagement.
- **Recommendations**—Uses artificial intelligence and machine-learning algorithms to perform a deep analysis of aggregated visitor data. This data, when combined with your catalog, results in a highly engaging, relevant, and personalized experience. Recommendations are surfaced on the storefront as units with labels, such as "Customers who viewed this product also viewed". You can create, manage, and deploy recommendations directly from [!DNL Adobe Commerce Optimizer].
- **Merchandising rules**—Enhances your site search functionality, ensuring a seamless and efficient shopper experience that maximizes conversion rates. It enables merchandisers to ensure that shoppers get the right products at the right time.
- **Facets**—Enhances your site search functionality, ensuring a seamless and efficient shopper experience that maximizes conversion rates. It enables merchandisers to ensure that shoppers get the right products at the right time.
- **Synonyms**—Enhances your site search functionality, ensuring a seamless and efficient shopper experience that maximizes conversion rates. It enables merchandisers to ensure that shoppers get the right products at the right time.
- **Settings**—Provides configuration options to customize and optimize your merchandising strategy according to your store's specific needs including configuring price facets, language, and advanced search.

>[!TAB Reports]

Use reports to measure the results of your merchandising efforts, identify opportunities for growth, and highlight areas for optimization.

- [**Success metrics**](./manage-results/success-metrics.md)—Provides an overview of the key performance metrics for your store so that you and your team can quickly understand results and see where to optimize.
- [**Search performance**](./manage-results/search-performance.md)—Provides insight into the search terms that shoppers use. Use this information to identify trends, increase click-through, and improve the conversion rate.

>[!TAB System Configuration]

Monitor the synchronization of your catalog data and storefront events from the Commerce Admin. This helps ensure that your product data is available for your storefront and can be promptly displayed to your shoppers.

- **Catalog Sync**—Displays an overview of the synchronization status for catalog data transferred from your Commerce data source. This is the same capability documented as [Data sync](./setup/data-sync.md).
- **Catalog View Sync Status**—Monitors synchronization and helps you troubleshoot catalog views, including their policies, price books, and access keys. See [Catalog View Sync Status](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/data-transfer/data-sync/catalog-view-sync/catalog-view-sync-status).
- **Events** - Displays storefront event data which powers Product Discovery and Recommendations. The **Events** page lets the merchant verify that they have implemented storefront eventing correctly and that events are being successfully captured. Merchants can use this page to identify potential problems and take steps to resolve any eventing issues.

>[!ENDTABS]

## Key capabilities

Key capabilities include:

- **Merchandising Services powered by Catalog views and Policies** - This solution is the foundational piece of [!DNL Adobe Commerce Optimizer]. Merchandising Services powered by Catalog views and Policies is a highly scalable, flexible catalog data model which unlocks multi-brand, multi-business unit, and multi-language use cases. These merchandising services provide building blocks that merchants can use to create and manage catalogs at scale. Within [!DNL Adobe Commerce Optimizer], you can manage your catalog by creating catalog views and policies that best define your business goals. In addition, the merchandiser can provide personalized experiences to drive traffic and engagement using product discovery, recommendations​, and intelligent merchandising.
- **Before and After metrics** - Provides real-time insights into the performance of your commerce initiatives. You can view before and after results of specific KPIs and evaluate the impact of changes and optimize for better results. You can export the results in a PDF.
- **Commerce storefront powered by Edge Delivery** - With Edge delivery, you can launch your site quickly using prebuilt storefront components with integrated commerce functionality — including product listing pages, product detail pages, cart, and checkout.
- **Third-party cart and checkout** - Use API mesh and App builder to integrate with third-party cart and checkout systems.

>[!NOTE]
>
>To understand system boundaries and licensing for Merchandising Services with capabilities, see [Limits and boundaries](boundaries-limits.md).

<!--

## Architecture

The following diagram describes the basic architecture of [!DNL Adobe Commerce Optimizer], from catalog data ingestion to the relationship between merchandising services, your storefront, and the integration with a third-party cart and checkout process.

![[!DNL Adobe Commerce Optimizer] Architecture](./assets/architecture.png)
-->
