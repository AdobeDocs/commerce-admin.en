---
title: Catalog price rule with multiple SKUs
description: <placeholder>
---
# Catalog price rule with multiple SKUs

A single catalog price rule can be applied to multiple SKUs, which makes it possible to create a variety of promotions based on a product, brand, or category. When creating this rule, you want to set conditions that match the selected SKUs. When building the rule, you can easily browse and select SKUs from the grid.

## Step 1. Verify storefront properties of the product attribute

Before you begin, make sure that the [Storefront Properties](../catalog/attributes-product.md) of the `sku` attribute are set to `Use in Promo Rules`.

1. On the _Admin_ sidebar, go to **Stores** > _Attributes_ > **Product**.

1. In the search filter at the top of the _Attribute Code_ column, enter `sku` and click **Search**.

1. Click to open the `sku` attribute in edit mode.

1. In the left panel, click **Storefront Properties** and make sure that **Use for Promo Rule Conditions** is set to `Yes`.

1. If you changed the value of the property, click **Save Attribute**.

## Step 2. Apply a price rule to multiple SKUs

1. On the _Admin_ sidebar, go to **Marketing** > _Promotions_ > **Catalog Price Rules**.

1. Do one of the following:

    - Follow the instructions to create a new [catalog price rule](price-rules-catalog.md).
    - Open an existing catalog price rule.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Conditions** section, and do the following:

    - In the first line, set the first parameter to `ANY`.

      ![Catalog price rule condition - ANY](./assets/multiple-skus-condition1.png)<!-- zoom -->

    - Click **Add** (![Add icon](../assets/icon-add-green-circle.png)) at the beginning of the next line and in the list under **Product Attribute**, click `SKU`.

      ![Catalog price rule condition - SKU is one of](./assets/multiple-skus-condition1a.png)<!-- zoom -->

    - For the comparison, you have options. If you want to locate at least one from a list of SKUs, `select is one of`. If you want to locate a group of SKUs that all must be found to apply, select `is`. We recommend selecting `is one of`.

      ![Catalog price rule condition - SKU is one of](./assets/multiple-skus-condition1b.png)<!-- zoom -->

    - To complete the condition, click the more (**…**) link and click the **Chooser** (![List icon](../assets/icon-list-chooser.png)) icon for the list of available products.

      ![Catalog price rule condition - multiple SKUs](./assets/multiple-skus-condition2b.png)<!-- zoom -->

    - Browse, filter, or search to find the SKUs you want to add. In the list, select the checkbox of each product that is to be included. Click **Save and Apply** to add the SKUs to the condition.

      ![Catalog price rule condition - multiple SKUs](./assets/multiple-skus-condition2.png)<!-- zoom -->

1. Complete the rule, including any [Actions](price-rules-catalog.md) to be taken when the conditions are met.

1. When your rule is complete, click **Save**.

{{new-price-rule}}
