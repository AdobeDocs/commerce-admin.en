---
title: Install AEM Assets Package for Commerce
description: Add the asset metadata required to enable the AEM Assets Integration for Commerce to synchronize assets between Adobe Commerce and Experience Manager Assets projects.
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
---
# Install the AEM Assets package

Adobe provides a project template, `commerce-assets`, to add Commerce namespace and metadata schema resources to the Experience Manager Assets as a Cloud Service environment configuration. Deploy this template to your environment as a Maven package. Then, configure the Commerce metadata in the AEM Assets authoring environment to complete the setup.

The template adds the following resources to the AEM Assets authoring environment.

- A [custom namespace](https://github.com/ankumalh/assets-commerce/blob/main/ui.config/jcr_root/apps/commerce/config/org.apache.sling.jcr.repoinit.RepositoryInitializer~commerce-namespaces.cfg.json), `Commerce` to identify Commerce-related properties.

- A custom metadata type `commerce:isCommerce` with the label `Eligible for Commerce` to tag Commerce assets associated with an Adobe Commerce project.

- A custom metadata type `commerce:productmetadata` and a corresponding UI component to add a *[!UICONTROL Product Data]* property. Product Data includes the metadata properties to associate a Commerce asset with product SKUs, and to specify image `role` and `position` attributes for the asset.

  ![Custom Product Data UI Control](./assets/aem-commerce-sku-metadata-fields-from-template.png){width="600" zoomable="yes"}

- A metadata schema form with a Commerce tab that includes the `Eligible for Commerce?` and `Product Data` fields for tagging Commerce assets. The form also provides options to show or hide the `roles` and `order` (position) fields from the AEM Assets UI.

   ![Commerce tab for AEM Assets metadata schema form](./assets/assets-configure-metadata-schema-form-editor.png){width="600" zoomable="yes"}

- A [sample tagged and approved Commerce asset](https://github.com/ankumalh/assets-commerce/blob/main/ui.content/src/main/content/jcr_root/content/dam/wknd/en/activities/hiking/equipment_6.jpg/.content.xml) `equipment_6.jpg` to support initial asset synchronization. Only approved Commerce assets can be synchronized from AEM Assets to Adobe Commerce.

>[!NOTE]
>For additional information about the `commerce-assets` AEM project template, see the [Readme](https://github.com/ankumalh/assets-commerce).

You need the following resources and permissions to use this AEM project to update the environment configuration:

- [Access to the AEM Assets Cloud Manager Program and environments](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager#access-sysadmin-bo) with the Program and Deployment Manager roles.

- A [local AEM development environment](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) and familiarity with the AEM local development process.

- Understand [AEM project structure](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) and how to deploy custom content packages using Cloud Manager.

## Install the `commerce-assets` package

1. From the Cloud Manager, create production and staging environments for your AEM Assets project, if needed.

1. Configure a deployment pipeline, if needed.

1. From GitHub, download the boilerplate code from the [Commerce-Assets AEM project](https://github.com/ankumalh/assets-commerce).

1. From your [local AEM development environment](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview), install the custom code into your AEM Assets environment configuration as a Maven package, or by manually copying the code into the existing project configuration.

1. Commit the changes and push your local development branch to the Cloud Manager Git repository.

1. From Cloud Manager, [deploy your code to update the AEM environment](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deploying-code-with-cloud-manager).

## Configure a metadata profile

In the AEM Assets author environment, set default values for Commerce asset metadata by creating a metadata profile. Then, apply the new profile to AEM Asset folders to automatically use these defaults. This configuration streamlines asset processing by reducing manual steps.

When you configure the metadata profile, you only have to configure the following components:

- Add a Commerce tab. This tab enables Commerce-specific configuration settings added by the template
- Add the `Eligible for Commerce` field to the Commerce tab.

The Product Data UI component is added automatically based on the template.

### Set up the metadata profile

1. Log in to the Adobe Experience Manager author environment.

1. From the Adobe Experience Manager workspace, go to the Author Content Administration workspace for AEM Assets by clicking the Adobe Experience Manager icon.

   ![AEM Assets authoring](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Open the Administrator tools by selecting the hammer icon.

   ![AEM Author Admin manage metadata profiles](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Open the profile configuration page by clicking **[!UICONTROL Metadata Profiles]**.

1. **[!UICONTROL Create]** a metadata profile for the Commerce integration.

   ![AEM Author Admin add metadata profiles ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Add a tab for Commerce metadata.

   1. On the left, click **[!UICONTROL Settings]**.

   1. Click  **[!UICONTROL +]** in the tab section, and then specify the **[!UICONTROL Tab Name]**, `Commerce`.

1. Add the `Eligible for Commerce` field to the form.

   ![AEM Author Admin add metadata fields to profile](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

   - Click **[!UICONTROL Build form]**.

   - Drag the `Single Line text` field to the form.

   - Add the `Eligible for Commerce` text for the label by clicking **[!UICONTROL Field Label]**.

   - On the Settings tab, add the label text to **Field Label**.

   - Set the placeholder text to `yes`.

   - In the **[!UICONTROL Map to Property]** field, copy and paste the following value

     ```terminal
     ./jcr:content/metadata/commerce:isCommerce
     ```

1. Optional. To automatically synchronize approved Commerce assets as they are uploaded to the AEM Assets environment, set the default value for the _[!UICONTROL Review Status]_ field on the `Basic` tab to `approved`.

1. Save the update.

#### Apply the metadata profile to Commerce assets source folder

   1. From the[!UICONTROL  Metadata Profiles] page, select the Commerce integration profile.

   1. From the action menu, select **[!UICONTROL Apply Metadata Profiles to Folders]**.

   1. Select the folder containing Commerce assets.

      Create a Commerce folder if it does not exist.

   1. Click **[!UICONTROL Apply]**.

## Next step

[Install Adobe Commerce packages](aem-assets-configure-commerce.md)
