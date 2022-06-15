---
title: Working with Shared Catalogs
description: Learn about using shared catalogs to maintain gated catalogs with custom pricing for different companies.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
---
# Working with Shared Catalogs

B2B for Adobe Commerce gives you the ability to maintain gated _shared_ catalogs with custom pricing for different companies. In addition to the standard, _primary_, product catalog, it provides customer access to two types of shared catalogs with different pricing structures.

If the [Shared Catalog feature](enable-basic-features.md) is enabled in the configuration, the original primary catalog remains visible from the Admin, but only the Default (General) public shared catalog is visible from the storefront. In addition, custom catalogs can be created that are visible only to members of specific [company](account-companies.md) accounts.

For the Default (General) public shared catalog, you must assign products to display the catalog on the storefront. By default, it is empty and does not contain any products.

>[!NOTE]
>
>When the shared catalog feature is enabled in the configuration, each category permission for the catalog is set to `Deny` for all customer groups automatically. Also, when a new category is created, it has the `Deny` category permissions by default to prevent showing that category on the storefront site before assignment to the shared catalog.

The Shared Catalogs page provides access to the tools used for managing your shared catalogs. The page is similar to the standard [Admin workspace](https://docs.magento.com/user-guide/stores/admin-workspace.html), with filters and action controls. The grid lists all shared catalogs, including the default public shared catalog, and any custom catalogs that you have set up.

![Shared Catalogs](./assets/shared-catalogs-grid.png)<!-- zoom -->

## Access the Shared Catalogs page

On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## Actions controls

The [Actions controls](https://docs.magento.com/user-guide/stores/admin-actions-control.html) in the upper-left corner can be used with the mass actions control to delete selected shared catalogs that are no longer needed. In the grid, the Actions column contains the full selection of tools to manage your shared catalogs.

![Shared Catalog Actions](./assets/shared-catalog-grid-action-column-controls.png)<!-- zoom -->

|Control|Description|
|------|-----------|
|[[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md)|Determines the product selection and custom pricing that is available in the shared catalog.|
|[[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md)|Determines which companies can access a shared catalog.|
|[[!UICONTROL General Settings]](catalog-shared-manage.md)|Determines the catalog detail information, including the name, catalog type, customer tax class, and description.|
|[!UICONTROL Delete]|Deletes the selected shared catalogs.|

{style="table-layout:auto"}

## Column descriptions

|Heading|Description|
|--- |--- |
|[!UICONTROL Select]|Selects shared catalog records for applying an action. The control in the header can be used to select all or deselect all shared catalog records in the grid. To select an individual shared catalog, select the checkbox.|
|[!UICONTROL ID]|A unique numeric identifier that is assigned in sequence when the catalog is created.|
|[!UICONTROL Name]|The name of the shared catalog. By default, the default (General) shared catalog is available.|
|[!UICONTROL Type]|Identifies the type of shared catalog as either: <br/>**[!UICONTROL Public]** - The default public shared catalog is created automatically when Adobe Commerce is installed. It is initially assigned to the `General` and `Not Logged In` customer groups, and is visible to guests and individual logged-in customers who are not associated with a company. The system supports only one public shared catalog at a time. <br/>**[!UICONTROL Custom]** - A custom shared catalog contains pricing that is visible only to logged-in associates of the assigned company accounts. You can create as many custom shared catalogs as you need.|
|[!UICONTROL Customer Tax Class]|The tax class that is assigned to the corresponding customer group. The Customer Tax Class column does not appear in the default grid, but can be added by changing the column layout.|
|[!UICONTROL Created At]|The date and time the shared catalog was created.|
|[!UICONTROL Created By]|The first and last name of the store administrator who created the shared catalog.|
|[!UICONTROL Action]|Lists actions that be applied to selected catalogs. Options: Set Pricing and Structure / Assign Companies / General Settings / Delete|

{style="table-layout:auto"}
