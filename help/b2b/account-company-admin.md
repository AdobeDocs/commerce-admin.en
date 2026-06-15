---
title: Assign a company administrator
description: Learn how to assign a company user account as the designated company administrator for the company account.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
TQID: https://experienceleague.adobe.com/5h4DaxiUVTz9UFOC3BZqd5ESPRLaLgvstCODPEEgCEk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
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
# Assign a company administrator

The company administrator is initially assigned when the company account is first created, and can be modified only by a store administrator from the Admin.

- Each company can have only one assigned administrator.
- A company user can be the administrator for only one company.
- Changes to the assigned company administrator must be completed by a store administrator from the Admin.

## Change assigned company administrator

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Companies](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Find the company in the list, and then click **[!UICONTROL Edit]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Company Admin]** section.

   ![Company Admin](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Enter the **[!UICONTROL Job Title]** of the new company administrator.

   This action clears the form and the required _[!UICONTROL First Name]_ and _[!UICONTROL Last Name]_ fields are highlighted.

1. Enter the **[!UICONTROL Email]** address of the new company administrator.

   If the system doesn't find the email address in the database, you are prompted to confirm that you want to replace the company administrator.

   - If a user account doesn't exist for the new company administrator, the system creates an account of the `Company Admin` type.

   - If the user account exists in the system, it is moved to the company administrator position in the company structure.

1. Enter the **[!UICONTROL First Name]** and **[!UICONTROL Last Name]**, and any other information as applicable for the new company administrator.

1. When complete, click **[!UICONTROL Save]**.

   The individual account of the former company administrator remains in the system as an active user account, assigned to the default user role. If this is the only company associated with the user account, the account type changes from *[!UICONTROL Company user]* to *[!UICONTROL Individual user]*.

   The system sends email notification of the change to the new and former company administrators.

