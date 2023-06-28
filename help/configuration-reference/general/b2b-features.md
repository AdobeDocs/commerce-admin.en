---
title: '[!UICONTROL General] &gt; [!UICONTROL B2B Features]'
description: Review the configurations settings on the [!UICONTROL General] &gt; [!UICONTROL B2B Features] page of the Commerce Admin.
exl-id: fc07a067-b92a-49c7-8512-2dfcc1c6ba0c
---
# [!UICONTROL General] > [!UICONTROL B2B Features]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>With the installation and enablement of B2B for Adobe Commerce, the buying experience can be personalized with company-specific features. B2B for Adobe Commerce is an integrated solution that supports both B2B and B2C models. For more information about the B2B features, see the [_B2B for Adobe Commerce User Guide_](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## [!UICONTROL B2B Features]

![B2B Features](./assets/b2b-features.png)<!-- zoom -->

| Field                                                                            | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                                                                                                                                  |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Enable Company]](../../b2b/account-companies.md)                    | Website                                                                | When enabled, allows customers to manage their company assignment from their account dashboard, and also enables the Shared Catalog and B2B Quote features by default. Options: `Yes` / `No` |
| [[!UICONTROL Enable Quick Order]](../../b2b/quick-order.md)                      | Website                                                                | When enabled, allows customers and guests to quickly place orders based on SKU or product name. Options: `Yes` / `No`                                                                        |
| [[!UICONTROL Enable Requisition List]](../../b2b/configure-requisition-lists.md) | Website                                                                | When enabled, allows customers to create and manage requisition lists from their account dashboard.                                                                                          |

{:style="table-layout:auto"}

![B2B Features with companies and shared catalogs enabled](./assets/b2b-features-company-enabled.png)<!-- zoom -->

When the Company feature is enabled, additional fields are available for Shared Catalog and B2B Quote.

| Field                                                              | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Enable Shared Catalog]](../../b2b/catalog-shared.md)  | Website                                                                | When enabled, makes it possible to create curated catalogs with custom pricing that are available either globally, or limited to specific companies. Options: `Yes` / `No`                                                                                                                                      |
| [!UICONTROL Enable Shared Catalog direct products price assigning] | Website                                                                | When the _[!UICONTROL Enable Shared Catalog]_ field is set to `Yes`, this option is available. When enabled, only products that are assigned to a shared catalog are stored in the price index. Products that are not assigned to the shared catalog are not displayed on the storefront. Options: `Yes` / `No` |
| [[!UICONTROL Enable B2B Quote]](../../b2b/configure-quotes.md)     | Website                                                                | When enabled, allows company buyers to submit a request for a quote from the shopping cart. Options: `Yes` / `No`                                                                                                                                                                                               |

{:style="table-layout:auto"}

### [!UICONTROL Default B2B Payment Methods]

![B2B configuration - default payment method settings](./assets/b2b-features-default-payment-methods.png)<!-- zoom -->

|[!UICONTROL Applicable Payment Methods]|Global|Determines the selection of payment methods that are available to B2B buyers. Options: `All Payment Methods` / `Specific Payment Methods`|
|[!UICONTROL Payment Methods]|Global|Specifies each payment method that is available to B2B buyers.|

{:style="table-layout:auto"}

### [!UICONTROL Default B2B Shipping Methods]

![B2B configuration - default shipping methods](./assets/b2b-features-shipping-methods.png)<!-- zoom -->

|[!UICONTROL Applicable Shipping Methods]|Global|Determines the selection of shipping methods that are available by default to B2B buyers. Options: `All Shipping Methods` / `Specific Shipping Methods`|
|[!UICONTROL Shipping Methods]|Global|Specifies each shipping method that is available by default to B2B buyers. <br/>**_Note:_** You can also limit the shipping methods for a specific [company account](../../b2b/account-companies.md).|

{:style="table-layout:auto"}

## [!UICONTROL Order Approval Configuration]

| Field                                                                          | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                     |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [[!UICONTROL Enable Purchase Orders]](../../stores-purchase/purchase-order.md) | Website                                                                | When enabled, allows companies to create purchase orders. Options: `Yes` / `No` |

![B2B Features - Order Approval Configuration](./assets/b2b-features-order-approval.png)<!-- zoom -->

{:style="table-layout:auto"}
