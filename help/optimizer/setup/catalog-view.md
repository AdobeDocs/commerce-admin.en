---
title: Catalog Views
description: Learn what catalog views are and how to create them to organize your product catalog by business structure, policies, and pricing.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="SaaS only" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service and [!DNL Adobe Commerce Optimizer] projects only (Adobe-managed SaaS infrastructure)."
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
---

# Catalog views for Merchandising Services

When catalog data is synchronized to Merchandising Services with the Composable Catalog Data Model (CCDM), catalog views can be created manually or projected from Adobe Commerce, depending on your setup.

## Adobe Commerce B2C catalog views

For Adobe Commerce B2C deployments, create and manage catalog view using the steps in [Create a catalog view](#create-a-catalog-view).

## Adobe Commerce B2B catalog views

When an Adobe Commerce B2B deployment uses Merchandising Services with the Composable Catalog Data Model (CCDM), custom shared catalogs are projected as protected catalog views. The integration creates and manages these views and their associated configuration. You do not need to create them manually.

The projection maps Adobe Commerce data to Merchandising Services as follows:

| Adobe Commerce data | Merchandising Services result |
| --- | --- |
| Enabled store view and product data | Catalog source |
| Website and customer group pricing | Price book |
| Custom shared catalog assortment | Policy that filters the view's assortment |
| Custom shared catalog and enabled store view | Protected catalog view with the applicable catalog source, policy, and price book |
| Company assignment to a shared catalog | Buyer context used by the Adobe Commerce backend to resolve the appropriate catalog view |

The default shared catalog is not projected as a B2B catalog view. Each projected protected catalog view can reference one price book. A price book determines which prices are requested; it does not authorize access to the view.

At runtime, the Adobe Commerce backend uses the buyer's company assignment and store view to resolve the appropriate catalog view and price book. Catalog Protection validates access to the protected view; it does not determine which view or price book applies. Protection covers catalog and search requests, not cart, checkout, or order operations.

For details, see [B2B shared catalog projection](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection) and [how catalog data maps from Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/overview#how-the-connector-works-with-adobe-commerce).



