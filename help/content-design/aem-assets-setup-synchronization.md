---
title: Set up the synchronization service
description: "Learn how to connect your Adobe Commerce and Experience Manager Assets projects with the Assets Rule Engine Service to enable asset synchronization between these two systems."
feature: CMS, Media
---

# Set up the synchronization service

The Asset Rules Engine Service (ARES) is a multi-tenant service that integrates AEM Assets with Adobe Commerce. This service synchronizes assets between Adobe Commerce and Experience Manager. The ARES service automatically matches assets in AEM to products in Adobe Commerce based on SKU or other key attributes. It also ensures that the latest product assets and variations are always available on the ecommerce site.

To set up the service, you need to register your tenant ID using the ARES GraphQL API and select the matching strategy for synchronizing assets.


## Register a tenant

>[!BEGINSHADEBOX]

**Prerequisite**

- A configured production environment is required for an Experience Manager Assets instance to connect with the Commerce tenant. See [Configure Experience Manager Assets](aem-assets-configure-aem.md)
- Program and environment identifier from the AEM asset organization owning the repository of assets. AEM project and environment ID—Get these credentials from the AEM URL `https://author-p<project-id>-e<environment-id>-cmstg.adobeaemcloud.com/aem/start.html`.
- Credentials to authenticate the authentication
  - projectId: SaaS project Id (from Commerce Services Connector)
  - commerce: Commerce credentials

>[!ENDSHADEBOX]

You complete tenant registration by submitting a registration request to the Assets Rule Engine Service using a GraphQL client. The request includes credentials and project identifiers required to establish the connections between the service, the Commerce project, and the Experience Manager Assets project.

Use a GraphQL client to send a POST request to the API endpoint.

**Required headers**

Specify the following HTTP headers for the request:

- `x-api-key`: API Key from your Magento account
- `magento-environment-Id`: SaaS identifier
- `x-gw-signature`: JWT Token associated with the MAGEID

**Request:**


**Syntax**

```graphql
mutation registerTenant($tenantInput: TenantInput!) {
   registerTenant(tenantInput: $tenantInput) {
      tenantId
      userErrors {
         message
         path
      }
    }
}
```

## Example usage


### Parameters

enabled: Enable/disable sync.
threshold (0-100): Not in use. Optional. A minimum % of accuracy is required to FULL sync an existing catalog in Commerce with its assets in AEM assets.
projectId: SaaS project Id (from Commerce Services Connector)
aem: Program and environment identifier from the AEM asset organization owning the repository of assets.
commerce: Commerce credentials
version and extensionVersion are optional and could be omitted.
ruleType: 2 different rules available: matchBySkuRule and externalMatcher

### Enable the Experience Manager Assets integration

After you set up synchronization services, the last step of the onboarding process is to  enable the Experience Manager Assets integration in the Admin.

1. Enable the integration.

   1. Go to **Stores** > Settings > **Configuration** > **Catalog**.

   1. Open the Catalog configuration by selecting **[!UICONTROL Catalog]**.

   1. Expand **[!UICONTROL AEM Assets integration]**.

   1. Set **[!UICONTROL Integration enabled]** to `yes`.

      ![AEM Assets Integration for Commerce Admin configuration](assets/aem-integration-admin-enable.png){width="600" zoomable="yes"}



