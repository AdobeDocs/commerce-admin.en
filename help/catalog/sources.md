---
title: Product settings - [!UICONTROL Sources]
description: For a product, the [!UICONTROL Sources] settings provides access to the [!DNL Inventory Management] sources from which the product can be distributed.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
TQID: https://experienceleague.adobe.com/7LFF4ufXyKtJwUp4DiNDdnRMhFRsM1tX8Z2TlPt1Kso
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Product settings - [!UICONTROL Sources]

The _[!UICONTROL Sources]_ section of the product settings lists the sources from which the product can be distributed. It is used to assign and unassign sources as well as manage the quantity and availability of the product. This section is displayed only if there is more than one source defined for your store. For more information about sources, see [Manage sources](../inventory-management/sources-manage.md).

## Assign a source for a product

1. Click **[!UICONTROL Assign Source]**.

1. Select the checkbox for the required sources.

1. Click **[!UICONTROL Done]**.

1. Select **[!UICONTROL Source Item Status]** and enter the **[!UICONTROL Qty]** and **[!UICONTROL Notify Qty]** values as needed.

1. Click **[!UICONTROL Save]** to save the changes.

![Sources View](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Field reference

|Field|Description|
|--- |--- |
|[!UICONTROL Name]|The unique name for a source.|
|[!UICONTROL Source Status]|Determines if the product is enabled or disabled in the catalog.|
|[!UICONTROL Source Item Status]|Determines the current availability of the product. Options:<br />**[!UICONTROL In Stock]** - Makes the product available for purchase.<br />**[!UICONTROL Out of Stock]** - Unless backorders are activated, prevents the product from being available for purchase and removes the listing from the catalog.|
|[!UICONTROL Qty]|On-hand stock amounts for each source.|
|[!UICONTROL Notify Qty]|An amount for the _Notify for Quantity_ for this specific source if `Notify Quantity Use Default` is not selected.|
|[!UICONTROL Notify Qty Use Default]|Indicates to use the default setting for _Notify for Quantity_ in the product Advanced Inventory or global setting in the store configuration. For more information about advanced inventory settings for your product, see [Configure advanced product options](../inventory-management/product-options.md).|
|[!UICONTROL Actions]|For an assigned source, click **[!UICONTROL Unassign]** to make the source not available for the product. For an unassigned source, click **[!UICONTROL Assign Sources]** to make a source available for the product. For more information about [!UICONTROL Assign Sources] options, see [Assigning Sources per Product](../inventory-management/sources-assign-per-product.md).|

{style="table-layout:auto"}

