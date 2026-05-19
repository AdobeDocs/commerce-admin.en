---
title: Disable the Commerce Admin Integration with Adobe ID
description: Follow this optional procedure for disabling the Adobe Commerce Admin integration with Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/KL6Cx3ymElo7ROx5SUJtlqtKivnw7-heqPWGksGP-pg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Disable the Commerce Admin Integration with Adobe ID

{{ee-feature}}

Merchants who have integrated their Commerce instance with the Adobe IMS authentication workflow may need to disable this optional integration. 

Commerce deployments revert to the default Commerce authentication workflow and password policies after the IMS integration is disabled. Only admin user workflows are affected when this integration is either enabled or disabled. 

See [Your Admin account](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) for an overview of the Commerce Admin sign-in.

## Step 1: Disable the integration 

You cannot disable this integration from the Admin. To disable the Adobe IMS integration with Commerce and return Commerce authentication to its default state, you must disable the integration from the command-line interface. 

To disable the integration:

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce displays the following message upon success:

```
Admin Adobe IMS integration is disabled.
```

## Step 2: Create or retrieve your Commerce password

After disabling the integration, admin users must use a Commerce password to log in to the Admin.

* Commerce admin users who remember their pre-existing Commerce password (that is, a Commerce password that was created before the IMS integration) can use it to log in to the Admin.

* Commerce admin users who either do not have a pre-existing Commerce password or have forgotten it must create a new password. To create a new password, admin users can use the [!UICONTROL Forgot your password?] feature on the Commerce login page to create a new password. See [Reset customer passwords](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerce will not accept an empty password field.

## After disabling the integration

The default Commerce authentication workflow resumes after IMS integration is disabled, and admin users are once again prompted for their password. 

Disabling the IMS integration deletes the credentials that were entered when the integration was enabled (`Organization ID`, `Client ID`, and `Client Secret` values) from the Commerce configuration files.
