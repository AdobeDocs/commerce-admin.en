---
title: Configure the Commerce Admin Integration with ID
description: Follow this optional procedure for integrating Adobe Commerce Admin user account logins with Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
---
# Configure the Commerce Admin Integration with Adobe ID

{{ee-feature}}

This integration supports Commerce merchants with Admin users who have an Adobe ID and who want to streamline login to Adobe Commerce and Adobe Business products. It is optional and is enabled on a per-instance basis. Only Admin user workflows are affected when enabled. 

>[!IMPORTANT]
>
>Admin users should save their Commerce Admin credentials (username and password) and 2FA credentials before enabling this integration. These credentials are needed if the IMS integration is disabled.

## Prerequisites

* Adobe Commerce 2.4.5 or later
* An Adobe.com account with access to the [Adobe Admin Console](https://adminconsole.adobe.com/).

The administrator who configures this integration needs the following credentials during module enablement:

* Organization ID (obtained from [Adobe Admin Console](https://adminconsole.adobe.com/)), which must be at least 24 characters in length. The authenticated user must belong to this IMS organization. For information about finding your organization ID, see [Organizations in Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA should be enforced on the Organization level in Adobe Admin Console to enable the module. Check [Authentication setings](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* Client ID
* Client secret
* Client ID and client secret are available after retrieving API keys from the [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Commerce Admin users must create an account with an Adobe ID to log in.

## General steps

* Get Adobe Org ID from the [Adobe Admin Console](https://adminconsole.adobe.com/)
* Generate a new project, IMS API keys, and secret from the [Adobe Developer Console](https://developer.adobe.com/)
* Configure Adobe Commerce users in the Adobe Admin Console
* Enable the `AdminAdobeIms` module.

A successful integration requires that all Adobe Commerce users have Admin user accounts with the same name and primary email address. If a matching Admin user account does not exist, a user with the required permissions (typically assigned the Administrator role) must manually [create the Admin user account](../systems/permissions-users-all.md#create-a-user) with the same name and email.

## Configure the integration

After the followings steps are completed by an administrator or developer with system access, the _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_ button is displayed in the Commerce Admin login page for all Admin users.

### Step 1: Get Adobe Org ID

Membership in at least one IMS organization is required to enable this feature. If you have an Adobe ID, you belong to at least one Adobe organization by default. Log in to the [Adobe Admin Console](https://adminconsole.adobe.com/) to retrieve your organization ID. 

### Step 2: Generate a new project, IMS API keys, and secret

To create projects for an organization, the Adobe Admin account for the organization must have the system administrator or developer role. See the [Developer Console Guide](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Log in to [Adobe Developer Console](https://developer.adobe.com/).
1. Go to the **[!UICONTROL Projects]** tab (adobe.io/projects) and click **[!UICONTROL Create a new project]**.
1. Click **[!UICONTROL Add API]** on the newly created Project page.
1. Select **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Select **[!UICONTROL Oauth 2.0 Web]**.
1. Specify the **[!UICONTROL Redirect URI]**: `https://<commerce_base_url>/`
1. Specify the **[!UICONTROL Redirect URI pattern]**: `https://<commerce_base_url>/.*`

   Escape any dots in the hostname by preceding the dots with `\\`. Adding a wildcard to the end of the URL supports the Adobe Commerce Admin secret key.

1. Click **[!UICONTROL Save configured API]**.
1. Copy the [!UICONTROL Client ID] and [!UICONTROL Client Secret] keys from the created project.

### Step 3: Configure Adobe Commerce users in the Adobe Admin Console

Before enabling the integration, verify that each Adobe Commerce Admin user account has a corresponding Adobe IMS account. Adobe Commerce users must belong to a specific Adobe organization to log in using an Adobe ID.

>[!TIP]
>
>You can create multiple user accounts by uploading the user information from a CSV file. See [Manage multiple users](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. In the [Adobe Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html), navigate to **[!UICONTROL Users]**  > **[!UICONTROL Users]**.

1. Click **[!UICONTROL Add User]**.

1. Enter the email address of the user.

   If applicable, the recommended ID Type is populated automatically. You can change this setting to one of the product IDs in the list, which is based on your organization's purchase plan.

   You can add up to ten users at one time. To add more, repeat the preceding steps after saving your changes.

1. Click **[!UICONTROL Save]**.

The user is added and displayed in the [!UICONTROL Users] list.

### Step 4: Enable the AdminAdobeIms module

The `AdminAdobeIms` module is responsible for the Adobe Commerce/Adobe IMS integration. After setting up the new project and copying your organization ID, client ID, and client secret, you can enable the `AdminAdobeIms` module.

Enter `bin/magento admin:adobe-ims:enable`. You are prompted to enter the following parameters. Use the values that were generated during project creation.

* Organization ID
* Client ID
* Client secret
* 2FA enabled

Adobe Commerce displays a message that indicates whether enablement succeeded or failed.

After successfully enabling this feature, you can transition other Adobe Commerce user accounts to Adobe IMS accounts. Adobe Commerce users must belong to the configured Adobe organization to log in using an Adobe ID.
