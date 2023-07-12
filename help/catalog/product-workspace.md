---
title: Product workspace
description: Learn about the settings and controls available in the product workspace.
exl-id: 8258b117-56d2-4d5f-9413-80d51fd5eae6
feature: Catalogs, Products, Admin Workspace
---
# Product workspace

The product workspace is basically the same for all product types, although the selection of fields changes depending on the attribute set that is used. The product attributes are at the top of the form, followed by expandable sections of product information. When a new product is saved for the first time, the _[!UICONTROL Store View]_ chooser appears at the upper left of the form.

![Product workspace](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## [!UICONTROL Enable Product] setting

The online status of the product is indicated by the switch at the top of the form. To change the online status, set the **[!UICONTROL Enable Product]** switch to `Yes` or `No`.

| Control | Description |
|-------- | ----------- |
| ![Toggle yes](../assets/toggle-yes.png) | Indicates that the product is online. |
| ![Toggle no](../assets/toggle-no.png) | Indicates that the product is offline. |

{style="table-layout:auto"}

## Attribute set

The name of the [attribute set](attribute-sets.md) appears in the upper-left corner and determines the fields that appear in the product record. To choose a different attribute set, click the down arrow next to the default attribute set name.

![Attribute set](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## Expand/collapse

To expand or collapse a section, click either the expand ![Expansion selector](../assets/icon-display-expand.png) or collapse ![Collapse selector](../assets/icon-display-collapse.png) icon.

## [!UICONTROL Save] menu

The _[!UICONTROL Save]_ menu includes several options that let you save and continue, save and create a product, save and duplicate the product, or save and close.

![Save menu](./assets/product-save-menu.png){width="600" zoomable="yes"}

|Command|Description|
|--- |--- |
|[!UICONTROL Save]|Save the current product and continue working.|
|[!UICONTROL Save & New]|Save and close the current product, and begin a new product based on the same product type and template.|
|[!UICONTROL Save & Duplicate]|Save and close the current product, and open a new duplicate copy.|
|[!UICONTROL Save & Close]|Save the current product and return to the _[!UICONTROL Products]_ workspace.|

{style="table-layout:auto"}

## Default field values

To save time when creating products, the default value of several product fields references values from another field. You can either accept the default value or enter another. The following fields have automatically generated default values:

|Field |Default |
|----- |------- |
|[!UICONTROL SKU]|Based on product name. |
|[!UICONTROL Meta Title]|Based on product name. |
|[!UICONTROL Meta Keywords]|Based on product name. |
|[!UICONTROL Meta Description]|Based on product name and description. |

{style="table-layout:auto"}

The placeholders that represent the value of another field are enclosed in double-curly braces. Any attribute code that is included in the product [attribute set](attribute-sets.md) can be used as a placeholder.

![Product Fields Auto-Generation](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

For a detailed list of these settings, see [Product Fields Auto-Generation](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) in the _Configuration Reference_.

### Edit the placeholder value

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Product Fields Auto-Generation]** section and make any needed changes to the placeholder values.

   For example, if there is a specific keyword that you want to include for every product or a phrase that you want to include in every meta description, enter the value directly into the appropriate field.

   >[!NOTE]
   >
   >If you want to keep the existing placeholder values, preserve the double curly braces that enclose each markup tag.

1. When complete, click **[!UICONTROL Save Config]**.

### Common placeholders

- `{{color}}`
- `{{country_of_manufacture}}`
- `{{description}}`
- `{{gender}}`
- `{{material}}`
- `{{name}}`
- `{{short_description}}`
- `{{size}}`
- `{{sku}}`
