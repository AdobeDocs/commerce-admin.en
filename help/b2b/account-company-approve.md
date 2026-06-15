---
title: Approve a company account
description: Learn how to approve company account requests in the Admin.
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
TQID: https://experienceleague.adobe.com/ZpDdYMYaSnG1lOwV22mmrkYjBvf90pUJVZxP2r526pw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
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
# Approve a company account

The status of requests received from the storefront to create a company are `Pending Approval` until the request is reviewed by the store administrator, and either approved or rejected. The status of a company account might be set to any of the following:

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

You can also use the [Actions control](account-company-manage.md) to approve multiple company requests.

![Pending Approval](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## Approve a pending company account

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   You can use the _[!UICONTROL Columns]_ selector above the grid to display the **[!UICONTROL Status]** column.

1. In the _[!UICONTROL Action]_ column, click **[!UICONTROL Edit]**.

1. Set **[!UICONTROL Company Status]** to `Active`.

   ![Set the company status](./assets/company-status-active.png){width="700" zoomable="yes"}

1. When prompted to confirm, click **[!UICONTROL Change status]**.

   The company administrator receives email notification that the company is now active.

1. If applicable, set **[!UICONTROL Sales Representative]** to a specific Admin user account.

1. Expand ![Expansion selector](../assets/icon-display-expand.png)  the **[!UICONTROL Account Information]** section and use the **[!UICONTROL Comment]** field to enter notes about the account.

   The comments are not visible from the storefront.

1. When complete, click **[!UICONTROL Save]**.

   A confirmation email is sent to the company and company administrator that the company account is approved.

## Company status

| Status           | Description                                                                                                                                |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | The company is approved and can be managed from the storefront by the company administrator.                                               |
| [!UICONTROL Pending Approval] | A request to create a company account was submitted from the storefront, but is not yet reviewed.                                          |
| [!UICONTROL Rejected] | The request to create a company account was rejected by the store administrator.                                                           |
| [!UICONTROL Blocked]| The company account is no longer in good standing. The customer can access the account from the storefront, but cannot make purchases. |

{style="table-layout:auto"}
