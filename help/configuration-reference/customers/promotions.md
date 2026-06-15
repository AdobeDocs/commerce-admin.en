---
title: "[!UICONTROL Customers] &gt; [!UICONTROL Promotions]"
description: Review the configurations settings on the [!UICONTROL Customers] &gt; [!UICONTROL Promotions] page of the Commerce Admin.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
TQID: https://experienceleague.adobe.com/Sc1-Wacd9emNUOl9GabUK-J3OLH-eNX2hvk6m8oyjYc
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
# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![Automated Email Reminder Rules](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules#configure-email-reminders) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Reminder Emails]|Global|Enables automated email reminders. If this is set to No, the remaining settings are ignored. Options: `Yes` / `No`|
|[!UICONTROL Frequency]|Global|Indicates the frequency with which Commerce should check for new customers who qualify for the automated email reminders. Options: <br/>**`Minute Intervals`** - Sends the email according to the selected interval. (5 minutes, 10 minutes, 15 minutes, 20 minutes, or 30 minutes) <br/>**`Hourly`** - Sends email hourly, at the minute after the hour specified. Enter a value between 0-59. <br/>**`Daily`** - Sends email daily, from the Start Time.|
|[!UICONTROL Interval]|Global|The interval should be equal or of greater than your cron.php launch period. Options: `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes`|
|[!UICONTROL Start Time]|Global|Sets the day, minute, and second the email is sent. Specified in 24-hour format, based on the system time on your server.|
|[!UICONTROL Maximum Emails per One Run]|Global|Limits the number of emails sent in a scheduled block.|
|[!UICONTROL Email Send Failure Threshold]|Global|The number of times the reminder attempts to send out notifications to specific email address and fails. When the value is set to 0, there is no threshold, and notifications continue to be sent despite any failures.|
|[!UICONTROL Reminder Email Sender]|Store View|The store identity that appears as the sender of the email.|

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![Auto Generated Specific Coupon Codes](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart-coupon#configure-coupon-codes)  -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Code Length]|Global|Defines the length of the coupon code, excluding the prefix, suffix, and separators.|
|[!UICONTROL Code Format]|Global|Defines the coupon code format. Options include: <br/>**`Alphanumeric`** - Any combination of letters and numbers. <br/>**`Alphabetical`** - Letters only. <br/>**`Numeric`** - Numbers only.|
|[!UICONTROL Code Prefix]|Global|A value that is appended to the beginning of all  coupon codes. If you do not want to use a prefix, leave the field blank.|
|[!UICONTROL Code Suffix]|Global|A value that is appended to the end of all codes. If you do not want to use a suffix, leave the field blank.|
|[!UICONTROL Dash Every X Characters]|Global|The interval for inserting a dash (-) into all coupon codes. If you do not want to use a dash, leave the field blank. <br/>_**Note:**_ Coupon  codes that differ by only a dash are considered to be different codes.|

{style="table-layout:auto"}
