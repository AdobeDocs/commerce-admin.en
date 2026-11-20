# Create and Manage Rules

Building a rule requires selecting the catalog view where the rule applies, configuring the rule description, type, and defining its conditions and ranking, testing the results, and publishing the rule.

## Create a rule {#create-a-rule}

1. From the menu, go to _Merchandising_ > **Merchandising Rules**.
1. (Optional) Select the catalog view where the rule applies using the **Catalog view** dropdown.
    The rule you create is scoped to the selected view (or to all catalog views if **All views** is selected). See [Select catalog view](workspace.md#select-catalog-view) for how catalog view scoping works.

1. Click **[!UICONTROL Create rule]** to launch the rule editor.

   ![Create Rule](/help/assets/ccdm-shared/rules/create-rule.png){zoomable="yes"}

### Rule types

Each rule type has an information icon in the editor with a short explanation. Use the type that matches where shoppers see the merchandising logic:

| Rule type | Purpose |
| --- | --- |
| **Default search rule** | Default ranking and merchandising across product listings when no more specific search or category rule applies. You can only create one such rule; it cannot contain conditions. |
| **Category rule** | Applies merchandising and ranking to a single category, controlling product order on that category page. |
| **Search rule** | Applies merchandising and ranking when shoppers run a search that matches the rule's query conditions. |

In the **Build your rule** section, you define the rule name, schedule, whether the rule applies to all listings or to specific search conditions, and ranking types.

1. In the **[!UICONTROL Name]** field, enter a name for the rule. All rule names must be unique.
1. In the **[!UICONTROL Description]** field, enter a description for the rule.
1. In the **[!UICONTROL Date range]** field, specify the date or range of dates you want the rule to be active.
1. In the **[!UICONTROL Rule applies to]** section, select the [rule type](#rule-types) you want to use.

>[!BEGINTABS]

>[!TAB Search rule]

A search rule applies merchandising and ranking logic when shoppers perform a search that matches the defined conditions.

The conditions are the requirements to trigger an event. A rule can have up to ten conditions and 25 events. A default rule cannot have any conditions.

![Select Rule Condition](/help/assets/ccdm-shared/rules/rule-set-condition.png){zoomable="yes"}

**Single condition**

1. Under *Build your rule*, select the **Condition** to be met, and follow the instructions to complete the statement.

   - Search query contains—Enter the string of text that must be in the shopper's query. The Match setting determines the degree to which the shopper's query matches the catalog. Options:<br /> Any—Any part of the shopper's query text can match the condition.<br />All—All of the shopper's query must match the condition.
   - Search query is—Enter a string of text that exactly matches the shopper's query. For example: "yoga pants". Rules with `Search query is` and Match `All` can have only one condition.
   - Search query starts with—Enter a character or string of text that must be at the beginning of the shopper's query.
   - Search query ends with—Enter a character or string of text that must be at the end of the shopper's query.

   The *Test your rule* pane displays results immediately, numbered by priority. You can use the *Results per row* slider in the upper right to change the number of products in each row.

1. To test other queries, change the query text in the *Test your rule* search box and press **Return**.
   Initially, the test pane renders the query from the Conditions search box. However, it is now rendering the query from the test query box. The test pane renders only one query at a time.
1. If you like the result, update the text in the *Conditions* search box. Then, click anywhere on the page to update the results in the test pane.
1. Optionally, set [Intelligent ranking](#intelligent-ranking), [Manual ranking](#manual-ranking), or [Attribute ranking](#attribute-ranking) as described in the following sections. The same controls apply to category pages, with any differences called out.

**Multiple conditions**

1. To build a rule with multiple conditions, click **Add condition**.
   A rule can have up to ten conditions. The logical operator that joins two conditions is based on the current *Match* setting. By default, *Match* is `All` and the logical operator is `AND`.

1. Select the second condition and enter the required query text.

1. To change the logic of the rule, change the **Match** setting to determine how closely the shopper's search criteria must match the query condition. Set **Match** to one of the following:

   - Any—(Default) All logical operators in the rule are set to `OR` and the results appear in the test pane.
   - All—All logical operators in the rule are set to `AND` and the results appear in the test pane.

   The *Match* value determines the logical operator that is used to join multiple conditions. Changing the *Match* setting changes all logical operators in the rule. It is not possible to combine `AND` and `OR` in the same rule.

   In this example, rather than searching for "yoga pants", there are two separate queries that search for "yoga" or "pants". This rule is less specific and is triggered more frequently in the storefront than the other rule.

1. To add another condition, click **Add condition** and repeat the process.
1. Optionally, set [Intelligent ranking](#intelligent-ranking), [Manual ranking](#manual-ranking), or [Attribute ranking](#attribute-ranking) as described in the following sections. The same controls apply to category pages, with any differences called out.

>[!TAB Category rule]

Category rules control how products are ordered on **category pages**. Combine **category rules** with **intelligent ranking** and **manual** actions to curate discovery, run promotions, and align category pages with your strategy.

**Select categories**

Under **Categories**, select one or more categories for the rule. Selected categories appear below the control so you can confirm the scope. Select categories in either of the following ways:

- **Browse the category tree**—To load immediate child categories, expand a category. To navigate to a deeper level, expand the child category. The tree loads one level at a time.
- **Search by category name**—Enter a category name in the **Search and select categories** field. Search results include matching category names from across the catalog, including categories outside the currently expanded branch. Search does not match category path text.

When multiple categories have similar names, use the category path displayed with each result (for example, `brakes/aurora`) to select the correct category.

>[!NOTE]
>
>Expanding a category only loads its child categories for browsing. It does not select the category or apply the rule to its subcategories. Select a category to add it to the rule. To apply the rule to a category's subcategories, use **Apply to subcategories** from the category's action menu, described below.

>[!TIP]
>
>If a child category is not visible, expand its parent category to load the next level. If you know the category name, use the search field instead of navigating through the tree. This behavior is useful for large catalogs, since category levels load on demand.

1. From the list of selected categories, click the three dots next to a category and select to:

   - **Delete**—Removes the category from the rule.
   - **Apply to subcategories**—Applies the rule to subcategories that do not already have an active merchandising rule defined.
   - **Preview**—Displays how the category page appears on your storefront.

1. Optionally, set [Intelligent ranking](#intelligent-ranking), [Manual ranking](#manual-ranking), or [Attribute ranking](#attribute-ranking) as described in the following sections. The same controls apply to search rules, with any differences called out.

   ![Category Action Menu](/help/assets/ccdm-shared/rules/category-action-menu.png){zoomable="yes"}

>[!ENDTABS]

### Intelligent ranking {#intelligent-ranking}

Intelligent ranking orders products using **behavioral signals** and, where applicable, AI. It applies to **search rules**, **default search rules**, and **category rules** (category pages). For shopper **searches**, ranking also weighs **textual relevance** to the query; **category pages** do not use query text in the same way—the editor focuses on behavioral strategies.

Store owners can set strategies such as the following. Exact labels and time windows match the rule editor and differ slightly by rule type.

![Intelligent Rankings](/help/assets/ccdm-shared/rules/rule-intelligent-ranking.png){zoomable="yes"}

- **Most purchased** / **Most bought**—Ranks by purchase frequency per SKU in a recent window (for example, the previous 7 days for search contexts).
- **Most added to cart**—Ranks by total add-to-cart activity in a recent window (for example, the previous 7 days for search contexts).
- **Most viewed**—Ranks by views per SKU in a recent window (for example, the previous 7 days for search contexts).
- **Recommended for you**—Uses the `viewed-viewed` signal: shoppers who viewed this SKU also viewed other SKUs; supports personalized ordering on category pages where available.
- **Trending**—Emphasizes recent popularity (for search, page views over the past 72 hours for background events and 24 hours for foreground events).
- **None**—For search and default listings, products are ordered by **Relevance**. For **category rules**, uses the default merchandising order for the category when you do not choose another intelligent strategy.

Select the strategy for your rule. The **[!UICONTROL Test your rule]** pane shows expected results for search-oriented rules; **category rules** use the category preview.

#### Behavioral signals for configurable products and variants {#behavioral-signals-variants}

Intelligent ranking collects behavioral signals against the specific product a shopper interacts with. For a configurable product, this means signals are recorded at the **variant** (simple product) level, not against the configurable parent.

When ranking a configurable product, intelligent ranking aggregates the behavioral signals collected from all of its variants and rolls them up to the configurable parent. A configurable product's ranking score reflects the combined signals of every variant.

This aggregation happens within the scope of the category being browsed. A variant only contributes its behavioral signals to the configurable parent's ranking score for categories to which that **variant** is assigned. If a variant is missing from a category, its signals do not count toward the parent's ranking in that category, even when the configurable parent itself is assigned there.

**Best practice:** Review category assignments for all product variants. Confirm that every variant is assigned to each category where it influences ranking.

**Example:**

A merchandiser organizes a catalog into size-specific subcategories, such as **200g** and **500g**. A configurable product has two variants, one for each size. If only the 200g variant is assigned to the 200g category, purchases and views of the 500g variant do not contribute to the configurable product's ranking score on that page. This behavior is true even if the 500g variant sells well elsewhere. The configurable product may then rank lower than expected, or inconsistent with actual sales performance, on the 200g category page. Assigning both variants to their respective categories resolves the mismatch.

#### Intelligent ranking boost {#intelligent-ranking-boost}

For **Recommended for you**, **Most viewed**, **Most purchased**, **Most added to cart**, and **Trending**, the editor shows **[!UICONTROL Intelligent Ranking Boost]** (the boost factor). It is not used when you select **None**.

Use this control to balance how **behavioral signals** influence ordering relative to **textual relevance** on search, and relative to other ranking signals on **category pages** and **default listings**. The boost is available for **search rules**, the **All products rule**, and **category rules**; each rule stores its own value.

| Behavior | Detail |
| --- | --- |
| Default | `50`. |
| Range | From `1` (gentler behavioral influence) through `1000` (stronger influence). |
| Scope | Applies only to queries or listings that the rule targets. Other rules keep their own boost values. |
| Preview | The rule preview uses the same boost as live results for that rule. |
| Indexing | Applied at **query time**; you do not need a catalog resync or full reindex solely because you changed this setting. |

**When to increase or decrease the boost**

- **Increase** the boost when strategies such as **Most viewed** should surface high-engagement SKUs more aggressively for ambiguous or broad queries, without hand-pinning every slot.
- **Decrease** the boost when you want textual match quality to drive the list more strictly and behavioral data to nudge order only slightly.

**When to use manual ranking instead**

Use **pin**, **boost**, or **bury** to place products in exact positions or guarantee visibility regardless of catalog-wide signals. **[!UICONTROL Intelligent Ranking Boost]** tunes a **global** behavioral weight for that rule, but does not replace SKU-level control.

>[!NOTE]
>
> A high **[!UICONTROL Intelligent Ranking Boost]** can outweigh a **manual boost** on the same product. If a boosted SKU ranks lower than you expect in the rule preview or on the storefront, lower **[!UICONTROL Intelligent Ranking Boost]** or **pin** the product to a specific position. Either change moves the manually ranked product higher in the listing.

#### How intelligent ranking scoring works (search)

For **search results** (and the test query in the rule editor), intelligent ranking determines the final product order by combining two key factors: **textual relevance** and **behavioral signals**. Understanding how these factors interact helps you set realistic expectations for your search results.

**Scoring components:**

- **Textual relevance**: The dominant factor in scoring. This measures how well a product's name, description, and attributes match the search query. The text relevance score is unbounded (has no specific upper limit), and factors like these influence it:

   - Frequency of occurrence of matching words.
   - Length (in words) of product names/descriptions.

- **Behavioral signals**: A bounded boost applied on top of the text relevance score. When you select an intelligent ranking strategy like "Most viewed" or "Most purchased," products with higher behavioral signals receive a larger relative weight. The strength of that weight is controlled by **[!UICONTROL Intelligent Ranking Boost]** (see [Intelligent ranking boost](#intelligent-ranking-boost)). The boost remains bounded, but you can increase how much it shifts ordering.

**Why the most viewed product might not appear first:**

Textual relevance often dominates ranking because its score is unbounded, while the boost model caps behavioral influence. Products with very strong text matches can still outrank SKUs with higher engagement unless you raise **[!UICONTROL Intelligent Ranking Boost]** for that rule. Even at higher boost values, an extreme text relevance gap may not fully invert the list; text match quality remains a primary driver. Always confirm in **[!UICONTROL Test your rule]** for the queries you care about.

**Example:**

A merchant uses the "Most viewed" intelligent ranking strategy and searches for **candle**. They expect product SKU YAN-K-E-512 to appear at the top of results because it has the highest view count. However, other products rank higher:

- **Texas Candle** (1st position): Has a shorter, cleaner product name that creates a high text relevance score. Even though it has fewer views than **YAN-K-E-512**, its superior text match outweighs the behavioral boost.

- **YAN-K-E-512** (lower position): Despite having the highest view percentile in the "Most viewed" behavioral data, its complex SKU-based name generates a lower text relevance score. At the default **[!UICONTROL Intelligent Ranking Boost]** (`50`), behavioral influence may not be enough to overcome that text gap. Increasing the boost can move **YAN-K-E-512** higher among products that already match the query. **YAN-K-E-512** must also match the query: at least one searchable attribute for that SKU must include **candle**, or it does not appear in results and the boost cannot apply.

**Example (broad query):**

For a query such as **wood**, several products can share similar textual relevance while view counts differ. With **Most viewed** selected, increasing **[!UICONTROL Intelligent Ranking Boost]** makes the historically most-viewed relevant SKU more likely to surface above lighter matches. Lowering the boost keeps results closer to pure textual ordering.

To improve product findability using rules, see [search rules](best-practice.md#tips-to-optimize-search-rules).

#### Caveats

- Apostrophes and quotes in queries may lead to some minor issues with ranking and relevance in some languages.
- If intelligent ranking results do not correlate with actual sales or view performance, confirm that all relevant product variants are assigned to the category being reviewed. Missing variant category assignments are a common and easily overlooked cause of unexpected ranking behavior. See [Behavioral signals for configurable products and variants](#behavioral-signals-variants).
- To ensure intelligent ranking works correctly for **search**, make sure that the **Search Weight** for any attributes that are used for search or filtering (facets) is `5` or less. (This guidance applies to search indexing, not to category-only merchandising flows.)

For information about setting search weights:

- For all Adobe Commerce deployments, see [Search Results](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/search/search-results) in the _Catalog Management Guide_.
- For stand-alone Adobe Commerce Optimizer deployments, see the [Metadata REST API](https://developer.adobe.com/commerce/services/reference/rest/#operation/createProductMetadata) in the _Merchandising Services Developer Guide_.

### Manual ranking {#manual-ranking}

**Manual ranking** events adjust product order for **search results** (when your rule's conditions are met), for **default product listings**, and for **category page** listings. A single rule can have up to 25 events.

- **[!UICONTROL Boost]**—Moves a SKU higher in the listing.
- **[!UICONTROL Bury]**—Moves a SKU lower in the listing.
- **[!UICONTROL Pin a product]**—Fixes a SKU at the selected position in the listing.
- **[!UICONTROL Hide a product]**—Excludes a SKU from the results (search-oriented; confirm behavior for category rules in the editor).

The easiest way to pin a product is by drag and drop.

1. Click and drag a product in the Test pane. Drag and drop it at the desired position. The Product and Position fields are automatically populated in the Events pane.

   Click the pin icon to pin a product to its current location. Use the ellipsis context menu to "Pin to top" or "Pin to bottom".

>[!NOTE]
>
>**Search rules**—You can only pin products that appear in the search results for the configured query and rule conditions. Products must be indexed, visible, in stock, and meet all rule filters to be eligible for pinning. If a product does not appear in the preview or results for your rule, pinning it has no effect.
>
>**Default sort**—Manual positions apply when the shopper uses the default sort: **Sort by: Most Relevant** for search, or **relevance** / **position** for category listings. If the shopper changes sort, for example by name, pinned, boosted, buried, or hidden behavior may no longer match the preview.

Or events can be set manually:

1. Under *Events*, choose the **Event** to take place when the associated conditions are met.

   For example, choose **[!UICONTROL Hide a product]**. Then, enter the phrase which matches part or the whole name or SKU of the product that you want to hide.

1. For multiple events, choose any other events that you want to trigger when conditions are met.

### Attribute ranking {#attribute-ranking}

>[!AVAILABILITY]
>
>This feature is in [beta](https://experienceleague.adobe.com/en/docs/commerce-operations/release/beta#attribute-ranking-public-beta).

**Attribute ranking** automatically applies a **[!UICONTROL Boost]**, **[!UICONTROL Bury]**, or **[!UICONTROL Hide]** action to every product that matches one or more attribute conditions, without requiring you to select individual SKUs. Attribute ranking appears in the rule editor alongside [Intelligent ranking](#intelligent-ranking) and [Manual ranking](#manual-ranking), and is available for the **All products rule**, **search rules**, and **category rules**. Use it to scale merchandising across large catalogs, for example, boosting every product from a given brand, or burying every product in a discontinued color.

![Attribute Ranking](/help/assets/ccdm-shared/rules/attribute-rank-rule.png){zoomable="yes"}

1. In the rule editor, expand **[!UICONTROL Attribute ranking]**.
1. Click **[!UICONTROL Add attribute]** to add an attribute condition.
1. From the dropdown at the top of the condition, select the action to apply to matching products: **[!UICONTROL Boost]**, **[!UICONTROL Bury]**, or **[!UICONTROL Hide]**.
1. Under **[!UICONTROL Attribute]**, select the product attribute to match, such as **Brand**, **Category**, **Country**, **Manufacturer**, or **Model**. Only filterable, text-based attributes are available.
1. Under **[!UICONTROL Value]**, type a value and press **Return** to add it. To add more values, repeat the process. Each value appears as a removable tag under **[!UICONTROL Selected values]**. A product matches the condition if it has any one of the listed values.

   >[!NOTE]
   >
   >The **[!UICONTROL Value]** field accepts free text and is case sensitive. After adding a value, check the test pane to confirm it matches the expected products.

1. To set how strongly the action moves matching products, drag the **[!UICONTROL Boost strength]** slider for **[!UICONTROL Boost]** and **[!UICONTROL Bury]**.
1. To add another condition, click **[!UICONTROL Add attribute]** and repeat the previous steps.

Pinning is not available in attribute ranking, because pinning assigns one product to one exact position, while an attribute condition can match many products at once. To pin a specific product, use [Manual ranking](#manual-ranking) on that SKU directly.

#### How attribute ranking interacts with intelligent ranking

When a rule combines an intelligent ranking strategy with one or more attribute conditions, the attribute action takes priority for any product it matches. Intelligent ranking continues to order the remaining, unmatched products.

#### When attribute conditions conflict with each other

A single product can match more than one attribute condition, whether within the same rule or across different rules. When matching conditions specify conflicting actions for the same product, **[!UICONTROL Hide]** takes priority over **[!UICONTROL Boost]** and **[!UICONTROL Bury]**.

For example, one condition boosts all products with `season = Christmas`, and another hides all products with `brand = Nike`. A product with `season = Christmas` and `brand = Nike` is hidden, because **[!UICONTROL Hide]** takes priority over **[!UICONTROL Boost]**.

#### Limits

A single rule can have up to 25 attribute conditions, the same limit as manual ranking events.

### Finalizing the rule {#finalizing-the-rule}

1. Examine the results of the rule in the test pane.
1. If the rule has multiple queries, test each one that might be affected by the rule.
1. When complete, click **Save and publish**.

   The rule is added to the list in the *Rules* workspace.

1. Although active rules go into effect immediately, you might have to wait up to 15 minutes for the cached query results in the storefront to be refreshed.

>[!NOTE]
>
>Rules and manually ranked products are applied to **search** results when the default sort order, "Sort by: Most Relevant," is selected. If a shopper changes the sort order to something like sort by name, rules and manual rankings are no longer in effect. For **category** listings, default-sort behavior is described in [Manual ranking](#manual-ranking).

## Edit, view, and delete rules {#edit-view-and-delete-rules}

To update the properties of existing rules, follow these instructions. You cannot change the catalog view (scope) of a rule after it is created; scope is set when you create the rule. See [Select catalog view](https://experienceleague.adobe.com/en/docs/commerce/optimizer/merchandising/rules/workspace#select-catalog-view).

### Edit rule

1. On the *Merchandising rules* workspace, find the rule in the grid that you want to edit and click **More** (...) options.
1. Click **Edit** to access the rule editor.
1. Update the conditions, operators, and events as needed.
1. Update the name, start and end date, and description fields as needed. All rule names must be unique.
1. Test the rule.
1. Publish the changes.
   The rule is added to the list in the *Rules* workspace. Although active rules go into effect immediately, it might take up to 15 minutes for cached query results in the storefront to be refreshed.

### View details

This option provides a quick way to see all the rule parameters, while staying on the *Rules* table.

1. On the *Merchandising rules* workspace, find the rule in the grid that you want to edit and click **More** (...) options.
1. Click **View details** to view the rule parameters.
1. Choose **Edit** or **Delete**, or click the X to close the panel.

### Delete rule

1. On the *Rules* workspace, find the rule in the grid that you want to edit and click **More** (...) options.
1. Click **Delete**.

## Field descriptions {#field-descriptions}

### Conditions (if)

| Condition | Description |
| --- | --- |
| Search query contains | A character or string of text that is included in the shopper's query. The shopper's query needs to match only a single character to meet this condition. |
| Search query is | A character or string of text that exactly matches the shopper's query. Complex queries with multiple conditions cannot be composed when this condition is used. |
| Search query starts with | The shopper's query begins with this character or string of text. |
| Search query ends with | The shopper's query ends with this character or string of text. |

### Logical operators

| Operator | Description |
| --- | --- |
| OR | (Default) The logical operator `OR` compares two conditions and meets the requirements to trigger an event if at least one condition is true. |
| AND | The logical operator `AND` compares two conditions and meets the requirements to trigger an event if both conditions are true. |

### Match operators

| Operator | Description |
| --- | --- |
| Any | Changes all logical operators in the rule to `OR` and returns the set of matching products. |
| All | Changes all logical operators in the rule to `AND` and returns the set of matching products. |

### Manual ranking events

| Event | Description |
| --- | --- |
| [!UICONTROL Boost] | Moves a SKU or range of SKUs higher in the listing (search or category). Each is marked with a "boosted" preview badge in the test results. |
| [!UICONTROL Bury] | Moves a SKU or range of SKUs lower in the listing. Each is marked with a "buried" preview badge in the test results. |
| [!UICONTROL Pin a product] | Attaches a single SKU to a specific position in the listing. The product is marked with a "pinned" preview badge in the test results. |
| [!UICONTROL Hide a product] | Excludes a SKU, or range of SKUs, from the results (search-oriented; confirm for category rules in the editor). |

### Attribute ranking conditions

| Field | Description |
| --- | --- |
| Action | The action applied to every product matching the condition: **[!UICONTROL Boost]**, **[!UICONTROL Bury]**, or **[!UICONTROL Hide]**. |
| [!UICONTROL Attribute] | The filterable, text-based product attribute the condition targets, such as **Brand**, **Category**, **Country**, **Manufacturer**, or **Model**. |
| [!UICONTROL Value] | One or more attribute values that a product must have to match the condition. Type a value and press Return to add it as a tag; a product matches if it has any one of the listed values. |
| [!UICONTROL Boost strength] | For **[!UICONTROL Boost]** and **[!UICONTROL Bury]**, a slider that controls how strongly the action moves matching products. Shown only for **[!UICONTROL Boost]** and **[!UICONTROL Bury]**, not **[!UICONTROL Hide]**. |

### Intelligent ranking controls

| Field | Description |
| --- | --- |
| [!UICONTROL Intelligent Ranking Boost] | When an intelligent strategy other than **None** is selected, this setting controls how strongly behavioral signals influence ranking for that rule. Default `50`; allowed range `1`–`1000`. Applied at query time; rule preview matches live behavior for the configured rule. |

### Details

| Field | Description |
| --- | --- |
| Name | The name of the rule. Rule names must be unique. |
| Rule Type | **Default search rule**, **Query** (specific search conditions), or **Category** (category pages), depending on **Rule applies to**. |
| Start date | The start date of the rule, if scheduled. |
| End date | The end date of the rule, if scheduled. |
| Description | A brief description of the rule. |
