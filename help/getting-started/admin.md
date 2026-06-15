---
title: What is the Admin?
description: Learn about the [!DNL Commerce] Admin, the place where merchants set up products and promotions, manage orders, and perform other administrative tasks.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
TQID: https://experienceleague.adobe.com/A0DuYohA907-EHXQ6fyy2Sz83Y6cFZ7PDY5SmtBa14Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
    internal-label: Accessibility
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# What is the Admin?

Your store _Admin_ is the password-protected back office where you, as the merchant, set up products and promotions, manage orders, and perform other administrative tasks. All basic configuration tasks and store management operations are performed from the _Admin_.

For additional security, the _Admin_ login is protected by [two-factor authentication](../systems/security-two-factor-authentication.md), and can be configured to require a [CAPTCHA](../systems/security-captcha.md). To learn more, go to [Configuring Admin Security](../systems/security-admin.md).

![Admin sidebar and dashboard](./assets/admin-dashboard.png){width="700" zoomable="yes"}

Your initial [sign-in](admin-signin.md) credentials were set up during Adobe Commerce or Magento Open Source installation. If you forget your password, a temporary password can be sent to the email address that is associated with the account. To increase security, configure your store to require a case-sensitive user name and strong password.

In addition to the default Admin user account, your business can create as many [additional accounts](../systems/permissions-users-all.md) that you require to manage the store and support customer accounts. Each account can be associated with a specific [role](../systems/permissions-user-roles.md) and level of access, based on business _need to know_. The email address that is associated with each Admin user account must be unique.

{{ims-admin-note}}

## Usage data collection

The first time you log in to the _Admin_, you are asked to grant Adobe permission to collect usage data for all Admin users. By allowing Admin usage data collection, you help Adobe improve the experience of using the Adobe Commerce Admin, and related products and services.

![Allow admin usage data collection](./assets/admin-usage-data.png){width="600"}

Individual users are not identified in usage data. Yours data collection setting can be changed at any time from the [Admin Usage](../configuration-reference/advanced/admin.md#admin-usage) configuration.

For Adobe Commerce, allowing data collection also enables _In-Product Guidance_, which is designed to bring interactive content to the _Admin_. It provides help, tool tips, walk-through guides, onboarding information, feature announcements, and more.
