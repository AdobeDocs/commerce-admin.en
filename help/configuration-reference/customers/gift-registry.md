---
title: "[!UICONTROL Customers] &gt; [!UICONTROL Gift Registry]"
description: Review the configurations settings on the [!UICONTROL Customers] &gt; [!UICONTROL Gift Registry] page of the Commerce Admin.
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
TQID: https://experienceleague.adobe.com/STCCRRp71FXvz-09LFiYKhJnsbdF8wokfdIa2Ij6-9A
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

For detailed information about using these settings to enable gift registries for your store customers, see [Configure gift registries](../../merchandising-promotions/gift-registry-configure.md). For information about including gift registry search on the storefront, see [Add gift registry search](../../merchandising-promotions/gift-registry-search.md).

## [!UICONTROL General Options]

![General Options](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Gift Registry]|Store View|Determines if gift registries are available. Options: <br/>**`Yes`** - Enables gift registries for the selected store view. The Gift Registry tab appears in the account dashboard of registered customers. <br/>**`No`** - Gift registries are not available for the store view.|
|[!UICONTROL Maximum Registrants]|Store View|Sets the number of people that a customer can add to a gift registry. The customer shares the gift registry with each registrant. In the storefront, the _Add Registrant_ button is available to customers until the maximum number is reached.|

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![Owner Notification](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Email Template]|Store View|Determines the template used for the Owner Notification email that is sent when a gift registry is created. Default template: Gift Registry Owner Notification|
|[!UICONTROL Email Sender]|Store View|Identifies the [store contact](../../getting-started/store-details.md#store-email-addresses) that appears as the sender of the Gift Registry Owner Notification email. Default value: `General Contact`|

{style="table-layout:auto"}

## Gift Registry Sharing

![Gift Registry Sharing](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Email Template]|Store View|Determines the template used for the Gift Registry Sharing email that is sent when a gift registry is created. When the owner clicks _Share Gift Registry_, the email is sent to each recipient. Default template: `Gift Registry Sharing`|
|[!UICONTROL Email Sender]|Store View|Identifies the [store contact](../../getting-started/store-details.md#store-email-addresses) that appears as the sender of the Gift Registry Sharing email. Default value: `General Contact`|
|[!UICONTROL Maximum Sent Emails Threshold]|Store View|The maximum number of Gift Registry Sharing email notification messages that can be sent at one time.|

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![Gift Registry Update](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Email Template]|Store View|Determines the template used for the Gift Registry Update email that is sent to the gift registry owner when a purchase is made from the gift registry. The update includes information about the item and quantity purchased, but does not include the name of the person who placed the order. Default template: `Gift Registry Update`|
|[!UICONTROL Email Sender]|Store View|Identifies the [store contact](../../getting-started/store-details.md#store-email-addresses) that appears as the sender of the Gift Registry Update email. Default value: `General Contact`|

{style="table-layout:auto"}
