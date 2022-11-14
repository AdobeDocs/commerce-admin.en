---
title: Instant Purchase
description: Learn about Instant Purchase how it can provide a speedy checkout for registered customer accounts.
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
---
# Instant Purchase

Instant Purchase allows customers to speed through the checkout process using information that is saved in their account. When enabled, the _Instant Purchase_ button appears below the _Add to Cart_ button on the product page for customers who meet the requirements.

![Product page with the Instant Purchase option displayed](./assets/storefront-checkout-instant-purchase.png)<!-- zoom -->

## Customer requirements

- Customer is [signed in](https://docs.magento.com/user-guide/customers/customer-sign-in.html) to their account.

- Customer account has a [default billing and shipping address](https://docs.magento.com/user-guide/customers/account-dashboard-address-book.html).

- At least one [shipping method](delivery.md) is available for the country that is specified in the default shipping address.

- Customer account has a [stored payment](https://docs.magento.com/user-guide/customers/account-dashboard-stored-payment-methods.html) method with vault enabled.

   The following payment methods can be used to provide secure access to saved credit card information:

   - [Braintree Credit Cards](braintree.md) (Instant Purchase cannot be used with Braintree Credit Cards if 3D Secure is enabled.)
   - [Braintree with PayPal Enabled](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## Instant Purchase on the storefront

1. On the storefront, the customer goes to the product page of the item to be purchased.

1. Selects the required options and clicks **[!UICONTROL Instant Purchase]**.

   ![Confirmation dialog to confirm the instant purchase](./assets/storefront-checkout-instant-purchase-confirmation.png)<!-- zoom -->

1. Reviews the **[!UICONTROL Instant Purchase Confirmation]** information and clicks **[!UICONTROL OK]** to complete the transaction.

   A confirmation message and order number appear at the top of the product page.

## Configure Instant Purchase

### Step 1: Open the configuration page

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

### Step 2: Configure the payment method vault

You can use Instant Purchase with Braintree or Payment Services for Adobe Commerce and Magento Open Source.

See [Braintree](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/payments/braintree.html) to learn how to configure Braintree, including enabling vaulting, in preparation for enabling Instant Purchase.

See [Payment Services documentation](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) to learn how to [configure Payment Services](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/settings.html#configure-general-settings), including [enabling vaulting](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/settings.html#card-vaulting), in preparation for enabling Instant Purchase.

### Step 3: Enable Instant Purchase

1. In the left panel under the _[!UICONTROL Sales]_ section, choose **[!UICONTROL Sales]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Instant Purchase]** section.

1. If this change is for a specific store view, [choose the store view](https://docs.magento.com/user-guide/configuration/scope-change.html) where the configuration applies.

   When prompted, click **[!UICONTROL OK]** to continue.

1. Set **[!UICONTROL Enabled]** to `Yes`.

1. Enter the **[!UICONTROL Button Text]** that you want to appear on the button.

   The button text can be changed for each store view, or language. By default, the button text is `Instant Purchase`.

   ![Configuration - instant purchase options](../configuration-reference/sales/assets/sales-instant-purchase.png)<!-- zoom -->

   For a detailed description of each of these configuration settings, see [Instant Purchase](https://docs.magento.com/user-guide/configuration/sales/sales.html#instant-purchase) in the _Configuration Reference Guide_.

1. Click **[!UICONTROL Save Config]**.

1. When prompted to update the cache, click **[!UICONTROL Cache Management]** in the system message and follow the instructions to flush the cache.
