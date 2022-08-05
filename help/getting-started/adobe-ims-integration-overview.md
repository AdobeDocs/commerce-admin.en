---
title: Adobe Identity Management Service (IMS) Integration Overview
description: Introduces the optional integration of Adobe Commerce Admin login with Adobe IMS
---
# Adobe Identity Management Service (IMS) Integration Overview

{{ee-feature}}

Adobe Commerce Admin users who have an Adobe account can now use their Adobe ID to log in to Adobe Commerce. Adobe Identity Management Service (IMS) is Adobe’s OAuth 2.0-based identity management feature that supports authentication. Integrating the Commerce Admin authentication into Adobe Business Product’s IMS authentication workflow can streamline the authentication process for users who work with other Adobe products. This integration is optional and is enabled on a per-instance basis. Only Admin user workflows are affected when this integration is enabled. 

To implement this integration, see [Configure the Commerce Admin Integration with IMS](./adobe-ims-config.md).

## Changes to Admin workflows and interface after integration with IMS

When this integration is enabled, Commerce Admin users experience changes to the default Commerce Admin login and authentication workflow as they perform routine tasks in the Admin that require reauthentication, such as creating an Admin user. 2FA enforcement on the Adobe organization level is required for module enablement. The default Admin login and 2FA are disabled, and the _[!UICONTROL Sign In with Adobe ID]_ button replaces the default Admin sign in form. Entitlements are still managed from the Admin.

## Web API token generation with IMS credentials

Adobe Commerce Admin APIs are affected when Admin authentication with Adobe IMS is enabled in a Commerce instance. Admin users can no longer use the credentials issued by the Commerce instance. These are the credentials required to log in to the Admin and to obtain access tokens that services can use to make requests to the Admin REST and SOAP APIs. 

After Adobe IMS integration is enabled, Admin users must use [Adobe IMS OAuth tokens](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/) for Adobe Commerce API endpoints that require authentication. Client solutions obtain these dynamically for web API use. This authentication mechanism is enabled for REST and SOAP web API areas as part of configuring this integration.

## Important files

`adobeImsApi` - Declares the interfaces that support integration with Adobe IMS.

`adobeIms` - Implements all the business logic that is related to integration with Adobe IMS (preserved to prevent backward incompatibilities).

`adminAdobeIms` - Provides an implementation of the Admin login based on the `AdobeImsApi` module.

`adminadobe-ims.log` - Error log file.

## Enable the integration

This feature is installed with Adobe Commerce 2.4.5 but must be configured for use. It extends the `AdobeIms` module to support the module that enables authentication logic (`AdminAdobeIms`).

See [Configure the Commerce Admin Integration with Adobe IMS](./adobe-ims-config.md).
