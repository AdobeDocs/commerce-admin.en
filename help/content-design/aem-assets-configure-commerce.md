---
title: Install and configure
description: "Learn how to install and configure the [!DNL AEM Assets Integration for Adobe Commerce]"
feature: CMS, Media
---
# Install and configure the AEM Assets Integration for Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Get started with the AEM Assets integration for Adobe Commerce by configuring the Commerce application to use the AEM Assets integration and the Adobe I/O Events service.

## System requirements

**Software requirements**

- Adobe Commerce 2.4.5+
- PHP 8.1, 8.2, 8.3
- Composer: 2.x

## Prerequisites

- Adobe Commerce must be configured to use [Adobe IMS authentication](/help/getting-started/adobe-ims-config.md).
- Account provisioning and permissions—Administrators must have access to the following resources to configure the Experience Manager Assets integration:
  - Commerce application administrator—Install required modules and configure the Commerce application server from the Admin or the command line
  - [Commerce Admin](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html)—Update store configuration and manage Commerce user accounts
  - [Experience Manager Assets](https://experienceleague.adobe.com/en/docs/experience-manager-assets-essentials/help/introduction)—Adobe IMS application administrator or user account with access to complete tasks such as creating a folder structure, uploading assets, setting up permissions, setting up metadata forms, and creating public collections.

## Configuration overview

Enable the integration by completing the following tasks

1. [Install the AEM Assets integration extension (`aem-assets-integration`)](#install-the-aem-assets-integration-extension).
1. [Configure the Commerce Service Connector](#configure-the-commerce-services-connector) to connect your Adobe Commerce instance and with the services that enable data to be transmitted between Adobe Commerce and AEM Assets.
1. [Configure Adobe I/O Events for Commerce](#configure-adobe-io-events-for-commerce)
1. [Get authentication credentials for API access](#get-authentication-credentials-for-api-access)
1. [Onboard a new tenant](#onboard-new-tenant)

## Install the AEM Assets Integration extension

>[!BEGINSHADEBOX]

**Prerequisite**

- Access [repo.magento.com](https://repo.magento.com) to install the extension. For key generation and obtaining the necessary rights, see [Get your authentication keys](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys). For cloud installations, see the [Commerce on Cloud Infrastructure Guide](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/authentication-keys)

- Access to the command line of the Adobe Commerce application server.

>[!ENDSHADEBOX]

Install the latest version of the AEM Assets Integration extension (`aem-assets-integration`) on an Adobe Commerce running Adobe Commerce 2.4.4 or later. The AEM Asset Integration is delivered as a composer metapackage from the [repo.magento.com](https://repo.magento.com/) repository.

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

1. Add the Catalog Service module.

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

1. Use Composer to add the Catalog Service module to your project:

   ```shell
   composer require "magento/aem-assets-integration" "version tbd"  --no-update
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
   >In some cases, particularly when deploying to production, you might wish to avoid clearing compiled code because it can take some time. Ensure that you back up your system before making any changes.

>[!ENDTABS]

## Configure the Commerce Services Connector

To transmit data between your Adobe Commerce instance and the services that enable the AEM Assets Integration, configure the Commerce Services Connector with the following:

- Configure your Commerce instance with production and sandbox API keys for authentication.
- Specify a data space (SaaS identifier) for secure cloud storage.
- Connect to your organizations dataset on Adobe Experience Platform by signing into the same IMS organization that you use to access AEM Assets.

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

>[!ENDSHADEBOX]

>[!NOTE]
>
>For detailed information about Adobe I/O Events for Commerce, see the [Adobe I/O Events for Commerce](https://developer.adobe.com/commerce/extensibility/events/) documentation on the Adobe Developer site.

Set up requires the following steps.

1. Enable the Commerce Eventing framework by configuring Adobe I/O events on the application server and in the Admin.
1. Enable data synchronization between Adobe Commerce and AEM Assets by using the Assets Rules Engine Service API to configure the connection
1. Enable the AEM Assets integration in the Admin

### Enable the Commerce Eventing framework

Enable the Commerce eventing framework by using the instructions for the environment where your Commerce project is deployed.

>[!BEGINTABS]

>[!TAB Cloud infrastructure]

1. Enable the Adobe I/O Events service from the [!DNL Store Settings Configuration] menu.

   1. From the Admin, go to **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Adobe I/O Events**.

   1. Expand **[!UICONTROL Commerce events]**.

   1. Set **[!UICONTROL Enabled]** to `Yes`.

      ![Adobe I/O Events Commerce Admin configuration - enable Commerce events](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >You must [enable cron](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration) so that Commerce can send events to the API endpoints for managing communication and workflows for the Commerce Assets integration.

1. Update the cloud project configuration.

   1. Add the `app/etc/config.php` file to your working repository:

     ```shell
     git add app/etc/config.php
     ```

   1. Run the `composer info magento/ece-tools` command to determine your version of ece-tools. If the version is less than `2002.1.13`, [update to the most recent version](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/ece-tools/update-package.html).

   1. Enable eventing in the `.magento.env.yaml` file:

      ```yaml
      stage:
         global:
            ENABLE_EVENTING: true
      ```

   1. Commit and push updated files to the Cloud environment.

>[!TAB On-premises]

1. Enable the Adobe I/O Events service from the [!DNL Store Settings Configuration] menu.

   1. From the Admin, go to **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **Adobe I/O Events**.

   1. Expand **[!UICONTROL Commerce events]**.

   1. Set **[!UICONTROL Enabled]** to `Yes`.

      ![Adobe I/O Events Commerce Admin configuration - enable Commerce events](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >You must [enable cron](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration) so that Commerce can send events to the API endpoints for managing communication and workflows for the Commerce Assets integration.

>[!ENDTABS]

## Get authentication credentials for API access

The AEM Assets Integration for Commerce requires OAuth authentication credentials to allow API access to the Commerce instance. You need these credentials to register the Commerce project with the Assets Rule Engine service during tenant onboarding, and to submit API requests to manage assets between Adobe Commerce and AEM Assets.

You generate the credentials by adding the integration to the Commerce instance and activating it.

### Add the integration

1. From the Admin, go to **System** > Extensions > **Integrations**, then click **Add New Integration**.

1. Enter information about the integration.

   In the **General** section, only specify the integration **Name** and **Email**. Use the email for an Adobe IMS account with access to the organization where Commerce and Experience Manager Assets are deployed.

   ![AEM Assets Integration for Commerce Admin configuration](assets/aem-add-commerce-integration.png){width="600" zoomable="yes"}

1. Verify your identity by clicking **Confirm Identity**.

   The system verifies your identity by authenticating to Experience Cloud with your Adobe Id.

1. Configure API resources.

   1. From the left panel, click **[!UICONTROL API]**.
E
   1. Select the external media resource (**[!UICONTROL Catalog > Inventory > Products > External Media]**.

     ![Admin Integration config for API resources](assets/aem-commerce-integration-api-resources.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save]**.

### Generate credentials

On the Integrations page, generate the OAuth authentication credentials by clicking **Activate** for the Assets integration. You need these credentials to register the Commerce project with the Assets Rule Engine service, and to submit API requests to manage assets between Adobe Commerce and AEM Assets.

1. From the Integrations page, generate the credentials by clicking **[!UICONTROL Activate]**.

   ![Activate Commerce configuration for Assets integration](assets/aem-activate-commerce-integration.png){width="600" zoomable="yes"}

1. Save the credentials for the consumer key and access token for later use.

  ![OAuth credentials to authenticate API requests](./assets/aem-commerce-integration-credentials.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Done]**.

>[!NOTE]
>
>You can also generate authentication credentials using the Adobe Commerce APIs. For details, about this process and more information about OAuth-based authentication for Adobe Commerce, see [OAuth-based authentication](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in the Adobe Developer documentation.












