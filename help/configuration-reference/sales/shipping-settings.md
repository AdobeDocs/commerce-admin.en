---
title: "[!UICONTROL Sales] &gt; [!UICONTROL Shipping Settings]"
description: Review the configurations settings on the [!UICONTROL Sales] &gt; [!UICONTROL Shipping Settings] page of the Commerce Admin.
exl-id: d7d46946-f8c9-4714-96c3-2173e28f7bfa
feature: Configuration, Shipping/Delivery
TQID: https://experienceleague.adobe.com/4-Kmcd3F8pQyMgxp-NmkBFVNuEXWuYn-BOzpvxuFMhU
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
# [!UICONTROL Sales] > [!UICONTROL Shipping Settings]

{{config}}

For more information about changing these settings, see [Shipping settings](../../stores-purchase/shipping-settings.md) in the _Stores and Purchase Experience Guide_.

## [!UICONTROL Origin]

![Origin](./assets/shipping-settings-origin.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Country]|Website|The point-of-origin country.|
|[!UICONTROL Region/State]|Website|The point-of-origin region or state.|
|[!UICONTROL ZIP/Postal Code]|Website|The point-of-origin ZIP or postal code.|
|[!UICONTROL City]|Website|The point-of-origin city.|
|[!UICONTROL Street Address]|Website|The point-of-origin street address.|
|[!UICONTROL Street Address Line 2]|Website|An extra line for the point-of-origin street address, if needed.|

{style="table-layout:auto"}

## [!UICONTROL Shipping Policy Parameters]

![Shipping Policy Parameters](./assets/shipping-settings-shipping-policy-parameters.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Apply Custom Shipping Policy]|Website|Determines if your shipping policy appears during checkout. Options: `Yes` / `No`|
|[!UICONTROL Shipping Policy]|Store View|Contains your shipping policy as text.|

{style="table-layout:auto"}

## [!UICONTROL Shipment Tracking URLs]

[!BADGE SaaS only]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service projects only (Adobe-managed SaaS infrastructure)."}

![Shipping Policy Parameters](./assets/shipping-settings-shipment-tracking-urls.png)<!-- zoom -->

|Field|[Scope](../../getting-started/websites-stores-views.md#scope-settings)|Description|
|--- |--- |--- |
|[!UICONTROL Enable Custom Tracking URLs]|Store View|Determines whether shipment tracking numbers sent in shopper emails are links or plain text. The default value of `No` indicates the numbers are plain text. Options: `Yes` / `No`|
|[!UICONTROL USPS Tracking URL]|Store View|The URL template for United States Postal Service shipments.|
|[!UICONTROL UPS Tracking URL]|Store View|The URL template for United Parcel Service shipments.|
|[!UICONTROL FedEx Tracking URL]|Store View|The URL template for Federal Express shipments.|
|[!UICONTROL DHL Tracking URL]|Store View|The URL template for DHL Express shipments.|

{style="table-layout:auto"}
