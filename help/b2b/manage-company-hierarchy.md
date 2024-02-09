---
title: Manage the Company Hierarchy
description: Build and manage company hierarchies to support B2B organizations with complex operational models.
feature: B2B, Companies
role: Admin
hide: no
hidefromtoc: no
exl-id: a277ed95-7935-4d27-adb2-35116972732b
---
# Manage the [!UICONTROL Company Hierarchy]

Administrators can build a [!UICONTROL Company Hierarchy] by assigning related companies to a designated parent company, which is the company at the top of the organizational hierarchy.

From the Admin, create a parent company by editing an individual company (`[!UICONTROL Company Type] = Company`) and assigning related companies in the [!UICONTROL Company Hierarchy] configuration.

![Company Hierarchy Grid](./assets/company-hierarchy-grid.png){width="700"}


>[!NOTE]
>
>For details about the [!UICONTROL Company Hierarchy] grid, see [Company Hierarchy](account-company-create.md#company-hierarchy) field descriptions.

Manage company assignments by editing a parent company and using the *[!UICONTROL Company Hierarchy]* grid to add or remove companies. Use the *[!UICONTROL Actions]* control to manage the [advanced settings configuration](#change-company-settings) for companies in the organization.

## Assign companies to a parent company

1. On the _Admin_ sidebar, navigate to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

     ![Companies Grid](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. From the [!UICONTROL Companies] grid, open the company detail page to create the assignments.

   - To assign additional companies to an existing parent company, select the **[!UICONTROL Edit]** action for the parent company.
   - To create a parent company, select the **[!UICONTROL Edit]** action for the company designated as the parent.

     You cannot create a new parent company from an existing parent or child company.

1. On the Company detail page, expand **[!UICONTROL Company Hierarchy]**, and then select **[!UICONTROL Assign Companies]**.

    ![Create parent company](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. From the list of available companies, choose the companies to assign, then select **[!UICONTROL Assign Selected Companies]**.

    ![Select companies to assign](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. When prompted, complete the company assignment by selecting **[!UICONTROL Assign]**.

## Unassign companies from a parent company

1. On the Companies page, open the company detail page for the parent company by selecting the **[!UICONTROL Edit]** action.

    ![Parent company detail page](./assets/company-update.png){width="700" zoomable="yes"}

1. View the list of assigned companies by expanding **[!UICONTROL Company Hierarchy]**.

1. Remove the company from the organization.

   - In the [!UICONTROL Action] column for the company to remove, **[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**.

     ![Remove a company from an organization](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   - When prompted, remove the assigned company from the hierarchy by selecting **[!UICONTROL Unassign]**.

## Manage company settings for an organization

Update the [Advanced Settings](account-company-create.md#advanced-settings) configuration for an organization to apply the parent configuration to all child companies, or to apply the same settings to selected companies in the organization.

During the update process the initial configuration values default to the the current values configured for the parent company. You must change at least one setting to update the configuration for selected companies.

**Change the Advanced Settings configuration for multiple companies**

1. On the _Admin_ sidebar, navigate to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. From the [!UICONTROL Companies] grid, edit the parent company by selecting **[!UICONTROL Edit]** from the **[!UICONTROL Action]** column.

1. On the parent company detail page, expand **[!UICONTROL Company Hierarchy]** section to view companies included in the organization.

1. Select the companies to configure.

   ![Select companies from company hierarchy](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. From the **[!UICONTROL Actions]** control above the grid, select **[!UICONTROL Change company settings]**.

   ![Change company settings for company hierarchy](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. Change the settings configuration.

   - On the [!UICONTROL Change company settings] page, find the configuration setting to modify.

   - Select the **[!UICONTROL Change]** checkbox to enable the setting.

   - Update the value as needed.

     ![Change company settings for multiple companies](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. After updating the configuration, select **[!UICONTROL Apply Changes]**.

1. When prompted, select **[!UICONTROL Change settings]** to update the configuration for the selected companies.

>[!TIP]
>
>Manage the advanced settings configuration for a single company by editing the company line item.
