---
title: Experience Manager Assets Integration for Commerce
description: Learn how to integrate Experience Manager Assets with your [!DNL Commerce] instance to access to countless media assets for use in your store.
feature: CMS, Media, Configuration, Integration
---
# Experience Manager Assets Integration for Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

The integration between Commerce and Adobe Experience Manager (AEM) Assets combines the robust capabilities of AEM as a Digital Asset Management (DAM) system with Adobe Commerce to enhance eCommerce experiences. This integration leverages AEM's powerful asset management features to provide a seamless, scalable, and efficient way to manage and deliver assets across commerce storefronts.

**Key features**

- **Centralized Asset Management**

  - **AEM Assets as the Single Source of Truth**–AEM Assets serves as the central repository for all digital assets, ensuring that all ecommerce platforms have access to on-brand, approved assets.

  - **Bulk Asset Management**–Organizations can manage large volumes of assets efficiently, thanks to AEM's robust asset management capabilities. This enables marketers and merchandisers to map large sets of images for new product lines efficiently.

- **Personalized Commerce Experiences**–Using GenAI services in AEM, organizations can generate millions of product variations for personalized ecommerce experiences. Marketers and merchandisers can use these images to create dynamic storefronts for product launches and seasonal campaigns, enhancing engagement and boosting conversion rates.

- **Automated Asset Matching**–The integration includes a Rules Engine Service that automatically matches assets in AEM to products in Adobe Commerce based on SKU or other key attributes. The service ensures that the latest product assets and variations are always available on ecommerce storefronts. It also reduces the manual effort required to manage assets, freeing up time for more strategic activities.

- **Streamlined Processes**
  - **Enable and configure the integration from the Commerce Admin**–Administrators and developers can install and configure the integration from Adobe Commerce using familiar tools and processes.
  - **Dynamic Updates**–Keep product images current with the latest changes in the asset management system. These automated updates ensure that commerce storefronts always have the most up-to-date product information.
  - **Efficient Catalog Management**–Simplifies the maintenance of the product catalog by automating asset cleanup and refresh.

## What changes when you enable the integration



## Integrate Commerce and Experience Manager Assets

[!BEGINSHADEBOX]

**Prerequisites**

- Adobe Commerce must be configured with the [Commerce Admin integration with Adobe ID](/help/getting-started/adobe-ims-config.md) with an assigned Organization ID.
- Experience Manager Assets must be assigned as a product to the same organization ID.
- The user configuring the integration must have an account in the same organization  with Administrative rights to access Adobe Commerce and Experience Manager Assets.

[!ENDSHADEBOX]


Enabling the Commerce integration with Experience Manager Assets is a three step process:

1. [Configure your Experience Manager Assets project to manage Commerce assets](aem-assets-configure-aem.md).

1. [Install the Experience Manager Assets Integration extension and configure Adobe Commerce](aem-assets-configure-aem.md)

1. [Set up synchronization services](aem-assets-setup-synchronization.md)

