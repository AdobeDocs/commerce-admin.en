---
title: Extensions
description: Review information about extensions for Adobe Commerce and Magento Open Source released by Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
---
# Extensions

This topic provides information about extensions for Adobe Commerce and Magento Open Source released by Adobe. Extensions add features, functionality, services, and integrations to the Admin and storefront. Some of these extensions are developed through Magento Open Source Community contributions. Some extensions require separate installation, and others are installed by default.

## Installed extensions

There are some extensions that are automatically installed with Adobe Commerce or Magento Open Source.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) provides enhanced stock and shipment management across one or multiple locations and sales channels with concurrent checkout protection and shipment-matching algorithms. Track your inventory quantities, provide accurate salable stock amounts to customers, and ship according to recommendations or manual selections to control your entire inventory. Configure management settings globally, per source, and per product.

>[!NOTE]
>
>This extension was developed as part of the [[!DNL Inventory Management]](https://github.com/magento/inventory) (formerly MSI) project through the Community Engineering program.

[!DNL Inventory Management] installs with all features enabled by default. No additional steps are required to enable these inventory features. For details about the [!DNL Inventory Management] capabilities, see the [[!DNL Inventory Management] User Guide](../inventory-management/guide-overview.md).

### Braintree

PayPal and Gene Commerce together developed the official Braintree extension for [!DNL Commerce] 2.4.x stores. Featuring an improved checkout experience designed to drive conversion, the updates include Pay Later options that automatically show relevant Pay Later messages and buttons to consumers while shopping and during checkout. 

This extension is installed by default, but requires a [Braintree account](https://signups.braintreepayments.com/) and configuration in the Admin to be enabled for your store. To determine the fees that apply when using Braintree to process your transactions, check the [Braintree pricing](https://www.braintreepayments.com/braintree-pricing).

For information about Braintree configuration in the Admin, see the [Braintree](../stores-purchase/braintree.md) topic in the _Sales and Purchase Experience Guide_.

### Google reCAPTCHA

Google reCAPTCHA provides a greater level of security for both the storefront and Admin UI than is available with standard CAPTCHA and gives you the ability to:

- Verify when customers create accounts, retrieve passwords, log in to their accounts, or contact your company.
- Enhance security when Admin users log in.

It reduces potential user error when entering a Captcha code and encourages cart conversion without adding hurdles during checkout. [Enable and configure reCAPTCHA](https://docs.magento.com/user-guide/stores/security-google-recaptcha.html) using invisible or interactive checks to enhance secure access to the [!DNL Commerce] Admin and storefront.

### Two-Factor Authentication

The [!DNL Commerce] Admin provides all access to your store, orders, and customer data. [Two-factor authentication](https://docs.magento.com/user-guide/stores/security-two-factor-authentication.html) (2FA or TFA) improves security by requiring additional authentication, beyond the standard login name and password, to access the [!DNL Commerce] Admin from all devices. The extension supports multiple authenticators including Google Authenticator, Authy, [!DNL Duo], and U2F keys. This authentication applies to Admin users only. It is not available for storefront customer accounts.

These features are enabled by default. Each Admin user must install and configure one of the supported authenticators.

>[!NOTE]
>
>Adobe Commerce stores that have enabled Adobe Identity Management Services (IMS) authentication for the Admin have native Commerce 2FA disabled. Users who are logged into the Admin with their Adobe credentials do not need to reauthenticate for many Admin tasks. Authentication is handled by Adobe IMS when the Admin user logs into their current session. See [Adobe Identity Management Service (IMS) Integration Overview](./adobe-ims-integration-overview.md).

## Extensions to add

The [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) is the global eCommerce resource for applications and services that expand [!DNL Commerce] solutions with powerful new features and functionality. Adobe releases several extensions through the [!DNL Marketplace] that can be installed and configured within your Adobe Commerce or Magento Open Source store to provide enhanced integrations and capabilities.

### Live Search

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce only

The Live Search extension connects your store to the Live Search service---a free search platform from Adobe Commerce that seamlessly empowers sellers to provide customers with an AI-enhanced search experience. Built with Adobe's artificial intelligence, Adobe Sensei, Intelligent Faceting helps merchants do more with less by removing the manual work around faceting/filtering.

See the [Live Search User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html) for more information.

### Product Recommendations

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce only

The [!DNL Product Recommendations] extension connects your store to the Product Recommendations service---a powerful marketing tool that you can use to increase conversions, revenue, and engagement. [!DNL Product Recommendations] was built by Adobe Commerce and is driven by its battle tested artificial intelligence, Adobe Sensei, so that you can confidently drive engagement and conversion. This feature removes the manual work required to make relevant product recommendations to every shopper. 

See the [[!DNL Product Recommendations] User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) for more information.

### Catalog Service

The [!DNL Catalog Service] enables you to deliver customers an optimized product experience while boosting performance, improving scalability, and increasing conversions. See the [Catalog Service User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html) for more information.

### Payment Services

[!DNL Payment services] for Adobe Commerce and Magento Open Source is a fully integrated payment solution that simplifies the process of managing payments and provides your customers with the opportunity to pay their way. Securely reconcile all payment and transaction data within the Adobe Commerce Admin – allowing you to manage orders and payments in one place while delivering a seamless checkout. See the [Payment Services User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) for more information.

### Quick Checkout

[!DNL Quick Checkout] for Adobe Commerce powers a seamless checkout experience designed to convert one-time guest shoppers into loyal account holders. 
See the [[!DNL Quick Checkout] User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/quick-checkout/overview.html) for more information.

### Store Fulfillment 

Store Fulfillment for Adobe Commerce and Magento Open Source enables a superior buy online, pick up in store (BOPIS) customer experience and maximizes employee productivity by providing a comprehensive fulfillment workflow enabled through a mobile device. See the [[!DNL Store Fulfillment] User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html) for more information.  

### Amazon Sales Channel

The Amazon Sales Channel for Adobe Commerce and Magento Open Source enables you to integrate your Amazon Seller Central listing database with your [!DNL Commerce] product catalog and manage your Amazon listings and sales in the [!DNL Commerce] Admin. See the [Amazon Sales Guide User Guide](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) for more information.

### Channel Manager

Channel Manager enables you to increase sales, reach new customers, streamline operations, and save time by integrating an Adobe Commerce or Magento Open Source product catalog with the Walmart Marketplace. After installing and configuring the extension, your staff can manage Walmart Marketplace listings, inventory, orders, returns and refunds seamlessly from the [!DNL Commerce Admin]. See the [[!DNL Channel Manager] User Guide](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) for more information.
