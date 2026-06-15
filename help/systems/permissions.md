---
title: Admin permissions
description: Learn about Admin user accounts and how roles are used to grant access to store management functions.
exl-id: 54e4a322-4747-4472-b60b-cfe84c109f86
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
TQID: https://experienceleague.adobe.com/7xyouYohAbOKbwVCxZPamD-7gEiqGrqEAAg9FDm8z-U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Admin permissions

Adobe Commerce and Magento Open Source use roles and permissions to create different levels of access to the Admin. When your store is first set up, you receive a set of login credentials for the Administrator role that has full permissions. However, you can restrict the level of permissions on a "need to know" basis for other people who work on your site. For example, a member of design team can be given access to only the content design tools, but not to areas with customer and order information.

In addition, you can further restrict Admin access to only a specific site, or set of sites and their associated data. If you have multiple brands or business units with separate stores on the same Commerce installation, you can provide Admin access to each business unit but hide and protect their data from other Admin users.

When an Admin user's access is restricted to a specific website or store, those where they are not authorized are either not visible or appear grayed out. Only the sales and other data for permitted websites and stores is displayed for the user.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) By default, the system automatically logs (records) all actions performed by a user when they apply changes to a store. Admin actions can be reviewed in the [Action Logs Report](action-log-report.md). Configure logging in [Admin Actions Logging](action-log.md) in your store's advanced admin settings.

![Admin - all user accounts](./assets/users-all.png){width="700" zoomable="yes"}
