---
title: Shipping settings
description: Learn how to configure the shipping settings that define the point of origin and shipping policy for your store.
---
# Shipping settings

The shipping configuration establishes the point of origin for all shipments, your shipping policy, and the handling of shipments to multiple addresses.

![Shipping Settings](./assets/shipping-settings.png)<!-- zoom -->

## Point of origin

The point of origin is used to calculate the charge for shipments made from your store or warehouse, and also determines the tax rate for products sold. When calculating [EU taxes](international-tax-guidelines.md#eu-tax-configuration), make sure that the [Default Tax Destination Calculation](https://docs.magento.com/user-guide/configuration/sales/tax.html) for each store view corresponds to the Shipping Settings point of origin.

![Origin](../configuration-reference/sales/assets/shipping-settings-origin.png)<!-- zoom -->

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Sales** and choose **Shipping Settings**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Origin** section and complete the following:

   - Country
   - Region / State
   - ZIP / Postal Code
   - City
   - Street Address (and line 2, if needed)

1. Click **Save Config**.

## Shipping policy

A shipping policy should explain your company's business rules and guidelines for shipments. For example, if you have price rules that trigger free shipping, you can explain the terms in your shipping policy.

![Shipping Policy During Checkout](./assets/storefront-checkout-shipping-policy.png)<!-- zoom -->

To display your shipping policy during checkout, complete the Shipping Policy Parameters in the configuration. The text appears when customers click **See our shipping policy** during checkout.

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Sales** and choose **Shipping Settings**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Shipping Policy Parameters** section.

1. Set **Apply Custom Shipping Policy** to `Yes`.

1. Either paste or enter your **Shipping Policy** into the text box.

   >[!NOTE]
   >
   >If you use a word processor to compose the text, make sure to save the document as a .txt file to remove any control characters from the text. Then, copy and paste the text into the Shipping Policy text box.

   ![Shipping Policy Parameters](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png)<!-- zoom -->

1. Click **Save Config**.

## Multiple addresses

The multiple address shipping options enable customers to ship an order to multiple addresses during checkout, and determine the maximum number of addresses to which an order can be shipped.

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Sales** and choose **Multishipping Settings**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Options** section.

   ![Multiaddress Shipping Options](../configuration-reference/sales/assets/multishipping-settings-options.png)<!-- zoom -->

1. Set **Allow Shipping to Multiple Addresses** to `Yes`.

1. Enter the **Maximum Qty Allowed for Shipping to Multiple Addresses**.

1. Click **Save Config**.

>[!NOTE]
>
>![B2B for Adobe Commerce](../assets/b2b.svg) (B2B for Adobe Commerce) For orders with multiple shipping addresses, the [Payment on Account](../b2b/enable-basic-features.md#configure-payment-on-account) payment method, even if enabled, are not available during the checkout.
