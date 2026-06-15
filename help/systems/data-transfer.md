---
title: Data transfer
description: Learn about support for data transfer, including data validation.
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
TQID: https://experienceleague.adobe.com/G-hJ2wQlhL95wmuLLYivfW8AGsbfdu5Cn0pOdGdTQto
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Data transfers

Use the import and export tools to manage multiple records in a single operation. You can import new items as well as update, replace, and delete existing product sets.

For example, you can add new products to your inventory, update product data and advanced price data, and replace a set of existing products with new products. The import and export tools help manage large product catalogs more efficiently because you can export the data, edit it in a spreadsheet, and import it back into your store instead of performing multiple operations in the Admin.


>[!NOTE]
>
>Adobe Commerce also supports SaaS data export to transfer product data from the Commerce server to SaaS services. SaaS data export is integrated with Commerce SaaS Services including [Product Recommendations](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html), [Live Search](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview), and [Catalog Service](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview). For details, see the [SaaS Data Export Guide](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview).

## Data validation

All data must pass validation to ensure the quality, accuracy, and integrity of the values before importing them into the store. Validation begins when you click **[!UICONTROL Check Data]**. During the process, all entities in the import file are verified for the following:

- **Attributes** - Column header names are verified to ensure that they match the corresponding attributes in the system database. The value of each attribute is checked to ensure that it meets the requirements of the data type (decimal, integer, varchar, text, and datetime).
- **Complex Data** - Values that originate from a defined set, such as a drop-down or multiple select input type, are verified to ensure that the values exist in the defined set.
- **Service Data** - The values in service data columns are verified to ensure that the properties or complex data values are consistent with what is already defined in the system database.
- **Required Values** - For new entities, the presence of required attribute values in the file is checked. For existing entities, there is no need to recheck the existence of required attribute values.
- **Separators** - Although the separators aren't visible when viewed in a spreadsheet, data values in a CSV file are separated by comma, and text values are enclosed in double-quotes. During the validation process, formatting for the separators and each set of quotes that enclose character strings are verified.

The results of the validation appear in the Validation Results section, and include the following information:

- The number of entities checked
- The number of invalid rows
- The number of errors found

If the data is valid, an _Import Success_ message appears.

![System message - file is valid](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

If validation fails, read the description of each error, and correct the problem in the CSV file. For example, if a row contains an invalid SKU, the import process stops, and that row, and all subsequent rows are not imported. After correctly the problem, import the data again. If many errors are encountered, it might take several attempts to pass validation.

### Data validation messages

#### Validation

- `Product with specified SKU not found in rows: 1`
- `URL key for specified store already exists`
- `'7z' file extension is not supported`
- `TXT file extension is not supported`

#### Errors

- `Wrong field type. Type in the imported file %decimal%, expected type is %text%.`
- `Value is not allowed. Attribute value does not exist in the system.`
- `Field %column name% is required.Wrong value separator is used.`
- `Wrong encoding used. Supported character encoding is UTF-8 and Windows-1252.`
- `Imported file does not contain SKU field.`
- `SKU does not exist in the system.`
- `Column name %column name% is invalid. Should start with a letter. Alphanumeric.`
- `Imported file does not contain a header.`
- `%website name% website does not exist in the system.`
- `%storeview name% storeview does not exist in the system.`
- `Imported attribute %attribute name% does not exist in the system.`
- `Imported resource (image) could not be downloaded from external resource due to timeout or access permissions.`
- `Imported resource (image) does not exist in the local media storage.`
- `Product creation error displayed to the user equal to the one seen during manual product save.`
- `Advanced Price creation error displayed to the user equal to the one seen during the manual product save.`
- `Customer creation error displayed to the user equal to the one seen during the manual customer save.`
