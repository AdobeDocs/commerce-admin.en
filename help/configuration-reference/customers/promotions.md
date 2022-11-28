---
title: "[!UICONTROL Customers] > [!UICONTROL Promotions]"
description: Review the configurations settings on the [!UICONTROL Customers] > [!UICONTROL Promotions] page of the Commerce Admin.
---
# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![Automated Email Reminder Rules](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://docs.magento.com/user-guide/marketing/email-reminder-rules-configure.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Reminder Emails]|Global|Enables automated email reminders. If this is set to No, the remaining settings are ignored. Options: `Yes` / `No`|
|[!UICONTROL Frequency]|Global|Indicates the frequency with which Commerce should check for new customers who qualify for the automated email reminders. Options: <br/>**`Minute Intervals`** - Sends the email according to the selected interval. (5 minutes, 10 minutes, 15 minutes, 20 minutes, or 30 minutes) <br/>**`Hourly`** - Sends email hourly, at the minute after the hour specified. Enter a value between 0-59. <br/>**`Daily`** - Sends email daily, from the Start Time.|
|[!UICONTROL Interval]|Global|The interval should be equal or of greater than your cron.php launch period. Options: `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes`|
|[!UICONTROL Start Time]|Global|Sets the day, minute, and second the email is sent. Specified in 24-hour format, based on the system time on your server.|
|[!UICONTROL Maximum Emails per One Run]|Global|Limits the number of emails sent in a scheduled block.|
|[!UICONTROL Email Send Failure Threshold]|Global|The number of times the reminder attempts to send out notifications to specific email address and fails. When the value is set to 0, there is no threshold, and notifications continue to be sent despite any failures.|
|[!UICONTROL Reminder Email Sender]|Store View|The store identity that appears as the sender of the email.|

{:style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![Auto Generated Specific Coupon Codes](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://docs.magento.com/user-guide/marketing/price-rules-cart-coupon-code-configure.md  -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Code Length]|Global|Defines the length of the coupon code, excluding the prefix, suffix, and separators.|
|[!UICONTROL Code Format]|Global|Defines the coupon code format. Options include: <br/>**`Alphanumeric`** - Any combination of letters and numbers. <br/>**`Alphabetical`** - Letters only. <br/>**`Numeric`** - Numbers only.|
|[!UICONTROL Code Prefix]|Global|A value that is appended to the beginning of all  coupon codes. If you do not want to use a prefix, leave the field blank.|
|[!UICONTROL Code Suffix]|Global|A value that is appended to the end of all codes. If you do not want to use a suffix, leave the field blank.|
|[!UICONTROL Dash Every X Characters]|Global|The interval for inserting a dash (-) into all coupon codes. If you do not want to use a dash, leave the field blank. <br/>_**Note:**_ Coupon  codes that differ by only a dash are considered to be different codes.|

{:style="table-layout:auto"}
