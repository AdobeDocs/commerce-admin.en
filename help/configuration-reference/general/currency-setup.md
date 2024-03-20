---
title: '[!UICONTROL General] &gt; [!UICONTROL Currency Setup]'
description: Review the configurations settings on the [!UICONTROL General] &gt; [!UICONTROL Currency Setup] page of the Commerce Admin.
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
---
# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>See [Currency configuration](../../stores-purchase/currency-configuration.md) for more details about these configurations.

## [!UICONTROL Currency Options]

![Currency Setup > Currency Options](./assets/currency-setup-currency-options.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Base Currency]|Website|The primary currency used for all online payment transactions. For multiple store views, the scope of the price  must be set in the [Catalog](../catalog/catalog.md) configuration.|
|[!UICONTROL Default Display Currency]|Store View|The primary currency used to display prices.|
|[!UICONTROL Allowed Currencies]|Store View|The currencies accepted by your store for payment.|

{style="table-layout:auto"}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>Starting with the 2.4.6 release, the [[!DNL Fixer.io]](https://fixer.io/) service is deprecated and replaced with the [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) service. It is highly recommended that you use an APILayer account instead of a deprecated [!DNL Fixer.io] account.

![Currency Setup > Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL API key]|Global|The key used to access the conversion service through your [!DNL fixer.io] account. For more information, see [[!DNL fixer.io]](https://fixer.io/).|
|[!UICONTROL Connection Timeout in Seconds]|Global|Determines the number of seconds of inactivity before a Fixer.io session times out. Default value: `100`|

{style="table-layout:auto"}

## [!UICONTROL Fixer Api (APILayer)]

![Currency Setup > Fixer Api (APILayer)](./assets/currency-setup-fixer-api.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL API key]|Global|The key used to access the conversion service through your [!DNL APILayer] account. For more information, see [[!DNL APILayer]](https://apilayer.com/).|
|[!UICONTROL Connection Timeout in Seconds]|Global|Determines the number of seconds of inactivity before an [!DNL APILayer] session times out. Default value is `100`.|

{style="table-layout:auto"}

## [!UICONTROL Currency Converter API]

![Currency Setup > Currency Converter API](./assets/currency-setup-converter.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL API key]|Global|The key used to access the conversion service. For more information, see [[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/).|
|[!UICONTROL Connection Timeout in Seconds]|Global|Determines the number of seconds of inactivity before a [!DNL Currency Converter] session times out. Default value:`100`|

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import Settings]

![Currency Setup > Scheduled Import Settings](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enabled]|Store View|Determines if scheduled import is enabled for currency rates. Options: `Yes` / `No`|
|[!UICONTROL Service]|Store View|Specifies the service that provides the data for the scheduled import. Default value is `fixer.io`|
|[!UICONTROL Start Time]|Store View|Indicates the start time by hour, minute, and second, based on a 24-hour clock.|
|[!UICONTROL Frequency]|Store View|Determines how often the scheduled import takes place. Options: `Daily` / `Weekly` / `Monthly`|
|[!UICONTROL Error Email Recipient]|Store View|Identifies the email address of each person who is notified by email about scheduled import errors. For multiple recipients, separate each entry with a comma.|
|[!UICONTROL Error Email Sender]|Website|Identifies the store contact that appears as the sender of the error email notification. Default sender: `General Contact`|
|[!UICONTROL Error Email Template]|Website|Specifies the template that is used as the basis of the error email notification. Default template: `Currency Update Warnings`|

{style="table-layout:auto"}
