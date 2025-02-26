---
title: Set up AEM Assets Integration for Commerce
description: Learn how to onboard the Experience Manager Assets with your [!DNL Commerce] instance to access to countless media assets for use in your store.
feature: CMS, Media, Configuration
---
# Set up AEM Assets Integration for Commerce

Setting up the AEM Assets integration requires administrative access to customize application and environment configuration.

- Administrative access to the Cloud Manager program where the AEM Assets as a Cloud Service environments are provisioned.

- Administrative access to the Adobe Commerce environment and ability to retrieve or generate API keys required for authentication.

## Requirements

Verify that you meet the following requirements:

- Adobe Commerce 2.4.5+

  - PHP 8.1, 8.2, 8.3
  - Composer: 2.x

- Adobe Experience Manager is provisioned with [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview)

- The Adobe Commerce user configuring the integration must have access to the [IMS Organization](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) where the AEM Assets project is provisioned.

- The Adobe Commerce user configuring the integration must have access to [AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

## Next steps

Enabling the Commerce integration with Experience Manager Assets is a three step process:

1. [Configure your AEM assets project to manage Adobe Commerce assets](aem-assets-configure-aem.md).

1. [Install the AEM assets integration extension and configure Adobe Commerce](aem-assets-configure-aem.md).

1. [Enable asset synchronization](aem-assets-setup-synchronization.md).
