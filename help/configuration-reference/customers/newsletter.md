---
title: "[!UICONTROL Customers] &gt; [!UICONTROL Newsletter]"
description: Review the configurations settings on the [!UICONTROL Customers] &gt; [!UICONTROL Newsletter] page of the Commerce Admin.
exl-id: a97003ca-985e-47fa-9ff3-677e05ef3729
feature: Configuration, Customers, Communications
TQID: https://experienceleague.adobe.com/rqG5WOxVnMnlKTSiSHYgl-3Q5Yy4nIKWOjAev35UYHA
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
# [!UICONTROL Customers] > [!UICONTROL Newsletter]

{{config}}

>[!NOTE]
>
>The newsletter is a part of marketing instruments that allow sending to customers news, discounts, and other marketing emails. Registered customers can manage their subscription from their [account dashboard](../../customers/account-dashboard-my-account.md).

## [!UICONTROL General Options]

![General Options](./assets/newsletter-general-options.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled]|Store View|Determines if newsletters are enabled for the store view scope. Options: `Yes` / `No`|

{style="table-layout:auto"}

## [!UICONTROL Subscription Options]

![Subscription Options](./assets/newsletter-subscription-options.png)<!-- zoom -->

<!-- [Subscription Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/newsletters/newsletters) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Allow Guest Subscription]|Store View|Determines if unregistered guests can subscribe to a newsletter. Options: `Yes` / `No`|
|[!UICONTROL Need to Confirm]|Store View|Determines if subscription requests must be confirmed. This double-opt-in method is a validation measure that prevents people from being subscribed without their consent. Options: `Yes` / `No`|
|[!UICONTROL Confirmation Email Sender]|Store View|Identifies the store contact that appears as the sender of email sent to confirm a subscription request.|
|[!UICONTROL Confirmation Email Template]|Store View|Determines the email template used for the notification sent to confirm a request to subscribe to a newsletter. Default template: `Newsletter subscription confirmation`|
|Success Email Sender|Store View|Identifies the store contact that appears as the sender of email sent to those who successfully subscribe to a newsletter.|
|[!UICONTROL Success Email Template]|Store View|Determines the email template used for the notification sent to those who successfully subscribe to a newsletter. Default template: `Newsletter subscription success`|
|[!UICONTROL Unsubscription Email Sender]|Store View|Identifies the store contact that appears as the sender of email sent to those who request to end their newsletter subscription.|
|[!UICONTROL Unsubscription Email Template]|Store View|Determines the email template used for the notification sent to those who request to end their newsletter subscription. Default template: `Newsletter unsubscription success`|

{style="table-layout:auto"}
