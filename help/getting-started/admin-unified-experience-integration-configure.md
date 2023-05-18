---
title: Configure the Commerce Admin Integration with Experience Cloud
description: Learn about the requirements and process to configure a Commerce on cloud infrastructure environment to deploy the Commerce Admin in the Adobe Unified Shell interface to provide Admin users with an improved user experience.
---
# Configure the Commerce Admin Integration with Experience Cloud

Get started with the Commerce Admin Integration with Experience Cloud by configuring the Commerce application to use the Commerce Admin Unified Experience and Commerce Events extensions.

## Prerequisites

- Adobe Commerce 2.4.5 or later
- Adobe IMS integration enabled on the cloud environment
- Account provisioning and permissions—Administrators must have access to the following resources to configure the integration for Commerce Admin:
  - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html)—Add and manage Adobe user and developer accounts for the organization
  - [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/)—Developer or system administrator access to generate connection credentials and information for the Adobe I/O Events service
  - [Commerce on cloud infrastructure project](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html?lang=en#get-started-with-the-project-web-interface)—Install required modules and configure the Commerce application server using the Adobe Commerce CLI
  - [Commerce Admin](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html)—Update store configuration and manage Commerce user accounts

## Configuration overview

The configuration process for the Experience Cloud integration requires access to the command line of the Commerce application server, access to the Adobe Developer and Adobe Admin Consoles, and experience [configuring and updating Commerce on cloud infrastructure projects](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/overview.html?lang=en).

Enable the integration by completing the following tasks:

1. [Check the Commerce environment and application configuration](#check-the-commerce-environment-and-application-configuration).

1. [Enable the Commerce Admin Unified Experience extension](#enable-the-commerce-admin-unified-experience-extension).

1. [Set up Adobe I/O Events for Commerce](#set-up-adobe-io-events).

1. [Test the integration](#test-the-integration).

## Check the Commerce environment and application configuration

Before configuring the Experience Cloud integration, verify that your project and Commerce application meet the requirements.

- IMS is enabled on the Commerce instance
- Commerce Admin administrators for the Commerce instance can successfully authenticate using their Adobe ID
- Required extensions are available in the cloud project environment

1. On your local workstation, change to the project directory for your Commerce project.

1. Check out the environment branch for the instance you want integrate with Experience Cloud.

1. Verify that Adobe IMS is enabled.

   - Use the [SSH Access URL](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) for the environment to connect to the Commerce application server.

   - From the command line, use the Adobe Commerce CLI to check the IMS module status.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

    If the module is not enabled, [enable it using the Organization and credentials for the IMS integration project](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module). If you don't have the credentials, submit an Adobe Support ticket.

1. Verify that the Admin user can log into the Commerce Admin using their Adobe ID.

   - Go the Commerce Admin URL.

   - If you are logged in, log out.

   - Ensure that the Admin user is redirected to log in using their Adobe ID.

     ![Experience Cloud](./assets/admin-adobeid-login.png){width="700" zoomable="yes"}

1. Verify that the Commerce Admin Unified Experience extension is available on your instance.

   - From the cloud project directory on your local workstation, use composer to find the extension.

     ```bash
     composer show *unified-experience**
     ```

    If the extension is installed, Composer returns the information about the extension.

    ```
    magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
    ```

    If the extension is not installed, use Composer to install it. Then, commit the changes and redeploy the cloud environment.

    ```bash
    composer require magento/module-unified-experience
    composer update
    ```

## Enable the Commerce Admin Unified Experience extension

Enable the Commerce Admin Unified Experience extension, and then log in through Experience Cloud.

1. From the root directory of your Cloud project environment on your local workstation, use the [magento-cloud CLI tool](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli.html) to log in to the Commerce application server.

   ```bash
   magento-cloud ssh
   ```

1. Enable the `magento/module-unified-experience` extension using the Adobe Commerce CLI:

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. Clear the cache.

   ```bash
   bin/magento cache:clean
   Admin Unified Experience integration is enabled
   ```

1. Verify that you can log in to the Commerce Admin through Experience Cloud.

   - In an incognito browser window, navigate to the store Admin URL to sign in through Experience League.

     ![Experience Cloud](./assets/admin-uex-login.png){width="700" zoomable="yes"}

1. Enter your Adobe ID to log in.

   If your Adobe ID is associated with more than one Organization ID, select the Organization ID associated with the Commerce instance.

1. After you log in, the Commerce Admin opens within the Experience Cloud interface.

   ![Commerce Admin view with Experience Cloud integration](./assets/admin-uex-commerceadmin-view.png){width="700" zoomable="yes"}

## Set up Adobe I/O Events for Commerce

After you can log in successfully through Experience Cloud, set up the Adobe I/O Events service.

The Commerce Admin Unified Experience extension uses the Adobe I/O Events service to send custom event data from the Commerce instance to Experience Cloud. The event data is used to coordinate workflows for the Experience Cloud integration, including redirecting Commerce Admin requests through Experience Cloud and managing access to available Commerce projects.

To enable the Adobe I/O Events service, complete the following set up and configuration tasks.

- Create an Adobe Developer App Builder project

- Enable the Commerce Events extension (`magento/commerce-eventing`)  on the cloud environment.

- Configure the Adobe I/O events service and Commerce event provider to send data from the Commerce instance to the App Builder project


>[!NOTE]
>
>The following procedures provide high-level instructions for setting up the Adobe I/O Events service with notes and links to more detailed documentation. Learn more about Adobe Developer App Builder and Adobe I/O events by completing the [Introduction to App Builder tutorial](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/adobe-developer-app-builder/introduction-to-app-builder.html#adobe-developer-app-builder).

### Create an App Builder project

Create an Adobe Developer App Builder project to consume the custom Commerce event data provided by the Commerce Admin Unified Experience extension and make it available to Adobe services and other third-party applications.

1. From the Adobe Developer Console, [create an App Builder project](https://developer.adobe.com/commerce/events/get-started/project-setup/) to consume event data from the Experience Cloud integration.

   - When you add and save the Adobe I/O Management API, the credentials to connect to the Commerce instance are downloaded to your local environment in a configuration file (`config.zip`).

   - After you add the Adobe I/O Events for Commerce API, download the workspace configuration file from the Workspace overview page by selecting **[!UICONTROL Download all]**.

### Enable the Commerce Events extension

Enable the Commerce Events extension (`magento/commerce-eventing`)  on the cloud environment. This extension manages the process to send custom event data from the Commerce application to the Adobe I/O Events service. The Commerce Events extension is installed automatically as a dependency of the Commerce Admin Unified Experience extension.

1. From your local Commerce project development environment, add the following configuration to the `.magento.env.yaml` file.

     ```yaml
     stage:
       global:
         ENABLE_EVENTING: true
       deploy:
         CRON_CONSUMERS_RUNNER:
           cron_run: true
           max_messages: 0
           consumers: []
     ```

1.  Add, commit, and deploy the updated `.magento.env.yaml file` to the cloud environment.

### Configure the Adobe I/O events service and event provider

Configure the Adobe I/O events service and Commerce event provider on the Commerce instance. Then, update the App Builder project to add the event provider and subscribe to the events used to monitor and manage the Experience Cloud integration.

1. From the Commerce Admin, [configure Adobe Commerce to use the Adobe I/O Events service](https://developer.adobe.com/commerce/events/get-started/configure-commerce/).

1. From the Adobe Developer Console, [add the Commerce event provider and subscribe to events](https://developer.adobe.com/commerce/events/get-started/configure-commerce/#subscribe-and-register-events) from the Commerce Admin Unified Experience extension.

   ![Experience Cloud](./assets/uex-event-registration-selection.png){width="700" zoomable="yes"}

## Test the integration

Verify that a Commerce Administrator can view and manage Commerce instances and access other Experience Cloud applications and services using the common interface.

1. [Sign in to Experience Cloud](https://experiencecloud.adobe.com/login?referrer_uri=https://experiencecloud.adobe.com/library) using the Adobe ID and the Company or School account associated with the Commerce instance.

  ![Experience Cloud ](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

1. View available Commerce Projects by selecting [!UICONTROL Commerce].

   ![Experience Cloud dashboard](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

1. Open the Commerce Admin for an instance by selecting **[!UICONTROL Open]**.

   ![Experience Cloud dashboard](./assets/admin-uex-commerceadmin-view.png){width="700" zoomable="yes"}

   Try out the [options available in the header](admin-unified-experience-integration-overview.md#access-experience-cloud-resources-from-the-commerce-admin) to open the Help Center, switch to another Experience Cloud application or back to [!UICONTROL Experience Cloud Home].





1. View available Commerce Projects

1. Open the Commerce Admin.

1. Verify access to Experience Cloud services

1. Verify that you can complete tasks in the Commerce Admin as expected.

