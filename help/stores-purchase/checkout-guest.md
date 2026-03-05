---
title: Guest checkout
description: Learn how to enable guest checkout capabilities on your store.
exl-id: ce25eba3-7503-46aa-a5cd-9b7d5662164b
feature: Checkout
---
# Guest checkout

Your store can be configured to require shoppers to open an account before making a purchase. The default setting allows guests to make purchases, with an option to register for an account after they complete the checkout process.

![Luma store displays Check Out as Guest](./assets/storefront-checkout-as-guest.png){width="600" zoomable="yes"}

**_To disable guest checkout:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. On the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Checkout]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Checkout Options]** section.

   ![Checkout options expanded on the configuration page](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

  For a detailed description of each of these configuration settings, see [Checkout Options](../configuration-reference/sales/checkout.md#checkout-options) in the _Configuration Reference Guide_.

1. If the setting is for a specific store view, [choose the store view](../configuration-reference/scope-change.md#set-the-scope) where the configuration applies.

   When prompted, click **[!UICONTROL OK]** to continue.

1. Set **[!UICONTROL Allow Guest Checkout]** to `No`.

   If necessary, clear the **[!UICONTROL Use system value]** checkbox to enable changes to this setting.

1. Click **[!UICONTROL Save Config]**.

## Allow guest order access for registered emails

[!BADGE SaaS only]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service projects only (Adobe-managed SaaS infrastructure)."}

An optional, store-level configuration, which is disabled by default, allows merchants to track guest orders placed using an email address that matches a registered customer account.

When enabled, guest checkout orders placed with a registered email remain accessible, while also appearing in the customer's order history.

To enable this feature, navigate to **Stores** > Settings > **Configuration** > Sales > **Sales** > **Guest Checkout** and set the **Allow Guest Order Access for Registered Emails** setting to `Yes`.
