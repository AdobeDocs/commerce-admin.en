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

When a company administrator creates a new company, you can unfold a dropdown called **Company Hierarchy** where you can view the parent company, or assign and unassign companies to that parent company:

* New Parent Company: When the company administrator has created the company, new companies can be added to this parent company.

* Existing Company: When the company administrator has created the company, new companies can be searched and added to this parent company.

>[!IMPORTANT]
>
> In the **Company Hierarchy** view for a parent company, it appears as empty. This section enables a sales representative to identify all companies that are part of that parent company.

Once the Master Account/Tax and Administrative users have been set up.  The merchant may specify inheritance rules as follows:
* Full Inheritance: All catalog entitlements, pricing, and terms are replicated from parent to child account.
* Partial Inheritance: Specify items that should be inherited including 1,2,3.
* No Inheritance: The Child Company must be manually configured without any inheritance between companies

Root organization

The root organization is the top-level organization and is its own parent. All organizations in the HCL Commerce organization structure are descendants of the root organization. The site administrators are owned by the root organization.

Default organization

The default organization is owned by the root organization. All guest customers and all customers in a B2C scenario belong to the default organization. Customers in a B2B or B2B indirect scenarios should not be placed under the default organization, but rather in the appropriate buyer organization. B2C users under the default organization can be managed by an administrator in HCL Commerce Accelerator. Business users outside of the default organization can be managed in the Organization Administration Console. Do no create stores under the default organization. Instead, create stores under a separate organization, such as the seller organization.
