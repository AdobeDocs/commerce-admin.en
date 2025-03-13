---
title: Extensions from Adobe
description: Review information about extensions for Adobe Commerce and Magento Open Source released by Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
---
# Extensions from Adobe

This topic provides information about extensions for Adobe Commerce and Magento Open Source that are released by Adobe.

Extensions add features, functionality, services, and integrations to the Admin and storefront. Some of these extensions are developed through Magento Open Source Community contributions. Some extensions require separate installation, and others are installed by default.

## Adobe extensions installed by default

Some Adobe extensions are installed automatically with Adobe Commerce or Magento Open Source.

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

  The following extensions require account provisioning and credentials to install. Contact your Adobe Account Representative for access permissions.

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

[!DNL Adobe Commerce B2B] provides comprehensive B2B (Business to Business) capabilities that transform your Commerce store into a customized B2B solution. Key features include:

- **Company Account Management**
  - Complex organizational structures
  - Company hierarchy management
  - Customizable roles and permissions
  - Company credit management
  - Self-service company administration

- **B2B Purchasing Tools**
  - Shared catalogs with custom pricing
  - Quick order functionality
  - Requisition lists
  - Purchase order management
  - Negotiable quotes

- **Streamlined Operations**
  - Company-specific catalogs and pricing
  - Automated approval workflows
  - Corporate account management
  - B2B and B2C support on single instance

For implementation details and configuration steps, see the [[!DNL B2B for Adobe Commerce] User Guide](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).


### [!DNL AEM Assets Integration for Commerce]

>[!NOTE]
>
>Requires Adobe Commerce and Adobe Experience Manager Assets licenses.

The Assets Integration for Commerce connects your Adobe Commerce store with Adobe Experience Manager Assets, providing a centralized digital asset management (DAM) system. Key features include:

- **Centralized Asset Management**
  - Single source of truth for product assets
  - Automated asset synchronization
  - Consistent brand experience across channels
  - Enterprise-grade DAM capabilities

- **Streamlined Workflows**
  - Direct access to approved assets from Commerce Admin
  - Automated metadata synchronization
  - Real-time asset updates
  - Efficient content reuse

- **Enhanced Performance**
  - Cloud-based asset delivery
  - Optimized image renditions
  - Fast loading product media
  - Reduced storage requirements

For implementation details and configuration steps, see the [[!DNL Assets Integration] User Guide](https://experienceleague.adobe.com/docs/commerce-admin/content-design/aem-asset-management/aem-assets-integration.html).

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce only

[!DNL Live Search] delivers an AI-powered search experience that transforms the way shoppers find products on your store. This extension replaces the default Commerce search capabilities with an intelligent, lightning-fast search solution that includes:

- "Search-as-you-type" results with product thumbnails
- AI-powered merchandising rules for product boosting and burying
- Intelligent faceting that automatically adjusts filters based on shopper behavior
- Synonym management to improve search relevance
- Analytics and search term management
- Support for Commerce search term redirects

The service is included with Adobe Commerce at no additional cost and requires minimal configuration to get started. For implementation details and technical requirements, see the [Live Search User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html).

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce only

[!DNL Product Recommendations] powered by Adobe Sensei delivers intelligent product recommendations that personalize the shopping experience. Key capabilities include:

- **AI-Powered Intelligence**
  - Machine learning analysis of shopper behavior
  - Automatic product relationship mapping
  - Real-time recommendation adjustments
  - Adobe Sensei artificial intelligence technology

- **Enhanced Shopping Experience**
  - Personalized product discoveries
  - Relevant recommendations throughout customer journey
  - Improved shopper engagement
  - More engaging product discovery

- **Business Benefits**
  - Increased conversion rates
  - Higher revenue potential
  - No manual merchandising rules required
  - Frees team to focus on strategic initiatives

For implementation details and best practices, see the [[!DNL Product Recommendations] User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html).

### [!DNL Catalog Service]

>[!NOTE]
>
>Compatible with both Adobe Commerce and Magento Open Source installations.

The [!DNL Catalog Service] delivers high-performance catalog data access for your Adobe Commerce storefront. Key benefits include:

- **Fast Product Data Delivery**
  - Real-time catalog synchronization
  - Optimized GraphQL API endpoints
  - Reduced page load times

- **Enhanced Shopping Experience**
  - High-performance product pages and listings
  - Improved storefront scalability
  - Better conversion rates

- **Flexible Implementation**
  - Ideal for headless commerce solutions
  - Supports custom storefront development
  - Minimal configuration required

For setup instructions and technical details, see the [[!DNL Catalog Service] User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html).


### [!DNL Payment Services]

>[!NOTE]
>
>Compatible with both Adobe Commerce and Magento Open Source installations.

[!DNL Payment Services] provides a complete payment solution for your Adobe Commerce or Magento Open Source store. Key features include:

- **Comprehensive Payment Processing**
  - Secure payment gateway integration
  - Built-in fraud protection tools
  - Transparent transaction reporting
  - Unified Admin management interface

- **Multiple Payment Options**
  - Credit and debit cards
  - PayPal
  - Venmo (US only)
  - PayLater payment plans
  - Additional regional payment methods

- **Business Benefits**
  - Simplified payment management
  - All-in-one order and payment tracking
  - Expanded market reach
  - Improved customer experience

For detailed configuration steps and payment options, see the [[!DNL Payment Services] User Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

