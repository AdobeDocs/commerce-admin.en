---
title: Enable asset synchronization
description: Learn how to connect your Adobe Commerce and Experience Manager Assets projects with the Assets Rule Engine Service to enable asset synchronization between these two systems.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
---
# Set up the synchronization

>[!BEGINSHADEBOX]

**Prerequisites**

- [Configure AEM Experience Manager Assets to manage Commerce assets](#aem-assets-configure-aem)
- [Install and configure the AEM Assets Integration for Commerce](#aem-assets-configure-commerce.md) to add the extension and generate the required credentials and connections to use the extension.

>[!ENDSHADEBOX]

To enable the integration, register your tenant ID. This process identifies the AEM Assets project that you are connecting to, and provides the credentials to enable communication and workflows between Commerce and AEM Assets.

After you enable the integration, select the matching rule to use for synchronizing assets between Adobe Commerce and AEM Assets.

The AEM Assets Integration for Commerce supports two matching strategies for synchronizing assets between Adobe Commerce and AEM Assets.

- **Match by product SKU**-This is the default matching rule that matches assets based on the Stock Keeping Unit (SKU) of the product. The SKU is a unique identifier for each product. This rule matches the SKU in the asset metadata with the Commerce product SKU to ensure that assets are associated with the correct products.

- **Custom match**–This matching rule is for more complex scenarios or specific business requirements that require custom matching logic. To use this rule, you must have custom code implemented in Adobe Developer App Builder that defines how assets are matched with products.

For initial onboarding, use the `MatchBySku` strategy. If needed, you can change the matching strategy later.

## Enable the integration

1. Get the project and environment ID for your [AEM Assets Authoring Environment](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start).

   1. Open the AEM Sites page, and select **[!UICONTROL Assets]**.

   1. Copy and save the project and environment IDs from the URL:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. From the Commerce Admin, open the AEM Assets Integration configuration.

   1. Select **[!UICONTROL Store]** > Configuration > **[!UICONTROL CATALOG]** > **[!UICONTROL Catalog]**.

   1. Expand **[!UICONTROL Experience Manager Assets integration]**.

      ![AEM Assets Integration enable the integration](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Identify the Experience Manager Assets project to connect to by entering the **[!UICONTROL Program ID]** and **[!UICONTROL Environment ID]**.

1. Add the OAUTH credentials to authenticate API requests between Adobe Commerce and the ARES service by selecting the **[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)** you created for AEM Assets Integration for Commerce extension, for example `Assets integration`.

1. Allow Commerce to accept incoming updates from AEM Assets by selecting **[!UICONTROL Enable integration]**.

   After enabling the integration, you can configure the asset matching rule.

   ![AEM Assets Integration select asset match rule](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Define the matching rule for asset synchronization.

   1. Select **[!UICONTROL Match by product SKU]**.

   1. Add the [AEM Assets metadata field name](aem-assets-configure-aem.md#configure-metadata) defined for Commerce product SKUs in the **[!UICONTROL Match by product SKU attribute name]** field, `commerce:skus` for example.

1. Apply the configuration and initiate the synchronization process by selecting **[!UICONTROL Save Config]**.
