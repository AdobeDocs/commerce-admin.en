---
title: Configure Experience Manager Assets
description: Add the asset metadata required to enable the AEM Assets Integration for Commerce to synchronize assets between Adobe Commerce and Experience Manager Assets projects.
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
---
# Configure Experience Manager Assets

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

To search and manage Commerce assets in AEM Assets, configure the AEM Assets environment with the Commerce metadata to identify and organize the assets. After completing the configuration, add a Commerce asset to the AEM Assets project. This asset is required to complete the initial Adobe onboarding process which enables asset synchronization between AEM Assets and the Commerce instance.

For the integration, you configure two types of metadata:

- **[Profile metadata](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles)** lets you apply metadata with predefined metadata values to assets. Then, you can apply the metadata profile to a folder so that assets within the folder inherit the default values.

- **[Schema metada](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas)** defines the layout of the properties page and the set of fields that can be used as metadata properties on an AEM asset.


## Prepare Assets environment


Create environments (if needed)
Configure a deployment pipeline (if needed)
Customize code based on https://github.com/ankumalh/assets-commerce
Git push & deploy changes
Create a new metadata schema or edit an existing one to include a Commerce tab containing commerce:isCommerce (Text) and commerce:skus (Product data UI component) with roles and positions. Creating schema will provide these fields to the Polaris API.
Create a new metadata schema profile containing commerce:isCommerce default to "yes".
Apply the metadata profile to a "Commerce" folder, a folder containing all Adobe Commerce assets.
Upload a new asset into the "Commerce" folder to allow internal commerce namespace creation.


 deploy the Commerce metadaEM Commerce boilerplate repository with boiler plate code that can be 


![AEM template for Commerce asset management](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}



[Deploy content packages using Cloud Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview)
[AEM content package](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#content-packages)


## Configure metadata

For the initial onboarding, add the following Commerce metadata to you Assets project

| Field type  | Label   | Property   | Default Value |
|------ | ------- | ---------- | ------------- |
| Text | **Does it exist in Adobe Commerce?** | `./jcr:content/metadata/commerce:isCommerce` | yes |
| Multi Value Text | **SKUs** | `./jcr:content/metadata/commerce:skus` | none |
| Multi Value Text | **Product Data** | `./jcr:content/metadata/commerce:positions` | none |


### Use Commerce asset boilerplate template

Adobe provides a GitHub repository with boilerplate code to update an AEM Assets environment to add metadata and configuration to support Commerce asset management. This code 


   ![AEM Assets authoring](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}


### Add Commerce fields to a metadata profile

1. From the Adobe Experience Manager workspace, go to the Author Content administration workspace for AEM Assets by clicking the Adobe Experience Manager icon.

   ![AEM Assets authoring](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Open the Administrator tools by selecting the hammer icon.

   ![AEM Author Admin manage metadata profiles](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Open the profile configuration page by clicking **[!UICONTROL Metadata Profiles]**.

1. **[!UICONTROL Create]** a metadata profile for the Commerce integration.

   ![AEM Author Admin add metadata profiles ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Add a tab for Commerce metadata.

   1. On the left, click  **[!UICONTROL Settings]**.

   1. Click  **[!UICONTROL +]** in the tab section, and then specify the **[!UICONTROL Tab Name]**, `Commerce`.

1. Add the [metadata fields](#configure-metadata) to the form.

   ![AEM Author Admin add metadata fields to profile](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. Save the update.

1. Apply the `Commerce integration` metadata profile to the folder where Commerce assets are stored.

   1. From the[!UICONTROL  Metadata Profiles] page, select the Commerce integration profile.

   1. From the action menu, select **[!UICONTROL Apply Metadata Profiles to Folder(s)]**.

   1. Select the folder containing Commerce assets.

      Create a Commerce folder if it does not exist.

   1. Click **[!UICONTROL Apply]**.

### Add Commerce fields to a metadata schema form

1. From the AEM Author Content administration panel for Assets, open **[!UICONTROL Metadata Schemas]** ([!UICONTROL Manage metadata schema forms]).

   ![AEM Author Admin update metadata schema](./assets/aem-assets-manage-metadata-schema.png){width="600" zoomable="yes"}

1. **[!UICONTROL Create]** a metadata schema for Commerce.

   ![AEM Author Admin update metadata schema](./assets/aem-assets-create-metadata-schema.png){width="600" zoomable="yes"}

1. On the [!UICONTROL Metadata Schema Form], create the `Does Commerce exist?` and `Commerce mappings` fields and map the properties.

1. Click **[!UICONTROL Save]**.


## Publish an asset

After configuring the AEM metadata and schema profile for Commerce assets, create the first Commerce asset to map the Commerce metadata fields.

1. From Experience Manager, go to [!UICONTROL Assets > Files] select the **Commerce** folder.

1. Upload an image for a Commerce project by dragging the file to the folder, or by clicking **[!UICONTROL Add Assets]**.

1. Verify the metadata configuration:  **isCommerce** is set to `true`, and that the `commerce:skus` property is set to the SKU for the Commerce product associated with the image.

1. Approve the asset.


## Add an asset to the Commerce folder

Create at least one asset in the AEM Assets Commerce folder that has the Commerce metadata attributes assigned.

This asset is required to setup synchronization between your Commerce instance and AEM Assets.

## Map metadata for assets

Metadata maps when a Commerce asset is published for the first time.  from Commerce for the first time. Media assets that have the built-in or custom fields automatically map to the specified fields the first time an asset is sent to Experience Manager Assets.

Before you can begin asset mapping, complete the following tasks:

- [Install and configure the AEM Assets Integration for Commerce](aem-assets-configure-commerce.md)
- [Enable asset synchronization to transfer assets between your Adobe Commerce project environment and the AEM Assets project environment](aem-assets-setup-synchronization.md)
