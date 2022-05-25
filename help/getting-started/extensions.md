---
title: Extensions
description: Review information about extensions for Adobe Commerce and Magento Open Source released by Adobe. 
---
# Extensions

This section provides information about extensions for Adobe Commerce and Magento Open Source released by Adobe. Some of these extensions are developed through Magento Open Source Community contributions. Some extensions require separate installation, and others are installed by default.

## Installed extensions

There are some extensions that are automatically installed as part of the 

### Inventory Management

Commerce [Inventory Management](../../inventory-management/introduction.md) provides enhanced stock and shipment management across one or multiple locations and sales channels with concurrent checkout protection and shipment-matching algorithms. Track your inventory quantities, provide accurate salable stock amounts to customers, and ship according to recommendations or manual selections to control your entire inventory. Configure management settings globally, per source, and per product.

>[!NOTE]
>
>This extension was developed as part of the [Inventory Management](https://github.com/magento/inventory) (formerly MSI) project through the Community Engineering program.

Inventory Management installs with all features enabled by default. No additional steps are required to enable these inventory features. For details about the Inventory Management capabilities, see the Inventory Management User Guide.

### Braintree

PayPal and Gene Commerce together developed the official Braintree extension for Commerce 2.4.x stores. Featuring an improved checkout experience designed to drive conversion, the updates include Pay Later options that automatically show relevant Pay Later messages and buttons to consumers while shopping and during checkout. 

This extension is installed by default, but requires a [Braintree account](https://signups.braintreepayments.com/) and configuration in the Admin to be enabled for your store. To determine the fees that apply when using Braintree to process your transactions, check the [Braintree pricing](https://www.braintreepayments.com/braintree-pricing).

For information about Braintree configuration in the Admin, see the [Braintree](https://docs.magento.com/user-guide/payment/braintree.html) topic in the _Sales Guide_.

### Google reCAPTCHA

Google reCAPTCHA provides a greater level of security for both the storefront and Admin UI than is available with standard CAPTCHA and gives you the ability to:

- Verify when customers create accounts, retrieve passwords, log in to their accounts, or contact your company.
- Enhance security when Admin users log in.

It reduces potential user error when entering a Captcha code and encourages cart conversion without adding hurdles during checkout. [Enable and configure reCAPTCHA](https://docs.magento.com/user-guide/stores/security-google-recaptcha.html) using invisible or interactive checks to enhance secure access to the Commerce Admin and storefront.

### Two-Factor Authentication

The Commerce Admin provides all access to your store, orders, and customer data. [Two-factor authentication](https://docs.magento.com/user-guide/stores/security-two-factor-authentication.html) (2FA or TFA) improves security by requiring additional authentication, beyond the standard login name and password, to access the Commerce Admin from all devices. The extension supports multiple authenticators including Google Authenticator, Authy, Duo, and U2F keys. This authentication applies to Admin users only. It is not available for storefront customer accounts.

These features are enabled by default. Each Admin user must install and configure one of the supported authenticators. For complete instructions, see Using Two-Factor Authentication.

## Extensions to add

The [Commerce Marketplace](https://marketplace.magento.com/) is the global eCommerce resource for applications and services that expand Commerce solutions with powerful new features and functionality. Adobe releases several extensions through the Marketplace that can be installed and configured within your Adobe Commerce or Magento Open Source store to provide enhanced integrations and capabilities.

### Payment Services

Payment services for Adobe Commerce and Magento Open Source is a fully integrated payment solution that simplifies the process of managing payments and provides your customers with the opportunity to pay their way. Securely reconcile all payment and transaction data within the Adobe Commerce Admin – allowing you to manage orders and payments in one place while delivering a seamless checkout. See the [Payment Services User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) for more information.
<!-- ### Quick Checkout

Add Quick Checkout when the extension reaches GA

-->
<!-- ### Store Fulfillment

This one will not be in Marketplace. We may need to omit this one from the list?

-->

### Live Search

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce only

The Product Recommendations extension connects your store to the Live Search service---a free search platform from Adobe Commerce that seamlessly empowers sellers to provide customers with an AI-enhanced search experience. Built with Adobe's artificial intelligence, Adobe Sensei, Intelligent Faceting helps merchants do more with less by removing the manual work around faceting/filtering.

See the [Live Search User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html) for more information.

### Product Recommendations

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce only

The Product Recommendations extension connects your store to the Product Recommendations service---a powerful marketing tool that you can use to increase conversions, revenue, and engagement. Product Recommendations was built by Adobe Commerce and is driven by its battle tested artificial intelligence, Adobe Sensei, so that you can confidently drive engagement and conversion. This feature removes the manual work required to make relevant product recommendations to every shopper. 

See the [Product Recommendations User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) for more information.
<!-- Channel Manager

Add Channel Manager, Walmart when the extension reaches GA

-->

### Amazon Sales Channel

The Amazon Sales Channel for Adobe Commerce and Magento Open Source enables you to integrate your Amazon Seller Central listing database with your Commerce product catalog and manage your Amazon listings and sales in the Commerce Admin. See the [Amazon Sales Guide User Guide](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) for more information.
