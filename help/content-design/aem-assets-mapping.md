---
title: Configure metadata for Commerce assets
description: Add metadata required for the AEM Assets Integration for Commerce to Experience Manager Assets metadata profile and schemas
feature: CMS, Media, Integration
---
# Configure Commerce metadata in AEM Assets

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

In Experience Manager assets, each asset is described by metadata which enables users to find assets, understand them more fully, and make decisions about managing and using them.

- **[Metadata profiles](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles)** let you apply default metadata to assets within a folder. All assets in the folder inherit the default metadata configured in the profile.
 A Metadata Schema defines a set of fields that can be used as metadata properties on an AEM asset.

- **[Metadata schema](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas)** defines the layout of the properties page and the set of fields that can be used as metadata properties on an AEM asset.

The Experience Manager Integration for Commerce requires all Commerce assets stored in AEM Assets to have certain metadata to manage communication and synchronization processes between Adobe Commerce and Experience Manager Assets. For the initial configuration, add the following fields to both an AEM Assets metadata profile and a metadata schema.

| Field type  | Label   | Property   | Default Value |
|------ | ------- | ---------- | ------------- |
| Text | **Does it exist in Adobe Commerce?** | `./jcr:content/metadata/commerce:isCommerce` | yes |
| Multi Value Text | **Commerce mappings** | `./jcr:content/metadata/commerce:mappings` | none |

## Create metadata profile

1. From the Adobe Experience Manager workspace, go to the Author Content administration workspace for AEM Assets by clicking the Adobe Experience Manager icon.

   ![AEM Assets authoring](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Open the Administrator tools by selecting the hammer icon.

   ![AEM Author Admin manage metadata profiles](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Open the profile configuration page by clicking **[!UICONTROL Metadata Profiles]**.

1. **[!UICONTROL Create]** a metadata profile for the Commerce integration.

   ![AEM Author Admin add metadata profiles ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Add `Does Commerce exist?` and `Commerce mappings` metadata fields for Commerce.

   ![AEM Author Admin add metadata fields to profile](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. Save the update.

1. Apply the `Commerce integration` metadata profile to the folder where Commerce assets are stored.

   1. From the[!UICONTROL  Metadata Profiles] page, select the Commerce integration profile.

   1. From the action menu, select **[!UICONTROL Apply Metadata Profiles to Folder(s)]**.

   1. Select the folder containing Commerce assets.

      Create a Commerce folder if it does not exist.

   1. Click **[!UICONTROL Apply].

## Add Commerce fields to metadata schema

1. From the AEM Author Content administration panel, open **[!UICONTROL Metadata Schemas (Manage metadata forms)]**

   ![AEM Author Admin update metadata schema](./assets/aem-assets-manage-metadata-schema.png){width="600" zoomable="yes"}

1. Create a metadata schema form for Commerce.

1. On the [!UICONTROL Metadata Schema Form], create the `Does Commerce exist?` and `Commerce mappings` fields and map the properties.

1. Click **[!UICONTROL Save]**.

