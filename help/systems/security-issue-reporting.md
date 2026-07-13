---
title: Security issue reporting
description: Learn how to configure the contact information and security-related links that can be used by security researchers to report security concerns about your site.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/tXZFSpgx9r2t-tN2Oc7L2aiPDlL6hSZBRC9pHjzcjQk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Security issue reporting

The `security.txt` file contains contact information and security-related links that can be used by security researchers to report security concerns about your site. If your security information changes over time, ensure that the information in the `security.txt` file is up to date.

**_To configure security.txt:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel under _[!UICONTROL Security]_, click **[!UICONTROL Security.txt]**.

1. In the _[!UICONTROL General]_ section, set **[!UICONTROL Enable]** to `Yes`.

   ![General security configuration](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. Under _[!UICONTROL Contact Information]_, enter the following:

   - The email address and phone number of the person who manages security issues for your store.

   - The URL of your store's **[!UICONTROL Contact Page]**. This page could either be a list of store security contacts or your _Contact Us_ page.

   ![Contact Information configuration](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. Under _[!UICONTROL Other Information]_, enter the following:

   - The URL of your public **[!UICONTROL Encryption]** key. For example: `https://example.com/pgp-key.txt`

   - The URL of an **[!UICONTROL Acknowledgments]** page where security researchers are recognized for their efforts on behalf of your store.

   - Your **[!UICONTROL Preferred Languages]** for security-related communications. Enter the standard two-character [language code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for each supported language, separated by a comma. For example, to specify English, Spanish, and French, enter `en, es, fr`. All specified languages have the same priority, regardless of their order of appearance.

   - The URL of a **[!UICONTROL Hiring]** page that lists security-related employment opportunities with your store.

   - The URL of your security **[!UICONTROL Policy]** page.

   - The URL of a digital **[!UICONTROL Signature]** file that is saved on your server. For example: `https://mystore.com/.well-known/security.txt.sig`

   The digital signature must be set up from the CLI (command-line interface) of the server. To learn more, see [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) on GitHub.

   ![Other Information](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. When complete, click **[!UICONTROL Save Config]**.
