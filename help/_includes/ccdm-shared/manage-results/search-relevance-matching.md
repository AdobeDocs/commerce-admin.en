# Search matching and ranking

>[!IMPORTANT]
>
>The following feature is in [private beta](https://experienceleague.adobe.com/en/docs/commerce-operations/release/beta).

Merchandising Services with the composable catalog data model (CCDM) ranks results so shoppers see the most relevant products first. The service boosts products whose catalog text **closely matches** the shopper's query, then favors matches where terms appear together, and finally includes broader matches.

## How matches are prioritized

Relevance uses three layers of matching strength (in addition to other scoring factors described below):

1. **Exact and near phrase match** — The full search phrase matches catalog text, or a near match after normalization such as stemming (for example, singular and plural forms resolve to the same root). These matches receive the highest relevance boost.

1. **All words in the same field** — Every query word appears in one searchable attribute (for example, `red` and `pants` in the product **name**). This layer receives the next highest boost.

1. **Words across different fields** — Query terms appear in different searchable attributes (for example, `red` in **color** and `pants` in **name**). This match layer is the broadest and receives the lowest relevance boost. It can also match partial queries used by autocomplete—for example, when a shopper types `red pan` before finishing `pants`. For German catalogs, see [Decompounding (German)](#decompounding-german).

### Example

For a query such as `red pants`:

- Products with the exact phrase **red pants** (or a close variant) rank **first**.
- Products where **red** and **pants** appear in the **same field** (for example, **name**) rank next.
- Products where the terms appear in **different fields** (for example, **color** and **name**) follow.

### Decompounding (German) {#decompounding-german}

German catalogs use many compound words. For example, **spülbecken** and **spül becken** can decompose into tokens such as **spul** and **beck** (after stemming) so a shopper who searches **spul becken** can still find **Spülbecken**. At this layer, decompounded subwords from a compound term must appear in the same field. Other query terms can match in different fields.

This **AND** requirement filters irrelevant matches where only one subword is present. For example, a search for **Brauseschlauch** no longer returns **Schlauchstück** when only part of the compound matches. A search for **spülbecken** can still match **spülbeckventil** because the longer word contains all expected tokens.

>[!NOTE]
>
>Exact and near phrase matching and same-field matching use the rules described above without decompounding.

#### Example

For a search phrase like `Brauseschlauch chrom`:

- **Exact and near phrase match** — Looks for the full phrase **brauseschlauch chrom** as typed, without decompounding (stemming still applies).
- **All words in the same field** — Looks for **brauseschlauch** and **chrom** in the **same** searchable attribute, still without decompounding (for example, both in **name**).
- **Words across different fields** — Decompounds **Brauseschlauch** into **brause** and **schlauch**. Those tokens must appear in the **same** field (not necessarily as an adjacent phrase). **chrom** can match in a **different** field (for example, **brause** and **schlauch** in **name**, **chrom** in **color**).

Set **Language** to **German** on the [Language](../settings.md#language) tab in [Settings](../settings.md) so decompounding rules apply. Validate high-value German queries on a staging storefront before you enable changes in production.

Decompounding is rule-based and can add edge cases at this layer. If a subword is missing from the dictionary, tokenization is incomplete and returns broader matches than expected—for example, **gas** missing from **gaszähler** emits only **zahl**, or **stat** missing from **thermostat**. The stemmer can also produce unexpected roots (for example, **schrauber** stemming to **schraub**, or **schelle** to **schell**). Adobe updates the dictionary and stemming overrides for known cases as issues are identified.

## What else affects ranking

Phrase matching alone does not determine relevance. Several signals interact:

- Boost from **exact / near** phrase matching
- Boost when **all query terms** appear in the **same** field
- **Intelligent ranking** (when enabled), which blends textual relevance with behavioral signals — see [How intelligent ranking scoring works](../merchandising/rules/add.md#how-intelligent-ranking-scoring-works-search)
- **[Search weight](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/search/search-results)** on each attribute and other textual relevance factors (for example, how often terms occur in name or description length). In *Settings*, configure which attributes participate in keyword search and their relative **[keyword search weights](../settings.md)**.
- **[Merchandising rules](../merchandising/rules/overview.md)** such as pin, boost, and bury

Because signals interact, a broad match sometimes ranks above a tighter phrase match when **search weights** or term frequency outweigh a weaker phrase match.

**Example:** If **red pants** appears in **description** with **search weight = 1**, but **red** and **pants** appear separately in **name** and **color** with **search weight = 10**, the split match outranks the phrase match.

Manual **pin** and **bury** rules remain strong; **boost** rules may require tuning to overcome new phrase and same-field boosts. Validate important queries after changing weights or rules.

### Search weight 1 and combined indexing

Attributes with **minimum search weight** (weight **1**) and no special match modes combine into a single internal field (`defaultSearchField`) to reduce mapping overhead. Treat that as one searchable surface for **same-field** matching: tokens that land only in those combined low-weight fields are evaluated together rather than as separate per-attribute fields. Adobe may refine this optimization over time as matching evolves.

## Related topics

- [Settings](../settings.md)
- [Search performance](search-performance.md)
- [Merchandising rules overview](../merchandising/rules/overview.md)
- [Add search rules](../merchandising/rules/add.md)
- [Synonyms overview](../merchandising/synonyms/overview.md)
