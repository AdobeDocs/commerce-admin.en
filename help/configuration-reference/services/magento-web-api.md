---
title: "[!UICONTROL Services] &gt; [!UICONTROL Magento Web API]"
description: Review the configurations settings on the [!UICONTROL Services] &gt; [!UICONTROL Magento Web API] page of the Commerce Admin.
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
TQID: https://experienceleague.adobe.com/62cy3cPVxGeI-W1LElSg1TEBEb0cZN30vGZQ74UNhm8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
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
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![SOAP Settings](./assets/web-api-soap-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Default Response Charset]|Store View|Determines the default character set. If empty, UTF-8 is used.|

{style="table-layout:auto"}

## [!UICONTROL GraphQl Input Limits]

![GraphQl Input Limits](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Input Limits]|Store View|Determines if input limits are enabled for GraphQL calls. Default Value: `No`.|
|[!UICONTROL Maximum Page Size]|Store View|Sets the maximum number of items allowed in a paginated search result in the GraphQL response. This option is not available when _Enable Input Limits_ = `No`.|

{style="table-layout:auto"}

## [!UICONTROL Web Api Input Limits]

![Web Api Input Limits](./assets/web-api-input-limits.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Input Limits]|Store View|Determines if input limits are enabled for Web API calls. Default Value: `No`.|
|Input List Limit|Store View|Sets the maximum number of items allowed in an entity array property in the Web API request. This option is not available when _Enable Input Limits_ = `No`.|
|[!UICONTROL Maximum Page Size]|Store View|Sets the maximum number of items allowed in a paginated search result in the Web API response. This option is not available when _Enable Input Limits_ = `No`.|
|[!UICONTROL Default Page Size]|Store View|Sets the default number of items in a paginated search result in the Web API response.|

{style="table-layout:auto"}

## [!UICONTROL Web API Security]

![Web API Security](./assets/web-api-security.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Allow Anonymous Guest Access]|Global|Determines is guests can anonymously access CMS, catalog, and store resources from both SOAP and REST APIs. By default, anonymous guest access is not allowed. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL JWT Authentication]

![JWT Authentication](./assets/web-api-jwt-authentication.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Algorithm to sign/encrypt JWTs used for authentication]|Global|Specifies the type of JWS or JWE algorithm used for JWT (JSON Web Token) encryption|
|[!UICONTROL Content encryption algorithm for JWEs]|Global|Specifies the type of content encryption algorithm used for JWT encryption when JWE algorithm is selected. This option is ignored for JWS algorithms.|
|[!UICONTROL Customer JWT Expires In]|Global|Sets the length of time (in minutes) before a customer JWT bearer token expires. The customer JWT bearer token expires in 30 minutes if this field is empty or has a negative value. Default value: `60`|
|[!UICONTROL Admin User JWT Expires In]|Global|Sets the length of time (in minutes) before the Admin JWT bearer token expires. The admin JWT bearer token expires in 30 minutes if this field is empty or has a negative value. Default value: `60`|

{style="table-layout:auto"}
