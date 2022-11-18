---
title: Configure email communications
description: Learn how to configure email communications, including the routing of returned email or replies to a specific email address.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
---
# Configure email communications

The _Mail Sending Settings_ give you the ability to route returned email or replies to email to a specific address. Also, if your store is running on a Windows server, you can verify the host and port settings.

>[!IMPORTANT]
>
>**Security Notice** All merchants should immediately set their mail sending configuration to protect against a recently identified potential remote code execution exploit. Until this issue is resolved, we highly recommend that you avoid using Sendmail for email communications. In the Mail Sending Settings, make sure that Set Return Path is set to `No`.

![Advanced configuration - mail sending settings](../configuration-reference/advanced/assets/system-mail-sending-settings.png)<!-- zoom -->

For a detailed list of the configuration settings, see [_Mail Sending Settings_](https://docs.magento.com/user-guide/configuration/advanced/system.html) in the _Configuration Reference_.

## Configure email communications

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL System]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Mail Sending Settings]** section and do the following:

   - If necessary, set **[!UICONTROL Disable Email Communications]** to `No`.

   - If running on a Windows server, verify the following settings:

      [!UICONTROL Host] - `localhost`

      [!UICONTROL Port (25)] - `25`

   - For **[!UICONTROL Set Return Path]**, choose one of the following options:

      - `No` - (Recommended security measure) Routes returned email to the default store email address.
      - `Yes` - Routes returned email to the default store email address.
      - `Specified` - Routes returned email to the email address specified in **[!UICONTROL Return Path Email]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Sales Emails]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL General Settings]** section.

1. Set **[!UICONTROL Asynchronous sending]** to `Enable`.

   ![Sales configuration - email general settings](../configuration-reference/sales/assets/sales-emails-general-settings.png)<!-- zoom -->

   For a detailed list of the configuration settings, see [_General Settings_](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html) in the _Configuration Reference_.

1. When complete, click **[!UICONTROL Save Config]**.
