---
title: '[!DNL Adobe Commerce Marketplace]'
description: Learn about the [!DNL Commerce Marketplace], which offers merchants a curated selection of solutions, and provides qualified developers the tools, platform, and prime location to build a thriving business.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
---
# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] is the application store that offers merchants a curated selection of solutions, and provides qualified developers the tools, platform, and prime location to build a thriving business. [!DNL Commerce Marketplace] offers a selection of extensions that are available for free, and others that are for sale. Purchases can be paid by credit card or [PayPal][2].

All extensions available on [!DNL Commerce Marketplace] have passed an extensive review. The [Extension Quality Program][3] (EQP) combines [!DNL Commerce] expertise, development guidelines, and verification tools to ensure that all extensions on Commerce Marketplace meet coding standards and best practices. The review process includes both an automated check and manual QA review. During the process, the structure and code of each extension is examined and tested for evidence of virus/malware infection, and any indication of plagiarism. The review includes a deep technical examination and sanity check conducted by a [!DNL Commerce] engineer, with a focus on documentation, coding structure, performance, scalability, security, and compatibility with the [!DNL Commerce] core.

Although you can purchase extensions from other sources, only the extensions that are available on [!DNL Commerce Marketplace] are verified through extensive technical and marketing review within the Extension Quality Program.

## App resources

Developers have traditionally used PHP to create in-process extensions to add features, functionality, services, and integrations to Adobe Commerce. By creating apps with out-of-process extensibility, as opposed to extensions, you can avoid compatibility issues.

The following resources provide a starting point for new adopters to familiarize themselves with apps:

### Commerce resources

-  [Setting up I/O Events for Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
-  [Configuring Events for Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
-  [Setting up Admin UI SDK](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
-  [Converting an extension to an app](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder resources

-  [Commerce App Builder Overview](https://developer.adobe.com/commerce/extensibility/app-development/)
-  [Setting up API Mesh for Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
-  [Deploying App Builder apps](https://developer.adobe.com/app-builder/docs/guides/deployment/)
-  [CI/CD for App Builder apps](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
-  Getting Started with App Builder/Developer Console
   -  [Getting started with App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   -  [Understanding Projects and Workspaces](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] credentials

Before you can install an extension purchased from [!DNL Commerce Marketplace], sign in to your [!DNL Commerce] account and verify that you have an active access key. You can sign in to your [!DNL Commerce] account from the header of [[!DNL Marketplace]][1] or [Magento.com][6].

Your access key is a set of public and private keys that is used to synchronize your [!DNL Commerce] installation with your [!DNL Commerce] account and verify your credentials. After your account is synchronized, you must enter your private key each time you install an extension or module from Commerce Marketplace or upgrade your [!DNL Commerce] installation.

You can create multiple access keys for different purposes and enable or disable them as needed. However, you must use the same access key that was used to install the [!DNL Commerce] software. For example, you cannot use a Magento Open Source access key to update or upgrade Adobe Commerce, or conversely. You also cannot use an access key that belongs to another user or one that is from a [shared account](commerce-account-share.md).

### Create an access key

1. Sign in to your [!DNL Commerce] account.

1. On the _[!UICONTROL My Account]_ page, choose the **[!UICONTROL Marketplace]** tab.

1. In the upper-right corner next to your name, click the down arrow and choose **[!UICONTROL My Profile]**.

    ![Your [!DNL Marketplace] profile](./assets/marketplace-profile.png){width="600"}

1. On the _[!UICONTROL Marketplace]_ tab under _[!UICONTROL My Products]_, click **[!UICONTROL Access Keys]**, and then do either of the following:

    - Check to see if you already have a set of access keys for your Marketplace purchases. You can create multiple sets of access keys for different purposes.

    ![Access Keys](./assets/access-keys.png){width="600"}

    - Click **[!UICONTROL Create a New Access Key]**. Enter a name for the new key pair and click **[!UICONTROL OK]**. Valid characters include upper- and lowercase characters and hyphens instead of spaces.

1. When complete, click **[!UICONTROL OK]**.

    Your new access key is enabled and appears in the list.

    Notice the _Copy_ link after each public and private key. In the next step, you will copy and paste these values to synchronize your store with Commerce Marketplace.

## Installation Process

>[!IMPORTANT]
>
>Starting with Adobe Commerce and Magento Open Source 2.4.0, the Web Setup Wizard is removed, and you must use the command line to [install](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) or [upgrade](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) your instance. This requirement also includes [modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) and [extensions](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

The installation process for [!DNL Marketplace] purchases is different for _on-premise_ installations of Commerce than for installations hosted on [the Adobe Cloud Architecture][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Support

If you need help with installing or with using an extension, look first in the documentation that accompanies the extension. If you can't find the answer to your question, use the contact information in the extension listing to contact the developer directly. If what you purchase on Marketplace does not meet your needs, you can [request a refund](#refund-requests) within 25 days from the date of purchase. Adobe reviews all refund requests and (if approved) issues the appropriate refund. For issues related to Commerce Marketplace:

Method 1: Go to the [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/), navigate to the bottom of the page and click [!UICONTROL Contact Us] which will open a form to submit a ticket. 

Method 2: [Email Support](mailto:commercemarketplacesupport@adobe.com).

### Checkout issues

The address fields in your account profile must be completed for verification purposes in the Marketplace purchasing system.

1. Add the address fields in your Marketplace account profile.
1. Save the updated profile.
1. Continue with your checkout.

### Log in issues

Log in issues are typically related to a mismatch between your MAGEID and email address in the account database. Contact Marketplace Support for assistance.

>[!INFO]
>
>App and extension purchases cannot be [transfered](#purchase-transfers) to a new account.

### Open source questions

The Marketplace Support team resolves issues related to the [commercemarketplace.adobe.com/](https://commercemarketplace.adobe.com/) and [commercedeveloper.adobe.com/](https://commercedeveloper.adobe.com/) sites only. Please direct questions about Magento Open Source to the [Community Forum](https://community.magento.com/) or [contact a partner](https://business.adobe.com/products/magento/partners.html) who can assist with Magento Open Source.

### Refund requests

To request a refund for a Marketplace purchase, log in to your account and follow these steps:

1. Click [!UICONTROL **My Profile**] > [!UICONTROL **Purchase History**].
1. Locate the purchase and click [!UICONTROL **Request a Refund**].
1. Complete the refund order form.

Marketplace Support will request information after the refund request is generated. The refund option is available for 25 days after date-of-purchase. See the [Marketplace Customer Agreement](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Order invoices

You can download order invoices from the [!UICONTROL **Purchase History**] in your Marketplace account. The invoice does not supply the VAT or address of the seller because it is not a Marketplace requirement at this time.

To download an order invoice for a Marketplace purchase, log in to your Marketplace account and follow these steps:

1. Click [!UICONTROL **My Profile**] > [!UICONTROL **Purchase History**].
1. Locate the purchase.
1. Click the printer icon in the top-right corner of the order.

### Purchase transfers

The Marketplace Support team does not have the ability to transfer purchases to a different account. You must purchase all apps and extensions under the primary Commerce account to avoid installation and deployment issues. Adobe Commerce is entitled to one unique identifier. Since Composer is used for installation, only one set of [access keys](#create-an-access-key) tied to the primary account can be used. The only available solution is to [request a refund](#refund-requests) from the Marketplace purchasing account (if allowed by the Adobe Commerce refund policy).

You can [share](commerce-account-share.md) a Commerce instance through the primary account. Shared access grants special permissions to a subordinate account from a primary account. The shared access point is generated from the primary account. The primary account can be the Commerce entitled account, the main merchant account, or an account shared within an organization.

These special permissions grant the same level of access on Adobe Commerce as the primary, however it does not carry over to the Adobe Commerce Marketplace or Developer Portal. This means that buying an extension from a subordinate account in the Marketplace cannot be shared with the primary account. Shared access is a one-way street (primary account to subordinate). It does not work when a subordinate account is trying to share back to the primary.

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[6]: https://business.adobe.com/products/magento/magento-commerce.html
