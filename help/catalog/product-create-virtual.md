---
title: Virtual product
description: Learn how to create a virtual product that represents a non-tangible item,  such as a membership, service, warranty, or subscription.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/L981f0c-abmRqbEf3A-8CxTgVyzAuN-u1WDuMZAKSP4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
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
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Virtual product

Virtual products, or digital goods, represent non-tangible items such as memberships, services, warranties, or subscriptions and digital downloads of books, music, videos, or other products. Virtual products can be sold individually or included as part of the [Grouped Product](product-create-grouped.md), [Configurable Product](product-create-configurable.md), or [Bundle Product](product-create-bundle.md) product types.

Aside from the absence of the _[!UICONTROL Weight]_ field, the process of creating a virtual product and a simple product is the same. The following instructions demonstrate the process of creating a virtual product using a [product template](attribute-sets.md), required fields, and basic settings. When you finish the basics, you can complete the other product settings as needed.

>[!NOTE]
>
>PayPal has deprecated support for the sale of digital goods through PayPal Express Checkout. They recommend that you use either [PayPal Payments Standard](../stores-purchase/paypal-payments-standard.md) or any other PayPal payment gateway to process any order that includes virtual products.

![Virtual Product](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## Step 1: Choose the product type

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. On the _[!UICONTROL Add Product]_ ( ![Menu arrow](../assets/icon-menu-down-arrow-red.png){width="25"} ) menu at the upper-right corner, choose **[!UICONTROL Virtual Product]**.

   ![Add Virtual Product](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## Step 2: Choose the attribute set

To choose the [attribute set](attribute-sets.md) that is used as a template for the product, do one of the following:

- Click in the **[!UICONTROL Attribute Set]** field and enter all or part of the name of the attribute set.

- In the displayed list, choose the attribute set that you want to use.

The form is updated to reflect the change.

![Choose Attribute Set](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Step 3: Complete the required settings

1. Enter the **[!UICONTROL Product Name]**.

1. Accept the default **[!UICONTROL SKU]** that is based on the product name or enter another.

1. Enter the product **[!UICONTROL Price]**.

1. Because the product is not yet ready to publish, set **[!UICONTROL Enable Product]** to `No`.

1. Click **[!UICONTROL Save]** and continue.

   When the product is saved, the [Store View](introduction.md#product-scope) chooser appears in the upper-left corner.

1. Choose the **[!UICONTROL Store View]** where the product is to be available.

   ![Choose Store View](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Step 4: Complete the basic settings

1. Set **[!UICONTROL Tax Class]** to one of the following:

   - `None`
   - `Taxable Goods`

1. Enter the **[!UICONTROL Quantity]** of the product that is in stock and do the following:

   - Accept the default **[!UICONTROL Stock Status]** setting of `In Stock`.

      Because a virtual product is not shipped, the **[!UICONTROL Weight]** field is not used.

   - Accept the default **[!UICONTROL Visibility]** setting of `Catalog, Search`.

   >[!NOTE]
   >
   >If you enable [Inventory Management](../inventory-management/introduction.md), single source merchants set the quantity in this section. Multi source merchants add sources and quantities in the Sources section. See the following _Assign Sources and Quantities (Inventory Management)_ section.

1. To assign **[!UICONTROL Categories]** to the product, click the **[!UICONTROL Select…]** box and do either of the following:

   **Choose an existing category**:

   - Start typing in the box until you find a match.

   - Select the checkbox of the category that is to be assigned.

   **Create a category**:

   - Click **[!UICONTROL New Category]**.

   - Enter the **[!UICONTROL Category Name]** and choose the **[!UICONTROL Parent Category]**, which determines its position in the menu structure.

   - Click **[!UICONTROL Create Category]**.

   There might be additional individual attributes that describe the product. The selection varies by attribute set and you can complete them later.

### Assign sources and quantities ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Step 5: Complete the product information

Complete the information in the following sections as needed:

- [Content](product-content.md)
- [Images and Videos](product-images-and-video.md)
- [Search Engine Optimization](product-search-engine-optimization.md)
- [Related Products, Up-Sells, and Cross-Sells](related-products-up-sells-cross-sells.md)
- [Customizable Options](settings-advanced-custom-options.md)
- [Products in Websites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Gift Options](product-gift-options.md)

>[!NOTE]
>
>The _[!UICONTROL Is this downloadable product?]_ option is disabled by default. Enabling this feature for a virtual product makes the product [Downloadable](product-create-downloadable.md#downloadable-product).

## Step 6: Publish the product

1. If you are ready to publish the product in the catalog, set **[!UICONTROL Enable Product]** to `Yes`.

1. Do one of the following:

   - **Method 1:** Save and preview

      - At the upper-right corner, click **[!UICONTROL Save]**.

      - To view the product in your store, choose **[!UICONTROL Customer View]** on the _Admin_ ( ![Menu arrow](../assets/icon-menu-down-arrow-black.png) ) menu.

      The store opens in a new browser tab.

      ![Customer View](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Method 2:** Save and close

      On the _[!UICONTROL Save]_ (![Menu arrow](../assets/icon-menu-down-arrow-red.png){width="25"} ) menu, choose **[!UICONTROL Save & Close]**.

## Things to remember

- Virtual products are used for non-tangible products such as services, subscriptions, and warranties.

- Virtual products are much like simple products, but without weight.

- Shipping options do not appear during checkout unless there is a tangible product in the cart.

<!-- Last updated from includes: 2023-05-19 17:14:58 -->
