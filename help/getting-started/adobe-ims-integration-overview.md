---
title: Adobe Identity Management Service (IMS) integration overview
description: Introduces the optional integration of Adobe Commerce Admin login with Adobe IMS
exl-id: 106d731c-a541-4a19-a38c-221e80740508
---
# Adobe Identity Management Service (IMS) integration overview

{{ee-feature}}

Adobe Commerce Admin users who have an Adobe account can now use their Adobe ID to log in to Adobe Commerce. Adobe Identity Management Service (IMS) is Adobe's OAuth 2.0-based identity management feature that supports authentication. Integrating the Commerce Admin authentication into Adobe Business Product's IMS authentication workflow can streamline the authentication process for users who work with other Adobe products. This integration is optional and is enabled on a per-instance basis. Only Admin user workflows are affected when this integration is enabled. 

The modules that are required for the Commerce Admin IMS integration are packaged in  `adobe-ims-metapackage`, which is bundled with Adobe Commerce core releases. 

To implement this integration, see [Configure the Commerce Admin Integration with IMS](./adobe-ims-config.md).

## Changes to Admin workflows and interface after integration with IMS

When this integration is enabled, Commerce Admin users experience changes to the default Commerce Admin login and authentication workflow as they perform routine tasks in the Admin that require reauthentication, such as creating an Admin user. Two-factor authentication (2FA) enforcement on the Adobe organization level is required for module enablement. The default Admin login and 2FA are disabled, and the _[!UICONTROL Sign In with Adobe ID]_ button replaces the default Admin sign in form. Entitlements are still managed from the Admin.

## How Admin integration with IMS affects Commerce passwords

Commerce deployments that have been integrated with Adobe IMS require an Adobe ID account under an Adobe org that is configured during the Commerce Admin integration with IMS. Commerce passwords and user names for admin users are no longer used for authentication. As a result, admin users are no longer prompted by Commerce for a password after this integration has been enabled.

Certain backend components that are involved in user authentication still require a non-null password. To meet this requirement, Commerce creates random passwords for newly created admin users in the `admin_user` table.


## Web API token generation with IMS credentials

Commerce Admin APIs are affected when Admin authentication with Adobe IMS is enabled in a Commerce instance. Admin users can no longer use the credentials issued by the Commerce instance. These are the credentials required to log in to the Admin and to obtain access tokens that services can use to make requests to the Admin REST and SOAP APIs. 

After the Adobe IMS integration is enabled, admin users must use [Adobe IMS OAuth tokens](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/) for Adobe Commerce API endpoints that require authentication. Client solutions obtain the tokens dynamically for web API use. This authentication mechanism is enabled for REST and SOAP web API areas as part of configuring this integration.

See [Token-based authentication](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) for an overview of how web APIs use Commerce access tokens, including IMS access tokens.

## Important files

`adminAdobeIms` - Provides an implementation of the Admin login based on the `AdobeImsApi` module.

`admin_adobe_ims_webapi` -  Maintains a record of all validated access tokens. When a token is validated or invalidated, a record of its status is preserved in this table.

`adobeIms` - Implements all the business logic that is related to integration with Adobe IMS (preserved to prevent backward incompatibilities).

`adobeImsApi` - Declares the interfaces that support integration with Adobe IMS.

`adminadobe-ims.log` - Error log file.

## Enable the integration

This feature is installed with Adobe Commerce 2.4.5 and higher, but must be configured for use. It extends the `AdobeIms` module to support the module that enables authentication logic (`AdminAdobeIms`).

For more information about enabling the integration, see [Configure the Commerce Admin Integration with Adobe IMS](./adobe-ims-config.md).
