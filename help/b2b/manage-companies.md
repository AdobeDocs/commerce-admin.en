---
title: Company Management
description: Streamline administration and management of B2B organizations with complex operational models.
feature: B2B, Companies, Storefront
role: Admin
hide: no
hidefromtoc: no
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
---
# Company management

Company management in Adobe Commerce provides comprehensive tools for administrators to organize, configure, and oversee B2B business relationships. This feature is essential for businesses that work with multiple corporate customers, subsidiaries, or complex organizational structures.

Company management enables you to:

- **Organize Business Relationships**: Create and manage individual company accounts for your B2B customers
- **Build Organizational Hierarchies**: Structure parent-child relationships that mirror real-world business organizations
- **Centralize Administration**: Manage multiple companies and their settings from a single administrative interface
- **Streamline Operations**: Apply consistent configurations and policies across related companies
- **Support Complex Structures**: Handle subsidiaries, franchises, multi-location businesses, and corporate divisions

## Prerequisites

Before managing companies, ensure that:

- B2B features are enabled in your Adobe Commerce installation
- You have administrative access with company management permissions
- Company accounts are properly configured with necessary business information
- User roles and permissions are defined for company administrators and users

## Use cases

Company management is ideal for:

- **Multi-location businesses** with centralized purchasing but location-specific needs
- **Franchise operations** requiring both corporate oversight and local autonomy
- **Corporate subsidiaries** with shared policies but independent operations
- **Large enterprises** with multiple divisions or business units
- **Distribution networks** with resellers, dealers, or channel partners

Admin users can build a company hierarchy to mirror a B2B organization by assigning companies to the designated parent company. This assignment allows the parent company administrator to view and manage companies within the organization.

Initiate company management tasks from the *[!UICONTROL Companies]* view. From the Admin, go to  **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

  ![B2B Manage Companies Grid](./assets/companies-grid-view.png){width="700" zoomable="yes"}

## Understanding Company Types

The *[!UICONTROL Company Type]* column in the Companies grid indicates how each company is structured within your B2B organization. Understanding these types helps you organize and manage your business relationships effectively.

- **`Parent`** - A business organization with one or more assigned companies
  - Acts as the central hub for organizational management
  - Can have multiple child companies but cannot be assigned to another parent
  - Inherits administrative control over all assigned child companies
  - **Use case**: Corporate headquarters, main franchise organization, or holding company

- **`Child`** - A company assigned to a parent organization
  - Operates under the governance and policies of its parent company
  - Can only belong to one parent company at a time
  - May inherit settings and configurations from the parent
  - **Use case**: Subsidiary offices, franchise locations, or regional divisions

- **`Company`** - An independent single company
  - Operates independently without organizational hierarchy
  - Can be converted to a parent company by assigning other companies
  - Can be assigned to an existing parent company to become a child
  - **Use case**: Individual business customers, standalone clients, or companies not part of larger organizations

### Converting between Company Types

- **Single Company → Parent**: Assign other companies to it
- **Single Company → Child**: Assign it to an existing parent company
- **Child → Single**: Unassign it from its parent company
- **Parent → Child**: Not possible without first removing all assigned companies

When you edit a parent or child company, expand *[!UICONTROL Company Hierarchy]* to view all companies in the organization. A `Current` flag indicates the company you are editing.

   ![B2B Company Hierarchy grid](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

For detailed step-by-step instructions on building and managing company hierarchies, see [Manage the Company Hierarchy](manage-company-hierarchy.md).

## View and configure the [!UICONTROL Company Hierarchy]

On initial company creation, the *[!UICONTROL Company Hierarchy]* grid is empty. It is also empty if the company is a single company.

![B2B Company Hierarchy Grid](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

## Core Company Management Tasks

When managing companies in the hierarchy, administrators can perform the following key tasks using the *[!UICONTROL Company Hierarchy]* grid:

### Viewing and Managing Company Relationships

- **View Associated Companies**: See all companies linked to a parent organization in one centralized view
- **Monitor Company Status**: Track active, pending, and inactive companies within the hierarchy
- **Access Company Details**: Navigate directly to individual company configuration pages

### Building and Modifying Hierarchies

- **Assign companies**: Add existing companies to a parent organization from the company detail page
- **Create parent-child relationships**: Structure companies to reflect real-world business relationships
- **Reorganize structures**: Move companies between different parent organizations as business needs change

### Bulk Configuration Management

- **Apply settings across companies**: Update advanced settings for multiple companies simultaneously
- **Standardize configurations**: Ensure consistent policies across related organizations
- **Override individual settings**: Push parent company configurations to selected child companies

### Administrative Actions

- **Remove company relationships**: Use the *[!UICONTROL Unassign from parent]* action to dissolve organizational ties
- **Manage company access**: Control which administrators can view and modify company relationships
- **Monitor hierarchy changes**: Track modifications to organizational structures

## Best Practices

When managing complex company structures, consider these recommendations:

### Organizational Strategy

- **Plan your hierarchy**: Design your company structure to match real business relationships and reporting lines
- **Keep it simple**: Avoid overly complex hierarchies that may confuse users or complicate administration
- **Document relationships**: Maintain clear records of why companies are grouped and their business connections

### Configuration Management

- **Test before applying**: Use individual companies to test configuration changes before applying to entire hierarchies
- **Backup settings**: Document current configurations before making bulk changes to company settings
- **Communicate changes**: Notify affected company administrators before implementing hierarchy or setting changes

### User Access and Security

- **Limit administrative access**: Only grant company management permissions to trusted administrators
- **Regular reviews**: Periodically review company relationships and access permissions
- **Monitor activity**: Track changes to company hierarchies and configurations for audit purposes

>[!MORELIKETHIS]
>
>*[Create a Company Account](account-company-create.md)
>* [Manage the Company Hierarchy](manage-company-hierarchy.md)
>* [Company Roles and Permissions](account-company-roles-permissions.md)
>* [Company Credit Management](credit-company.md)
>* [Enable B2B Features](enable-basic-features.md)
