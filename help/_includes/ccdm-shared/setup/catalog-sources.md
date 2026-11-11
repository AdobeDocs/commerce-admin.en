# Catalog sources

Catalog sources represent authoritative scopes of products, attributes, and categories. They typically map to language, audience, or system-of-origin boundaries and determine search, filter, and sort behavior.

## Catalog sources versus related concepts

Understanding how catalog sources relate to other Merchandising Services concepts helps you model your data correctly:

* **Catalog source** - The underlying data context that supplies product information. A catalog source typically represents a locale (for example, `en-US`, `fr-CA`) or a data context supplied by an external system such as a PIM or ERP. Products, attribute metadata, and categories are all scoped per catalog source. A catalog source defines the origin of raw catalog data and its effect on product discovery (search results, filtering, and sorting behavior).

* **[Catalog view](/help/optimizer/setup/catalog-view.md)** - A configured view of your catalog for a specific business need. A catalog view selects catalog sources (or locale), applies [policies](/help/optimizer/setup/policies.md) to filter products visibility, and associates [price books](/help/optimizer/setup/pricebooks.md) with the view. A single catalog source can power many catalog views (for example, one `en-US` source with separate catalog views for different brands or regions). Think of a catalog view as *how* you expose that data to a storefront, channel, or audience.

* **[Catalog layer](catalog-layer.md)** - A layer applied on top of base catalog data to modify product attributes (name, description, images, metadata) without changing the source data. Use catalog layers when differences must affect storefront display only - not product discovery.

## How catalog sources are populated

Catalog sources are populated through catalog data ingestion. How you supply that data depends on your implementation:

- **Adobe Commerce as a Cloud Service with CCDM**—Native synchronization supplies catalog data from Commerce Foundation. Manage the underlying products and store-view configuration in Commerce Foundation, and monitor synchronization in the [Data sync](data-sync.md) workspace. No separate Data Ingestion API integration is required.
- **Adobe Commerce Optimizer with a third-party backend**—Your integration supplies products and catalog source information through the [Data Ingestion API](https://developer.adobe.com/commerce/services/optimizer/data-ingestion/).


## Rules and limitations

* A catalog source is created when catalog data for a new locale or source system is first received by the Merchandising Services data layer.
* Product uniqueness is determined by SKU + catalog source.
* Shoppers do not access catalog sources directly. Catalog data is exposed to the storefront via [catalog views](catalog-view.md).

## Modeling guidance

Use the following guidance when planning your catalog structure. For Adobe Commerce as a Cloud Service with CCDM, manage the underlying configuration in Commerce Foundation rather than creating catalog sources through a separate ingestion integration.

* Use a separate catalog source for each catalog language.
* Use separate catalog sources when product and attribute differences must affect search, filtering, or sorting behavior, such as different searchability or filterability settings.
* Use [catalog layers](catalog-layer.md) when product and attribute differences must affect product presentation without changing search, filtering, or sorting behavior.

>[!MORELIKETHIS]
>
> * [Catalog views](catalog-view.md) - Configure filtered, priced views on top of a catalog source
> * [Catalog layers](catalog-layer.md) - Modify product presentation without changing source data
> * [Policies](policies.md) - Create attribute-based filters for catalog views
> * [Price books](/help/optimizer/setup/pricebooks.md) - Manage pricing structures for different customer segments
> * [Restricted access keys](restricted-access-keys.md) - Protect a catalog view with signed-token authentication
