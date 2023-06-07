---
title: "Setup the [!DNL AR Quick View] for Adobe Commerce"
description: "Learn how to onboard, setup and use the [!DNL AR Quick View] extension."
---

# Install

Normal composer procedure installation https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html

## Add a USDZ schema

Step 1: Create a product in the Admin menu.
Step 1: Edit a product in the Admin menu.

  ![Menu Pop-up](assets/catalog-menu.png)

  ![OTP Pop-up](assets/product-options.png)

Step 2: In **Product 3D Model** attribute, upload a 3d model of the product. (Current supported file format: .usdz)



  ![OTP Pop-up](assets/select-usdz-schema.png)

Step 3: After click save button, the extension will generate the AR file at the backend, and insert an QR code to the product description which encodes the AR file.

Step 4: At customer's frontend, customer can see the QR code in product page.

  ![OTP Pop-up](assets/qr-code.png)

Step 5: Customers use their mobile device to scan this QR code, AR experience will rendered on the device.

  ![OTP Pop-up](assets/product-storefront.png)
