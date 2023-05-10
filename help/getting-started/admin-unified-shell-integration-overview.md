---
title: Adobe Experience Cloud Integration for Commerce Admin
description: Streamline cross-application workflows between Commerce and other Experience Cloud applications and improve user experience by enabling Experience Cloud common interface components for Commerce Admin users.
---
# Adobe Experience Cloud Integration for Commerce Admin

Streamline cross-application workflows between Adobe Commerce and other Experience Cloud applications and improve the user experience by integrating the Commerce Admin with Experience Cloud.

![Experience Cloud ](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

The Experience Cloud extension for Commerce Admin, `magento/unified-shell-module` enables the integration. When the extension is enabled, Commerce Admin users have single sign-on access through Experience Cloud and a common interface to manage available Experience Cloud applications.

- **Commerce Admin users** continue using the same workflows to manage Commerce sites but can now complete additional tasks:

  - Search for product documentation, tutorials, and community posts in Adobe Experience League
  - Access both Commerce-specific and global product announcements and notifications
  - Globally search business objects using a global search (available for applications that have enabled search and Adobe Business Platform users)
  - Manage account preferences (alerts, notifications, and subscriptions)
  - Report issues or share ideas using the Feedback form
  - Switch seamlessly between Adobe Commerce and other Experience Cloud applications

- **Commerce application administrators** can deliver this enhanced experience by enabling the `magento/unified-shell-module` and configuring the Adobe I/O Events service from the Commerce Admin.

- **Commerce extension developers** can integrate with the Experience Cloud to deliver custom content, for example adding custom URLs to the integrated Help Center.

>[!IMPORTANT]
>
>The Experience Cloud integration with the Commerce Admin is available only for Commerce sites deployed on Adobe cloud infrastructure that use the [Adobe Identity Management Service (IMS)](../getting-started/adobe-ims-config.md) for authentication.


## View available Commerce projects

Commerce administrators can view and manage available projects by selecting [!UICONTROL Commerce] from the [!UICONTROL Experience Cloud Home].

![Experience Cloud dashboard](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Commerce Projects displays the available Commerce development, staging, and production environments and provides project details and access links:

- **Snapshot of Commerce storefront home page**—If you have multiple sites, the storefront snapshot helps identify the right project more quickly.

- **[Environment name and type](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=en)**— Displays the cloud project environment name and indicates whether it is Development, Staging, or Production environment. The environment name corresponds to the [Git branch name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) that has the source code for the project.

- **Commerce Admin access**—Open the Commerce Admin by clicking **[!UICONTROL Select]**.

- **Storefront access**—Open the storefront by selecting [!UICONTROL Open storefront] from the options menu. Also, the [Storefront URL](../getting-started/login-urls.md#storefront-url) is displayed on the card.

- **Quick access to select projects**—Select **[!UICONTROL Add to Favorites]** from the options menu to add a project to Favorites.



## Access Experience Cloud resources from the Commerce Admin

When the integration with Experience Cloud is enabled, Commerce Admin users sign in through Experience Cloud. Then, they can use the additional options available in the Experience Cloud header.

![Experience Cloud dashboard](./assets/admin-uex-commerceadmin-view.png){width="700" zoomable="yes"}

Admin users can use the options in the header to manage Commerce and other Experience Cloud applications provisioned for their account, their Adobe account, and quickly access resources from the integrated Help Center.

| Option                                                     | Action                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Organization Switcher](./assets/menu-icon.png)           | If your Adobe business profile is associated with multiple organizations, selecting the organization name displays the available organizations. When logged into an organization, the applications available depend on profile account provisioning. If a Commerce Admin user switches to an organization where they do not have Commerce application permission, the Commerce Admin session closes and the Experience Cloud home page is displayed. |
| ![Search icon](./assets/search-icon.png)                   | Globally search the current application context. For example, from the Commerce Admin you can search for any value in the Commerce database including product, customer, and order records.                                                                                                                                                                                                                                                          |
| ![Help Center](./assets/help-icon.png)                     | Find product documentation, tutorials, and support articles in Adobe Experience League, and report issues or submit feedback from the integrated Help Center.                                                                                                                                                                                                                                                                                        |
| ![Notifications](./assets/notifications-icon.png)          | View alerts and actionable updates, including product announcements, maintenance notices, and other important information                                                                                                                                                                                                                                                                                                                            |
| ![User profile and account](./assets/preferences-icon.png) | View the account configuration for your Adobe profile  and set account preferences for notifications, subscriptions, and product data usage and collection.                                                                                                                                                                                                                                                                                          |

{style="table-layout:auto"}

>[!NOTE]
>
>Find technical information and more detailed instructions for using the Experience Cloud header in the [Experience Cloud Central Interface Components Guide](https://experienceleague.adobe.com/docs/core-services/interface/experience-cloud.html#support).

## Authentication flow

When the Commerce Admin is integrated with Experience Cloud, the Commerce Admin URL is redirected to a proxy URL. All Commerce Admin requests are then routed through Experience Cloud.

If the user has not authenticated through Experience Cloud, they are redirected to Experience Cloud to sign in.

![Experience Cloud login](./assets/admin-uex-experience-cloud-login.png){width="700" zoomable="yes"}

To authenticate, Commerce Admins must sign in with the Adobe business profile for the organization associated with the Commerce instance. See [Manage Adobe profiles](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).


>[!TIP]
>
>If your Adobe ID is associated with more than one organization, you might have to switch organizations to access the Commerce application. See [Sign in to Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/experience-cloud.html#signin).


## Prerequisites

Your Commerce project must meet the following requirements to enable the Commerce Admin extension and configure the integration.

- Adobe Commerce 2.4.5 or later
- Adobe Commerce must be configured to use the following Adobe Services
  - [Adobe IMS for authentication services](../getting-started/adobe-ims-config.md)
  - [Adobe I/O Events for Adobe Commerce](https://developer.adobe.com/commerce/events/get-started/)

>[!NOTE]
>
>Configuring the integration between Adobe Commerce and Adobe Services requires an Adobe Developer account with System Administrator or Developer Role permissions. See [Getting Started with Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/)

### Adobe organization and user account provisioning

Organization and account provisioning required to integrate the Commerce Admin from Experience Cloud is completed by system administrators or developers [SSH access to the Commerce application server](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html).


| Role                                                                                                                        | Tasks                                                                                                                                                                                                                                                                                                                                | Access                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Adobe Organization Administrator**                                                                                        | Create the organization and provision the user accounts, access permissions, and product entitlements from the [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html).                                                                                                                                           | [Adobe Admin Console System Administrator](https://helpx.adobe.com/enterprise/using/admin-roles.html)                                                                                                                                                                                                                                            |
| **Commerce system integrator (SI)**<br>**Technical administrator for Commerce project**<br>**Adobe Support representative** | Use the Developer Console to [configure the Adobe IMS integration](../getting-started/adobe-ims-config.md) for an instance<br><br>Create the Adobe I/O Events App Builder project for the Commerce instance.<br><br>Provide the credentials and connection information to configure the IMS integration and Adobe I/O Events service | [Developer Console access](https://developer.adobe.com/developer-console/docs/guides/getting-started/)— System Administrator or Developer role for organization<br></br>[Commerce project admin](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) with  Commerce application server using SSH |
| **Commerce Administrator**                                                                                                  | Add and manage user accounts from Commerce Admin and the Adobe Admin Console<br><br>View and manage Commerce projects from Experience Cloud, and manage the Commerce application, system, and service configuration from the Commerce Admin.                                                                                         | [Adobe Admin Console Product Profile Admin](https://helpx.adobe.com/enterprise/using/admin-roles.html)<br><br>[Commerce Admin user](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html?lang=en)                                                                                                                |

After organization and account provisioning is complete, Commerce Admin users have the permissions required to sign in to Experience Cloud to view and manage their Commerce instances.

When a new user is added to an organization, they receive an invitation with information about their access rights, the organization they have been added to, and a link to sign in. See [Organizations in Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=en).


>[!IMPORTANT]
>
>Role and resource permissions for Commerce Admin user accounts are still managed from the Commerce application. Commerce Admin users with the required access can add or update permissions from the Commerce Admin [System menu](../systems/permissions.md).

## Onboarding steps

1. Prepare the Commerce application environment.

1. Enable the Experience Cloud integration for the Commerce Admin using the Commerce command-line tool.

1. Test the integration.

