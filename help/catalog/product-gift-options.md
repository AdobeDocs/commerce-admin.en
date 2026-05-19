---
title: Product settings - [!UICONTROL Gift Options]
description: For a product, the [!UICONTROL Gift Options] settings determine if a gift message can be included or if gift-wrapping options are available during checkout.
exl-id: 21597e38-60f5-45e5-8d99-955d088c5c48
feature: Catalog Management, Products, Gift
TQID: https://experienceleague.adobe.com/MIzb2vY-DiVqODkNFmgX3tFLejQFZMtOETUDPoHrt-Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Product settings - [!UICONTROL Gift Options]

In the _[!UICONTROL Gift Options]_ section, you can set gift message and gift-wrapping options at checkout at the product level. To override the default configuration setting, deselect the **[!UICONTROL Use Config Settings]** checkbox.

![Gift Options](./assets/product-gift-options-ee.png){width="600" zoomable="yes"}

## Set gift options for a single product

1. Open the product in edit mode.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the _[!UICONTROL Gift Options]_ section and do the following:

   - To override the default setting, deselect the **[!UICONTROL Use Config Settings]** checkbox.

   - Set **[!UICONTROL Allow Gift Message]** as needed for the product.

   - ![Adobe Commerce](../assets/adobe-logo.svg) ([Adobe Commerce](../landing/home.md#product-editions) only) Set **[!UICONTROL Allow Gift Wrapping]** as needed for the product.

   - ![Adobe Commerce](../assets/adobe-logo.svg) ([Adobe Commerce](../landing/home.md#product-editions) only) If applicable, enter the **[!UICONTROL Price for Gift Wrapping]**.

1. When complete, click **[!UICONTROL Save]**.

## Enable gift messages for your store

By default, Commerce allows the customers to add a personalized gift message to their orders and products during the checkout process.

You can provide this feature to customers by enabling _gift message_ for your store:

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Sales]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]** on the page.

1. For **[!UICONTROL Allow Gift Messages on Order Level]**, select `Yes` to enable a single gift message for the whole order.

1. For **[!UICONTROL Allow Gift Messages for Order Items]**, select `Yes` to enable adding gift messages separately to individual items in the customer shopping cart.

1. Click **[!UICONTROL Save Config]**.

With this configuration, customers can add a gift message to the cart page from storefront as shown in the following example:

![Gift Message](./assets/gift-message.png){width="600" zoomable="yes"}
