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

## Who this guide is for {#who-this-guide-is-for}

- Digital marketers and merchandisers who want product data to be accurate and useful in AI-assisted product discovery.
- Merchandisers who need a controlled way to enrich selected products or prepare copy for a campaign.
- [!DNL Adobe Commerce] administrators responsible for catalog data, services, and Admin access.

## Prerequisites {#prerequisites}

Prerequisites depend on your deployment type and the enrichment workflow you plan to use. Optimize at Edge is required for PDP enrichment, but not for Catalog enrichment.

### [!DNL Adobe Commerce] on PaaS

- **IMS organization and sign-in:** An [!DNL Adobe IMS] organization must be available. If your organization does not have one, follow the [Adobe IMS integration overview](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview). Catalog Enrichment uses the signed-in Admin user's IMS access token; a native Commerce username and password alone do not provide this token.
- **Commerce Admin IMS integration:** The Commerce Admin Integration with Adobe ID must be enabled for IMS sign-in. Enabling it is an instance-wide change: all Admin users must sign in through IMS, and native Commerce username-and-password sign-in is no longer available. See [Configure the Commerce Admin Integration with Adobe ID](/help/getting-started/adobe-ims-config.md) and the [IMS integration overview](/help/getting-started/adobe-ims-integration-overview.md).
- **Catalog Enrichment organization access:** The IMS organization associated with the Commerce instance is typically different from the organization that holds the [!DNL Adobe Brand Visibility] entitlement. The organizations do not need to be the same. Ask your Adobe administrator or account team to confirm the supported organization access for your account.
- **Optimize at Edge:** Required for PDP enrichment, but not for Catalog enrichment. Commerce-specific setup instructions are needed. The [Optimize at Edge with [!DNL Fastly] BYOCDN guide](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn) is a reference, not a Commerce setup guide.
- **Log forwarding:** Optional. Configure log forwarding to enable agentic traffic-based recommendations for both workflows. Without it, you can still select PDPs or SKUs manually for enrichment.

#### Install the shared enrichment extension {#install-enrichment-extension}

Install the Catalog Enrichment extension once to enable both Catalog Enrichment and PDP enrichment:

```bash
composer require magento/module-catalog-enrichment --no-update
composer update magento/module-catalog-enrichment
```

If Catalog Services is not installed, install the [Catalog Service extension](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/installation#install-the-catalog-service-extension).

#### Additional Catalog Enrichment requirements

- Enable and maintain the required Commerce services and catalog connectivity. See [Configure catalog enrichment](catalog-enrichment.md#configure-catalog-enrichment).
- Make the storefront accessible to relevant LLM-oriented and agentic bots when you need crawl-based catalog recommendations.
- Have access to the Adobe Admin Console. During setup, [!DNL Adobe Commerce] checks whether your organization has signed the GenAI rider or opted out for the underlying AI services.

### [!DNL Adobe Commerce as a Cloud Service] (ACCS)

- **Optimize at Edge:** Required for PDP enrichment, but not for Catalog enrichment. Commerce-specific setup instructions are needed. The [Optimize at Edge with [!DNL Fastly] BYOCDN guide](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn) is a reference, not a Commerce setup guide.
- **Log forwarding:** Optional. Configure log forwarding to enable agentic traffic-based recommendations for PDP enrichment and Catalog enrichment. Without it, you can still select PDPs or SKUs manually for enrichment.
