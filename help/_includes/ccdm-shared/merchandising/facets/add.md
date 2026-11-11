# Create and Manage Facets

Any filterable product attribute can be used as a facet. Facets help customers filter and find products more easily in your store. This article explains how to add, manage, and configure facets in your storefront.

![Create a Facet](/help/assets/ccdm-shared/facets/create-facet.png)

## Create a facet

1. From the menu, select _Merchandising_ > **Facets** then click **Create facets**.
1. In the *Create facets* list, each available attribute has a separate ![Add button](/help/assets/ccdm-shared/facets/btn-add.png). Complete either of the following:

     - In the *Facets attributes* list, choose the product attribute that you want to use as a facet and click **Add**.
     - To find a specific product attribute, enter the first few characters of the attribute name in the *Search* box. Then, click **Add**.

     The facet is added to the bottom of the *Dynamic facets* list and the *Publish changes* button becomes available.

1. If the facet you want to add cannot be found, use the [Metadata API](https://developer.adobe.com/commerce/services/reference/rest/#tag/Metadata){target="_blank"} to set the `filterable` parameter:

   `"filterable": true`

   The facet becomes available in the storefront the next time the catalog is synchronized with the Merchandising Services data layer. If the facet isn't available after two hours, see [data sync](../../setup/data-sync.md).

## Edit facet properties (optional)

1. Find the facet that you want to edit.
1. Click the (![More selector](/help/assets/ccdm-shared/recommendations/btn-more.png)) more selector.
1. On the menu, click **Edit**. Then, adjust the following properties as needed:

   - Label—Enter the facet label that you want to use.
   - Sort type—Choose one of the following:
      - Alphabetical—Sorts facets alphabetically
      - Count—Sorts facets based on the number of matches found
   - Max Value—Enter the maximum number of facet values displayed in the storefront. Valid entries: 0 - 100; Default: 8.

1. When complete, click **Save**.

## Pin/unpin facets

The pin changes color when clicked and is used to move the facet to either the *Pinned Facets* or the *Dynamic Facets* section.

1. To pin a facet to the top of the *Filters* list, find the facet in the *Dynamic Facets* list and click the gray pin (![Pin selector](/help/assets/ccdm-shared/facets/btn-pin-gray.png)).

   The pin turns blue and the facet moves to the *Pinned Facets* section.

1. To unpin a facet, find the facet in the *Pinned Facets* list and click the blue pin (![Pin selector](/help/assets/ccdm-shared/facets/btn-pin-blue.png)).

   The pin turns gray and the facet moves to the *Dynamic Facets* section.

>[!NOTE]
>
>Pinned facet ordering may be inconsistent if there are two labels with the same name.

## Delete facets

1. Find the facet in the list and click the (![More selector](/help/assets/ccdm-shared/recommendations/btn-more.png)) more selector.
1. Click **Delete**.
1. When prompted to confirm, click **Delete facet**.
   The facet is removed from the storefront after the changes are published.

## Publish changes

1. To update the storefront with your changes, click **[!UICONTROL Publish]**.
1. Wait about 15 minutes for the updates to appear in your store.

## Additional information

- To configure price faceting intervals and groupings, see [Settings](../../settings.md).
- Learn more about the [types](type.md) of facets.
