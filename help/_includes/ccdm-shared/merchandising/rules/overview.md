Merchandising rules combine logic with actions to shape how products appear in **search results**, in **default product listings** through the **default search rule**, and on **category pages**. You can boost, bury, pin, or hide products and apply **intelligent ranking** so listings reflect your business goals. Use **search suppression rules** to prevent matching search queries from returning results.

Each **search rule** has three main components:

- **Conditions** – Query-based requirements that trigger an action when the shopper's search matches.
- **Events** – The actions that take place when the conditions are met (manual ranking and related events).
- **Details** – The name of the rule, and optional time frame and description.

**Category rules** use **category selection** instead of search query conditions; intelligent ranking and manual ranking work the same way as for search, with differences called out in [Create and Manage Rules](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add).

You can combine multiple conditions and actions for search rules, and schedule rules to be active for a period. Search suppression rules use query conditions to block results rather than rank products. You can also set a **default search rule** that applies when no more specific search or category rule applies.

## Search suppression rules {#search-suppression-rules}

Search suppression rules are a merchandising rule type that blocks results for matching shopper queries. Those searches return no products on the storefront. After the rule becomes active, verify the storefront's actual no-results presentation.

Use search suppression for regulatory search restrictions, branding restrictions, or specific terms that should not return results. Conditions support **Query is**, **Query contains**, **Query starts with**, and **Query ends with**. For configuration and management steps, see [Create and manage search suppression rules](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#search-suppression-rules). For examples, see [Best practices](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/best-practice#search-suppression-best-practices).

Search suppression affects only the search experience. It does not change product visibility through category navigation, merchandising pages, recommendations, or direct product URLs. It is not a substitute for catalog-wide product visibility or access controls.

### Interaction with other merchandising capabilities

| Capability | Interaction with search suppression |
| --- | --- |
| Search rules | For a query matched by an active search suppression rule, the storefront displays a search-results page with zero products.. Ranking actions in a search rule do not override the suppression. Queries that are not blocked continue to use applicable merchandising rules.  |
| Category rules | Category navigation and category merchandising are unaffected by search suppression. A product can remain visible in a category even when a search query for it is blocked. |
| Default search rule | Search suppression blocks matching queries, whereas the default search rule defines default ranking and product exclusions. Default ranking does not restore results for a blocked query. |
| Attribute Based Merchandising Events | These events apply actions to products that match attribute conditions, as described in [Attribute ranking](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add#attribute-ranking). Search suppression instead blocks results for a matching query, regardless of which products would otherwise match. |

Products excluded by the **default search rule**, through either manual exclusions or **Attribute Based Merchandising Events** with a **Hide** action, are also excluded from **search suggestions and autocomplete**. This keeps product exclusions consistent across the search experience and is separate from blocking a query with a search suppression rule.

## Category rules {#category-rules}

**Category rules** control product order on **category pages**. You select one or more categories, then apply intelligent ranking (for example, most viewed, trending) and manual actions such as pin, boost, and bury. They do not use search query conditions. For setup steps, rule types, and how ranking applies on category versus search, see [Create and Manage Rules](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add).

## Requirements

A simple **search rule** can have a single condition and a single event, while a complex rule can have up to ten conditions that trigger up to 25 events. **Category rules** follow the same event limits for manual ranking; they do not use query conditions.

Rules can have:

- Up to ten **conditions** (search rules only)
- Up to 25 **events**

Query text can contain:

- Alphanumeric characters (letters and numbers)
- Either upper or lowercase characters. Capitalization is ignored.

## Logical operators

The logical operators `AND` and `OR` join two conditions and return different results. All logical operators used in a rule with multiple conditions are the same. It is not possible to use both `AND` and `OR` in the same rule.

### Match operators

The Match operators `All` and `Any` determine the logical operator that is used to join multiple conditions in the rule, and can be used to change the existing operator.

- `All`—Uses the `AND` logical operator to join multiple conditions. A rule that uses the `All` Match operator can have only one `Search query is` condition.
- `Any`—Uses the `OR` logical operator to join multiple conditions.

When composing a complex rule, it can help to write it out with indentation to describe the conditions, associated events, and product names or SKUs that are needed to return the results you want to achieve. Then, build the rule and test the result.

## Default rule

You can set a **default search rule** that applies when no search term is provided, or no other search rule can be applied. If you set the default rule to "Most Purchased", then queries default to that ranking type unless superseded by a more specific search term. No search term can be set for the default rule. **Category rules** are separate: they apply only to the categories you select and do not replace the default listing rule.

## Order of precedence with multiple rules

This section explains how ranking search rules apply to a shopper's query and interact with one another. Search-rule ranking does not override search suppression: when an active suppression rule matches a query, the storefront returns no products for that search. Category rules apply to selected categories. See [Create and Manage Rules](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/add) for details about search, category, and default search rules.

Only one search rule is applied to a search term at any one time.
If multiple rules are found to be applicable to a search phrase, then all these rules are applied. If there is a collision between two rules---`rule 1` that boosts sku1 but `rule 2` hides the same SKU---then the most recently applied rule (`rule 2`) takes precedence.

- Rules are ordered by the "Last Modified" timestamp. The most recently modified rule is applied first, and older rules after that, in timestamp order.
- The `query is` condition takes precedence over other conditions. If a newer rule contains a `query contains` condition, but an older rule has a `query is` condition, the `query is` rule is applied.

### Storefront requests

If an active rule containing a `query is` condition matches the search phrase, it is applied. If there are multiple matching rules with a `query is` condition, the most recently updated active rule is applied.
Otherwise, the most recently updated active rule is applied.

### Preview requests

Requests made in preview work slightly differently. When previewing, all rules are applied, including those expired and scheduled.

- If rule being previewed has a `query is` condition, it is applied.
- If rule being previewed does not have a `query is` condition, and a subsequent active, matching rule with a `query is` condition is found, the `query is` rule is applied.
- If rule being previewed does not have a `query is` condition, and no other rule with a `query is` condition is found, then the rule being previewed is applied.
