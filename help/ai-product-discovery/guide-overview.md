---
title: AI Product Discovery
description: Learn how [!DNL Adobe Commerce] Catalog enrichment and PDP enrichment address gaps in structured product data and shopper-focused copy for AI product discovery.
role: Admin, User, Leader
---
# AI product discovery

Product discovery is how shoppers find and evaluate products that meet their needs. In conversational AI tools such as [!DNL ChatGPT] and [!DNL Gemini], shoppers can describe what they want in everyday language and use AI-generated responses to explore and compare products. The usefulness of those responses depends in part on whether AI agents can access and interpret relevant product data.

## Why product discovery matters

Shoppers often describe a need, use, or preference rather than search for an exact product name or technical attribute. To match those requests with relevant products, AI agents need product information that is both structured and meaningful to shoppers.

When product records are incomplete, inconsistent, or focused only on technical specifications, agents may have difficulty understanding which products fit a shopper's intent. Shoppers can miss relevant products, and merchants may need to spend time correcting and enriching catalog content manually.

## Gaps in product data

Two common catalog gaps can limit AI-assisted product discovery:

### Product facts are difficult to use

Catalog information may be stored across attributes, variants, options, categories, and price or availability fields. If agents cannot access the relevant facts in a useful structure, they may not understand a product's features or how it compares with alternatives.

### Product copy does not reflect shopper intent

Product names and descriptions may repeat technical attributes without explaining the benefit or context that matters to a shopper. This can make it harder for AI agents to connect a product with a natural-language request.

## Enrichment workflows for product discovery

In [!DNL Adobe Commerce], two enrichment workflows address these different catalog gaps.

### Make structured facts available with PDP enrichment

PDP enrichment lets you select catalog facts for AI agents to receive, such as product attributes, variants and options, feature bullets, category relationships, and price and availability. This helps agents interpret product details without changing the storefront content that shoppers see. See [Create a PDP enrichment job](pdp-enrichment.md).

### Align catalog copy with shopper intent

Catalog enrichment uses catalog and URL signals to suggest improvements to product names and long descriptions. You can review and deploy approved suggestions to the [!DNL Adobe Commerce] catalog so product copy describes items more clearly for AI-assisted discovery. See [Catalog enrichment](catalog-enrichment.md).

Brand governance rules let you define product copy requirements for Catalog enrichment, including length, phrases, tone, and capitalization. These rules apply only to Catalog enrichment, not PDP enrichment. See [Create Catalog Enrichment brand rules](brand-governance.md).

## Choose an enrichment workflow

Use PDP enrichment to control which structured product facts AI agents receive. Use Catalog enrichment to improve product names and descriptions for discovery. These workflows address different data gaps and remain separate.

## Prerequisites

Prerequisites differ by deployment type. Optimize at Edge is required for PDP enrichment, while Catalog enrichment does not require it.

### Adobe Commerce on PaaS

- **Required: Adobe IMS organization.** Make an Adobe IMS organization available. If your organization does not have one, follow the [Adobe IMS integration overview](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview).
- **Required: Commerce enrichment extension.** Install the Commerce enrichment extension to enable both PDP enrichment and Catalog enrichment. See [Enable catalog enrichment](catalog-enrichment.md#enable-catalog-enrichment).
- **Required for PDP enrichment: Optimize at Edge.** Set up Optimize at Edge for PDP enrichment. Catalog enrichment does not require this setup. Commerce-specific instructions are required; the [Optimize at Edge with Fastly BYOCDN guide](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn) is a reference only and is not a Commerce setup guide.
- **Optional: Log forwarding.** Configure log forwarding to enable agentic traffic-based recommendations for PDP enrichment and Catalog enrichment. Without log forwarding, you can still select product detail pages (PDPs) or SKUs manually for enrichment.

### Adobe Commerce as a Cloud Service (ACCS)

- **Required for PDP enrichment: Optimize at Edge.** Set up Optimize at Edge for PDP enrichment. Catalog enrichment does not require this setup. Commerce-specific instructions are required; the [Optimize at Edge with Fastly BYOCDN guide](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn) is a reference only and is not a Commerce setup guide.
- **Optional: Log forwarding.** Configure log forwarding to enable agentic traffic-based recommendations for PDP enrichment and Catalog enrichment. Without log forwarding, you can still select product detail pages (PDPs) or SKUs manually for enrichment.
