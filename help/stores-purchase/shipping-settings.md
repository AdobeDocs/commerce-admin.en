---
title: Shipping settings
description: Learn how to configure the shipping settings that define the point of origin and shipping policy for your store.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
TQID: https://experienceleague.adobe.com/9sMHWFMnoS-OVhdWjjq8r-KE9hdVD2owO2tI8LoGN0s
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Shipping settings

The shipping configuration establishes the point of origin for all shipments, your shipping policy, and the handling of shipments to multiple addresses.

## Point of origin

The point of origin is used to calculate the charge for shipments made from your store or warehouse, and also determines the tax rate for products sold. When calculating [EU taxes](international-tax-guidelines.md#eu-tax-configuration), make sure that the [Default Tax Destination Calculation](../configuration-reference/sales/tax.md) for each store view corresponds to the Shipping Settings point of origin.

![Origin](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Shipping Settings]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Origin]** section and complete the following:

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (and line 2, if needed)

1. Click **[!UICONTROL Save Config]**.

## Shipping policy

A shipping policy should explain your company's business rules and guidelines for shipments. For example, if you have price rules that trigger free shipping, you can explain the terms in your shipping policy.

![Shipping Policy During Checkout](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

To display your shipping policy during checkout, complete the Shipping Policy Parameters in the configuration. The text appears when customers click _See our shipping policy_ during checkout.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Shipping Settings]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Shipping Policy Parameters]** section.

1. Set **[!UICONTROL Apply Custom Shipping Policy]** to `Yes`.

1. Either paste or enter your **[!UICONTROL Shipping Policy]** into the text box.

   >[!NOTE]
   >
   >If you use a word processor to compose the text, make sure to save the document as a .txt file to remove any control characters from the text. Then, copy and paste the text into the Shipping Policy text box.

   ![Shipping Policy Parameters](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save Config]**.

## Multiple addresses

The multiple address shipping options enable customers to ship an order to multiple addresses during checkout, and determine the maximum number of addresses to which an order can be shipped.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Multishipping Settings]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Options]** section.

   ![Multiaddress Shipping Options](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Allow Shipping to Multiple Addresses]** to `Yes`.

1. Enter the **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. Click **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg) (Adobe Commerce B2B) For orders with multiple shipping addresses, the [Payment on Account](../b2b/enable-basic-features.md#configure-payment-on-account) payment method, even if enabled, are not available during the checkout.

## Email shipment tracking URLs

[!BADGE SaaS only]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service projects only (Adobe-managed SaaS infrastructure)."}

By default, shipment tracking numbers sent in shopper emails are plain text. You can convert these tracking numbers into clickable links by enabling the custom tracking URL feature. This feature allows you to define a template for tracking URLs for various shipping carriers. Each template includes the full URL to the tracking website and a placeholder for the tracking number. Commerce replaces the placeholder with the actual tracking number in the email.

The following shipping carriers are supported:

- United States Postal Service (USPS)
- United Parcel Service (UPS)
- Federal Express (FedEx)
- DHL Express (DHL)

To enable or edit custom tracking URLs:

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Shipping Settings]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Shipment Tracking URLs]** section.

1. Set **[!UICONTROL Enable Custom Tracking URLs]** to `Yes`.

1. Default URL templates are provided for each supported carrier. If you need to change any of these values, enter a new URL template in the corresponding field. Use `{{tracking_number}}` as a placeholder for the actual tracking number. If, for example, UPS changes their URL to `https://www.ups.com/newtracker?tracknumber`, the new tracking URL template might look like this:

   ```text
   https://www.ups.com/newtracker?tracknumber={{tracking_number}}
   ```

1. Click **[!UICONTROL Save Config]**.
