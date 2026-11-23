---
title: AI Product Discovery Prerequisites
description: Review the requirements for Catalog enrichment and PDP enrichment, and install the shared enrichment extension on Adobe Commerce on cloud infrastructure or on-premises.
role: Admin, Developer
---
# Prerequisites

Before you use Catalog enrichment or PDP enrichment, confirm the requirements that apply to every deployment, then complete the setup for your Commerce platform.

## Requirements for all deployments {#all-deployments}

| Requirement | Applies to | Details |
| --- | --- | --- |
| Optimize at Edge | PDP enrichment | Required. Optimize at Edge delivers the enriched product data to AI agents. See the [Optimize at Edge guide](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn). |
| Log forwarding | Both workflows | Optional. Enables enrichment recommendations based on agentic traffic. Without it, you can still select products or product pages manually. See the [Log forwarding guide](https://experienceleague.adobe.com/en/docs/brand-visibility/using/log-forwarding/log-forwarding-overview). |
| Crawlable storefront | Catalog enrichment | Required for crawl-based recommendations. LLM-oriented and agentic bots must be able to access your product pages. |
| [!DNL Adobe Admin Console] access | Catalog enrichment | Required. During setup, [!DNL Adobe Commerce] checks whether your organization has signed the GenAI rider or opted out for the underlying AI services. |

<!--
TBD (SME): The Optimize at Edge guide is a Brand Visibility reference, not a Commerce setup guide. Add Commerce-specific Optimize at Edge setup instructions (this might be automated by GA).
TBD (SME): Confirm whether the Admin Console and GenAI rider check also applies to PDP enrichment.
-->

## Set up your Commerce platform {#set-up}

>[!BEGINTABS]

>[!TAB Commerce on Cloud infrastructure or on-premises]

For [!DNL Adobe Commerce] on cloud infrastructure or on-premises, you install the shared enrichment extension, which enables both Catalog enrichment and PDP enrichment.

**Before you begin:**

- [!DNL Adobe Commerce] 2.4.7 or later on PHP 8.3 or later. See [Release notes](release-notes.md).
- An [!DNL Adobe IMS] organization. If your organization does not have one, see the [Adobe IMS integration overview](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview). Catalog enrichment uses the IMS access token of the signed-in Admin user. Signing in with only a Commerce username and password does not provide this token.
- Command-line access to the Commerce application server, and permission to download packages from `repo.magento.com`.

**Install and verify:**

1. If neither [!DNL Live Search] nor [!DNL Product Recommendations] is enabled, add [!DNL Catalog Service] from your Commerce project directory:

   ```bash
   composer require magento/catalog-service --no-update
   composer update magento/catalog-service
   ```

   [!DNL Catalog Service] is installed automatically with [!DNL Live Search] and [!DNL Product Recommendations], so skip this step if either service is enabled.

1. If it is not already configured for another Commerce service, configure the [Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas) with API keys and a SaaS Data Space.

1. Add the shared enrichment extension:

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. Deploy the changes:

   - **Cloud infrastructure:** Commit and push the changes to `composer.json` and `composer.lock`.
   - **On-premises:** Upgrade the application and clear the cache:

     ```bash
     bin/magento setup:upgrade
     bin/magento cache:clean
     ```

1. In the Admin, go to **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**, and confirm that Commerce exports catalog data.

   The number of successfully sent product records should match the source records, with no failed or awaiting submissions. For failed records, review the error details, resolve the issue, and schedule a resync for the affected records.

1. Go to **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Management Dashboard]**, and confirm that the expected catalog data is available in [!DNL Catalog Service].

For status details and troubleshooting, see [Monitor data feed status](/help/systems/data-feed-sync-status.md#monitor-data-feed-status).

>[!TAB Adobe Commerce as a Cloud Service]

For [!DNL Adobe Commerce as a Cloud Service], installation of [!DNL Catalog Service], Catalog enrichment, and PDP enrichment are handled for you during account provisioning.

Complete the [requirements for all deployments](#all-deployments) that apply to the workflows you plan to use.

<!-- TBD (SME): Confirm whether merchants on Adobe Commerce as a Cloud Service should verify catalog data on the Data Management Dashboard, and whether the IMS and Admin Console requirements apply. -->

>[!ENDTABS]

## Next step {#next-step}

[Configure enrichment settings](settings.md) to connect your Commerce instance to AI Product Discovery.
