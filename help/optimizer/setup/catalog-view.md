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

# Catalog views

Catalog views organize catalog data for a storefront context. Catalog views can be associated with policies and price books to shape the catalog experience for different business needs.

This topic applies to Adobe Commerce as a Cloud Service instances provisioned with the composable catalog data model (CCDM). Catalog views and policies are managed in the Commerce Admin in Unified Experience.

>[!NOTE]
>
>CCDM administration is available through Commerce Admin in Unified Shell. Adobe Commerce as a Cloud Service customers with instances that rely on Catalog Service with Live Search and Product Recommendations, do not have access to Catalog Views and other Merchandising Services with CCDM capabilities from the Commerce Admin.

## How catalog views work

A catalog view brings together catalog data and configuration for a storefront context. It can be used to represent a business unit, brand, region, or other storefront experience.

- **Catalog sources** provide product data for catalog experiences.
- **Policies** filter product data for a catalog view.
- **Price books** provide pricing data associated with a catalog view.

Catalog views do not replace the website, store, and store-view structure in Adobe Commerce as a Cloud Service. Commerce Core continues to manage that structure and transactional operations.

Catalog data synchronizes one way from Commerce Core into CCDM. CCDM supports storefront catalog experiences and product discovery. Commerce Core continues to handle cart, checkout, promotions, customers, and orders.

## Before you start

Before configuring a catalog view:

- Confirm that the Adobe Commerce as a Cloud Service instance is provisioned with CCDM.
- Confirm that the catalog data required for the storefront has been populated and synchronized.
- Identify the catalog source, policies, and price books needed for the storefront context.
- Determine whether the implementation will configure views manually or use supported B2B synchronization.

>[!NOTE]
>
>For supported B2B synchronization, the integration creates the corresponding catalog structures automatically by mapping the B2B Commerce configuration. Do not create duplicate catalog views or policies for structures managed by synchronization.

## Create a catalog view for a B2C implementation

Use this workflow when the B2C implementation requires catalog views to be configured manually.

1. Sign in to Commerce Admin in Unified Shell and select the Adobe Commerce as a Cloud Service instance provisioned with CCDM.
1. In the left navigation, go to **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Views]**.
1. Select **[!UICONTROL Create catalog view]**.
1. Enter a name for the catalog view.
1. Select the catalog source or sources for the storefront context.
1. Associate the relevant policies with the catalog view.
1. Associate the relevant price books with the catalog view.
1. Create the catalog view.

## B2B catalog views

For supported B2B synchronization, the integration creates the corresponding catalog structures automatically. The exact structures depend on the supported synchronization workflow.

Before configuring B2B storefront behavior:

1. Configure the required B2B catalog and company relationships in Adobe Commerce as a Cloud Service.
1. Confirm that the supported synchronization workflow has completed.
1. Review the resulting catalog configuration in the integrated Commerce Admin.
1. Validate the product assortment and displayed pricing in the storefront.
1. Test add-to-cart and checkout to confirm that transactional behavior and pricing are correct.

Do not manually create catalog views or policies that are already managed by synchronization. Use the documentation for the supported B2B synchronization workflow to determine which settings are managed automatically and which require merchant configuration.

## Price books and checkout

A price book provides pricing data associated with a catalog view. Price-book creation is API-driven, and pricing must remain consistent with Commerce Core.

A price that is available only in CCDM does not automatically become the price used by cart and checkout. Validate the displayed storefront price and the transaction price as part of testing.

## Review and validate a catalog view

After configuring a catalog view, verify the complete storefront experience:

- Confirm that the intended catalog data is synchronized.
- Confirm that the catalog view is associated with the intended policies and price books.
- Check that the storefront returns the expected product assortment.
- Verify displayed pricing against the corresponding Commerce Core pricing.
- Test add-to-cart, cart, and checkout.

For B2B implementations, also confirm that the catalog structures generated by synchronization match the intended company and catalog configuration.

## Troubleshooting

### Products are missing from the storefront

- Confirm that the instance is provisioned with CCDM.
- Confirm that catalog data has synchronized.
- Check that the storefront is using the intended catalog context.
- Review the policies associated with the catalog view.

### The displayed price is unexpected

- Confirm that the intended price book is associated with the catalog view.
- Check that the price data is synchronized and consistent with Commerce Core.
- Validate the price again in cart and checkout.

### CCDM catalog screens are not visible in Commerce Admin

Confirm that the selected instance is provisioned with CCDM and that you are accessing Commerce Admin through Unified Shell. An instance running catalog services v1 does not have the CCDM administration screens.

## Related content

- [Getting started with Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/getting-started)
- [Adobe Commerce B2B shared catalog overview](../../b2b/catalog-shared.md)
- [Adobe Commerce as a Cloud Service release notes](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/release-notes)
