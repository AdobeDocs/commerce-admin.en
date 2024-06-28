---
title: Set up the synchronization service
description: "Learn how to connect your Adobe Commerce and Experience Manager Assets projects with the Assets Rule Engine Service to enable asset synchronization between these two systems."
feature: CMS, Media
---

# Set up the synchronization service

The Asset Rules Engine Service (ARES) is a multi-tenant service that integrates AEM Assets with Adobe Commerce. This service synchronizes assets between Adobe Commerce and Experience Manager. The ARES service automatically matches assets in AEM to products in Adobe Commerce based on SKU or other key attributes. It also ensures that the latest product assets and variations are always available on the ecommerce site.

To set up the service, you need to register your tenant ID using the ARES GraphQL API and select the matching rule for synchronizing assets.

## Choose a matching strategy

The AEM Assets Integration for Commerce supports two matching strategies for synchronizing assets between Adobe Commerce and AEM Assets.

- **MatchBySku**-This is the default matching rule that matches assets based on the Stock Keeping Unit (SKU) of the product. The SKU is a unique identifier for each product, and this rule ensures that images and other assets are correctly associated with their corresponding products by matching the SKU in the asset metadata with the SKU in the Commerce catalog.

- **ExternalMatcher**–This matching rule is for more complex scenarios or specific business requirements that require custom matching logic. To use this rule, you must have custom code implemented in Adobe Developer App Builder that defines how assets are matched with products. <!--Add link to separate topic with more info-->.

For initial onboarding, use the `MatchBySku` strategy. If needed, you can change the matching strategy later.

## Register a tenant

>[!BEGINSHADEBOX]

**Prerequisite**

- [AEM Assets project has been configured with Commerce metadata required for mapping assets](aem-assets-configure-aem.md).

- [Install and configure the Experience Manager Assets Integration in Adobe Commerce](aem-assets-configure-commerce.md).

>[!ENDSHADEBOX]

## Gather credentials

You need the following credentials to authenticate and connect your Commerce project environment and AEM Assets project environment with Commerce SaaS services.

| Required Data | Source | Where to find it|
| ---------- | ------ | ------------- |
| API Key from Magento account | Commerce | Provide the public API key associated with the 
| Commerce SaaS Identifiers <ul><li>`magento-environment-Id`</li><li>`Project ID`</li></ul> | Commerce Admin | These values identify the SaaS data space environment and project to connect to. Values come from the [Commerce Services Connector SaaS Identifier configuration](aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
|AEM `programId`<br>`environmentId` | [AEM Assets Authoring environment](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) | Open AEM Sites page, and select Assets.  Copy the project and environment IDs from the URL: `https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|
| baseURL | Commerce storefront | The [base URL](../stores-purchase/store-urls.md) for your Commerce storefront.|
| OAuth credentials for API access | Commerce Admin | You can find these credentials in the Commerce [configuration settings for the Assets integration](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).|

## Register tenant

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

**Example usage**

Register a tenant and select `matchBySku` rule to map assets between Adobe Commerce and the AEM Assets project.

**Request:**

```graphql
   {
      "tenantInput": {
         "enabled": true,
         "projectId": "8231afb6-90cd-65e8-84ba-d9abac0f94e6",
         "aem": {
               "programId": "11111",
               "environmentId": "222222"
         },
         "commerce": {
               "baseUrl": "https://assets-rp3st7y-efo2rc3kezxte.eu-4.magentosite.cloud",
               "credentials": {
                  "consumerKey": "***",
                  "consumerSecret": "***",
                  "accessToken": "***",
                  "accessTokenSecret": "***"
               }
         },
         "ruleType": "matchBySKU",
         "matchBySkuRule": {
               "metadataField": "commerce:skus"
         }
       }
   }
```

**Response**

```graphql

Add response here
```

### Input Fields

#### TenantInput

| Field | Data Type | Description |
| ----- | --------- | ----------- |
|`aem` | [AemInput](#aeminput) | Identifies the AEM Assets instance within the AEM Cloud Service where you will store the Commerce Assets. |
|`commerce` | [CommerceInput](#commerceinput) | Provides Commerce project information and credentials for API access |
|`enabled`| boolean | Enable or disable the assets sync between Adobe Commerce and AEM Assets.|
|`projectId` | String! | The SaaS Project ID from the [Commerce Services Connector SaaS Identifier configuration](aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
|`ruletype` | String! | Specifies the matching rule for synchronizing assets between Adobe Commerce and AEM Assets. Specify either `matchBySkuRule` or `externalMatcher`. |
|`threshold` | integer | Not in use. Optional. A minimum % of accuracy is required to FULL sync an existing catalog in Commerce with its assets in AEM assets. |
|`externalMatcher`| ExternalMatcherInput |            |
|`matchbySkuRule` | MatchBySkuRuleInput | Provides the |

#### AemInput

Identifies the AEM Assets instance where you will store the Commerce Assets. You can get this information from the Cloud Manager My Programs view, or from the content authoring URL.

| Field | Data Type | Description |
| ----- | --------- | ----------- |
|`programId` | String! | Unique identifier for your project within AEM Cloud Service |
|`environmentId`| String! | Id for the project environment you are using, such as Production, Staging, or Development |

#### CommerceInput

Provides the OAuth authentication credentials for API access to the Commerce Catalog. You can find these credentials in the Commerce [configuration settings for the Assets integration](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).


| Field | Data Type | Description |
| ----- | --------- | ----------- |
| `baseUrl` | String | The [base URL](../stores-purchase/store-urls.md) for your Commerce storefront.|
| `credentials` | [CommerceCredentialsInput](#commercecredentialsinput)! | Specifies the credentials to access the Commerce instance.|
| `extensionVersion` | String | Optional. The version of the AEM Assets Integration for Commerce extension installed on the Commerce instance.|
| `version` | String | Optional. The version of the Commerce application currently installed.|

#### CommerceCredentialsInput

Provides the OAuth credentials for API access to the Commerce Catalog. You can find these credentials in the Commerce [configuration settings for the Assets integration](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).


| Field | Data Type | Description |
| ----- | --------- | ----------- |
| `accessToken` | String! | The access token generated for the Assets integration. |
| `accessTokenSecret` | String! |The access token secret generated for the Assets integration.|
| `consumerKey` | String! | The consumer key generated for the Assets integration. |
| `consumerSecret` | String! | The consumer secret generated for the Assets integration.|

#### ExternalMatcherInput

| Field | Data Type | Description |
| ----- | --------- | ----------- |
| assetToProductUrl | String! | <!--Add field description--> |
| productToAssetUrl | String! | <!--Add field description--> |
| credentials | [ExternalMatcherCredentialsInput](#externalmatchercredentials)! | Credentials for accessing the App builder project for the AEM Assets integration for Commerce. |

#### ExternalMatcherCredentials

| Field | Data Type | Description |
| ----- | --------- | ----------- |
|`oauthServerUrl` | String! |    |
|`clientId` | String! |      |
|`clientSecret` | String! |    |
|`imsOrgId` | String! | The IMS or |

#### MatchBySkuRuleInput

| Field | Data Type | Description |
| ----- | --------- | ----------- |
| metadataField | String! | Specify the assets metadata field to use for matching. Use `commerce:skus` |

## Enable the Experience Manager Assets integration

After you register the tenant, the last step of the onboarding process is enabling the Experience Manager Assets Integration for Commerce extension in the Admin.

1. Enable the extension.

   1. Go to **Stores** > Settings > **Configuration** > **Catalog**.

   1. Open the Catalog configuration by selecting **[!UICONTROL Catalog]**.

   1. Expand **[!UICONTROL AEM Assets integration]**.

   1. Set **[!UICONTROL Integration enabled]** to `yes`.

      ![AEM Assets Integration for Commerce Admin configuration](assets/aem-integration-admin-enable.png){width="600" zoomable="yes"}


### Error messages





