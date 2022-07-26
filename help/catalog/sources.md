---
title: Product settings - Sources
description: <placeholder>
---
# Product settings - Sources

The _Sources_ section of the product settings lists the sources from which the product can be distributed. It is used to assign and unassign sources as well as manage the quantity and availability of the product. This section is displayed only if there is more than one source defined for your store. For more information about sources, see [Manage sources](../inventory-management/sources-manage.md).

## Assign a source for a product

1. Click **Assign Source**.

1. Select the checkbox for the required sources.

1. Click **Done**.

1. Select **Source Item Status** , fill in the **Qty** and **Notify Qty** fields as needed.

1. Click **Save** to save the changes.

![Sources View](./assets/catalog-sources-list.png)<!-- zoom -->

## Field reference

|Field|Description|
|--- |--- |
|Name|The unique name for a source.|
|Source Status|Determines if the product is enabled or disabled in the catalog.|
|Source Item Status|Determines the current availability of the product. Options:<br />**In Stock** - Makes the product available for purchase.<br />**Out of Stock** - Unless backorders are activated, prevents the product from being available for purchase and removes the listing from the catalog.|
|Qty|On-hand stock amounts for each source.|
|Notify Qty|An amount for the _Notify for Quantity_ for this specific source if `Notify Quantity Use Default` is not selected.|
|Notify Qty Use Default|Indicates to use the default setting for _Notify for Quantity_ in the product Advanced Inventory or global setting in the Store configuration. For more information about advanced inventory settings for your product, see [Configure advanced product options](../inventory-management/product-options.md).|
|Actions|For an assigned source, click **Unassign** to make the source not available for the product. For an unassigned source, click **Assign Sources** to make a source available for the product. For more information about Assign Sources options, see [Assigning Sources per Product](../inventory-management/sources-assign-per-product.md).|
