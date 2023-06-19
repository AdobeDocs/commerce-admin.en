---
title: Adobe Experience Cloud Integration for Commerce Admin
description: Learn about the Admin Unified Experience extension which integrates Commerce with Experience Cloud so that customers can access Commerce projects from the Experience Cloud home page.
hide: yes
hidefromtoc: yes
---
# Adobe Experience Cloud Integration for Commerce

{{ee-feature}}

>[!NOTE]
>
> This feature is for Beta users only and is not yet accessible to all customers. Contact your Adobe Commerce Beta program manager for assistance and questions.

Integrate Adobe Commerce projects with Experience Cloud by enabling the Admin Unified Experience extension. When the integration is active, administrators can access Commerce projects from Adobe Experience Cloud.

![Access Commerce from the Experience Cloud home page](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

From the Experience Cloud home page, select **[!UICONTROL Commerce]** to open the [!DNL Commerce Projects] workspace.

![Commerce Projects workspace on Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

The workspace displays the available Commerce development and production environments with project details and access links:

- **Snapshot of Commerce storefront home page**—Snapshot of the storefront home page. If a project has multiple websites, the snapshot shows the home page for the default site.

- **[Project name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Identifies the cloud project environment for the instance. The Project name defaults to the [Git branch name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) in the cloud project. Change or update the project name in the [Unified Experience store configuration settings](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[Storefront URL](../stores-purchase/store-urls.md)**—Shows the base URL for the default website.

- **[Environment type](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Commerce instances deployed to a development or staging environment are identified with a [!UICONTROL Development] or [!UICONTROL Staging] label. Instances that do not have a label are deployed to a Production environment.

- **Commerce Admin access**—Open the Admin by clicking **[!UICONTROL Open]**.

- **Storefront access**—Open the storefront by selecting **[!UICONTROL Open storefront]** from the options menu.

- **Quick access to select projects**—Select **[!UICONTROL Add to Favorites]** from the options menu to add a project to the [!UICONTROL Favorites] tab.

## Authentication flow

When the Experience Cloud integration is enabled, Commerce administrators can log in through the Experience Cloud sign in page.
![Experience Cloud Signin page](./assets/admin-uex-experience-cloud-login.png){width="700" zoomable="yes"}

Administrators must sign in to Experience Cloud with the Adobe business profile for the organization associated with the Commerce instance. See [Manage Adobe profiles](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

>[!NOTE]
>
>See [Manage the Experience Cloud Integration](admin-unified-experience-integration-manage.md) for details on how the authentication workflow is impacted when the Experience Cloud integration is enabled or disabled.

## Requirements

Your Commerce project must meet the following requirements to enable the Commerce Admin extension and configure the integration.

- Adobe Commerce 2.4.5 or later
- Adobe Commerce on cloud infrastructure
- Adobe Commerce must be configured to use [Adobe IMS authentication](../getting-started/adobe-ims-config.md)

## Enable the integration

The following components are required to enable the Experience Cloud integration on a Commerce instance:

- Commerce Admin Unified Experience extension (`magento/admin-unified-experience`)

  If the module is not available on the Commerce instance, it can be [installed using Composer](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/extensions.html).

- [Adobe I/O Events service](https://developer.adobe.com/commerce/events/get-started/)—Required to send event data to manage administrator access to Commerce projects from Experience Cloud.

  The Adobe I/O Events integration with Commerce is enabled by the Commerce Event extension (`magento/commerce-eventing`) which is installed along with the Commerce Admin Unified Experience extension.

For detailed configuration instructions, see [Configure the Commerce Admin integration with Experience Cloud](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>If the Experience Cloud integration is already enabled on the Commerce instance, see [Manage the Experience Cloud Integration](admin-unified-experience-integration-manage.md) for details about changing or updating the configuration, managing administrator access, and troubleshooting.
