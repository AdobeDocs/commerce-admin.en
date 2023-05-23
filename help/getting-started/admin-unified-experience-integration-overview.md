---
title: Adobe Experience Cloud Integration for Commerce Admin
description: Streamline cross-application workflows between Commerce and other Experience Cloud applications and improve user experience by enabling Experience Cloud common interface components for Commerce Admin users.
---
# Adobe Experience Cloud Integration for Commerce Admin

{{ee-feature}}

Streamline cross-application workflows between Adobe Commerce and other Experience Cloud applications and improve the user experience by integrating the Commerce Admin with Experience Cloud.

![Access Commerce from the Experience Cloud home page](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

The Commerce Admin Unified Experience extension (`magento/unified-shell-module`) enables the integration which provides single sign-on access to Admin from Experience Cloud.

- **Commerce Admin users** can use the same workflows to manage Commerce sites and complete additional tasks:

  - Search for product documentation, tutorials, and community posts in Adobe Experience League
  - Access both Commerce-specific and global product announcements and notifications
  - Globally search business objects using a global search (available for applications that have enabled search and Adobe Business Platform users)
  - Manage account preferences (alerts, notifications, and subscriptions)
  - Report issues or share ideas using the Feedback form
  - Switch seamlessly between Adobe Commerce and other Experience Cloud applications
  - Use the Commerce Projects workspace to view available projects and access both the storefront and Admin for each instance

- **Commerce application administrators** can deliver this enhanced experience by enabling the `magento/unified-shell-module` and configuring the Adobe I/O Events service.

- **Commerce extension developers** can integrate with Experience Cloud to deliver custom content, for example adding custom URLs to the integrated Help Center.

## View available Commerce projects

The Experience Cloud integration adds a Commerce Projects workspace to view available cloud environments from Experience Cloud.

![Commerce Projects workspace on Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

The workspace displays the available Commerce development and production environments with project details and access links:

- **Snapshot of Commerce storefront home page**—Snapshot of the storefront home page. If a project has multiple websites, the snapshot shows the home page for the default site.

- **[Project name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Identifies the cloud project environment for the instance. The Project name defaults to the [Git branch name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) in the cloud project. You can change or update the project name by updating the configuration for the Experience Cloud integration.

- **[Storefront URL](../stores-purchase/store-urls.md)**—Shows the base URL for the default website.

- **[Environment type](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Commerce instances deployed to a development or staging environment are identified with a [!UICONTROL Development] or [!UICONTROL Staging] label. Instances that do not have a label are deployed to a Production environment.

- **Commerce Admin access**—Open the Admin by clicking **[!UICONTROL Open]**.

- **Storefront access**—Open the storefront by selecting **[!UICONTROL Open storefront]** from the options menu.

- **Quick access to select projects**—Select **[!UICONTROL Add to Favorites]** from the options menu to add a project to the [!UICONTROL Favorites] tab.

## Access Experience Cloud resources from the Commerce Admin

When you open the Admin from the Commerce Projects workspace, the header includes additional options available with the Experience Cloud integration.

![Commerce Admin view when integrated with Experience Cloud](./assets/admin-uex-commerceadmin-view.png){width="700" zoomable="yes"}

Administrators can use these options to manage Commerce and other Experience Cloud applications provisioned for their account and quickly access resources from the integrated Help Center.

| Option                                                     | Action                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Organization Switcher](./assets/menu-icon.png)           | If your Adobe business profile is associated with multiple organizations, selecting the organization name displays the available organizations. When logged into an organization, the applications available depend on profile account provisioning. If an Admin user switches to an organization where they do not have permission for the Commerce application, the Commerce Admin session closes and the Experience Cloud home page is displayed. |
| ![Search icon](./assets/search-icon.png)                   | Globally search the current application context. For example, from the Commerce Admin you can search for any value in the Commerce database including product, customer, and order records.                                                                                                                                                                                                                                                          |
| ![Help Center](./assets/help-icon.png)                     | Find product documentation, tutorials, and support articles in Adobe Experience League, and report issues or submit feedback from the integrated Help Center.                                                                                                                                                                                                                                                                                        |
| ![Notifications](./assets/notifications-icon.png)          | View alerts and actionable updates, including product announcements, maintenance notices, and other important information                                                                                                                                                                                                                                                                                                                            |
| ![User profile and account](./assets/preferences-icon.png) | View the account configuration for your Adobe profile  and set account preferences for notifications, subscriptions, and product data usage and collection.                                                                                                                                                                                                                                                                                          |

{style="table-layout:auto"}

>[!NOTE]
>
>For more about the options available with the Experience Cloud integration, see the [Experience Cloud Central Interface Components Guide](https://experienceleague.adobe.com/docs/core-services/interface/experience-cloud.html#support).

## Authentication flow

When the Experience Cloud integration is enabled, the Admin URL for the Commerce application is redirected to a proxy URL. All Commerce Admin requests are then routed through Experience Cloud.

If the user has not authenticated through Experience Cloud, they are redirected to Experience Cloud to sign in.

![Experience Cloud Signin page](./assets/admin-uex-experience-cloud-login.png){width="700" zoomable="yes"}

To authenticate, administrators must sign into Experience Cloud with the Adobe business profile for the organization associated with the Commerce instance. See [Manage Adobe profiles](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

## Requirements

Your Commerce project must meet the following requirements to enable the Commerce Admin extension and configure the integration.

- Adobe Commerce 2.4.5 or later
- Adobe Commerce on cloud infrastructure
- Adobe Commerce must be configured to use [Adobe IMS authentication](../getting-started/adobe-ims-config.md)

## Enable the integration

The following components are required to enable the Experience Cloud integration on a Commerce instance:

- Commerce Admin Unified Experience extension (`magento/admin-unified-experience`)

  If the module is not available on the Commerce instance, it can be installed using Composer.

- [Adobe I/O Events service](https://developer.adobe.com/commerce/events/get-started/)  Required to send event data to coordinate workflows between Adobe services and the Commerce instance.

  The Adobe I/O Events integration with Commerce is enabled by the Commerce Event extension (`magento/commerce-eventing`) which is installed along with the Commerce Admin Unified Experience extension.

For detailed configuration instructions, see [Configure the Commerce Admin integration with Experience Cloud](admin-unified-experience-integration-configure.md).
