---
title: "Manage product 3D models with the [!DNL AR Viewer] for Adobe Commerce"
description: "Learn about managing 3D model assets using the [!DNL AR Viewer] module for your product listings."
---

# Install the [!DNL AR Viewer] module

[!DNL AR Viewer] is installed as an extension from [Adobe Commerce Marketplace](https://marketplace.magento.com/){target=_blank}.

See [install](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) guide for more information on this process.

After the [!DNL AR Viewer] module is installed and configured, _Admin_ users can set up, customize, and manage product listings to include 3D models.

## Manage product 3D models

For each product, you can upload a `.USDZ` schema that allows for AR and 3D models to be used in your product listing.

The [!DNL AR Viewer] only supports `.USDZ` schemas. See [requirements](../catalog/ar-viewer-requirements.md) topic for more information.

## Add a 3D model

1. Open the product in edit mode.

1. To work with a specific store view, set the **[!UICONTROL Store View]** chooser in the upper-left corner to the applicable view.

   >[!NOTE]
   >
   >New product 3D models are **_always_** uploaded and visible in **_all_** store views, even if the `All Store Views` scope is not used for upload. <br/><br/>To hide any product 3D models from a specific store view, you must switch to that Store View , select the **[!UICONTROL Hide from Product Page]** checkbox for the 3D model, and click **[!UICONTROL Save]**.

1. Scroll down and expand the _[!UICONTROL Product 3D Model]_ section.

   ![Menu Pop-up](assets/ar-viewer-product-options.png)

1. Add the 3D model (`.USDZ` schema) of the product.

1. Click **[!UICONTROL Save]**.

### Delete a 3D model

To remove a 3D model from the product details: 

1. Click the **[!UICONTROL Delete]** icon. 

1. Click **[!UICONTROL Save]**.

## View product 3D models

Once the product details are updated with the 3D model:

1. The [!DNL AR Viewer] generates a QR code in the product description that encodes the AR file.

1. A customer can see this QR code in the product page.

1. When customers scan the QR code with their mobile devices, an AR experience is rendered on the mobile device.
