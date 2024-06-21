---
title: Assign a customer group to a company
description: Learn about assigning a customer group to a company account in your Adobe Commerce store.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
---
# Assign a customer group to a company

Assigning a customer group to a company is essentially the same as assigning a shared catalog. If Shared Catalog is not [enabled in the configuration](enable-basic-features.md), a Customer Group — rather than a Shared Catalog — is assigned to a company.

>[!NOTE]
>
> Only one customer group or shared catalog can be assigned to a company at a time. A customer group that is associated with a shared catalog cannot be deleted.

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Find the company in the grid and click **[!UICONTROL Edit]** in the _[!UICONTROL Action]_ column.

   ![Edit Company](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. On the company page, scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Advanced Settings]** section.

1. Set the appropriate **[!UICONTROL Customer Group]**.

   >[!NOTE]
   >
   >The [!UICONTROL Customer Group] list includes all existing shared catalogs, even if Shared Catalogs is disabled in the configuration.

   Changing the customer group assigned to the company updates the profiles of all company members.

   >[!NOTE]
   >
   >To see a new prices in the catalog, company users must re-login on the Storefront after the company group is changed.

   ![Change customer group or shared catalog](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   >[!NOTE]
   >
   >If the customer group assignment is changed from a shared catalog to a regular customer group, company members lose access to the shared catalog and the primary catalog becomes available to them from the storefront.

1. When prompted to confirm, click **[!UICONTROL Proceed]**.

1. Click **[!UICONTROL Save]**.
