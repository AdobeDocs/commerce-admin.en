---
title: Action log archive
description: Learn how to configure and view the Admin action log archive.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/xgyeoO5XJFZPopM9bsIn2oOtrxl4fyuEY2du5ryXeTY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Action log archive

{{ee-feature}}

The Admin [actions](action-log.md) archive lists the CSV log files that are stored on the server. In the configuration, you can specify how long the log entries are stored, and how often they are archived. By default, the file name includes the current date in ISO format:  `yyyyMMddHH`

>[!NOTE]
>
>Log archiving requires a [cron job](cron.md) to be set up.

## Configure the log archive

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL System]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Admin Actions Log Archiving]** section and set these options:

   - **[!UICONTROL Log Entry Lifetime, Days]** — Enter the number of days that you want to keep the log entries in the database before they are removed.
   - **[!UICONTROL Log Archiving Frequency]** — Set to `Daily`, `Weekly`, or `Monthly`.

   ![Advanced configuration - admin actions log archiving](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   For a detailed list of the configuration settings, see [Admin Actions Log Archiving](../configuration-reference/advanced/system.md) in the _Configuration Reference_.

1. When complete, click **[!UICONTROL Save Config]**.

## View the archive

On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_ > **[!UICONTROL Archive]**.

![Action log archive](./assets/action-log-archive.png){width="600" zoomable="yes"}
