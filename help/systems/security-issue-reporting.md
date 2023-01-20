---
title: Security issue reporting
description: Learn how to configure the contact information and security-related links that can be used by security researchers to report security concerns about your site.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
---
# Security issue reporting

The `security.txt` file contains contact information and security-related links that can be used by security researchers to report security concerns about your site. If your security information changes over time, ensure that the information in the `security.txt` file is up to date.

**_To configure security.txt:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel under _[!UICONTROL Security]_, click **[!UICONTROL Security.txt]**.

1. In the _[!UICONTROL General]_ section, set **[!UICONTROL Enable]** to `Yes`.

   ![General security configuration](../configuration-reference/security/assets/txt-general.png)<!-- zoom -->

1. Under _[!UICONTROL Contact Information]_, enter the following:

   - The email address and phone number of the person who manages security issues for your store.

   - The URL of your store's **[!UICONTROL Contact Page]**. This page could either be a list of store security contacts or your _Contact Us_ page.

   ![Contact Information configuration](../configuration-reference/security/assets/txt-contact-info.png)<!-- zoom -->

1. Under _[!UICONTROL Other Information]_, enter the following:

   - The URL of your public **[!UICONTROL Encryption]** key. For example: `https://example.com/pgp-key.txt`

   - The URL of an **[!UICONTROL Acknowledgments]** page where security researchers are recognized for their efforts on behalf of your store.

   - Your **[!UICONTROL Preferred Languages]** for security-related communications. Enter the standard two-character [language code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for each supported language, separated by a comma. For example, to specify English, Spanish, and French, enter `en, es, fr`. All specified languages have the same priority, regardless of their order of appearance.

   - The URL of a **[!UICONTROL Hiring]** page that lists security-related employment opportunities with your store.

   - The URL of your security **[!UICONTROL Policy]** page.

   - The URL of a digital **[!UICONTROL Signature]** file that is saved on your server. For example:`https://mystore.com/.well-known/security.txt.sig`

   The digital signature must be set up from the CLI (command-line interface) of the server. To learn more, see [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) on GitHub.

   ![Other Information](../configuration-reference/security/assets/txt-other-info.png)<!-- zoom -->

1. When complete, click **[!UICONTROL Save Config]**.
