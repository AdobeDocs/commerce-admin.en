---
title: Disable the Commerce Admin Integration with Adobe ID
description: Follow this optional procedure for disabling the Adobe Commerce Admin integration with Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
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
