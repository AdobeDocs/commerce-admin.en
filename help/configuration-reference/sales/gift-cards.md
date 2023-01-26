---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Gift Cards]'
description: Review the configurations settings on the [!UICONTROL Sales] &gt; [!UICONTROL Gift Cards] page of the Commerce Admin.
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
---
# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![Gift Card Email Settings](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Gift Card Notification Email Sender]|Store View|Identifies the [store contact](../../getting-started/store-details.md#store-email-addresses) that appears as the sender of the gift card notification email. Default value: `General Contact`|
|[!UICONTROL Gift Card Notification Email Template]|Store View|Determines the [template](../../systems/email-templates.md) that is used for the gift card notification email.|

{:style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![Gift Card General Settings](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Redeemable]|Global|Determines if the holder of the gift card can redeem its value for cash. Options: `Yes` / `No`.|
|[!UICONTROL Lifetime (days)]|Global|Determines the number of days that the card is valid. If left blank, the card does not expire. <br/><br/>**_Important:_** In some places, it is illegal to set an expiration data on gift cards. Check your local laws before setting a lifetime for your gift cards.|
|[!UICONTROL Allow Gift Message]|Store View|Determines if the option to include a gift message  is available to customers who purchase a gift card. Options: `Yes` / `No`.|
|[!UICONTROL Gift Message Maximum Length]|Store View|Determines the maximum number of characters allowed in a gift card message. Default value: 255|
|[!UICONTROL Generate Gift Card Account when Order Item is]|Global|Determines if a gift card account is generated when a customer places an order, or when the order is invoiced. Options: `Ordered` / `Invoiced`|

{:style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![Email Sent from Gift Card Account Management](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Gift Card Email Sender]|Store View|Identifies the [store contact](../../getting-started/store-details.md#store-email-addresses) that appears as the sender of the gift card email. Default value: `General Contact`|
|[!UICONTROL Gift Card Template]|Store View|Determines the [template](../../systems/email-templates.md) that is used for the gift card email.|

{:style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![Gift Card Account General Settings](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Code Length]|Global|Determines the length of the gift card code.|
|[!UICONTROL Code Format]|Global|Determines the format of the gift card code. Options: `Alphanumeric` / `Numeric`|
|[!UICONTROL Code Prefix]|Global|Defines any prefix added to the beginning of the code.|
|[!UICONTROL Code Suffix]|Global|Defines any suffix added to the end of the code.|
|[!UICONTROL Dash Every X Characters]|Global|If you want to include dashes in the code, determines the number of characters between each dash.|
|[!UICONTROL New Pool Size]|Global|Determines the size of the new code pool to be generated.|
|[!UICONTROL Low Code Pool Threshold]|Global|Determines the number of records in the code pool that triggers an alert that the pool needs to be replenished.|
|[!UICONTROL Generate]|Global|Click to generate the list of gift card codes.|

{:style="table-layout:auto"}
