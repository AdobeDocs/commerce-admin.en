---
title: Configure Quotes
description: Learn about quote configuration, which controls the minimum required order amount for quote requests, the quote lifetime, and file attachments. 
---
# Configure Quotes

If quotes are enabled in the general [B2B features](enable-basic-features.md), you can configure support for quotes in the Admin. The quote configuration determines the minimum required order amount for quote requests, the quote lifetime, and the supported file formats for attached files. 

>[!NOTE]
>
>Quote configuration options and the ability to use quote negotiation functions are controlled using the [role resources](https://docs.magento.com/user-guide/system/permissions-role-resources.html). These role resources must be selected for the Admin [user role](https://docs.magento.com/user-guide/system/permissions-user-roles.html) that is assigned to the Admin user account. To grant access to quote functions in the Admin, go to **System** > _Permissions_ > **User Roles**, select the role, and navigate to Sales > Operations > Quotes in the _Role Resources_ tree.

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Sales** and choose **Quotes**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **General** section and do the following:

   ![Sales quotes configuration - general](./assets/quotes-general.png)<!-- zoom -->

   See [Quotes](https://docs.magento.com/user-guide/configuration/sales/quotes.html) in the _Configuration Reference_ for a full list of Quotes feature options and their functions.

   - Enter the **Minimum Amount** in the shopping cart that must be met before a request for a quote can be submitted.

   - For **Minimum Amount Message**, enter the message that you want to appear when the shopping cart total does not meet the minimum required amount.

   - For **Default Expiration Period**, enter the number of **days**, **weeks**, or **months** that a quote is to remain valid.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Attached files** section and do the following:

   - For **File formats for upload**, enter the suffix of each file type that you support for files that are attached to a quote.

      Enter each file suffix in lowercase, and separated by a comma.

      By default, the following formats are supported: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`, and `jpeg`

   - For **Maximum file size**, enter the maximum size of an attached file in megabytes.

      The value you enter might be overridden by the server setting.

      ![Sales quotes configuration - attached files](./assets/quotes-attached-files.png)<!-- zoom -->

1. When complete, click **Save Config**.
