# Facets Best Practices

Filter and facet functionality is a critical component of Commerce experiences, designed to enhance the shopper experience by allowing shoppers to narrow down search results and find products more efficiently. This functionality helps shoppers sort through vast catalogs of items by applying specific criteria, making the shopping process faster, easier, and more satisfying. By implementing effective, shopper-friendly filters and facets, you can help customers find exactly what they need quickly and efficiently, ultimately boosting satisfaction and conversion rates.

## Tips to optimize facets

- Determine relevant product attributes, such as title, category, brand, price range, color, and size, and set them as [dynamic facets](type.md). 
- Set and sort product attributes that are consistent across your catalog and highly relevant for your products to improve relevancy and filtering capabilities for your shoppers.
- Ensure that facet labels are easy to understand and consistently named across the site. For example, use `Price Range` instead of `Cost`.
- Avoid overwhelming shoppers by limiting the number of facets to the most important ones. Too many options can cause decision fatigue. The facet configuration supports up to 100 attributes configured as facets and up to 100 values per facet. Learn more about [facet limitations](/help/optimizer/boundaries-limits.md#product-discovery).
- Allow shoppers to select multiple filter criteria simultaneously to refine results. For example, letting shoppers select both "Red" and "Blue" colors.
- Display the number of available products next to each facet option to give shoppers an idea of the search results they can expect.
- To keep the interface clean and manageable, especially on mobile devices, implement collapsible facet sections.
- Allow shoppers to reset individual facets or all selected filters to start a new search easily.
- If you have a large number of attributes, consider combining attributes into a single meta-attribute. For example, shoes have numeric sizes, while shirts are commonly sized "S/M/L/XL". These two types of sizes can be combined into a single searchable attribute.
