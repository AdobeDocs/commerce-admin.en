---
title: Commerce Admin in Adobe Unified Experience
description: Learn how Adobe Commerce as a Cloud Service customers access and navigate the Commerce Admin in Adobe Unified Experience and return to Classic UI.
feature: Admin Workspace
role: Admin, User
level: Beginner
badgeSaas: label="SaaS only" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service projects only (Adobe-managed SaaS infrastructure)."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
    internal-label: Admin tools and workspace
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
    internal-label: Admin workspace
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Commerce Admin in Adobe Unified Experience

The Commerce Admin for Adobe Commerce as a Cloud Service opens in Adobe Unified Experience when you select an instance name in Commerce Cloud Manager.

The Adobe Unified Experience interface provides the shared top navigation used across Adobe products, an updated left navigation, and refreshed Admin page styling.

You can switch between organizations, products, and Commerce instances, and access help, notifications, and account preferences from the top navigation. Your existing Commerce role permissions continue to determine which Admin menu items you can access.

>[!NOTE]
>
>Commerce Admin in Unified Experience (Unified Shell UI) is available only for Adobe Commerce as a Cloud Service. Adobe Commerce on cloud infrastructure and Adobe Commerce on-premises customers continue to use the [classic Commerce Admin UI](admin.md).

![Commerce Admin dashboard with Unified Experience top navigation and Commerce left navigation](./assets/admin-unified-experience-overview.png){width="700" zoomable="yes" border="light"}

## Open the Commerce Admin

After you sign in to [Adobe Experience Cloud](https://experience.adobe.com/), open Commerce Cloud Manager. Then, select an instance to open the Admin in Unified Experience.

The sign-in flow lets you move between Commerce instances without signing in separately to each instance.
You can move between Adobe products and Commerce instances without further sign-in prompts.

For the access procedure, see [Access an instance](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/getting-started#access-an-instance) in the _Adobe Commerce as a Cloud Service Guide_.

>[!BEGINTABS]

>[!TAB Open the Admin from Commerce Cloud Manager]

![Open the Admin](./assets/admin-uex-seamless-login-cloud-manager-to-instance.png){width="700" zoomable="yes" border="light"}

>[!TAB See it in action]

![Open the Admin from Commerce Cloud Manager](./assets/admin-uex-seamless-login-cloud-manager-to-instance.gif){width="700" zoomable="yes" border="light"}

>[!ENDTABS]

### Choose an Admin interface {#classic-ui}

For the initial release of the Commerce Admin in Unified Experience, Adobe Commerce as a Cloud Service supports two Commerce Admin experiences, the Unified Experience (Unified Shell UI) and the Classic UI interface.

By default, when you select a Commerce instance in Commerce Cloud Manager, the Commerce Admin opens in the Unified Experience (Unified Shell UI). To switch back to the Classic UI, use an existing bookmark or find the URL for the Classic UI. See [Open Classic UI](#open-classic-ui).

The links for the Unified Experience and Classic UI are available in the instance details panel in Commerce Cloud Manager.

| Link | Experience |
| --- | --- |
| **[!UICONTROL Admin URL (Unified Shell UI)]** | Opens the Admin in Unified Experience. |
| **[!UICONTROL Admin URL (Classic UI)]** | Opens the previous Admin interface. |

![Illustration of Commerce Cloud Manager instance details showing the Unified Shell UI and Classic UI Admin URL choices](./assets/admin-unified-experience-cloud-manager-instance-details.png){width="960" zoomable="yes" border="light"}

_Illustration based on the instance-list screenshot and the updated instance-details design. The URLs shown use staging hosts._

#### URL formats

| Experience | URL pattern |
| --- | --- |
| Unified Experience | `https://<experience-cloud-host>/#/@<organization>/in:<instance-id>/commerce/cloud-service/admin` |
| Classic UI | `https://<commerce-admin-host>/<instance-id>/admin/` |

Unified Experience identifies the organization after `@` and the instance after `in:`. Classic UI places the instance ID directly after the hostname.

For example, these staging URLs open the same instance:

- **Unified Experience**: `https://experience-stage.adobe.com/#/@adobe-commerce-uex/in:<instance-id>/commerce/cloud-service/admin`
- **Classic UI**: `https://na1-stage.admin.commerce.adobe.com/<instance-id>/admin/`

These staging hostnames are not production URLs. Always use your instance links from Commerce Cloud Manager rather than constructing URLs.

#### Open Classic UI

To open the Classic UI:

- Use an existing Classic Admin bookmark or URL. These URLs only open the Classic UI and do not redirect to Unified Experience.
- Select **[!UICONTROL Admin URL (Classic UI)]** in the Commerce Cloud Manager instance details.

There is no interface switch inside the Admin. Use Commerce Cloud Manager or a saved Admin URL to return to the classic interface if you need it.

## Identify your organization and instance

Before you make changes, check the organization and instance that you are working in:

- The account menu shows your current organization.
- The instance switcher in the top navigation shows the instance name and a **[!UICONTROL Production]** or **[!UICONTROL Sandbox]** badge.

Use the environment badge to distinguish a production instance from a sandbox when you switch between instances.

## Switch organizations, products, and instances

The top navigation provides separate controls for switching your working context.

### Switch organizations

Use the organization switcher in the top navigation to move between the organizations that you have access to.

1. In the top navigation, select the organization name.

1. Select an organization from the list.

   The list shows the organizations that you have access to. A check mark identifies the organization that you are working in.

>[!BEGINTABS]

>[!TAB Organization switcher]

![Organization switcher](./assets/admin-uex-org-switcher.png){width="700" zoomable="yes" border="light"}

>[!TAB See it in action]

![Organization switcher](./assets/admin-uex-org-switcher.gif){width="700" zoomable="yes" border="light"}

>[!ENDTABS]

The account menu also shows which organization you are working in. Select your profile picture (![Account](./assets/admin-unified-experience-icon-account.png){width="24"}) in the top navigation, and then check the **[!UICONTROL Organization]** line.

![Account menu showing the current organization](./assets/admin-uex-account-menu-organization.png){width="700" zoomable="yes" border="light"}

The instances that you can open belong to the organization that you are working in. To change instances, see [Switch Commerce instances](#switch-commerce-instances).

### Switch products

Use the product switcher (![Product switcher](./assets/admin-unified-experience-icon-product-switcher.png){width="24"}) in the top navigation to change applications at any time. It works the same way as in other Adobe products.

- **Admin Console**: Open Adobe Admin Console from the product switcher to manage users and their access (**[!UICONTROL Administer]** > **[!UICONTROL Users]**). You do not need to remember the URL. Adobe Admin Console is separate from the Commerce Admin, where you manage your store.
- **Adobe Exchange**: Find third-party extensions, plugins, scripts, and enterprise integrations across Adobe Creative Cloud, Adobe Experience Cloud, and Adobe Document Cloud.
- **Other products**: Open products such as Coworker.

>[!BEGINTABS]

>[!TAB Product switcher menu]

![Product switcher menu](./assets/admin-uex-product-dropdown.png){width="700" zoomable="yes" border="light"}

>[!TAB See it in action]

![Product switcher menu](./assets/admin-uex-product-dropdown.gif){width="700" zoomable="yes" border="light"}

>[!ENDTABS]

For Adobe Commerce as a Cloud Service user and role management, see [User management](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/user-management).

### Switch Commerce instances

The top navigation includes an instance switcher button. It always shows the **[!UICONTROL Production]** or **[!UICONTROL Sandbox]** badge and the name of the instance that you are in.

1. In the top navigation, select the instance switcher that displays your current instance name and environment badge.

1. Select an instance from the list.

   The list contains the Adobe Commerce as a Cloud Service instances that you can access in the current organization. You do not need to return to Commerce Cloud Manager to switch instances, so you can move back and forth between instances.

1. Check the instance name and environment badge before continuing your work.

The instance is part of the page URL, so you can bookmark or share a link that opens a specific instance. If you open the Admin without an instance in the link, it loads the last instance that you used.

## Use the left navigation

The Commerce Admin menu appears in the left navigation of the Adobe Unified Experience shell. Expand or collapse menu sections to find the tools that you need, or type to jump to a menu item.

The menu is specific to the instance that you are working in. When you switch instances, the left navigation updates to match.

Your existing role permissions carry over. You see only the menu items that your role allows.

Continue to use the Admin Guide for tasks such as managing products, orders, customers, and configuration. Admin pages have refreshed styling, so their appearance can differ from screenshots of Classic UI in this guide.

>[!BEGINTABS]

>[!TAB Commerce Admin left navigation]

![Commerce Admin left navigation](./assets/admin-uex-left-navigation.png){width="700" zoomable="yes" border="light"}

>[!TAB See it in action]

![Commerce Admin left navigation](./assets/admin-uex-left-navigation.gif){width="700" zoomable="yes" border="light"}

>[!ENDTABS]

## Get help and provide feedback

To access resources without leaving your Commerce Admin, open the help panel using the help icon (![Help](./assets/admin-unified-experience-icon-help.png){width="24"}) in the top navigation.

- **Help**: Search Adobe Experience League for documentation directly from the panel.
- **Support**: Access community forums and other learning resources, and find your support tickets on Adobe Experience League.
- **Feedback**: Submit feedback to Adobe from the same panel.

Help, support, and feedback are available in context. You stay in your Commerce Admin and do not lose your place.

>[!BEGINTABS]

>[!TAB Help panel]

![Help panel](./assets/admin-uex-help-search.png){width="700" zoomable="yes" border="light"}

>[!TAB See it in action]

![Help panel](./assets/admin-uex-help-search.gif){width="700" zoomable="yes" border="light"}

>[!ENDTABS]

## View notifications {#view-notifications}

To view notifications, requests, and product announcements in context, open the notifications panel using the bell icon (![Notifications](./assets/admin-unified-experience-icon-notifications.png){width="24"}) in the top navigation.

The panel brings your **[!UICONTROL Requests]**, **[!UICONTROL Notifications]**, and **[!UICONTROL Announcements]** together in one place. You do not need to leave the Commerce Admin to see any of them.

Use the bell icon in the Unified Experience top navigation for this panel, rather than the notification control within the Commerce page header. For instructions about Commerce Admin inbox messages, see [Message inbox](admin-message-inbox.md).

>[!BEGINTABS]

>[!TAB Notifications panel]

![Notifications panel](./assets/admin-uex--notifications-bell.png){width="700" zoomable="yes" border="light"}

>[!TAB See it in action]

![Notifications panel](./assets/admin-uex--notifications-bell.gif){width="700" zoomable="yes" border="light"}

>[!ENDTABS]

## Manage account preferences

Select your profile picture (![Account](./assets/admin-unified-experience-icon-account.png){width="24"}) in the top navigation to open the account menu. From this menu, you can:

- View the organization that you are working in.
- Turn on dark mode with the **[!UICONTROL Dark theme]** toggle.
- Open your user preferences.

>[!BEGINTABS]

>[!TAB Account menu with dark mode]

![Account menu with dark mode](./assets/admin-uex-dark-mode.png){width="700" zoomable="yes" border="light"}

>[!TAB See it in action]

![Account menu with dark mode](./assets/admin-uex-dark-mode.gif){width="700" zoomable="yes" border="light"}

>[!ENDTABS]

## Updated page styling

Pages in the Commerce Admin have a refreshed look that matches the Adobe Unified Experience shell. More restyling is planned for later releases.
