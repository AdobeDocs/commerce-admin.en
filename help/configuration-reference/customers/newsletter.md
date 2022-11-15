---
title: Customers >  Newsletter
description: Placeholder
---
# Customers >  Newsletter

{{config}}

>[!NOTE]
>
>The newsletter is a part of marketing instruments that allow sending to customers news, discounts, and other marketing emails. Registered customers can manage their subscription from their [account](https://docs.magento.com/user-guide/customers/account-dashboard-newsletter-subscriptions.html).

## General Options

![General Options](./assets/newsletter-general-options.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Enabled|Store View|Determines if newsletters are enabled for the store view scope. Options: `Yes` / `No`|

## Subscription Options

![Subscription Options](./assets/newsletter-subscription-options.png)<!-- zoom -->

<!-- Subscription Options](https://docs.magento.com/user-guide/marketing/newsletter-configuration.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|Allow Guest Subscription|Store View|Determines if unregistered guests can subscribe to a newsletter. Options: `Yes` / `No`|
|Need to Confirm|Store View|Determines if subscription requests must be confirmed. This double-opt-in method is a validation measure that prevents people from being subscribed without their consent. Options: `Yes` / `No`|
|Confirmation Email Sender|Store View|Identifies the store contact that appears as the sender of email sent to confirm a subscription request.|
|Confirmation Email Template|Store View|Determines the email template used for the notification sent to confirm a request to subscribe to a newsletter.  Default template: Newsletter subscription confirmation|
|Success Email Sender|Store View|Identifies the store contact that appears as the sender of email sent to those who successfully subscribe to a newsletter.|
|Success Email Template|Store View|Determines the email template used for the notification sent to those who successfully subscribe to a newsletter.  Default template: Newsletter subscription success|
|Unsubscription Email Sender|Store View|Identifies the store contact that appears as the sender of email sent to those who request to end their newsletter subscription.|
|Unsubscription Email Template|Store View|Determines the email template used for the notification sent to those who request to end their newsletter subscription.  Default template: Newsletter unsubscription success|
