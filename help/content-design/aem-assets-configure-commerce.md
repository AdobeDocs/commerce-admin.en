---
title: Install and Configure the Experience Manager Assets Integration
description: Learn how to install and configure the [!DNL AEM Assets Integration for Adobe Commerce] on an Adobe Commerce instance.
feature: CMS, Media
exl-id: 2f8b3165-354d-4b7b-a46e-1ff46af553aa
---
# Install and configure the AEM Assets Integration for Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Prepare your Commerce environment to use the AEM Assets Integration for Commerce by installing the `aem-assets-integration` PHP extension. Then, update the Admin configuration to enable communication and workflows between Adobe Commerce and AEM Assets.

## System requirements

The AEM Assets Integration for Commerce has the following system and configuration requirements.

**Software requirements**

- Adobe Commerce 2.4.5+
- PHP 8.1, 8.2, 8.3
- Composer: 2.x

**Configuration requirements**

- Adobe Commerce must be configured to use [Adobe IMS authentication](/help/getting-started/adobe-ims-config.md).
- Account provisioning and permissions
  - [Commerce cloud project administrator](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access)—Install required extensions and configure the Commerce application server from the Admin or the command line
  - [Commerce Admin](https://experienceleague.adobe.com/en/docs/commerce-admin/start/guide-overview)—Update store configuration and manage Commerce user accounts

## Configuration overview

Enable the integration by completing the following tasks:

1. [Install the AEM Assets integration extension (`aem-assets-integration`)](#install-the-aem-assets-integration-extension)
1. [Configure the Commerce Service Connector](#configure-the-commerce-services-connector)
1. [Configure Adobe I/O Events for Commerce](#configure-adobe-io-events-for-commerce)
1. [Get authentication credentials for API access](#get-authentication-credentials-for-api-access)

## Install the AEM Assets Integration extension

>[!BEGINSHADEBOX]

**Prerequisite**

- Access [repo.magento.com](https://repo.magento.com/admin/dashboard) to install the extension.

   For key generation and obtaining the necessary rights, see [Get your authentication keys](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). For cloud installations, see the [Commerce on Cloud Infrastructure Guide](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/authentication-keys)

- Access to the command line of the Adobe Commerce application server.

>[!ENDSHADEBOX]

Install the latest version of the AEM Assets Integration extension (`aem-assets-integration`) on an Adobe Commerce instance with version Adobe Commerce 2.4.5+. The AEM Asset Integration is delivered as a composer metapackage from the [repo.magento.com](https://repo.magento.com/admin/dashboard) repository.

>[!BEGINTABS]

>[!TAB Cloud infrastructure]

Use this method to install the [!DNL AEM Assets Integration] extension for a Commerce Cloud instance.

1. On your local workstation, change to the project directory for your Adobe Commerce on cloud infrastructure project.

   >[!NOTE]
   >
   >For information about managing Commerce project environments locally, see [Managing branches with the CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) in the _Adobe Commerce on Cloud Infrastructure User Guide_.

1. Check out the environment branch to update using the Adobe Commerce Cloud CLI.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Add the AEM Assets Integration for Commerce extension.

   ```shell
   composer require "magento/aem-assets-integration" "<version-tbd>" --no-update
   ```

1. Update package dependencies.

   ```shell
   composer update "magento/aem-assets-integration"
   ```

1. Commit and push code changes for the `composer.json` and `composer.lock` files.

1. Add, commit, and push the code changes for the `composer.json` and `composer.lock` files to the cloud environment.

   ```shell
   git add -A
   git commit -m "Install AEM Assets Integration extension for Adobe Commerce"
   git push origin <branch-name>
   ```

   Pushing the updates initiates the [Commerce cloud deployment process](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) to apply the changes. Check the deployment status from the [deploy log](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

>[!TAB On-premises]

Use this method to install the [!DNL AEM Assets Integration] extension for an on-premises instance.

1. Use Composer to add the AEM Assets Integration for Commerce extension to your project:

   ```shell
   composer require "magento/aem-assets-integration" --no-update
   ```

1. Update dependencies and install the extension:

   ```shell
   composer update  "magento/aem-assets-integration"
   ```

1. Upgrade Adobe Commerce:

   ```shell
   bin/magento setup:upgrade
   ```

1. Clear the cache:

   ```shell
   bin/magento cache:clean
   ```

>[!TIP]
>
>When deploying to production, consider not clearing compiled code to save time. Always back up your system before making changes.

>[!ENDTABS]

## Configure the Commerce Services Connector

The Commerce Services Connector enables data synchronization and communication between the Commerce instance, the Asset Rule Engine Service, and other supporting services.

>[!NOTE]
>
>Commerce Services Connector setup is a one-time process required to use [Adobe Commerce SaaS services](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#availableservices). If you have already configured the connector for another service, you can view the existing configuration from the Commerce Admin by selecting **[!UICONTROL Systems]** > [!UICONTROL Services] > **[!UICONTROL Commerce Services Connector]**.

To transmit data between your Adobe Commerce instance and the services that enable the AEM Assets Integration, configure the Commerce Services Connector with the following:

- Configure your Commerce instance with production and sandbox API keys for authentication.
- Specify a data space (SaaS identifier) for secure cloud storage.
- Sign into the same IMS organization that you use to access AEM Assets to establish the connection between your data set and the Adobe Experience Platform.

For detailed instructions, see [Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#organizationid).

When you configure the Commerce Services Connector, the system generates the SaaS project and database Ids. You need these ids during the tenant onboarding process.

![SaaS project and data space ids for AEM Assets integration](assets/aem-saas-project-config.png){width="600" zoomable="yes"}

## Configure Adobe I/O Events for Commerce

The AEM Assets Integration uses the Adobe I/O Events service to send custom event data between the Commerce instance and Experience Cloud. The event data is used to coordinate workflows for the AEM Assets integration.

>[!BEGINSHADEBOX]

**Prerequisite**

- Ensure that RabbitMQ is enabled and listening for events.
  - [RabbitMQ Setup for Adobe Commerce on premises](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
  - [RabbitMQ Setup for Adobe Commerce on cloud infrastructure](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)

- For projects on Commerce version 2.4.5, you must [install the Adobe I/O modules](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce). In Commerce version 2.4.6+, These modules are loaded automatically.

>[!ENDSHADEBOX]

### Enable the Commerce Eventing framework

Enable the eventing framework from the Commerce Admin.

1. From the Admin, go to **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Adobe I/O Events**.

1. Expand **[!UICONTROL Commerce events]**.

1. Set **[!UICONTROL Enabled]** to `Yes`.

   ![Adobe I/O Events Commerce Admin configuration - enable Commerce events](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Verify that [cron jobs are enabled](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration). Cron jobs are required for Commerce to manage communication and workflows between AEM Assets and Commerce.

## Get authentication credentials for API access

The AEM Assets Integration for Commerce requires OAuth authentication credentials to allow API access to the Commerce instance. These credentials are required to authenticate API requests when managing assets using the AEM Assets integration.

You generate the credentials by adding the integration to the Commerce instance and activating it.

### Add the integration to the Commerce environment

1. From the Admin, go to **System** > Extensions > **Integrations**, then click **Add New Integration**.

1. Enter information about the integration.

   In the **General** section, only specify the integration **Name** and **Email**. Use the email for an Adobe IMS account with access to the organization where Commerce and Experience Manager Assets are deployed.

   ![AEM Assets Integration for Commerce Admin configuration](assets/aem-add-commerce-integration.png){width="600" zoomable="yes"}

1. Verify your identity by clicking **Confirm Identity**.

   The system verifies your identity by authenticating to Experience Cloud with your Adobe Id.

1. Configure API resources.

   1. From the left panel, click **[!UICONTROL API]**.

   1. Select the external media resource **[!UICONTROL Catalog > Inventory > Products > External Media]**.

      ![Admin Integration config for API resources](assets/aem-commerce-integration-api-resources.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save]**.

### Generate credentials

On the Integrations page, generate the OAuth authentication credentials by clicking **Activate** for the Assets integration. You need these credentials to register the Commerce project with the Assets Rule Engine service, and to submit API requests to manage assets between Adobe Commerce and AEM Assets.

1. From the Integrations page, generate the credentials by clicking **[!UICONTROL Activate]**.

   ![Activate Commerce configuration for Assets integration](assets/aem-activate-commerce-integration.png){width="600" zoomable="yes"}

1. If you plan to use the API, save the credentials for the consumer key and access token to configure authentication in your API client.

   ![OAuth credentials to authenticate API requests](./assets/aem-commerce-integration-credentials.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Done]**.

>[!NOTE]
>
>You can also generate authentication credentials using the Adobe Commerce APIs. For details about this process and more information about OAuth-based authentication for Adobe Commerce, see [OAuth-based authentication](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in the Adobe Developer documentation.

