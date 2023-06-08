---
title: Disable the Commerce Admin Integration with Adobe ID
description: Follow this optional procedure for disabling the Adobe Commerce Admin integration with Adobe IMS.
---
# Disable the Commerce Admin Integration with Adobe ID

{{ee-feature}}

Commerce merchants who have integrated their Commerce instance with the Adobe IMS authentication workflow may need to disable this optional integration. 

Commerce deployments revert to the Commerce authentication workflow and password policies after the IMS integration is disabled. Only Admin user workflows are affected when this integration is either enabled or disabled. 

See [Your Admin account](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) for an overview of the Commerce Admin sign-in.


## Step 1: Disable the AdminAdobeIms module

You cannot disable this integration from the Admin. To disable the Adobe IMS integration with Commerce and return Commerce authentication to its default state, you must disable the `AdminAdobeIms` module. 

To disable this module, enter

`bin/magento admin:adobe-ims:disable`

Adobe Commerce displays this message upon success: `Admin Adobe IMS integration is disabled`.

See [Enable or disable modules](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) for information on working with modules in Commerce deployments.

## Step 2: Create or retrieve your Commerce password

After the `AdminAdobeIms` module is disabled, admin users must use a Commerce password to log into Commerce.

* Commerce admin users who remember their pre-existing Commerce password (that is, a Commerce password that was created before the IMS integration) can use it to log in to Commerce.

* Commerce admin users who either do not have a pre-existing Commerce password or have forgotten it must create a new password. To create a new password, admin users can use the Forgot your password? feature on the Commerce login page to create a new password. See [Reset customer passwords](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerce will not accept an empty password field.

## After disabling the AdminAdobeIms module

The default Commerce authentication workflow resumes after module disablement, and admin users are once again prompted for their password before 

The disablement process deletes the credentials that were entered during module enablement (`Organization ID`, `Client ID`, and `Client Secret` values) from the Commerce configuration files.


