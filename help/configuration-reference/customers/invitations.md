---
title: "[!UICONTROL Customers] &gt; [!UICONTROL Invitations]"
description: Review the configurations settings on the [!UICONTROL Customers] &gt; [!UICONTROL Invitations] page of the Commerce Admin.
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
TQID: https://experienceleague.adobe.com/UOJF8r7CsXWK6qG7FjkJoJTIqnH2fPQhnRyZrJ7u4nE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
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
# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![General](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Invitations Functionality]|Global|Determines whether the Invitations module is enabled. Options: `Yes` / `No`|
|[!UICONTROL Enable Invitations on Frontend]|Website|Determines if invitations can be managed from the storefront. Options: `Yes` / `No`|
|[!UICONTROL Referred Customer Group]|Store View|Determines the customer group of the invitee. Options: <br/>**`Same as Inviter`** - Invitees are automatically assigned to the same customer group as the customers who invited them. <br/>**`Default Customer Group from Configuration`** - Invitees automatically have the default [customer group](../../customers/customer-groups.md).|
|[!UICONTROL New Accounts Registration]|Store View|Determines how invitees can create an account. Options: <br/>**`By Invitation Only`** -  Invitees must follow the link in the Invitation email to create an account. <br/>**`Available to All`** - Invitees can use the account registration form that is available in the store.|
|[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]|Store View|Determines whether there is a field in the Invitation form in which the inviter can add a custom message that is sent to the invitee via email. This does not affect the administrator's ability to add a message to an Invitation. Options: `Yes` / `No`.|
|[!UICONTROL Max Invitations Allowed to be Sent at One Time]|Store View|Determines the maximum number of invitations that the inviter can send at once. A different invitation is sent out to each email address that the inviter includes in the form. This protects server resources by preventing large numbers of Invitations from being sent at once, and makes it less likely for invitations to be sent as spam.|

{style="table-layout:auto"}

## [!UICONTROL Email]

![Email](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Customer Invitation Email Sender]|Store View|Determines the sender of the email that invitees receive when an invitation email is sent. Default value: `General Contact`|
|[!UICONTROL Customer Invitation Email Template]|Store View|Determines the template of the email that invitees receive when an invitation email is sent. Default template: `Customer Invitation`|

{style="table-layout:auto"}
