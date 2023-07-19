---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Newsletter]'
description: Review the configurations settings on the [!UICONTROL Customers] &gt; [!UICONTROL Newsletter] page of the Commerce Admin.
exl-id: a97003ca-985e-47fa-9ff3-677e05ef3729
feature: Configuration, Customers, Communications
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

{:style="table-layout:auto"}

## [!UICONTROL Subscription Options]

![Subscription Options](./assets/newsletter-subscription-options.png)<!-- zoom -->

<!-- [Subscription Options](https://docs.magento.com/user-guide/marketing/newsletter-configuration.html) -->

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

{:style="table-layout:auto"}
