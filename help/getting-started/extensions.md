---
title: Extensions from Adobe
description: Review information about extensions for Adobe Commerce and Magento Open Source released by Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/-QGqm0VMRlCNuKqHGdGVKjs8ZgNcjYZjFaeIFsOLWCA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: c32adafa-ed01-4b31-997e-2413013911b0
    internal-label: Integrations
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
    internal-label: 2FA
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
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
  - id: a09a5a04-e30b-4d55-b031-38e6f5ec86db
    internal-label: Experience design
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: da3860b0-d637-47df-bef0-273751180266
    internal-label: Digital asset management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
  - id: f5c2a4bb-71ca-4d7e-8efd-442250e6ba48
    internal-label: Content reuse
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

[!DNL Product Recommendations] is an Adobe Commerce-exclusive feature powered by Adobe AI technology that delivers personalized product suggestions throughout the customer shopping journey. The solution analyzes shopper behavior and product relationships in real-time to automatically generate relevant recommendations, requiring no manual merchandising rules. This AI-driven approach helps increase conversion rates and revenue potential while creating more engaging product discovery experiences for shoppers.

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
