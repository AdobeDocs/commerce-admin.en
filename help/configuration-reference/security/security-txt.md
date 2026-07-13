---
title: "[!UICONTROL Security] &gt; [!UICONTROL Security.txt]"
description: Review the configurations settings on the [!UICONTROL Security] &gt; [!UICONTROL Security.txt] page of the Commerce Admin.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
TQID: https://experienceleague.adobe.com/fXStEab1k6GKC5Tj7CStSGou3uNB-wJk5rZ-7EiFkcg
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
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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
# [!UICONTROL Security] > [!UICONTROL Security.txt]

For more information about changing these configuration settings, see [Security issue reporting](../../systems/security-issue-reporting.md).

{{config}}

## [!UICONTROL General]

![General](./assets/txt-general.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable]|Website|When enabled, a `security.txt` file is saved that contains information that is needed by security researchers to report potential vulnerabilities to you. Options:<br />**`Yes`** - Creates the `security.txt` file based on information entered in the _Contact information_ and _Other information_ sections.<br />**`No`** - (default) Does not create the `security.txt` file.|

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![Contact information](./assets/txt-contact-info.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Email]|Website|The email address where security reports can be sent.|
|[!UICONTROL Phone]|Website|A phone number that can be used to report security concerns.|
|[!UICONTROL Contact Page]|Website|The URL of a page on your site that lists security contacts, or your _Contact Us_ page. Examples: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/`|

{style="table-layout:auto"}

## [!UICONTROL Other information]

![Other information](./assets/txt-other-info.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Encryption]|Website|A URL that points to the location of an encryption key that security researchers can use to send encrypted communications. _**Do not enter the encryption key in this field.**_ <br/><br/>It is the responsibility of the researcher to verify that the key is from a trustworthy source. Researchers must not assume that the key is the same as that used to generate the digital signature. Example:<br />OpenPGP key from web server - `https://mystore.com/pgp-key.txt`|
|[!UICONTROL Acknowledgments]|Website|A URL that points to a page in your store where security researchers are acknowledged, such as`https://mystore.com/hall-of-fame.html`. To prevent future attacks, include only a general description without revealing specific information about vulnerability issues. Example:<br />We would like to thank the following researchers:<br />(yyyy/mm/dd) Justin Thyme - SQL injection|
|[!UICONTROL Preferred Languages]|Website|Specifies at least one preferred security reporting language. Separate multiple two-character [language codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) with a comma. All specified languages have the same priority. For example, to specify English, Spanish, and French, enter `en, es, fr`.|
|[!UICONTROL Hiring]|Website|The URL of a page on the site that lists security-related job positions. Example: `https://mystore.com/jobs.html`|
|[!UICONTROL Policy]|Website|The URL of the page that describes your security policy and vulnerability reporting practices. Example: `https://mystore.com/security-reporting.html` Default: `https://mystore.com/security`|
|[!UICONTROL Signature]|Website| A link to your digital signature file. The digital signature must be generated from the command line, and is saved in the `.well-known` folder on the server. For more information, see [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) on GitHub. Example: `https://mystore.com/.well-known/security.txt.sig`|

{style="table-layout:auto"}
