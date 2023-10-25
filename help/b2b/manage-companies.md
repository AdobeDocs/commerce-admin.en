---
title: Company management
description: Learn about company management and how they function between companies in B2B.
feature: B2B, Companies, Management, Storefront
role: Admin
hide: yes
hidefromtoc: yes
---

# Company management

The Company management feature allows company Administrators to view and manage the parent company and its internal organization with all related companies. Administrators will be able to assign or unassign companies to the parent company or manage the roles and permissions within those companies. B2B company management is an excellent opportunity to improve the performance within a company.

From a business point of view, the controlling or owning company is generally called a parent company. While many parent companies will completely own their related companies, they can also be just one of the owners or members as well. In most cases, however, the parent company will be the majority shareholder. Although those companies are connected, they are two distinct legal entities.

Each company contains unique identifiers, such as:

* Company ID
* Company name
* Company type
* Company email
* Phone number
* Country
* State/Province
* City
* Company admin

## Company Hierarchy

In the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Companies Grid](./assets/companies-grid.png){width="700" zoomable="yes"}

The [!UICONTROL Companies] grid lists all companies regardless of status. 

When a company administrator creates a new company, there is  a dropdown section called **Company Hierarchy** where you can view, assign or unassign companies to a parent company.

When Parent or Child Company is selected, the merchant will be able to manage the setup in the "Advanced Settings" section which will expand this page section enabling the sales rep to identify all child companies that are part of the parent company.
The sequencing of this step may precede the creation of child accounts or occur after child accounts have already been set up.
New Parent Company: When the sales rep configures the Parent Account, they will complete the same fields that are currently available in the Add New Company process and they will have an option to create "Child Companies".  During this step, they have an option to duplicate (or copy) the same catalog entitlements, pricing, and terms from parent to Child Companies as a starting point
Existing Child Companies Exist: When the merchant creates a new parent company, they may search for all child companies and designate them as child companies under this parent company grouping.
NOTE: The details of this story are captured in B2B-2849 Establish Inheritance Logic: Once the Master Account/Tax and Administrative users have been set up.  The merchant may specify inheritance rules as follows:
Full Inheritance: All catalog entitlements, pricing, and terms are replicated from parent to child account.
Partial Inheritance: Specify items that should be inherited including 1,2,3.
No Inheritance: The Child Company must be manually configured without any inheritance between companies


>[!IMPORTANT]
>
>Company users can be added, edited, or removed only by the company administrator. Removal cannot be reversed because the user is removed from the company structure.

![Company Users](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

Root organization

The root organization is the top-level organization and is its own parent. All organizations in the HCL Commerce organization structure are descendants of the root organization. The site administrators are owned by the root organization.

Default organization

The default organization is owned by the root organization. All guest customers and all customers in a B2C scenario belong to the default organization. Customers in a B2B or B2B indirect scenarios should not be placed under the default organization, but rather in the appropriate buyer organization. B2C users under the default organization can be managed by an administrator in HCL Commerce Accelerator. Business users outside of the default organization can be managed in the Organization Administration Console. Do no create stores under the default organization. Instead, create stores under a separate organization, such as the seller organization.
Note the following considerations about the Default Organization:
OrgAdminConsole: This tool to manage business users and administrators does not list users under the Org -2000 (Default Org), or allow users to be created under the Default Org, since it assumes that is where B2C Shoppers (and guest users) are kept. Accelerator can be used to manage B2C shoppers.
Access Control: By default, Default Org (-2000) subscribes to GuestShopperManagementPolicyGroup which allows for some administrators (regardless of where they play their role) to manage the users under the Default Org. Guest users are implicitly owned by the Default Organization (-2000), when an access control check is done on this type of user, since guest users do not exist in the MBRREL table.
MemberRegistrationAttributes.xml: By default, it has configurations that assume the Default Org DN.
UserRegistrationAdd command: If no parentMember is specified (for example, the B2C scenario), the user will be placed under the Default Org.
One or more other levels of organizational entities can exist beneath the parent organizational entities. You can add as many child organizational entities as necessary to support your business.

Organizational structure provides guidance to all employees by laying out the official reporting relationships that govern the workflow of the company. A formal outline of a company's structure makes it easier to add new positions, roles, and authorizations in the company.

Structure provides clarity, helps to manage expectations, enables better purchase decision-making, and provides consistency. It also helps with assignment of responsibility regarding budgets, cost, purchase limits, and workflow processes.

Administrators need to manage such organizational-related activities whenever required. This feature enables administrators to view and edit the company structure and the entities related to the company.