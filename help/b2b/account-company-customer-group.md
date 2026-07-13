---
title: Assign a customer group to a company
description: Learn about assigning a customer group to a company account in your Adobe Commerce store.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
TQID: https://experienceleague.adobe.com/O03eRkYyE78HIHjmwYRXqfOR2A7k1KFL11AspJGCi-U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Assign a customer group to a company

Assigning a customer group to a company is essentially the same as assigning a shared catalog. If Shared Catalog is not [enabled in the configuration](enable-basic-features.md), a Customer Group — rather than a Shared Catalog — is assigned to a company.

- Only one customer group or shared catalog can be assigned to a company at a time. A customer group that is associated with a shared catalog cannot be deleted.
- Changing the customer group assigned to the company updates the profiles of all company members.
- If the customer group assignment is changed from a shared catalog to a regular customer group, company members lose access to the shared catalog and the primary catalog becomes available to them from the storefront.
- After changing the company group, a company user must log out and log in on the Storefront to see new prices in the catalog.

## Change the customer group

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Find the company in the grid and click **[!UICONTROL Edit]** in the _[!UICONTROL Action]_ column.

   ![Edit Company](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. On the company page, scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Advanced Settings]** section.

1. Set the appropriate **[!UICONTROL Customer Group]**.
   
   The [!UICONTROL Customer Group] list includes all existing shared catalogs, even if Shared Catalogs is disabled in the configuration.

   ![Change customer group or shared catalog](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. When prompted to confirm, click **[!UICONTROL Proceed]**.

1. Click **[!UICONTROL Save]**.
