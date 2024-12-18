---
title: Session management
description: Learn how to configure session management to secure the Admin and storefront.
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
---
# Session management

[Session management](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) is an anti-denial of service (DoS) best practice for API security. A session represents the amount of time a visitor spends on your site and is not related to how long Admin users or customers are logged in to their accounts.

A session is a sequence of network HTTP request and response transactions associated with the same user. It is a way to associate a client (Admin) with their data when they access the server. Sessions are used to establish variables, such as access rights and localization settings, which apply to every interaction a user has with a web application during the session.

## Session size

Use the following configuration settings to limit the maximum session size for Admin users and storefront visitors:

- **[!UICONTROL Max Session Size in Admin]**—Limit the maximum sessions size in bytes. Use `0` to disable.
- **[!UICONTROL Max Session Size in Storefront]**—Limit the maximum sessions size in bytes. Use `0` to disable.

>[!TIP]
>
>Both settings are measured in bytes and default to `256000` bytes (or 256 KB).

**_To configure maximum session size:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]**  > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL System]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Security]** section to access the session settings.

   ![Session settings](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. Enter new session sizes in bytes.

   >[!WARNING]
   >
   >Setting the value too low can cause issues. If you set either of the options below the default of 256000 bytes, you see a warning message. If you click **[!UICONTROL No]**, the system changes the value to `256000`.

1. Click **[!UICONTROL Save Config]**.

### Admin sessions

If you exceed the maximum session size, an error message is displayed and the system logs the session size constraint to the `var/log` directory.

If you lose access to the Admin after setting the session size too low, use the CLI to reset the configuration:

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### Storefront sessions

If you exceed the maximum session size, no error displays but the system logs the session size constraint to the `var/log` directory.

## Session validation

Adobe Commerce and Magento Open Source allow you to validate session variables as a protective measure against possible session fixation attacks or attempts to poison or hijack user sessions. The Session Validation Settings determine how session variables are validated during each store visit and if the session ID is included in the URL of the store.

For technical information, see [Use Redis for session storage](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) in the _Configuration Guide_.

![General configuration - Web session validation](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

The validation checks that visitors are who they say they are by comparing the value in the validation variables against the session data that is stored in `$_SESSION` data for the user. Validation fails if the information is not transmitted as expected, and the corresponding variable is empty. Depending on the session validation settings, if a session variable fails the validation process, the client session immediately terminates.

Enabling all validation variables can help prevent attacks, but might also impact the performance of the server. By default, all session variable validation is disabled. We recommend that you experiment with the settings to find the best combination for your Adobe Commerce or Magento Open Source installation. Activating all validation variables might prove to be unduly restrictive, and could prevent access to customers who have Internet connections that pass through a proxy server or originate from behind a firewall. To learn more about session variables and their use, see the system administration documentation for your Linux&reg; system.

**_To configure the session validation:_**

1. On the _Admin_ sidebar, go to  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand _[!UICONTROL General]_ and choose **[!UICONTROL Web]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Session Validation Settings]** section.

1. Set each of the configuration options:

   - **[!UICONTROL Validate REMOTE_ADDR]** — Set to `Yes` to verify that the IP address of a request matches what is stored in the `$_SESSION` variable.

   - **[!UICONTROL Validate HTTP_VIA]** — Set to `Yes` to verify that the proxy address of an incoming request matches what is stored in the `$_SESSION` variable.

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — Set to `Yes` to verify that the forwarded-for address of a request matches what is stored in the `$_SESSION` variable.

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — Set to `Yes` to verify that the browser or device that is used to access the store during a session matches what is stored in the `$_SESSION` variable.

1. When complete, click **[!UICONTROL Save Config]**.

## Admin session lifetime

As a security measure, the _Admin_ is initially set to time out after 900 seconds (15 minutes) of keyboard inactivity. You can adjust the lifetime of the session to fit your work style.

**_To adjust Admin session lifetime:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. Scroll down and expand **[!UICONTROL Advanced]** in the left side panel.

1. Click **[!UICONTROL Admin]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Security]** section.

1. For **[!UICONTROL Admin Session Lifetime (seconds)]**, enter the number of seconds that a session remains active before it times out.

   ![Advanced configuration - Admin security settings](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. When complete, click **[!UICONTROL Save Config]**.
