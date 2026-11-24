---
title: AI Product Discovery
description: Learn how [!DNL Adobe Commerce] Catalog enrichment and PDP enrichment address gaps in structured product data and shopper-focused copy for AI product discovery.
role: Admin, User, Leader
---
# AI product discovery

Product discovery is how shoppers find and evaluate products that meet their needs. In conversational AI tools such as [!DNL ChatGPT] and [!DNL Gemini], shoppers can describe what they want in everyday language and use AI-generated responses to explore and compare products. The usefulness of those responses depends in part on whether AI agents can access and interpret relevant product data.

## Who this guide is for {#who-this-guide-is-for}

- Digital marketers and merchandisers who want product data to be accurate and useful in AI-assisted product discovery.
- Merchandisers who need a controlled way to enrich selected products or prepare copy for a campaign.
- [!DNL Adobe Commerce] administrators responsible for catalog data, services, and Admin access.

## Why product discovery matters

Shoppers often describe a need, use, or preference rather than search for an exact product name or technical attribute. To match those requests with relevant products, AI agents need product information that is both structured and meaningful to shoppers.

When product records are incomplete, inconsistent, or focused only on technical specifications, agents may have difficulty understanding which products fit a shopper's intent. Shoppers can miss relevant products, and merchants may need to spend time correcting and enriching catalog content manually.

Additionally, unbranded shopper queries create new opportunities for product discovery. When shoppers describe their needs without specifying a brand, AI surfaces show relevant products across competing brands based on how well those products match shopper intent. For merchants, this creates an opportunity to reach new customers who may not be familiar with their brand, expanding product visibility beyond existing brand awareness.

However, there are some challenges in product discovery on AI surfaces, such as gaps in your catalog that can limit AI-assisted product discovery.

## Product facts are difficult to access and interpret

Product information is often distributed across attributes, variants, options, categories, and other catalog fields. While this information may be available to shoppers on the storefront, it is not always accessible or easily interpreted by AI crawlers. Product details presented through dynamically rendered content, JavaScript-dependent components, interactive shopping wizards, pop-ups, or linked pages may be difficult for crawlers to retrieve.

Even when this information is accessible, it may not be structured in a way that AI agents can reliably interpret. As a result, AI agents may lack a complete understanding of a product's features, available options, and capabilities, limiting their ability to accurately match products to shopper needs.

## Product catalog does not reflect shopper intent

Shoppers increasingly describe their needs, problems, and intended use cases in natural language rather than searching for specific product names or technical specifications. However, product names and descriptions often focus on technical attributes without clearly communicating the benefits, use cases, or real-world problems a product addresses.

This creates a gap between how shoppers express their needs and how products are described in the catalog. Without clear, shopper-focused product content, AI agents may struggle to interpret a product's value and relevance to a shopper's intent, potentially overlooking suitable products in favor of alternatives whose descriptions more clearly align with the shopper's needs.

[!DNL Adobe Commerce] solves these catalog gap issues by providing two complementary enrichment workflows: product detail page enrichment and catalog enrichment. These two enrichments improve how AI agents access, understand, and match products to shopper intent. They are accessible in the _Admin_ > **AI Product Discovery** menu.

## Make structured facts available with Product Detail Page Enrichment

PDP Enrichment creates a structured data payload containing relevant product information, including attributes, variants, options, feature bullets, category relationships, pricing, and availability. This provides AI agents with a more complete and structured understanding of a product's features, capabilities, and available configurations.

Using [Optimize at Edge](#prerequisites) technology, the enriched product information is made directly accessible to AI crawlers without requiring changes to the human-visible storefront. Merchants can improve how product information is presented to AI agents without modifying storefront layouts, introducing new shopper-facing components, or requiring custom storefront development.

See [product detail page enrichment](pdp-enrichment.md).

## Optimize product catalog content with shopper intent using Catalog Enrichment

Catalog Enrichment transforms technical product attributes and existing catalog information into shopper-focused product names and descriptions that clearly communicate a product's benefits, capabilities, and real-world use cases. Product names and descriptions are among the most influential sources of information AI surfaces use to understand product capabilities and determine their relevance to shopper intent. 

By connecting technical product specifications to the needs and problems shoppers describe in natural language, Catalog Enrichment helps AI agents better understand a product's value, reduce ambiguity in interpreting its capabilities, and more accurately match relevant products to shopper intent.

Merchants can review and approve suggested improvements before applying them directly to their Adobe Commerce product catalog. This ensures that storefronts and sales channels powered by the catalog can consistently communicate the same enriched, value-driven product information to shoppers across touchpoints.

See [Catalog enrichment](catalog-enrichment.md).

### Brand governance rules

Brand governance rules let you define product copy requirements for catalog enrichment, including length, phrases, tone, and capitalization. These rules apply only to catalog enrichment, not PDP enrichment.

See [Create Catalog Enrichment brand rules](brand-governance.md).

## Choose an enrichment workflow

Use Catalog enrichment to improve product names and descriptions for discovery. Use PDP enrichment to maximize crawlability for LLMs with structured product data without making any changes to your human visible experience. These workflows address different data gaps and remain separate.
