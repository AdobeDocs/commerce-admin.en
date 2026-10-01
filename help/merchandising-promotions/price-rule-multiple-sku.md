---
title: Catalog price rule with multiple SKUs
description: Learn how to apply a single catalog price rule to multiple SKUs.
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
TQID: https://experienceleague.adobe.com/nChe-8VA4V0nrC46PbeKyh7DB4Ta-0lpcezMV3uHEw0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
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
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Catalog price rule with multiple SKUs

A single catalog price rule can be applied to multiple SKUs, which makes it possible to create various promotions based on a product, brand, or category. When creating this rule, you want to set conditions that match the selected SKUs. When building the rule, you can easily browse and select SKUs from the grid.

## Step 1. Verify storefront properties of the product attribute

Before you begin, make sure that the [Storefront Properties](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties) of the `sku` attribute are set to `Use in Promo Rules`.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_ > **[!UICONTROL Product]**.

1. In the search filter at the top of the _[!UICONTROL Attribute Code]_ column, enter `sku` and click **[!UICONTROL Search]**.

1. Click to open the `sku` attribute in edit mode.

1. In the left panel, click **[!UICONTROL Storefront Properties]** and make sure that **[!UICONTROL Use for Promo Rule Conditions]** is set to `Yes`.

1. If you changed the value of the property, click **[!UICONTROL Save Attribute]**.

## Step 2. Apply a price rule to multiple SKUs

1. On the _Admin_ sidebar, go to **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_ > **[!UICONTROL Catalog Price Rules]**.

1. Do one of the following:

    - Follow the instructions to create a [catalog price rule](price-rules-catalog.md).
    - Open an existing catalog price rule.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Conditions]** section, and do the following:

    - In the first line, set the first parameter to `ANY`.

      ![Catalog price rule condition - ANY](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

    - Click _Add_ (![Add icon](../assets/icon-add-green-circle.png)) at the beginning of the next line and in the list under **[!UICONTROL Product Attribute]**, click `SKU`.

      ![Catalog price rule condition - SKU is one of](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}

    - For the comparison, you have options. If you want to locate at least one from a list of SKUs, `select is one of`. If you want to locate a group of SKUs that all must be found to apply, select `is`. We recommend selecting `is one of`.

      ![Catalog price rule condition - SKU is one of](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}

    - To complete the condition, click the more (**…**) link and click the _Chooser_ (![List icon](../assets/icon-list-chooser.png)) icon for the list of available products.

      ![Catalog price rule condition - multiple SKUs](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

    - Browse, filter, or search to find the SKUs you want to add. In the list, select the checkbox of each product that is to be included.
    
    - Click **[!UICONTROL Save and Apply]** to add the SKUs to the condition.

      ![Catalog price rule condition - multiple SKUs](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. Complete the rule, including any [Actions](price-rules-catalog.md) to be taken when the conditions are met.

1. When your rule is complete, click **[!UICONTROL Save]**.

{{new-price-rule}}
