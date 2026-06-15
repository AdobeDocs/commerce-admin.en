---
title: "[!UICONTROL Sales] &gt; [!UICONTROL Quotes]"
description: Review the configurations settings on the [!UICONTROL Sales] &gt; [!UICONTROL Quotes] page of the Commerce Admin.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
TQID: https://experienceleague.adobe.com/puZjB2YCCyZXT0U6AdDBd-YjxopU637-yxgOaB6hkvM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
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
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>With the installation and enablement of Adobe Commerce B2B, the buying experience can be personalized with company-specific features. Adobe Commerce B2B is an integrated solution that supports both B2B and B2C models. For more information about the B2B features, see the [Adobe Commerce B2B User Guide](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/quotes/quotes) -->

## [!UICONTROL General]

![General](./assets/quotes-general.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Minimum Amount]|Website|The minimum amount of the shopping cart subtotal, after any discounts, that is required before a customer can submit a request for a quote. Default value: `0`|
|[!UICONTROL Minimum Amount Message]|Store View|The message that appears in the shopping cart when a customer tries to submit a request for a quote, but the minimum amount required is not met.|
|[!UICONTROL Default Expiration Period]|Website|Determines the default lifespan of a [quote](../../b2b/quote-price-negotiation.md) as time period from the date the request for a quote is submitted. Options: `Days` / `Weeks` / `Months`|

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![Attached Files](./assets/quotes-attached-files.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL File formats for upload]|Global|Determines the file formats that can be attached to a quote. Default values supported: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`, and `jpeg`|
|[!UICONTROL Maximum file size]|Global|Determines the maximum size for a file that is attached to a quote. This setting can be overridden by the server configuration.|

{style="table-layout:auto"}
