---
title: Snippets
description: Reused notes and visual elements to note a feature or page applying to a specific edition
---
# Snippets

## EE only feature {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce feature" src="../assets/adobe-logo.svg" width="20" height="20" /> Exclusive feature only in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Learn more</a>)</td></tr>
</table>

## B2B only feature {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B feature" src="../assets/b2b.svg" width="20" height="20" /> Exclusive feature available only with <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">Adobe Commerce B2B</a></td></tr>
</table>

## CE only feature {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source feature" src="../assets/open-source.svg" width="20" height="20" /> Alternative method is required for Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Learn more</a>)</td></tr>
</table>

## IMS admin authentication note {#ims-admin-note}

>[!NOTE]
>
>Adobe Commerce merchants who have an Adobe ID and want a streamlined login to Adobe Commerce and Adobe Business products can integrate Commerce Admin authentication with the Adobe IMS authentication workflow. After this integration is enabled for your Commerce store, each Admin user must use their Adobe credentials — not their Commerce account credentials — to log in. See [Integrating Adobe Commerce with Adobe IMS overview](/help/getting-started/adobe-ims-integration-overview.md).

## GTag APIs note {#gtag-api-note}

>[!NOTE]
>
>Starting with the 2.4.5 release, the Google services integration is updated to support use of the GTag APIs. GTag is a unified mechanism for integration with Google functionality for web pages and supports the newest capabilities and opportunities for tracking and managing content through Google Services.

## URL rewrite automatic skip note {#url-rewrite-skip}

>[!NOTE]
>
>When automatic redirects are enabled and you save a category, all product and category rewrites are generated in real time and stored in rewrite tables by default. This process could result in significant performance issues for categories with many assigned products. The solution is to change this default and skip the generation of category/products URL rewrites of products for category save. In this case, product rewrites are generated only for the canonical product URL. See [Automatic product redirects](/help/merchandising-promotions/url-redirect-product-automatic.md) for more information.

## URL rewrite parameters note {#url-rewrite-params}

>[!IMPORTANT]
>
>In the process of redirection, all GET parameters specified in the URL are removed for security reasons.

## New price rule {#new-price-rule}

>[!NOTE]
>
>Price rules are automatically processed with other system rules. Processing frequency depends on the [cron configuration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). When you create a price rule, allow enough time for it to get into the system. WHen you are sure it is in the system, test the rule.

## Configuration settings {#config}

To access the store configuration settings, choose **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]** from the _Admin_ sidebar.

## UPS API deprecation {#ups-api}

>[!IMPORTANT]
>
>Beginning June 2024, Adobe Commerce merchants can no longer transact with the current UPS integration. This is because the United Parcel Service (UPS) APIs used by the native Adobe Commerce integration do not currently support the required OAuth 2.0 security model. To enable the integration, [create an application on the UPS developer platform](https://developer.ups.com/get-started) to obtain the credentials required for OAuth 2.0. Use the new credentials as the `username` and `password` in the Commerce UPS Shipping configuration. To learn more about the security model change, see [Developer Portal Access Key Migration Guide_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>Merchants should [apply a quality patch update](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) to their store to migrate from the SOAP API to the RESTful API, which supports OAuth 2.0 authentication protocols.


## Available documentation {#docs-links}

| Documentation resource | Description |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 Admin User Guides](../landing/home.md) | Documentation and resources for merchants working in the Admin. |
| [Services for Adobe Commerce Documentation](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html) | Documentation to support a collection of merchandising services that help merchants integrate key components of their business with their store. |
| [Commerce on Cloud Infrastructure Guide](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Step-by-step procedures for deploying Adobe Commerce on a managed, automated hosting cloud platform. |
| [Adobe Commerce 2.4 Operational Guides](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Systems documentation about the concepts, processes, tools, and best practices to develop, deploy, and maintain Adobe Commerce on Cloud and on-premises projects. |
| [Adobe Commerce 2.4 Developer Documentation](https://developer.adobe.com/commerce/docs) | Developer-focused documentation used to customize Adobe Commerce and integrate with third-party systems. |

{style="table-layout:auto"}

## B2B compatibility {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B version 1.4.2+ is compatible with PHP 8.2. If you upgrade the Commerce instance to version 2.4.7+, ensure that the instance uses PHP version 8.2 to maintain compatibility with the Adobe Commerce B2B release. Additionally, the B2B 1.4.2+ release does not support the [GraphQL Application Server](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/concepts/application-server).
