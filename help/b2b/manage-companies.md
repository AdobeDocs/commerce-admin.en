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

Company management streamlines business operations for companies with complex organizational structures. Admin users can build a company hierarchy to mirror a B2B organization by assigning companies to the designated parent company. This assignment allows the parent company administrator to view and manage companies within the organization.

Initiate company management tasks from the *[!UICONTROL Companies]* view. From the Admin, go to  **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

  ![B2B Manage Companies Grid](./assets/companies-grid-view.png){width="700" zoomable="yes"}

In the *[!UICONTROL Companies grid]*, the *[!UICONTROL Company Type]* column indicates whether a company is managed as part of an organization, or as a separate company.

- `Parent` is a business organization with one or more assigned companies. A parent company cannot be assigned as a child of another company.

- `Child` is a company that has been assigned to an organization. A company can be assigned to only one parent company.

- `Company` represents a single company. A single company can become part of an organization by making it a parent company or by assigning it to an existing parent company.

When you edit a parent or child company, expand *[!UICONTROL Company Hierarchy]* to view all companies in the organization. A `Current` flag indicates the company you are editing.

   ![B2B Company Hierarchy grid](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## View and configure the [!UICONTROL Company Hierarchy]

On initial company creation, the [!UICONTROL Company Hierarchy] grid is empty. It is also empty if the company is a single company.

![B2B Company Hierarchy Grid](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

For parent companies, Admin users with appropriate permissions can complete the following tasks:

- Build the company hierarchy by creating a new parent organization, or updating an existing one.
- Manage an existing organization to add or remove companies.

For details, see [Manage the company hierarchy](assign-companies.md).
