---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Invitations]'
description: Review the configurations settings on the [!UICONTROL Customers] &gt; [!UICONTROL Invitations] page of the Commerce Admin.
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
---
# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![General](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Invitations Functionality]|Global|Determines whether the Invitations module is enabled. Options: `Yes` / `No`|
|[!UICONTROL Enable Invitations on Frontend]|Website|Determines if invitations can be managed from the storefront. Options: `Yes` / `No`|
|[!UICONTROL Referred Customer Group]|Store View|Determines the customer group of the invitee. Options: <br/>**`Same as Inviter`** - Invitees are automatically assigned to the same customer group as the customers who invited them. <br/>**`Default Customer Group from Configuration`** - Invitees automatically have the default [customer group](../../customers/customer-groups.md).|
|[!UICONTROL New Accounts Registration]|Store View|Determines how invitees can create an account. Options: <br/>**`By Invitation Only`** -  Invitees must follow the link in the Invitation email to create an account. <br/>**`Available to All`** - Invitees can use the account registration form that is available in the store.|
|[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]|Store View|Determines whether there is a field in the Invitation form in which the inviter can add a custom message that is sent to the invitee via email. This does not affect the administrator's ability to add a message to an Invitation. Options: `Yes` / `No`.|
|[!UICONTROL Max Invitations Allowed to be Sent at One Time]|Store View|Determines the maximum number of invitations that the inviter can send at once. A different invitation is sent out to each email address that the inviter includes in the form. This protects server resources by preventing large numbers of Invitations from being sent at once, and makes it less likely for invitations to be sent as spam.|

{:style="table-layout:auto"}

## [!UICONTROL Email]

![Email](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Customer Invitation Email Sender]|Store View|Determines the sender of the email that invitees receive when an invitation email is sent. Default value: `General Contact`|
|[!UICONTROL Customer Invitation Email Template]|Store View|Determines the template of the email that invitees receive when an invitation email is sent. Default template: `Customer Invitation`|

{:style="table-layout:auto"}
