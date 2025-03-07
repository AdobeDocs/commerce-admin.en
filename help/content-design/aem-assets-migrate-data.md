---
title: Migrate media files to AEM
description: Learn how to migrate media files to the AEM Assets DAM using the Bulk Import Tool.
feature: CMS, Media, Integration
---
# Migrate media files to the AEM Assets DAM

 Both Adobe Commerce and Adobe Experience Manager (AEM) provide built-in features to streamline media file migration from Commerce to the AEM Assets digital asset management system (DAM). You can also migrate media files from other sources.

## Migration workflow

Follow the same migration workflow described here to migrate media files from Adobe Commerce or another external system into the AEM Assets DAM.

### Step 1: Export content from the existing data source

For merchants using Adobe Commerce, the Remote Storage module simplifies the process of exporting media files from Adobe Commerce and importing them into AEM Assets. This module allows you to store and manage media files using remote storage services, such as AWS S3. For details about configuring remote storage, see [Configure Remote Storage](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage-aws-s3) in the *Commerce Configuration Guide*.

If you have media files stored outside of Adobe Commerce, upload them directly to one of the [data sources](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/assets-view/bulk-import-assets-view#prerequisites) supported by AEM as a Cloud Service.

### Step 2: Build a CSV file for metadata mapping

Create a metadata mapping file in CSV format and upload it to the source folder containing your media files. This file provides metadata that helps organize and find assets in the DAM.

For each media file you plan to migrate, provide values for the metadata fields included in the [AEM Assets metadata profile for Commerce assets](aem-assets-configure-aem.md) as described in the following table.

| Metadata | Description | Value |
|-------|-------------|--------|
| assetPath | The full path where the asset will be stored in AEM Assets repository.<br><br>Use the path to create sub-folders to organize Commerce assets, for example `content/dam/commerce/<brand>/<type>`. | `/content/dam/commerce/<sub-folder>/..<filename>` |
| dc:title | The display title of the asset in AEM Assets | String value (for example, `Sample 1`) |
| dam:status | The approval status of the asset in AEM Assets | `approved` |
| commerce:positions | The position/order of the asset in product galleries | Numeric value (e.g., "1") |
| commerce:isCommerce | Flag indicating if the asset is used in commerce | `Yes` |
| commerce:skus | Product SKUs associated with this asset | String value (for example, `sample1`) |
| commerce:roles | The roles or types of images for the asset (for example, `thumbnail`, `main image`, `swatch`) | Multiple values separated by semicolons (for example, "thumbnail; image; swatch_image; small_image") |

+++CSV code

Use this sample CSV code to create the file in a code editor or spreadsheet application like Microsoft Excel.

```csv
assetPath,dc:title{{String}},dam:status{{String}},commerce:positions{{String: multi}},commerce:isCommerce{{String}},commerce:skus{{String: multi}},commerce:roles{{String: multi}}
/content/dam/commerce/sample1.jpg,Sample 1,approved,1,Yes,sample1,thumbnail; image; swatch_image; small_image
/content/dam/commerce/sample2.jpg,Sample 2,approved,1,Yes,sample2,thumbnail; image; swatch_image; small_image
/content/dam/commerce/sample3.jpg,Sample 3,approved,1,Yes,sample3,thumbnail; image; swatch_image; small_image
```

+++

## Step 3: Bulk Import Assets into AEM Assets

After creating the metadata mapping file, use the AEM Assets Bulk Import Tool to import your assets.

The following is a high-level overview for using the tool. For detailed instructions, see [Bulk upload assets](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/add-assets#bulk-upload) in the  *AEM as a Cloud Service User Guide*.

1. Log in to your AEM Assets as a Cloud Service environment.

1. From the Experience Manager Tools view, select **[!UICONTROL Assets]** > **[!UICONTROL Bulk Import]**.

  ![AEM Assets authoring](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Create and save the bulk import configuration.

   You'll need:

   - Authentication credentials for your data source
   - The path to your metadata mapping CSV file
   - The target folder in AEM Assets where imported files will be stored
   - Information about the MIME types, file size, and other parameters to customize the import configuration

    >[!NOTE]
    >
    >The AEM Assets Integration for Commerce supports image and video media types.

1. Use the bulk import configuration to test and run the import operation.

## Migration best practices

1. Curate assets before migration by removing unused and duplicate content.
1. Organize assets logically by size, format, or use case.
1. Consider breaking large migrations into smaller batches.
1. Schedule resource-intensive imports during off-peak hours.
1. Validate metadata mapping before full import.


>[!MORELIKETHIS]
>
>*[Bulk Import tool video demo](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/add-assets#asset-bulk-ingestor)
>*[Tips, best practices, and limitations](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/add-assets#tips-limitations)
>*[Upload or ingest assets using APIs](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/admin/developer-reference-material-apis#asset-upload)

