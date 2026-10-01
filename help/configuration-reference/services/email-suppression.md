---
title: "[!UICONTROL Adobe Services] &gt; [!UICONTROL Email Suppression]"
description: Review the configuration settings on the [!UICONTROL Adobe Services] &gt; [!UICONTROL Email Suppression] page of the Commerce Admin.
feature: Configuration, Communications
badgeSaas: label="SaaS only" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service and Adobe Commerce Optimizer projects only (Adobe-managed SaaS infrastructure)."
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
# [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]

{{config}}

[!UICONTROL Email Suppression] allows administrators to turn off specific categories of automated system email without affecting the rest of the store's email or requiring developer involvement. Use this feature to temporarily or permanently stop certain notifications, for example, order emails during a data migration, or marketing emails.

>[!IMPORTANT]
>
>Security-related admin notifications, such as two-factor authentication codes and admin password reset emails, are never suppressed by this feature.

Settings on this page apply per [store view](../../getting-started/websites-stores-views.md#scope-settings) so you can suppress different email categories for different storefronts.

>[!NOTE]
>
>Turning suppression off immediately restores normal email delivery, but emails sent during the suppression period are not queued.

## [!UICONTROL Email Suppression]

![Email Suppression](./assets/email-suppression.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Email Suppression]|Store View|Master on/off switch for the feature. When set to `No` (default), every other setting on this page is ignored and all email sends normally.|
|[!UICONTROL Disabled Functional Areas]|Store View|Select one or more business categories whose emails are suppressed. See [Business categories](#business-categories) for what each category includes.|
|[!UICONTROL Disabled Template IDs]|Store View|Optional comma-separated list of specific email templates to suppress individually, regardless of category. Use the template code (for example, `customer_password_forgot_email_template`) or the numeric template ID for a custom template you created in the Admin.|

{style="table-layout:auto"}

### Business categories {#business-categories}

|Category|Typical emails included|
|--- |--- |
|Customer Account|Account creation, password reset, account information changes.|
|Order Management|Order confirmation, invoice, shipment, credit memo, order cancellation.|
|Returns (RMA)|Return merchandise authorization notifications.|
|Checkout & Payment|Checkout and pay-by-link related emails.|
|Marketing|Newsletters, product alerts, wish list sharing, email a friend, reminders, invitations, gift registry.|
|Store Credit & Rewards|Gift cards, reward points, store credit balance changes.|
|B2B|Company, negotiable quote, and purchase order notifications.|
|System Notifications|Operational notifications such as scheduled import, export and contact form emails.|

{style="table-layout:auto"}
