---
title: Snippets
description: Reused visual elements to note feature or pages applying to a specific edition
---
# Snippets

## EE only feature {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce feature" src="../assets/adobe-logo.svg" width="20" height="20" /> Exclusive feature only in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Learn more</a>)</td></tr>
</table>

## B2B only feature {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="B2B for Adobe Commerce feature" src="../assets/b2b.svg" width="20" height="20" /> Exclusive feature available only with <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">B2B for Adobe Commerce</a></td></tr>
</table>

## CE only feature {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source feature" src="../assets/open-source.svg" width="20" height="20" /> Alternative method required for Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Learn more</a>)</td></tr>
</table>

## IMS admin authentication note {#ims-admin-note}

>[!NOTE]
>
>Adobe Commerce merchants who have an Adobe ID and want a streamlined login to Adobe Commerce and Adobe Business products can integrate Commerce Admin authentication with the Adobe IMS authentication workflow. After this integration is enabled for your Commerce store, each Admin user must use their Adobe credentials — not their Commerce account credentials — to log in. See [Integrating Adobe Commerce with Adobe IMS overview](/help/getting-started/adobe-ims-integration-overview.md).

## GTag APIs note {#gtag-api-note}

>[!NOTE]
>
>Starting with the 2.4.5 release, the Google services integration is updated to support use of the GTag APIs. GTag is a unified mechanism for integration with Google functionality for web pages and supports the newest capabilities and opportunities for tracking and managing content through Google Services. For more information, see the [Google Analytics developer documentation](https://developers.google.com/analytics/devguides/collection/gtagjs).

## URL rewrite automatic skip note {#url-rewrite-skip}

>[!NOTE]
>
>When automatic redirects are enabled and you save a category, all product and category rewrites are generated in real time and stored in rewrite tables by default. This could result in significant performance issues for categories with many assigned products. The solution is to change this default and skip the generation of category/products URL rewrites of products for category save. In this case, product rewrites are generated only for the canonical product URL. See [Automatic product redirects](/help/merchandising-promotions/url-redirect-product-automatic.md) for more information.

## URL rewrite parameters note {#url-rewrite-params}

>[!IMPORTANT]
>
>In the process of redirection, all GET parameters specified in the URL are removed for security reasons.

## New price rule {#new-price-rule}

>[!NOTE]
>
>Price rules are automatically processed with other system rules. Processing frequency depends on the [cron configuration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). When you create a new price rule, allow enough time for it to get into the system and then test the rule to make sure that it works correctly.

## Configuration settings {#config}

To access the store configurations settings, choose **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]** from the _Admin_ sidebar.

## Available documentation {#docs-links}

| Documentation resource | Description |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 Merchant Documentation](../landing/home.md) | Merchant-focused documentation for both Adobe Commerce and Magento Open Source |
| [Services for Adobe Commerce Documentation](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | Documentation to support a collection of services that help merchants integrate key components of their business with their store. |
| [Commerce on Cloud Infrastructure Guide](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Step-by-step procedures for deploying Adobe Commerce on a managed, automated hosting Cloud platform. |
| [Adobe Commerce 2.4 Operational Guides](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Systems documentation about the concepts, processes, tools, and best practices to develop, deploy, and maintain projects deployed on Adobe Commerce and Magento Open Source platforms.|
| [Adobe Commerce 2.4 Developer Documentation](https://developer.adobe.com/commerce/) | Developer-focused documentation used to build and customize Adobe Commerce or Magento Open Source |

{style="table-layout:auto"}
