# Catalog views overview for Adobe Merchandising Services

<!--This shared include file contains the conceptual and architecture overview of catalog views for Adobe Merchandising Services-->

A catalog view defines the products and pricing that a client can retrieve. It combines catalog sources, catalog layers, policies, and price books to support different brands, regions, business units, or channels.

## What are catalog views?

Catalog views define how your product catalog is organized and displayed. They act as filters that determine:

- **Which products are visible** based on business structure (brands, regions, dealers)
- **What pricing is shown** through linked price books
- **How products are filtered** using policies (attributes like brand, model, category)
- **What [catalog source](/help/optimizer/setup/catalog-sources.md) is used** based on attributes like locale
- **Who can access the view's data** through [Catalog Protection](private-catalog-view.md) and [restricted access keys](restricted-access-keys.md)

For example, you can create separate catalog views for:

- A brand or business unit
- A geographic region
- A dealer or partner channel
- A customer segment with specific pricing

## Architecture overview

Catalog views are part of the Adobe Merchandising Services framework that replaces the website, store, storeview framework used in Adobe Commerce foundations with a more flexible model:

![[!DNL Merchandising Services] Architecture](/help/assets/ccdm-shared/setup/merchandising-svcs-architecture.png)

### How it works

**1. Data Ingestion**
Catalog data from an Adobe Commerce backend or another third-party backend (for example, PIM or ERP) and other systems is ingested into the Adobe Merchandising Services data layer. Each SKU contains locale information and product attributes that map to catalog views, policies, and locales. The data ingestion process depends on the source system and integration method:

- **Adobe Commerce backend**—The system exports Commerce catalog feeds, maps them to the format expected by the data ingestion REST API, and synchronizes feed data to the Adobe Merchandising Services data layer. In this model, Adobe Commerce manages the initial sync and subsequent updates. Feeds include products, categories, product attributes, prices, and price books.

- **Third-party backend or source system**—A connector or integration service retrieves catalog data from the source—through APIs, events, or export feeds, and then maps and validates it against the composable catalog data model (CCDM) schema, and synchronizes the data to the Adobe Merchandising Services layer using the Data Ingestion REST API. The integration is responsible for the initial load and for sending later changes. A platform-specific connector, such as Adobe's [Salesforce Commerce Connector](https://experienceleague.adobe.com/en/docs/commerce/optimizer/developer/salesforce-connector), can provide a starting point.

**2. Unified Base Catalog**
The ingested data creates a unified base catalog in the Catalog Service data pipeline. This single source eliminates data duplication across business units.

**3. Catalog Views**
Multiple catalog views represent different business units (for example, "Texas Retail," "Texas Retail Seasonal"). Locales, policies, and price books can be shared across catalog views for flexibility.

**4. Multi-Channel Delivery**
The filtered catalog data is delivered to destinations like Edge Delivery Services, marketplaces, advertising platforms, and custom micro-storefronts. For more information about catalog data delivery, see the [developer documentation](https://developer.adobe.com/commerce/services/optimizer/).

When a catalog view has **[!UICONTROL Catalog Protection]** enabled, delivery to that destination requires a valid signed token from an assigned [restricted access key](restricted-access-keys.md); unauthorized requests are denied instead of receiving catalog data.

### Key components

|Component|Purpose|Example|
|---|---|---|
|**Catalog view**|Business unit or distribution channel|Dealer network, Regional store|
|**Policy**|Product filter based on attributes|Brand, Model, Category|
|**Locale**|Language/region setting|en-US, fr-CA, es-MX|
|**Price Book**|Pricing structure|Retail, Wholesale, Employee|
|**Restricted access key**|Signed-token credential that gates access to a protected catalog view|Partner portal key, B2B pricing key|

### Data flow

1. **Ingest** - catalog data from the Adobe Commerce backend
2. **Process** - Apply catalog views, policies, and pricing
3. **Deliver** - Serve filtered catalog to storefronts, marketplaces, and so on

## Key features

|Feature|Benefit|
|---|---|
|**Single Base Catalog**|Eliminate data duplication across business units|
|**Flexible Pricing**|Multiple price books per SKU for different customer segments|
|**Scalable**|Manage 200M+ SKUs efficiently|
|**Multi-Channel**|Serve catalogs to storefronts, marketplaces, and advertising platforms|
|**Real-time Updates**|Quickly update catalog data for promotions and campaigns|
|**Private catalog views**|Restrict a catalog view to authorized clients using signed-token validation|

## Use cases

### Multi-brand conglomerate

**Challenge**: Manage multiple brands, countries, and languages<br>
**Solution**: Single catalog with catalog views for each brand/region combination

### Automotive parts dealer

**Challenge**: 3,000 dealers with same products but different pricing<br>
**Solution**: One catalog with dealer-specific catalog views and price books

### Multi-location retailer

**Challenge**: Different pricing and inventory per location<br>
**Solution**: Location-based catalog views with region-specific policies

>[!NOTE]
>
>For detailed information about catalog data ingestion and delivery, see the [developer documentation](https://developer.adobe.com/commerce/services/optimizer/).
