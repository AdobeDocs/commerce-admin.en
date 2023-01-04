---
title: Configure the Commerce Admin Integration with ID
description: Follow this optional procedure for integrating Adobe Commerce Admin user account logins with Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
---
# Configure the Commerce Admin Integration with Adobe ID

{{ee-feature}}

This integration supports Commerce merchants with Admin users who have an Adobe ID and who want to streamline login to Adobe Commerce and Adobe Business products. It is optional and is enabled on a per-instance basis. Only Admin user workflows are affected when enabled. 

## Prerequisites

* Adobe Commerce 2.4.5 or later
* An Adobe.com account with access to the [Adobe Admin Console](https://adminconsole.adobe.com/). 

The administrator who configures this integration needs the following credentials during module enablement:

* Organization ID (obtained from [Adobe Admin Console](https://adminconsole.adobe.com/)), which must be at least 24 characters in length. The authenticated user must belong to this IMS organization. [How to find your Organisation ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html)
* 2FA should be enforced on the Organization level in Adobe Admin Console to enable the module. Please check [the documentation](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification)
* Client ID
* Client secret
* Client ID and client secret are available after retrieving API keys in the [Adobe Developer Console](https://developer.adobe.com/).

Commerce Admin users must create an account with an Adobe ID to log in.

## General steps

* Get Adobe Org ID from the [Adobe Admin Console](https://adminconsole.adobe.com/)
* Generate a new project, IMS API keys, and secret from the [Adobe Developer Console](https://developer.adobe.com/)
* Enable the `AdminAdobeIms` module
* Configure Adobe Commerce users in the Adobe Admin Console.

A successful integration requires that all Adobe Commerce users have Admin user accounts with the same name and primary email address. If a matching Admin user account does not exist, a user with the required permissions (usually assigned the Administrator role) must manually [create the Admin user account](https://docs.magento.com/user-guide/system/permissions-users-all.html) with the same name and email.

## Configure the integration

After the followings steps are completed by an administrator or developer with system access, the [!UICONTROL Sign into Adobe Commerce with Adobe IMS] button is displayed in the Commerce Admin login page for all Admin users.

### Step 1: Get Adobe Org ID

You must belong to at least one IMS organization to enable this feature. If you have an Adobe ID, you belong to at least one Adobe organization by default. Log in to the [Adobe Admin Console](https://adminconsole.adobe.com/) to retrieve your organization ID. 

### Step 2: Generate a new project, IMS API keys, and secret

You must have an Adobe account to generate a new project and register it in IMS.

1. Log in to [Adobe Developer Console](https://developer.adobe.com/).
1. Go to the **[!UICONTROL Projects]** tab (adobe.io/projects) and click **[!UICONTROL Create a new project]**.
1. Click **[!UICONTROL Add API]** on the newly created Project page.
1. Select **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Select **[!UICONTROL Oauth 2.0 Web]**.
1. Specify the **[!UICONTROL Redirect URI]**: `https://<hostname>/<backend_frontname>/adobe_ims/oauth/callback/`
1. Specify the **[!UICONTROL Redirect URI pattern]**: `https://<hostname>/<backend_frontname>/adobe_ims/oauth/callback/.*`

   Escape any dots in the hostname by preceding the dots with `\\`. Adding a wildcard to the end of the URL supports the Adobe Commerce Admin secret key.

1. Click **[!UICONTROL Save configured API]**.
1. Copy the [!UICONTROL Client ID] and [!UICONTROL Client Secret] keys from the created project.

### Step 3: Enable the AdminAdobeIms module

The `AdminAdobeIms` module is responsible for the Adobe Commerce/Adobe IMS integration. After setting up the new project and copying your organization ID, client ID, and client secret, you can enable the `AdminAdobeIms` module.

Enter `bin/magento admin:adobe-ims enable`. You are prompted to enter the following parameters. Use the values that were generated during project creation.

* Organization ID
* Client ID
* Client secret
* 2FA enabled

Adobe Commerce displays a message to report that enablement succeeded or failed.

After successfully enabling this feature, you can transition other Adobe Commerce user accounts to Adobe IMS accounts. Adobe Commerce users must belong to the configured Adobe organization to log in using an Adobe ID.

### Step 4: Configure Adobe Commerce users in the Adobe Admin Console

After successfully enabling this feature, you can transition other Adobe Commerce user accounts to Adobe IMS accounts. Adobe Commerce users must belong to at least one Adobe organization to log in using an Adobe ID.

1. In the Admin Console, navigate to **[!UICONTROL Users]**  > **[!UICONTROL Users]**.
1. Click **[!UICONTROL Add User]**.
1. Enter the email address of the user.

   If applicable, the recommended ID Type is populated automatically. You can change this setting to one of the product IDs in the list, which is based on your organization's purchase plan.
   
   You can add up to ten users at one time. To add more, repeat the preceding steps after saving your changes.

1. Click **[!UICONTROL Save]**.

The user is added and displayed in the [!UICONTROL Users] list.
