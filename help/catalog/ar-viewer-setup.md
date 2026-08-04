---
title: "[!DNL AR Viewer] for Adobe Commerce setup"
description: Learn about managing 3D model assets using the [!DNL AR Viewer] extension for your product listings.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
TQID: https://experienceleague.adobe.com/6OlcZ4Psm3INgVm7f-Y9JvqfUdmR6Rg48tcigLAHiaE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Manage product 3D models with the [!DNL AR Viewer] for Adobe Commerce

For each product, you can upload a `.USDZ` file that allows for AR and 3D models to be used in your product listing.

The [!DNL AR Viewer] only supports `.USDZ` files.

## Install the extension

[!DNL AR Viewer] is installed as an extension from the [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

See the [_Installation Guide_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) for more information about the extension installation process.

After the [!DNL AR Viewer] extension is installed and configured, Admin users can set up, customize, and manage product listings to include 3D models.

## Add a 3D model

1. Open the product in edit mode.

1. To work with a specific store view, set the **[!UICONTROL Store View]** chooser to the applicable view.

   >[!NOTE]
   >
   >New product 3D models are _always_ uploaded and visible in _all_ store views, even if the `All Store Views` scope is not used for upload. <br/><br/>To hide any product 3D models from a specific store view, you must switch to that Store View, select the **[!UICONTROL Hide from Product Page]** checkbox for the 3D model, and click **[!UICONTROL Save]**.

1. Scroll down and expand the _[!UICONTROL Product 3D Model]_ section.

   ![Menu Pop-up](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Add the 3D model (`.USDZ` file) of the product.

1. Click **[!UICONTROL Save]**.

### Delete a 3D model

To remove a 3D model from the product details: 

1. Click **[!UICONTROL Delete]**. 

1. Click **[!UICONTROL Save]**.

## View product 3D models

When the product details are updated with the 3D model:

1. The [!DNL AR Viewer] generates a QR code in the product description that encodes the AR file.

1. A customer can see this QR code in the product page.

1. When customers scan the QR code with their mobile devices, an AR experience is rendered on the mobile device.

>[!NOTE]
>
> For a series of demonstration videos of a user adding a 3d model to a product, see the [AR Viewer for Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) page in _Commerce Videos and Tutorials_.

