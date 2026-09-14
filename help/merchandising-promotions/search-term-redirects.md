---
title: Search-Term Redirects and Storefront Routing
description: Learn how to choose search-term redirects, URL rewrites, Live Search rules, or storefront routing by deployment for Adobe Commerce and Edge Delivery Services.
feature: Merchandising, Search
role: Admin, User
level: Intermediate
topic: Commerce, Administration
autotag-review: '2026-09-10T17:42:01.349Z'
TQID: 'https://experienceleague.adobe.com/Vxw3B0zOzLZfAm3qn8gJKHGSNtVhkN2Bfmcauhj0sdM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Search-term redirects and storefront routing

Search-term redirects, URL redirects, and search merchandising solve different problems. Use this guide to choose the right capability for standard [!DNL Adobe Commerce] search, [!DNL Live Search], and [!DNL Commerce Storefront] powered by [!DNL Edge Delivery Services].

## Understand redirect types

These capabilities differ in what triggers the behavior and what the shopper sees:

* A **search-term redirect** sends a shopper who enters a specific search term to a designated page.

* A **URL redirect** sends a request for an old URL to a new URL, usually with an HTTP 301 or 302 response. The browser address bar changes to the new URL.

* **Search merchandising** changes which products appear, or their order, in search results without changing the requested URL.

* A **URL rewrite** maps one URL to another on the server. The [!DNL Adobe Commerce] URL Rewrite tool creates a permanent redirect (301) for the old URL. For more information, see [URL rewrites](url-rewrite.md).

## Choose a routing capability

Use the following guidance to identify the capability that matches your requirement:

| Requirement | Recommended capability |
| --- | --- |
| Send a specific query from standard [!DNL Adobe Commerce] search to a page | Configure a search term in [Manage search terms](../catalog/search-terms.md), where supported. |
| Change product ranking or visibility in search results | Use [!DNL Live Search] [synonyms](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/synonyms/synonyms) or [merchandising rules](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/rules/rules-add). |
| Redirect an old product, category, or CMS URL | Use the Commerce [URL Rewrite](url-rewrite.md) tool when it applies to your deployment. |
| Redirect an [!DNL Edge Delivery Services] path | Use storefront or CDN routing. |
| Preserve legacy URLs after a storefront migration | Create and test a legacy-to-new URL redirect map. |

## Standard Commerce search

With standard catalog search, you can configure a search term to open a content page, category page, product page, or external page where the deployment supports this capability. Use it when a shopper-entered query, such as `gift cards` or `returns`, must open a campaign or informational page.

To create or update this type of redirect, see [Manage search terms](../catalog/search-terms.md). The search-term configuration is separate from the URL Rewrite tool because the trigger is the shopper's query, not an existing URL.

>[!NOTE]
>
>Confirm that the storefront uses standard catalog search and supports native search-term redirects. The behavior and available configuration can differ for [!DNL Live Search], [!DNL Adobe Commerce as a Cloud Service], or a headless storefront.

## URL redirects and rewrites

Use a URL rewrite when the source is an existing URL rather than a shopper-entered search term. Common examples include redirecting:

* An old product URL to a new product URL.

* A retired category URL to a replacement category URL.

* An outdated CMS page URL to a new content page URL.

For deployments that support the URL Rewrite tool, go to **[!UICONTROL Marketing]** > **[!UICONTROL SEO & Search]** > **[!UICONTROL URL Rewrites]** to create the redirect. For step-by-step guidance, see [URL rewrites](url-rewrite.md).

>[!NOTE]
>
>The [URL rewrites](url-rewrite.md) topic is marked PaaS only. For [!DNL Adobe Commerce as a Cloud Service] or an [!DNL Edge Delivery Services] storefront, use the routing guidance for that storefront instead.

## Live Search

[!DNL Live Search] replaces the default storefront search experience and provides capabilities such as synonyms, facets, and merchandising rules.

Use [!DNL Live Search] when you need to change search relevance, product ranking, or product visibility. Use synonyms when different words should return similar products. Use merchandising rules when products must be boosted, buried, or ranked differently.

[!DNL Live Search] search behavior should not be treated as a drop-in replacement for every native Commerce search-term configuration. When a query must navigate to a content or campaign page, implement the redirect in the storefront or edge-routing layer that receives the request. For more information, see the [[!DNL Live Search] documentation](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview).

## Edge Delivery Services

For a storefront powered by [!DNL Edge Delivery Services], manage redirects in the storefront or edge-routing layer. Do not assume that [!DNL Adobe Commerce] Admin URL rewrites control every request.

When you use document authoring, maintain redirect mappings in the site's redirect configuration. For redirects that must execute before a request reaches the origin, use the appropriate CDN or edge configuration. For related SEO guidance, see [SEO guidelines for Commerce Storefront](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/).

## Migrate from Luma

Treat redirect migration as part of the storefront migration. Preserve the customer journey and SEO intent, then reimplement routing for the target storefront.

Before switching traffic to the new storefront:

1. Export and inventory existing Luma URLs and search-term landing pages.

1. Classify each item as a search-term redirect, URL redirect, or merchandising rule.

1. Map every legacy URL to its new storefront path.

1. Implement each redirect at the layer that receives the request.

1. Test status codes, query parameters, canonical URLs, locale paths, and redirect loops.

1. Monitor logs and analytics after launch for unresolved legacy URLs.

## Troubleshoot redirects

### A search term does not redirect

Confirm that the storefront uses standard catalog search, the search query matches the configured term, and the search term is assigned to the correct store view. If [!DNL Live Search] is enabled, verify that the redirect is implemented in the storefront or edge layer.

### A redirect works on Luma but not on Edge Delivery Services

Confirm that the redirect is configured in the [!DNL Edge Delivery Services] storefront or CDN routing layer. [!DNL Adobe Commerce] Admin URL rewrites might not receive the request.

### Live Search returns results instead of redirecting

Use [!DNL Live Search] rules for product ranking and visibility. For navigation to a content or campaign page, configure the redirect in the storefront or edge layer.

### A redirect works in one store view but not another

Check the store view assigned to the search term or URL rule. Test the full locale path and query in each affected store view.

## More help on this topic

* [SEO overview and best practices](seo-overview.md)

* [What is the storefront?](../getting-started/storefront.md)

* [Manage search terms](../catalog/search-terms.md)

* [URL rewrites](url-rewrite.md)
