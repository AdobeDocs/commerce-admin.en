<!--
SOURCE OF TRUTH: Edit this file in the commerce.en repo:
https://github.com/Adobe-Enterprise-Docs/commerce.en/blob/main/help/_includes/ccdm-shared/merchandising/rules/best-practice.md

This content is shared by the Adobe Commerce Optimizer Guide (commerce.en) and the
Merchandising Services with CCDM Guide (commerce-admin.en). Changes made in commerce.en
are synced automatically to commerce-admin.en, so do not edit the copy in that repo.
This includes related images in help/assets/ccdm-shared/.
-->

# Merchandising Rules Best Practices

To optimize conversion and revenue, implement effective **search rules**, a strong **default listing** rule, and **[category rules](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#rule-types)**. Adjust rankings using sales data, stock, promotions, and [intelligent ranking](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#intelligent-ranking).

Use [search suppression rules](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/overview#search-suppression-rules) only when matching shopper queries must return zero products—not when products need a different ranking.

It is crucial to establish a well thought out **default rule**. Your [default rule](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/overview#default-rule) determines how search results are initially sorted when no more specific search rule applies, which improves discovery and purchase likelihood. Review it regularly so it keeps pace with shopper needs and campaigns.

## Tips to optimize search rules

- Pin or boost products with high sales volumes or recent sales activity.
- Prioritize products with high ratings and positive reviews.
- Ensure that in-stock items are ranked higher.
- Slightly prioritize products with higher profit margins without compromising relevance.
- Highlight products that are on sale or part of special promotions.
- Set search rules during promotion or sales periods automatically by using the date range during your promotion period.
- Tailor search results based on individual shopper behavior using [intelligent ranking](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#intelligent-ranking), such as "recommended for you", "most viewed" and so on.
- When an intelligent strategy other than **None** is selected, tune **[Intelligent ranking boost](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#intelligent-ranking-boost)** per rule and validate in **Test your rule** before publishing.
- Always use the "Test your rule" panel to preview how your intelligent ranking strategy affects actual search results for different queries.

## Tips for category rules

- Use [category rules](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#rule-types) on high-traffic or high-margin **category pages** where curated order matters as much as search—for example, seasonal collections or featured departments.
- Align **intelligent ranking** (for example, trending, most viewed) with how shoppers browse that category; category pages do not use search query text the way search rules do. See [Intelligent ranking](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#intelligent-ranking). For intelligent methods other than **None**, use **[Intelligent ranking boost](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#intelligent-ranking-boost)** and category preview to tune behavioral strength for that category rule.
- Apply **pin**, **boost**, and **bury** consistently with your campaign plan; remember that manual positions usually apply only when the shopper uses the **default sort** for the listing. See [Manual ranking](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#manual-ranking).
- Preview in the **category** rule flow in the editor and validate on the storefront after publish, the same discipline you use for the "Test your rule" panel on search.

## Search suppression best practices and use cases {#search-suppression-best-practices}

A search suppression rule blocks results for queries that match its conditions, so the storefront displays a search-results page with zero products. The rule editor doesn’t provide a preview for suppression rules. Use the narrowest condition that meets the restriction, then follow [Create and manage search suppression rules](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#search-suppression-rules). After the rule becomes active, verify matching and nonmatching searches on the storefront. Check the storefront’s actual no-results presentation.

| Use case | Suggested configuration | What to check |
| --- | --- | --- |
| Regulatory compliance for search | Scope the rule to the affected catalog view and match the restricted search terms. | Confirm the terms with your compliance team. Search suppression alone does not prevent access through category navigation, merchandising pages, recommendations, or direct product URLs. |
| Branding restrictions | Use **Query contains** when a restricted brand name must be blocked within longer queries. | After the rule becomes active, check unrelated storefront queries that contain similar text to avoid suppressing legitimate searches. |
| Prevent a specific search term from returning results | Use **Query is** for an exact phrase that should return no products. | Check related phrases separately. An exact-match condition does not block every query containing that phrase. |
| Restrictions on query prefixes or suffixes | Use **Query starts with** or **Query ends with** when the location of the restricted text matters. | After the rule becomes active, check storefront queries with the text at the beginning, middle, and end to confirm the intended scope. |
| Temporary search restrictions | Set a start and end date for a time-limited restriction. | Confirm the schedule and enabled status, and review whether the rule is still needed after the restriction ends. |

- Give each rule a descriptive name and record the reason for the restriction in its description.
- Review query conditions before publishing changes. After the rule becomes active, check storefront queries that should be blocked and queries that should still return products. Cached query results can take up to 15 minutes to refresh.
- Review the storefront’s no-results state and make sure shoppers have a useful way to continue browsing, such as revising the query or navigating to a category, where supported by the storefront.
- Do not use query suppression as a substitute for product-level exclusions. To exclude products across search results, search suggestions, and autocomplete, use manual exclusions or **Attribute Based Merchandising Events** with a **Hide** action in the **default search rule**.
- Review active suppression rules regularly. Disable rules that are no longer needed, or edit and publish them when restrictions change.
