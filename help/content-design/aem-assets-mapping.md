---
title: Map assets metadata and attributes
description: To be added
feature: CMS, Media
---
# Configure Commerce metadata in AEM Assets

In Experience Manager assets, each asset is described by metadata which enables users to find assets, understand them more fully, and make decisions about managing and using them. **Metadata profiles** let you apply default metadata to assets within a folder. All assets in the folder inherit the default metadata configured in the profile.

The AEM integration for Commerce requires all Commerce assets stored in Experience Manage asset to have certain metadata to manage communication and synchronization processes between Adobe Commerce and Experience Manager Assets.

After you create the metadata profile, you add the metadata to the metadata schema that is used by the Experience Manager Assets to define the interface for users to 


Before using the integration, you need to add this  

Commerce folder automatically. In this case, we plan to assign a flag to each one of the assets contained inside the folder Commerce to be used later on by the search API.

We will use a metadata schema to show a read-only field to identify if an asset is present in commerce or not and 2 more fields for future usage, SKU name and brand.

We have to keep in mind that the metadata schema is used by the UI to display the asset edition form and that the API will get properties from both the metadata profile and schema.


## Prerequisites

- Familiar with AEM assets metadata profiles (<https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/configuring/metadata-profiles>)
- Familiar with AEM asset [metadata schemas]((https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/configuring/metadata-schemas))


Wiki source documentation:  <https://wiki.corp.adobe.com/pages/viewpage.action?pageId=3091610558>


After enabling the AEM Assets integration for Commerce, you need to setup metatdata in AEM Assets to trigger events 


[Metadata schemas](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/configuring/metadata-schemas) define the interface users interact with asset metadata in AEM, and their definition and application to assets are critical to digital asset management.

Add the metadata required to manage Commerce assets to the Experience Manager Assets profile.  This metadata is used to define the interface that users interact with  the interface AEM nfigure the asset metadata required to  AEM

| Type  | Label   | Property   | Default Value |
|------ | ------- | ---------- | ------------- |
| Text | Does it exist in Adobe Commerce? | `./jcr:content/metadata/commerce:isCommerce` | yes |
| Multi Value Text | Commerce mappings | `./jcr:content/metadata/commerce:mappings` | none |



## Add metadata profile to apply to Commerce assets stored in AEM

Steps:

1. In AEM Assets, create a [metadata profile](https://experienceleague.adobe.com/en/docs/experience-manager-learn/assets/configuring/metadata-profiles) to apply default metadata automatically to folders containing Commerce assets.

1. Edit an existing profile or create a new one specifically for the Commerce integration.

1. Add required Commerce fields (we have to tell them what to add)

- Does it exist in Adobe Commerce?

1. Save the profile.

1. Apply the metadata profile to folders containing by selecting **Apply Metadata Profile to Folders**.


## Update the metadata schema to add Commerce metadata

Add required Commerce fields:

- Does it exist in Adobe Commerce (read-only)
- Commerce SKU name
- Commerce brand name

Save the changes.





1. Select Metadata schema.  -- what 

1. Add required Commerce fields  

- Does it exist in Commerce (read-only)
- Commerce 

4. After adding the Commerce metadata to the profile


4. Apply changes to the comm


In AEM Assets, select Metadata profiles.

Create a metadata profile to apply default metadata automatically to folders containing Commerce assets.

Commerce folder automatically. In this case, we plan to assign a flag to each one of the assets contained inside the folder Commerce to be used later on by the search API.

We will use a metadata schema to show a read-only field to identify if an asset is present in commerce or not and 2 more fields for future usage, SKU name and brand.

We have to keep in mind that the metadata schema is used by the UI to display the asset edition form and that the API will get properties from both the metadata profile and schema.
