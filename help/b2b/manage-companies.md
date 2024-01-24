---
title: Company management
description: Streamline administration and management of B2B organizations with complex operational models.
feature: B2B, Companies, Storefront
role: Admin
hide: no
hidefromtoc: no
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
---
# Company management

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Available only for Beta program participants"}

Company management streamlines business operations for companies with complex organizational structures. Admin users can mirror the structure in Adobe Commerce by building a company hierarchy that assigns related companies to the designated parent company. This assignment allows the parent company administrator to view and manage their own account and the company hierarchy for all assigned companies.

Initiate company management tasks from the *[!UICONTROL Companies]* grid.

From the *[!UICONTROL Admin]*, go to  **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

  ![Companies Grid](./assets/companies-grid-view.png){width="675
   " zoomable="yes"}

The *[!UICONTROL Company Type]* column indicates whether a company is managed as part of an organization, or as a separate company.

- `Parent` is a business organization with one or more assigned companies. A parent company cannot be assigned as a child of another company.

- `Child` is a company that has been assigned to an organization. A company can be assigned to only one parent company.

- `Company` represents a single company. A single company can be added to an organization by assigning it to a parent company.

When you edit a parent or child company from the grid, the company details list all associated companies in the *[!UICONTROL Company Hierarchy]*.  A `Current` flag indicates the company you are editing.

   ![Companies Grid](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

>[!NOTE]
>
>See the [Manage company accounts](account-company-manage.md) for more information on the Companies grid.

See the [Manage company accounts](account-company-manage.md) for more information on the Companies grid.

## View and configure the [!UICONTROL Company Hierarchy]

On initial company creation, the [!UICONTROL Company Hierarchy] grid is empty. It is also empty if the company is a single company.

![Companies Hierarchy Grid](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

If the company is a designated parent company, Admin users with appropriate permissions can build the company hierarchy by assigning companies to it **[!UICONTROL Assign Companies]**.

After you create a parent company by assigning a company to it, use the *[!UICONTROL Company Hierarchy]* grid for other company management tasks:

- View all companies associated with parent company.
- From a parent company detail page, assign more companies to the organization.
- Remove a company from an organization by using the *[!UICONTROL Unassign from parent]* action.
- Update the [Advanced Settings](account-company-create.md#advanced-settings) configuration to apply the same settings to multiple companies.

For detailed instructions, see [assign and unassign companies](assign-companies.md).
