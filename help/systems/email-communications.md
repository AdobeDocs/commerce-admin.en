---
title: Configure email communications
description: Placeholder
---
# Configure email communications

The _Mail Sending Settings_ give you the ability to route returned email or replies to email to a specific address. Also, if your store is running on a Windows server, you can verify the host and port settings.

>[!IMPORTANT]
>
>**Security Notice!** All merchants should immediately set their mail sending configuration to protect against a recently identified potential remote code execution exploit. Until this issue is resolved, we highly recommend that you avoid using Sendmail for email communications. In the Mail Sending Settings, make sure that Set Return Path is set to `No`.

![Advanced configuration - mail sending settings](../configuration-reference/advanced/assets/system-mail-sending-settings.png)<!-- zoom -->

[_Mail Sending Settings_](https://docs.magento.com/user-guide/configuration/advanced/system.html)

## Configure email communications

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Advanced** and choose **System**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Mail Sending Settings** section and do the following:

   - If necessary, set **Disable Email Communications** to `No`.

   - If running on a Windows server, verify the following settings:

      Host - localhost

      Port (25) - 25

   - Set **Set Return Path**:

      -  `No` - (Recommended security measure) Routes returned email to the default store email address.
      - `Yes` - Routes returned email to the default store email address.
      - `Specified` - Routes returned email to the email address specified in the **Return Path Email** field.

1. In the left panel, expand **Sales** and choose **Sales Emails**. Then, do the following:

   - Expand ![Expansion selector](../assets/icon-display-expand.png) the **General Settings** section.

   - Set **Asynchronous sending** to `Enable`.

   ![Sales configuration - email general settings](../configuration-reference/sales/assets/sales-emails-general-settings.png)<!-- zoom -->

   [_General Settings_](https://docs.magento.com/user-guide/configuration/sales/sales-emails.html)

1. When complete, click **Save Config**.
