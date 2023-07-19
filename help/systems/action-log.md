---
title: Action logs
description: Learn about action logs and how to configure logged actions to help you to track all the changes made to your store.
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
---
# Action logs

{{ee-feature}}

The Action Logs feature records (logs) every change made by an Admin user who works in your store. This allows you to track all the changes made to your store. Tracking these changes, along with setting [Admin permissions](permissions.md) for a user, can help to secure your store from unwanted changes.

For most Admin actions, the logged information includes the action, the name of the user, success or failure of the action, and the ID of the object affected by the action. The IP address and date are also logged.

By default, all admin actions are enabled and logged. To configure Admin actions Logging, review the options and select or clear the checkbox for each action type. Adobe Commerce logs only checked types.

View the [Action Logs Report](action-log-report.md) to review logged admin actions and details.

![Advanced configuration - admin actions logging](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

For a detailed list of the configuration settings, see [Admin Actions Log Archiving](../configuration-reference/advanced/system.md) in the _Configuration Reference_.

## Configure Admin actions for logging

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL Admin]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Admin Actions Logging]** section and do the following for each action:

   - To enable Admin logging for the action, select the checkbox.
   - To disable Admin logging for the action, clear the checkbox.

1. When complete, click **[!UICONTROL Save Config]**.

## Archive Admin actions log

Admin action logs can be archived for any number of days. Archives can also be deleted after a specified duration.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL System]**.

1. Expand **[!UICONTROL Admin Action Log Archiving]** and set the options:

   - **[!UICONTROL Logs Entry Lifetime, Days]** - Set the number of days to retain archived log.
   - **[!UICONTROL Log Archiving Frequency]** - Set the Frequency for creating archives.

1. When complete, click **[!UICONTROL Save Config]**.
