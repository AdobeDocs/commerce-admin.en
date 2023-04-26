---
title: Adobe Unified Shell Integration for Commerce Admin
description: Streamline cross-application workflows between Adobe Commerce and other Experience Cloud applications and improve user experience by integrating the Commerce Admin with Adobe Unified Shell
---
# Adobe Unified Shell for the Commerce Admin

Streamline cross-application workflows between Adobe Commerce and other Experience Cloud applications and improve the user experience by integrating the Commerce Admin with Adobe Unified Shell.

![Experience Cloud dashboard](./assets/uex-home-dashboard.png){width="700" zoomable="yes"}

When the extension is enabled, Commerce Admin users have single sign on access through Experience Cloud and a common interface to manage Experience Cloud applications and access Experience Cloud Platform services.

- **Commerce Admin users** continue using the same workflows to manage Commerce sites but can now complete additional tasks:

  - Search for product documentation, tutorials, and community posts
  - Access both Commerce-specific and global product announcements and notifications
  - Globally search within the context of the active application
  - Manage account preferences (alerts, notifications, and subscriptions)
  - Report issues or share ideas using the Feedback form
  - Switch seamlessly between Adobe Commerce and other Experience Cloud applications

- **Commerce application administrators** can deliver this enhanced experience by configuring the Commerce Admin for Unified Shell extension to enable the integration. The extension is available with Commerce 2.4.5 and later.

- **Commerce extension developers** can integrate with the Unified Shell application to deliver custom content, for example adding custom URLs to the integrated Help Center.

>[!IMPORTANT]
>
>This integration is available only for Commerce projects that use the [Adobe Identity Management Service (IMS)](../getting-started/adobe-ims-config.md) for authentication.

## Accessing Unified Shell capabilities from the Commerce Admin

When the Commerce Admin is integrated with Unified Shell, the Commerce Admin is hosted within the Unified Shell application framework, and the Commerce application header is replaced by the Unified Shell application header.

![Experience Cloud dashboard](./assets/uex-commerce-admin.png){width="700" zoomable="yes"}

Commerce Admin users can access additional capabilities from Unified Shell header.

| Option                                                     | Action                                                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Application Switcher](./assets/menu-icon.png)            | Navigate seamlessly between Adobe Commerce and other Experience Cloud applications using the Application selector. The applications and services available for selection depend on the applications and permissions provisioned for you within the organization. |
| ![Search icon](./assets/search-icon.png)                   | Globally search the current application context. For example, from the Commerce Admin you can search for any value in the Commerce database including product, customer, and order records.                                                                      |
| ![Help Center](./assets/help-icon.png)                     | Find product documentation, tutorials, and support articles in Adobe Experience League, and report issues or submit feedback from the integrated Help Center.                                                                                                    |
| ![Notifications](./assets/notifications-icon.png)          | View alerts and actionable updates, including product announcements, maintenance notices, and other important information                                                                                                                                        |
| ![User profile and account](./assets/preferences-icon.png) | View the account configuration for your Adobe profile  and set account preferences for notifications, subscriptions, and product data usage and collection.                                                                                                      |

{style="table-layout:auto"}

>[!NOTE]
>
>Find technical information and more detailed instructions for using the Unified Shell application header in the [Experience Cloud Central Interface Components Guide](https://experienceleague.adobe.com/docs/core-services/interface/experience-cloud.html#support).

## Authentication flow

When the Commerce Admin is integrated with Unified Shell, the Commerce Admin URL is redirected to a proxy URL. All Commerce Admin requests are then routed through the Unified Shell application.

If a Commerce Admin user opens the Commerce Admin URL configured for the project, they are are redirected to Experience Cloud to sign in.

![Experience Cloud login](./assets/uex-experience-cloud-login.png){width="700" zoomable="yes"}

To authenticate, Commerce Admins must sign in with the Adobe business profile for the organization associated with the Commerce instance. See [Manage Adobe profiles](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).


>[!TIP]
>
>If your Adobe ID is associated with more than one organization, you might have to switch organizations to access the Commerce application. See [Sign in to Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/experience-cloud.html#signin).


## Requirements

Your Commerce project must meet the following requirements to enable the Commerce Admin on Unified Shell extension and configure the integration.

- Adobe Commerce 2.4.5 or later
- Commerce instance configured to use [Adobe IMS for authentication services](../getting-started/adobe-ims-config.md)

### Adobe organization and user account provisioning

Organization and account provisioning required for the Unified Shell integration is performed by system administrators or developers with access to the root directory of the Commerce application and the Adobe Admin Console.

- Organization administrators create the organization and provision the user accounts, access permissions, and product entitlements from the [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html).

  When a new user is added to an organization, they receive an invitation with information about their access rights, the organization they have been added to, and a link to sign in. See [Organizations in Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=en).

- Commerce application technical administrators link the Commerce instance to an Adobe organization when they [configure the Adobe IMS integration](../getting-started/adobe-ims-config.md).

- Administrators with access to the organization from the Adobe Admin console can add and manage user accounts.  See [Configure Adobe Commerce users in the Admin Console](../getting-started/adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).


After organization and account provisioning is complete, Commerce Admin users have the permissions required to access the Commerce Admin when the Unified Shell integration is enabled.


>[!IMPORTANT]
>
>Role and resource permissions for Commerce Admin user accounts are still managed from the Commerce application. Commerce Admin users with the required access can add or update permissions from the Commerce Admin [System menu](../systems/permissions.md).

## Onboarding steps

1. Prepare the Commerce application environment.

1. Enable the Commerce Admin for Unified Shell integration using the Magento CLI.

1. Test the integration.

