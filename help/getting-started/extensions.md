---
title: Extensions from Adobe
description: Review information about extensions for Adobe Commerce and Magento Open Source released by Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
---
# Extensions from Adobe

This topic provides information about PHP extensions for Adobe Commerce and Magento Open Source that are released by Adobe.

Extensions add features, functionality, services, and integrations to the Admin and storefront. Some of these extensions are developed through Magento Open Source Community contributions. Some extensions are installed by default, and others require separate installation.

+++Learn more about extending Adobe Commerce

Adobe provides two main approaches to extend or customize your Adobe Commerce projects:

- In-process extensibility: Uses custom code and extensions that run within the Adobe Commerce application process like PHP extensions. This traditional approach allows deep integration but requires careful management during upgrades.

- Out-of-process extensibility: Uses custom code and applications that operate independently from the core software. This modern approach helps reduce total cost of ownership by:

  - Simplifying upgrades since extensions are decoupled from the core
  - Giving developers more control over implementation timing and methods
  - Enabling independent scaling and maintenance of extension components

Adobe Commerce offers strategies and tools to support both types of extensibility. To learn more, see [Adobe Commerce extensibility](https://developer.adobe.com/commerce/extensibility/).

+++

## Adobe extensions installed by default

The following Adobe extensions are included with Adobe Commerce and installed automatically with the Adobe Commerce application. Some extensions require further configuration or enablement in the Admin as noted in the extension description.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) provides enhanced stock and shipment management across one or multiple locations and sales channels with concurrent checkout protection and shipment-matching algorithms. Track your inventory quantities, provide accurate salable stock amounts to customers, and ship according to recommendations or manual selections to control your entire inventory. Configure management settings globally, per source, and per product.

>[!NOTE]
>
>This extension was developed as part of the [[!DNL Inventory Management]](https://github.com/magento/inventory) (formerly MSI) project through the Community Engineering program.

[!DNL Inventory Management] installs with all features enabled by default. No additional steps are required to enable these inventory features. For details about the [!DNL Inventory Management] capabilities, see the [[!DNL Inventory Management] User Guide](../inventory-management/guide-overview.md).

### Braintree

PayPal and Gene Commerce together developed the official Braintree extension for Commerce 2.4.x stores. Featuring an improved checkout experience designed to drive conversion, the updates include PayLater options that automatically show relevant PayLater messages and buttons to consumers while shopping and during checkout.

This extension is installed by default, but requires a [Braintree account](https://www.braintreepayments.com/) and configuration in the Admin to be enabled for your store. To determine the fees that apply when using Braintree to process your transactions, check the [Braintree pricing](https://www.braintreepayments.com/braintree-pricing).

For information about Braintree configuration in the Admin, see the [Braintree](../stores-purchase/braintree.md) topic in the _Sales and Purchase Experience Guide_.

### Google reCAPTCHA

Google reCAPTCHA provides a greater level of security for both the storefront and Admin UI than is available with standard CAPTCHA and gives you the ability to:

- Verify when customers create accounts, retrieve passwords, log in to their accounts, or contact your company.
- Enhance security when Admin users log in.

It reduces potential user error when entering a Captcha code and encourages cart conversion without adding hurdles during checkout. [Enable and configure reCAPTCHA](../systems/security-google-recaptcha.md) using invisible or interactive checks to enhance secure access to the [!DNL Commerce] Admin and storefront.

### Two-factor authentication

The [!DNL Commerce] Admin provides all access to your store, orders, and customer data. [Two-factor authentication](../systems/security-two-factor-authentication.md) (2FA or TFA) improves security by requiring additional authentication, beyond the standard login name and password, to access the [!DNL Commerce] Admin from all devices. The extension supports multiple authenticators including Google Authenticator, Authy, [!DNL Duo], and U2F keys. This authentication applies to Admin users only. It is not available for storefront customer accounts.

These features are enabled by default. Each Admin user must install and configure one of the supported authenticators.

>[!NOTE]
>
>Adobe Commerce stores that have enabled Adobe Identity Management Services (IMS) authentication for the Admin have native Commerce 2FA disabled. Users who are logged into the Admin with their Adobe credentials do not need to reauthenticate for many Admin tasks. Authentication is handled by Adobe IMS when the Admin user logs into their current session. See [Adobe Identity Management Service (IMS) Integration Overview](./adobe-ims-integration-overview.md).

## Adobe extensions that require installation

Adobe offers additional extensions that must be installed separately using Composer. These extensions are available through different channels:

- Repository Access (repo.magento.com)

  The following extensions require account provisioning and credentials to install. Contact your Adobe Account Representative for assistance.

  - [Adobe Commerce B2B](#adobe-commerce-b2b)
  - [AEM Assets Integration for Commerce](#assets-integration-for-commerce)

- Adobe Commerce Marketplace

  The following Adobe extensions are publicly accessible at [marketplace.magento.com](https://marketplace.magento.com). These extensions are available at no additional cost.

  - [Live Search](#live-search)
  - [Product Recommendations](#product-recommendations)
  - [Catalog Service](#catalog-service)
  - [Payment Services](#payment-services)

### [!DNL Adobe Commerce B2B]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce only, requires a separate license.

[!DNL Adobe Commerce B2B] is an integrated extension that transforms standard Commerce stores into comprehensive business-to-business platforms. It enables companies to manage complex organizational structures with multiple buyers, custom roles, and purchasing permissions under unified company accounts. Key functionalities include company-specific catalogs and pricing, negotiable quotes, purchase order management, requisition lists, and quick ordering capabilities. The solution supports both B2B and B2C models on a single instance, making it flexible for diverse business needs. The extension requires a separate license and seamlessly integrates with Adobe Commerce's core features to provide a complete B2B e-commerce solution.

For provisioning, contact your Adobe Account Representative. For implementation details and configuration steps, see the [[!DNL B2B for Adobe Commerce] User Guide](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

### [!DNL AEM Assets Integration for Commerce]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce only, also requires licenses for Adobe Experience Manager (AEM) Assets and AEM Dynamic Media.

[!DNL AEM Assets Integration for Commerce] connects Adobe Commerce with Adobe Experience Manager's Digital Asset Management (DAM) system to provide centralized control over all digital assets. This integration enables automated asset synchronization, real-time updates, and efficient content reuse across commerce storefronts. By combining AEM's robust asset management capabilities with Commerce, businesses benefit from streamlined workflows, consistent brand experiences, and optimized media delivery through cloud-based infrastructure.

For provisioning, contact your Adobe Account Representative. For implementation details and configuration steps, see the [[!DNL Assets Integration] User Guide](../content-design/aem-assets-integration.md).

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce only

Live Search is an Adobe Commerce-exclusive feature that provides an AI-powered search solution with real-time "search-as-you-type" functionality. It delivers fast, relevant results with product thumbnails while shoppers type, along with intelligent faceting that automatically adjusts filters based on shopping behavior. The solution includes merchandising capabilities for product boosting and burying, synonym management, and search analytics. Included with Adobe Commerce at no additional cost, [!DNL Live Search] replaces the default search functionality with a more sophisticated, SaaS-based search experience. It requires minimal configuration to get started.

For implementation details and technical requirements, see the [Live Search User Guide](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html).

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce only

[!DNL Product Recommendations] is an Adobe Commerce-exclusive feature powered by Adobe Sensei AI technology that delivers personalized product suggestions throughout the customer shopping journey. The solution analyzes shopper behavior and product relationships in real-time to automatically generate relevant recommendations, requiring no manual merchandising rules. This AI-driven approach helps increase conversion rates and revenue potential while creating more engaging product discovery experiences for shoppers.

For implementation details and best practices, see the [[!DNL Product Recommendations] User Guide](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html).

### [!DNL Catalog Service]

[!BADGE Supported]{type=Informative tooltip="Supported"} Adobe Commerce and Magento Open Source installations

[!DNL Catalog Service] is a high-performance solution for Adobe Commerce and Magento Open Source that provides optimized access to catalog data through GraphQL endpoints. It maintains a separate synchronized database for product details and related information, bypassing direct application communication to deliver faster page load times. The service is particularly valuable for product detail pages, category listings, and search results pages, making it ideal for both traditional and headless commerce implementations.

For setup instructions and technical details, see the [[!DNL Catalog Service] User Guide](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html).

>[!NOTE]
>
>Catalog Services is installed automatically when Live Search or Product Recommendations are enabled. Manual installation is not required.

### [!DNL Payment Services]

[!BADGE Supported]{type=Informative tooltip="Supported"} Adobe Commerce and Magento Open Source installations

[!DNL Payment Services] is a turnkey payment solution for Adobe Commerce and Magento Open Source stores that provides comprehensive payment processing capabilities. The service integrates secure payment gateway functionality with built-in fraud protection, while offering multiple payment options including credit/debit cards, PayPal, Venmo (US), and PayLater plans. It features unified transaction reporting and order management through the Commerce Admin interface, making it easy for merchants to track payments, manage cash flow, and reconcile financial data all in one place.

For detailed configuration steps and payment options, see the [[!DNL Payment Services] User Guide](https://experienceleague.adobe.com/en/docs/commerce/payment-services/overview).
