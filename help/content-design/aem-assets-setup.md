---
title: Set up the AEM Assets Integration
description: Learn about the requirements and steps to set up the integration between Adobe Commerce and AEM Assets as a Cloud Service.
feature: CMS, Media, Configuration, Integration
exl-id: 75cf72ed-0110-4aed-b44a-193ad4dae202
---
# Set up the AEM Assets Integration

Enable advanced asset management capabilities by setting up your AEM Assets environment and installing and configuring the AEM Assets integration for Commerce.

 When the integration is active, administrators can use Experience Manager Assets as a Cloud Service as the single source of truth for asset creation and management, and as a central digital asset management tool (DAM) to create, manage, organize, and distribute assets for Commerce projects.

## Requirements

- Adobe Commerce 2.4.5+
  - PHP 8.1, 8.2, 8.3
  - Composer: 2.x
- Adobe Experience Manager is provisioned with [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview)
-  The Adobe Commerce user configuring the integration must have access to the [IMS Organization](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) where the AEM Assets project is provisioned.

## Set up the integration

>[!BEGINSHADEBOX]

**Prerequisites**

Setting up the AEM Assets integration requires administrative access to customize application and environment configuration.

- Administrative access to the Cloud Manager program where the AEM Assets as a Cloud Service environments are provisioned.
- Administrative access to the Adobe Commerce environment and ability to retrieve or generate API keys required for authentication.

>[!ENDSHADEBOX]

Enabling the Commerce integration with Experience Manager Assets is a three step process:

1. [Configure your Experience Manager Assets project to manage Commerce assets](aem-assets-configure-aem.md).

1. [Install the Experience Manager Assets Integration extension and configure Adobe Commerce](aem-assets-configure-aem.md).

1. [Enable asset synchronization](aem-assets-setup-synchronization.md).
