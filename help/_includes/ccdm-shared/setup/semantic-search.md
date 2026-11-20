# Semantic search

Semantic search uses AI to understand what shoppers mean, not just the exact words they type. Queries such as "dress for a beach wedding" or "comfortable shoes for standing all day" can return relevant products even when your catalog does not use those exact phrases.

The product discovery system combines keyword matching and semantic matching in one search experience. You do not manage separate keyword and semantic modes on the storefront.

## Configure semantic search

Semantic search is **enabled by default** for eligible English catalogs. You manage it on the **[!UICONTROL Advanced search]** tab of the [Settings](../settings.md#advanced-search) workspace, where you can confirm or change the setting and optionally tune semantic boost, similarity threshold, and fuzzy search. See [Settings](../settings.md#access-the-settings-workspace) for how to open the workspace.

You do not need to publish a separate configuration or change storefront settings after you save.

## Benefits

- **Fewer empty search pages**—Shoppers find products when their wording does not match catalog text exactly.
- **Better intent matching**—Natural, descriptive queries return useful results.
- **Less synonym maintenance**—Common word variations (for example, couch and sofa) are often handled without manual synonym lists.
- **No storefront or developer work**—Semantic search is enabled by default and requires no theme code, drop-in, or API changes.

## How it works

When semantic search is enabled, the system uses predefined catalog attributes (such as product name and description) to interpret query meaning alongside traditional keyword search. You do not select or prioritize attributes in Settings.

For example:

- A search for "leather couch" can return products labeled "leather sofa."
- "Spring dress" can surface seasonal dresses even when "spring" is not in the product name.
- "Shoes for trail running" can match products described as off-road or hiking footwear.

## What happens when you enable semantic search

Semantic search works alongside your existing search configuration. You do not replace keyword search or reconfigure the storefront.

When semantic search is active:

- Your existing [merchandising rules](../merchandising/rules/overview.md), [synonyms](../merchandising/synonyms/overview.md), [facets](../merchandising/facets/overview.md), boosts, and filters continue to apply.
- Semantic search adds AI-powered understanding of shopper intent to improve result relevance alongside keyword matching.
- Predefined catalog attributes are indexed automatically. You do not select attributes or publish a separate configuration.

## Validate after enablement

After semantic search is active and indexing completes, Adobe recommends validating search performance. Use the [Search performance](../manage-results/search-performance.md) page to review metrics and test queries that matter to your business.

1. Review your top searched terms in the **Unique searches** report.
1. Test historical zero-result queries from the **Zero results** report on the storefront.
1. Compare search results for the same queries before and after enablement.
1. Monitor search conversion and engagement metrics, including click-through rate, conversion rate, and zero results rate.

## Best practices

- Use clear, descriptive product names and descriptions (ideally 50-100 words) so both keyword and semantic matching have strong catalog text to work with.
- Start with the default **[!UICONTROL Enable semantic search]** setting, then adjust **[!UICONTROL Semantic boost]** or **[!UICONTROL Similarity threshold]** only if results feel too broad or too narrow.
- Keep brand-specific or highly technical [synonyms](../merchandising/synonyms/overview.md) where semantic search may not cover specialized terms.

## Troubleshooting

| Issue | What to do |
| --- | --- |
| No change on the storefront right after saving | Wait for indexing to finish. Large catalogs can take longer. |
| Results feel too broad | Raise **[!UICONTROL Similarity threshold]** or lower **[!UICONTROL Semantic boost]** on the **[!UICONTROL Advanced search]** tab. |
| Results feel too narrow | Lower **[!UICONTROL Similarity threshold]** or raise **[!UICONTROL Semantic boost]**. |
| Semantic search is unavailable | Confirm **[!UICONTROL Language]** is set to **English**. |

## Limitations {#semantic-search-limitations}

- **Catalog language:** Semantic search is available only for **English**-language catalogs.

## More help on this topic

- [Advanced search](../settings.md#advanced-search)
- [Synonyms](../merchandising/synonyms/overview.md)
- [Search performance](../manage-results/search-performance.md)
