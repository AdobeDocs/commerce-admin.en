---
title: Manage the Experience Cloud Integration
description: Learn how to manage the Experience Cloud integration and troubleshoot issues
---
# Manage the Experience Cloud Integration

After initial enablement, change the status of the the Experience Cloud integration by enabling or disabling the Commerce Admin Unified Experience extension.

Before disabling or enabling the extension, notify Commerce Admin users about changes to the authentication and Admin workflows to prevent business disruptions.

The following table outlines different scenarios for enabling or disabling the Experience Cloud integration and the impact on authentication and Admin workflows.

| Scenario                                                                                         | Action                                                 | Changes to authentication workflow                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Troubleshoot Commerce application issues<br><br>Administrators cannot log into Commerce instance | Disable the integration                                | <ul><li>Admin users that are logged in get application or `404 page not found` errors when they refresh, or when their session expires.</li><li>Navigate to the default Admin URL to be redirected sign in using Adobe ID account credentials.</li><li>Requests to Commerce Admin are routed through the Commerce application.</li></ul>                                                            |
| Testing completed<br><br>Administrator access restored                                           | Enable the integration                                 | <ul><li>Log in through Experience Cloud or navigate to default Admin URL to be redirected to Experience Cloud.</li><li>All requests to Admin are routed through Experience Cloud.</li></ul>                                                                                                                                                                                                         |
| Adobe Identity Management Service (IMS) integration is disabled                                  | Experience Cloud integration is disabled automatically | <ul><li>Admin users that are logged in get application or `404 page not found` errors when they refresh, or when their session expires.</li><li>Navigate to the default Admin URL for the Commerce project to be redirected to [log in with Adobe Commerce account credentials](admin-signin.md#admin-sign-in).</li><li>Admin requests are routed through the Adobe Commerce application.</li></ul> |

{style="table-layout:auto"}

>[!NOTE]
>
>If the IMS integration is disabled and an administrator is missing the 2FA authorization code configured for their Commerce Admin user account, a System Administrator with access to the Commerce project can [reset the 2FA configuration](https://experienceleague.adobe.com/docs/commerce-operations/reference/commerce-on-premises.html?lang=en#security%3Atfa%3Areset) on the account.

## Manage the integration from the Admin

1. From the Commerce Admin, open the Store Configuration menu by selecting **[!UICONTROL Stores]** from the left navigation menu, and then select **[!UICONTROL Configuration]**.

1. From the Configuration menu, select **[!UICONTROL Advanced > Admin]**, and then expand the [!UICONTROL Unified Experience option]**.

   ![Admin Store Configuration for Experience Cloud integration](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Enable or disable the integration by selecting the **[!UICONTROL Enable]** value.

1. Change the project name that displays in the Commerce Projects workspace by adding or updating the **[!UICONTROL Project Name]** value.

1. Save the configuration.

1. Clear the cache.

## Manage the integration using the Adobe Commerce CLI

Commerce system administrators with Admin access to the Commerce cloud project can use Adobe Commerce CLI commands to manage the Experience Cloud integration.

1. From your local development environment, log in to the cloud project.

   ```bash
   magento-cloud login
   ```

1. From the root directory of your Cloud project environment, connect to the Commerce application server.

   ```bash
   ssh magento-cloud
   ```

1. Check the status of the Admin Unified Experience extension:

   ```bash
   bin/magento admin:uex:status
   ```

1. Change the status of the extension to disable the integration

   - **Enable**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **Disable**—`bin/magento config:set admin/unified_experience/enabled 0`

## Manage Admin users

When the Experience Cloud integration is enabled, all Commerce Admin users must have both an Admin account on the Commerce instance and an Adobe user account with access to Adobe products and services. Both accounts must be associated with the same email address.

- **Commerce Admin account**—[Manage Commerce Admin users](../systems/permissions-users-all.md) from the Admin for the Commerce instance. User accounts for administrators must have the Admin user role and be associated with an Adobe ID, for example `<username>@adobe.com`.

  System administrators on the Commerce project can use [SSH to connect to the remote environment](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment), and use the Commerce CLI `admin:user:create` and `admin:user:unlock` commands to add or unlock Admin user accounts.

- **Adobe user account**–An administrator for the Adobe organization associated with the Commerce instance must create a corresponding user account for each Commerce administrator from the Adobe Admin Console. The account must have the same Adobe ID as the Commerce Admin account. See [Configure Adobe Commerce users in the Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

  Administrators that manage the configuration for the Experience Cloud integration from the Adobe Developer Console must have an Adobe user account with System Administrator or Developer access.
