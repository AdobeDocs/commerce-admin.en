---
title: Configure log rotation
description: Configure log rotation for the AEM Assets Integration for Commerce.
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
---
# Configure Experience Manager Assets

The AEM Assets Integration for Commerce provides the following log files in your Commerce instance:

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Ask your System Administrator to check the log file rotation schedule for these logs to prevent them from growing too large. In some environments, the log files are rotated automatically, but in other environments you must set up log rotation manually. For details, see the following topics:

- For Adobe Commerce on-premises installations, ask your System Administrator to set up [log rotation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings).
- For Adobe Commerce on cloud infrastructure projects, see [View and manage logs](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html).
