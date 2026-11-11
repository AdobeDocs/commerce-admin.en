# Catalog layers

Catalog layers allow you to modify product data without changing the original source data. Layers modify product attributes, such as name, description, images, links, and metadata, by creating a layer on top of your base catalog. Your original product data remains intact, allowing you to customize products safely and revert changes at any time.

![Catalog Layers](/help/assets/ccdm-shared/setup/catalog-layers.png)

## Access the Catalog views workspace

You manage catalog layers from the *Catalog views* workspace by selecting a catalog view. How you open the workspace depends on the product you use:

- **Adobe Commerce Admin** (Adobe Commerce as a Cloud Service)—Select *Catalog* > **Catalog views**.
- **Adobe Commerce Optimizer Studio**—Select *Store setup* > **Catalog views**.

## How catalog layers work

When a customer views your storefront, the system combines your base catalog data with active catalog layers to display the final product information. The process works as follows:

1. **Layer application**—When a request is made with a channel ID and environment ID, the store service retrieves the relevant catalog view.

1. **Data merging**—The system applies catalog layers to product data based on layer priority order.

1. **Field handling**—Different field types are processed differently:

   * **Override fields**—Text fields like name, description, and meta titles are replaced with layer values, and the higher-priority layer takes precedence.
   * **Merge fields**—Array fields like images, links, and attributes are combined from multiple layers, providing a unified response.

1. **Priority resolution**—The order field determines which layer takes precedence. When multiple layers modify the same field, the layer with the higher order number has higher priority (for example, order 10 is the highest).

## Catalog layer use cases

Catalog layers are commonly used for:

* **SEO optimization**—Override product meta titles and descriptions based on AI recommendations from [Sites Optimizer](../manage-results/opportunities.md).
* **Seasonal campaigns**—Temporarily update product names, descriptions, or images for promotions without changing source data.
* **Regional customization**—Display different product information based on geographic location or language.
* **A/B testing**—Test different product presentations to optimize conversion rates.
* **Multi-brand management**—Customize product attributes for different brand catalog views.
* **Product Visuals**—Apply product images from AEM Assets as a layer on top of your base catalog.

## AEM-Assets layer

This layer contains product images synchronized from AEM Assets. Like other catalog layers, it is populated via the [Product Layers API](https://developer.adobe.com/commerce/services/reference/rest/#tag/Product-Layers){target=_blank}. The Assets Integration Service transforms AEM asset metadata and delivery URLs into the API format and sends the data automatically when assets are approved in AEM Assets.

The integration supports one source per tenant (one locale + one layer).

### How the AEM-Assets layer works

1. **Automatic creation**: The layer is created when the AEM Assets Integration is configured for your instance.

1. **Image synchronization**: When assets are approved in AEM Assets, Assets Integration Service transforms the asset data and updates the `AEM-Assets` layer via the Product Layers API.

1. **Layer assignment**: Assign the `AEM-Assets` layer to catalog views where you want AEM Assets images to appear.

### Assign the AEM-Assets layer to a catalog view

>[!CAUTION]
>
> Assign the AEM-Assets layer to your catalog view. If the layer is not assigned, product image data is overwritten unexpectedly.

To display AEM Assets images on your storefront:

1. From the Catalog Views workspace, select the catalog view where you want to apply the layer.

1. In the catalog layers section, locate the **AEM-Assets** layer.

1. To enable the layer for this catalog view, activate it.

1. Click **[!UICONTROL Save]** to apply the changes.

Once assigned, the Merchandising Services and Storefront GraphQL APIs return both base catalog images, and AEM Assets images for products.

## Add a catalog layer via data ingestion

You can add catalog layers to your products during the data ingestion process. This method is ideal for bulk operations or automated workflows. You import catalog layers using the ingestion API, but [setting the order](#manage-layer-priorities) of the layers is done using the UI.

**Prerequisites:**

* API credentials with permission to access the data ingestion service
* Product SKUs that already exist in your base catalog

**Steps:**

1. Prepare your layer data in the required format with the product attributes you want to modify.

1. Use the Product Layers API endpoint to ingest the layer data.

1. Verify the layer was successfully ingested by checking the catalog view configuration.

For detailed API specifications and payload examples, see [Product Layers](https://developer.adobe.com/commerce/services/reference/rest/#tag/Product-Layers){target=_blank} in the developer documentation.

## Add a catalog layer manually in the UI

The catalog view UI allows you to create and manage layers manually, which is particularly useful for integrations like Sites Optimizer that generate AI-powered recommendations. For bulk layer operations, use the data ingestion API method [described above](#add-a-catalog-layer-via-data-ingestion).

If a Sites Optimizer layer does not exist in your catalog view, the auto-fix feature in Sites Optimizer automatically creates one and assigns it the highest priority (highest number). If you delete this layer, it is recreated the next time the auto-fix feature in Sites Optimizer runs and shifts existing layers to lower order numbers. If the Sites Optimizer layer already exists at a different order number, the auto-fix feature does not change its priority.

**To create a manual layer:**

1. From the **[!UICONTROL Catalog views]** workspace, select the catalog view where you want to apply the layer.

1. In the catalog layers section, click **Add catalog layer**.

1. Configure the layer properties:

   * **Layer name**—Enter a descriptive name to identify the layer purpose.
   * **Products**—Select the products to which this layer applies.
   * **Attributes**—Choose which product attributes to modify (name, description, images, meta tags, and so on).
   * **Values**—Enter the new values for each selected attribute.

1. Click **[!UICONTROL Save]** to create the layer.

The new layer is added to the catalog view and is automatically assigned the next available order number.

## Preview layer effects


Before activating layers or changing priorities, you can preview how they affect product data.

**To preview layer changes:**

1. From the **[!UICONTROL Catalog views]** workspace, select the catalog view with the layers you want to preview.

1. In the catalog layers section, select a specific product or use the preview function.

1. Review the combined product data showing how layers modify the base catalog values.

1. Make adjustments to layer content or priority order as needed.

## Manage layer activation and deletion

You can enable or disable catalog layers without deleting them, allowing you to control when specific customizations are applied.

**To activate or deactivate a layer:**

1. From the **[!UICONTROL Catalog views]** workspace, select the catalog view containing the layer.

1. In the catalog layers section, locate the layer you want to toggle.

1. Click the activation toggle to enable or disable the layer.

   * **Active**—The layer is applied to product data.
   * **Inactive**—The layer is preserved but not applied to product data.

1. The change takes effect immediately on your storefront.

**To delete a layer:**

Use the data ingestion API to [delete a catalog layer](https://developer.adobe.com/commerce/services/reference/rest/#operation/deleteProductLayers){target=_blank}.

## Manage layer priorities

The order in which layers are applied determines which values appear on your storefront when multiple layers modify the same product attribute. Managing priorities ensures the correct data is displayed.

**Understanding priority order:**

* Each layer is assigned an order number (1, 2, 3, and so on)
* Higher numbers indicate higher priority and override all other layers
* When multiple layers modify the same field, the layer with the higher order number takes precedence
* Priority only applies to override fields (name, description, meta tags)
* Merge fields (images, links, attributes) combine data from all layers

**To reorder layer priorities:**

1. From the **[!UICONTROL Catalog views]** workspace, select the catalog view containing the layers you want to reorder.

1. In the catalog layers section, locate the layer you want to move.

1. Drag and drop the layer to change its position, or use the reorder controls.

1. The system automatically updates order numbers based on the new sequence.

1. Click **[!UICONTROL Save]** to apply the new priority order.

>[!IMPORTANT]
>
>Changes to layer priority take effect immediately and impact what customers see on your storefront. Review the preview before saving to ensure the correct values are applied.

## Best practices

Follow these recommendations when working with catalog layers:

* **Use descriptive names**—Name layers clearly to indicate their purpose (for example, "Holiday 2025 Campaign" or "SEO Optimization — Product Pages").

* **Limit layers**—While the system supports multiple layers, using too many can impact performance. Consolidate layers when possible.


* **Document priority logic**—Keep track of which layers take precedence to avoid unintended overrides.

* **Review Sites Optimizer layers**—When using auto-fix from Sites Optimizer, the system creates layers at the highest priority. Be mindful when adding manual layers that override AI recommendations. Learn more about using [Sites Optimizer](../manage-results/opportunities.md).

* **Monitor performance**—If you notice slow product page loads, review your layer configuration and consider consolidating layers.

## More like this

* [Catalog views](catalog-view.md)—Configure catalog views for different storefronts
* [Product Visuals](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/product-visuals)—Use AEM Assets for product images
* [Opportunities](../manage-results/opportunities.md)—Learn about AI-powered optimization using catalog layers
* [Restricted access keys](restricted-access-keys.md)—Protect a catalog view with signed-token authentication
