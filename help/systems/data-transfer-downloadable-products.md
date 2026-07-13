---
title: Import downloadable products
description: Review an example of importing product data for a downloadable product.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/a62y8GDLpN0PHxlm8EYHHMsHfzzkjB4mSNa-BV78Ra8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
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
# Import downloadable products

The flow for importing downloadable products is the same as for [Bundle Products](data-transfer-bundle-products.md) or [Configurable Products](data-transfer-configurable-products.md). The difference is that a downloadable product has [downloadable links](../catalog/product-create-downloadable.md) and [downloadable samples](../catalog/product-create-downloadable.md) with its images.

The default root directory for downloadable links and samples is `<Magento-root-folder>/pub/media/import`. If the remote storage module is enabled, the default root directory for downloadable links and samples is the `<remote-storage-root-folder>/media/import` directory.

The CSV file has separate columns for `downloadable_links` and `downloadable_samples`.

- **Downloadable link images** — In the following example, downloadable link images (`red.jpg` and `black.jpg`) are in the `<Magento-root-folder>/pub/media/import/test` folder. If remote storage is enabled, these images are in the `<remote-storage-root-folder>/media/import/test` folder.

  ![Example data - downloadable product with downloadable links](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **Downloadable sample images** — In the following example, the downloadable sample image (`white.jpg`) is in the `<Magento-root-folder>/pub/media/import/test` folder. If remote storage is enabled, this image is in the `<remote-storage-root-folder>/media/import/test` folder.

  ![Example data - downloadable product with downloadable samples](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

For more information about enabling and managing the remote storage module, see [Configure remote storage](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) in the _Configuration guide_.
