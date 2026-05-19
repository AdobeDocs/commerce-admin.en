---
title: System backups
description: Learn how to create and schedule system backups, including the file system, database, and media files.
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/kx2acbOSrWMJGv3ST6qKAXjLPgL2Lsh16wWvOxNO7FE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
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
# System backups

Adobe Commerce and Magento Open Source give you the ability to back up different parts of the system—such as the file system, database, and media files—and to roll back automatically. A record for each backup appears in the grid on the _Backups_ page. Deleting a record from the list deletes the archived file as well. Database backup files are compressed using the GZ format. For the system backups and the database and media backups, the TGZ format is used. As a best practice, you should restrict access to backup tools, and back up before installing extensions and updates.

- **Restrict access to backup tools.** Access to the backups and roll back management tool can be restricted by configuring [user roles](permissions-user-roles.md) for backup and roll back resources. To restrict access, leave the corresponding checkbox unselected. To give access to roll back resources, you must grant access to backup resources as well.

- **Back up before installing extensions and updates.** Always perform a backup before you install an extension or update.

{{$include /help/_includes/backups-note.md}}

## Enable and schedule backups

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL System]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Backup Settings]**.

1. Set **[!UICONTROL Enabled Schedule Backup]** to `Yes`.

1. To schedule automatic beckups, set the scheduling options:

   - Set **[!UICONTROL Enabled Schedule Backup]** to `Yes`.
   - Set **[!UICONTROL Scheduled Backup Type]** to the type of backup to run at the scheduled interval.
   - Set **[!UICONTROL Start Time]** to the time of day to run the backup operation.
   - Set **[!UICONTROL Frequency]** to `Daily`, `Weekly`, or `Monthly`.
   - Set **[!UICONTROL Maintenance Mode]** to `Yes`.

   ![Advanced configuration - backups](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. When complete, click **[!UICONTROL Save Config]**.

## Create a backup

1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Tools]_ > **[!UICONTROL Backups]**.

1. In the upper-right corner, click the type of backup you want to create:

   - **[!UICONTROL System Backup]** - Creates a complete backup of the database and the file system. During the process, you can choose to include the media folder in the backup.

   - **[!UICONTROL Database and Media Backup]** - Creates a backup of the database and the media folder.

   - **[!UICONTROL Database Backup]** - Creates a backup of the database.

   ![System tools - backups](./assets/tools-backups.png){width="600" zoomable="yes"}

1. To put the store into maintenance mode during the backup, select the checkbox.

   When the backup is complete, maintenance mode is turned off automatically.

1. For a system backup, select the **[!UICONTROL Include Media folder to System Backup]** checkbox to include the media folder.

1. When prompted, confirm the action.



<!-- Last updated from includes: 2023-02-22 09:59:54 -->
