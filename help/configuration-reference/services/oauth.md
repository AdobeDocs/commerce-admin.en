---
title: '[!UICONTROL Services] &gt; [!UICONTROL OAuth]'
description: Review the configurations settings on the [!UICONTROL Services] &gt; [!UICONTROL OAuth] page of the Commerce Admin.
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
---
# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![Access Token Expiration](./assets/oauth-token-expire.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Customer Token Lifetime (hours])|Global|Determines the length of time in hours before a customer API token expires. The customer token never expires if field is empty. Default value: `1`|
|[!UICONTROL Admin Token Lifetime (hours)]|Global|Determines the length of time in hours before an admin API token expires. The admin token never expires if the field is empty. Default value: `4`|

{style="table-layout:auto"}

>[!NOTE]
>
>Bearer customer and admin API token Lifetime and encryption algorithms are controlled by the [JWT Authentication](magento-web-api.md#jwt-authentication) configuration settings.

## [!UICONTROL Cleanup Settings]

![Cleanup Settings](./assets/oauth-cleanup.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Cleanup Probability]|Global|Specifies the number of OAuth requests before cleanup is launched. Do not enter `0` to disable cleanup.|
|[!UICONTROL Enable WSDL Cache]|Global|Determines the age of entries in minutes, before they are cleaned.|

{style="table-layout:auto"}

## [!UICONTROL Consumer Settings]

![Consumer Settings](./assets/oauth-consumer-settings.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL OAuth consumer credentials HTTP Post timeout]|Global|Specifies the number of seconds it takes for the system to time out when customers post their credentials.|
|[!UICONTROL OAuth consumer credentials HTTP Post maxredirects]|Global|Specifies the maximum number of redirects that are related to a posting of consumer credentials.|
|[!UICONTROL Expiration Period]|Global|Determines the number of seconds before an unused key/secret expires after the OAuth token exchange begins.|

{style="table-layout:auto"}

## [!UICONTROL Authentication Locks]

![Authentication Locks](./assets/oauth-locks.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Maximum Login Failures to Lock Out Account]|Global|Specifies the Maximum Number of authentication failures to lock out account.|
|[!UICONTROL Lockout Time (seconds)]|Global|Specifies the time period in seconds after which account is unlocked.|

{style="table-layout:auto"}
