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

* **Organize Business Relationships**—Create and manage individual company accounts for your B2B customers
* **Build Organizational Hierarchies**—Structure parent-child relationships that mirror real-world business organizations
* **Centralize Administration**—Manage multiple companies and their settings from a single administrative interface
* **Streamline Operations**—Apply consistent configurations and policies across related companies
* **Support Complex Structures**—Manage subsidiaries, franchises, multi-location businesses, and corporate divisions

Admin users can build a company hierarchy to mirror a B2B organization by assigning companies to a designated parent company. This assignment allows the parent company administrator to view and manage companies within the organization.

Initiate company management tasks from the *[!UICONTROL Companies]* view. From the Admin, go to  **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![B2B Manage Companies Grid](./assets/companies-grid-view.png){width="700" zoomable="yes"}

## Prerequisites

Before managing companies, ensure that:

* B2B features are enabled in your Adobe Commerce installation
* You have administrative access with company management permissions
* Company accounts are properly configured with necessary business information
* User roles and permissions are defined for company administrators and users

## Use cases

Company management is ideal for:

* **Multi-location businesses** with centralized purchasing but location-specific needs
* **Franchise operations** requiring both corporate oversight and local autonomy
* **Corporate subsidiaries** with shared policies but independent operations
* **Large enterprises** with multiple divisions or business units
* **Distribution networks** with resellers, dealers, or channel partners

## Understanding Company Hierarchy and Company Types

Company hierarchy structures business relationships by organizing multiple companies under a single parent company. This feature mirrors real-world organizational structures while enabling centralized management and preserving individual company identities.

### Company Types

The *[!UICONTROL Company Type]* column in the Companies grid shows how each company fits within your B2B organization:

* **Parent**—Central hub with one or more assigned companies
  * Controls multiple child companies but cannot be assigned to another parent
  * **Use case**—Corporate headquarters, main franchise organization, or holding company

* **Child**—Company assigned to a parent organization
  * Operates under parent governance and may inherit configurations
  * Can only belong to one parent at a time
  * **Use case**—Subsidiary offices, franchise locations, or regional divisions

* **Company**—Independent single company
  * Operates independently without hierarchy relationships
  * Can convert to parent (by assigning companies) or child (by assignment to parent)
  * **Use case**—Individual business customers or standalone clients

### Converting Company Types

* **Single Company → Parent**—Assign other companies to it
* **Single Company → Child**—Assign it to an existing parent company
* **Child → Single**—Unassign the child company from its parent
* **Parent → Child**—Not possible without first removing all assigned companies

### Managing Company Hierarchies

When editing companies within a hierarchy, expand *[!UICONTROL Company Hierarchy]* to view all related companies. A `Current` flag indicates the company being edited.

![B2B Company Hierarchy grid](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

For detailed step-by-step instructions, see [Manage the Company Hierarchy](manage-company-hierarchy.md).

## Company management tasks

When managing companies from the company grid, administrators can perform the following tasks from the *[!UICONTROL Company Hierarchy]* grid:

* **View and manage company relationships**
  * **View Associated Companies**—See all companies linked to a parent organization in one centralized view
  * **Monitor Company Status**—Track active, pending, and inactive companies within the hierarchy
  * **Access Company Details**—Navigate directly to individual company configuration pages

* **Build and modify hierarchies**
  * **Assign companies**—Add existing companies to a parent organization from the company detail page
  * **Create parent-child relationships**—Structure companies to reflect real-world business relationships
  * **Reorganize structures**—Move companies between different parent organizations as business needs change

* **Bulk configuration management**
  * **Apply settings across companies**—Update advanced settings for multiple companies simultaneously using the [!UICONTROL Actions] control on the Company grid
  * **Standardize configurations**—Ensure consistent policies across related organizations
  * **Override individual settings**—Push parent company configurations to selected child companies

* **Administrative actions**
  * **Remove company relationships**—Use the *[!UICONTROL Unassign from parent]* action to dissolve organizational ties
  * **Manage company access**—Control which administrators can view and modify company relationships
  * **Monitor hierarchy changes**—Track modifications to organizational structures

## Best practices

When managing companies, consider the following best practices:

* **Building company hierarchies**—When managing complex company structures, plan your hierarchy to match real business relationships while keeping structures simple to avoid user confusion. Document all company relationships and their business connections for future reference.

* **Configuration management**—Test configuration changes on individual companies before applying them to entire hierarchies, and always document current settings before making bulk changes. Communicate planned changes to affected company administrators in advance.

* **Security**—Limit company management permissions to trusted administrators only, conduct regular reviews of company relationships and access permissions, and monitor all hierarchy changes for audit purposes.

>[!MORELIKETHIS]
>
>* [Create a company account](account-company-create.md)
>* [Manage company hierarchies](manage-company-hierarchy.md)
>* [Company roles and permissions](account-company-roles-permissions.md)
>* [Company credit management](credit-company.md)
>* [Enable B2B features](enable-basic-features.md)
