---
title: Sales documents
description: Learn how to configure sales documents to support customer orders and fulfillment for your Commerce store.
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
TQID: https://experienceleague.adobe.com/0SZsaPiyOc4E-0e34IDvWATtKz9HMaeZAIMhKeysvTg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Sales documents

To support the order workflow and provide documentation to your customers about the orders they submit, configure the related sales documents to reflect your store brand and include reference information.

## Configure invoices and packing slips

Unlike the logo images used in storefront pages, the logo for PDF invoices and other sales documents can be a high-resolution, 300-dpi image. Be careful to preserve the aspect ratio when you resize the logo. Resize the logo so that it fits the height, and don't worry about any unused space to the right.

![Sample logo](./assets/logo-pdf.png){width="200"}

One way to resize your logo to fit the required size is to create a new, blank image with the correct dimensions. Then, paste your logo image and resize it to fit the height. With most image-editing programs, you can either scale it by a percentage to preserve the aspect ratio, or hold down the Shift key and manually resize the image.

**_To update the logo:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Sales]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Invoice and Packing Slip Design]** section and do the following:

   ![Sales configuration - sales invoice and packing slip design](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - To upload the **[!UICONTROL Logo for PDF Print-outs]**, click **[!UICONTROL Choose File]**, find the logo that you have prepared, and click **[!UICONTROL Open]**.

   - To upload the **[!UICONTROL Logo for HTML Print View]**, click **[!UICONTROL Choose File]**, find the logo that you have prepared, and click **[!UICONTROL Open]**.

   - Enter your address as you want it to appear on invoices and packing slips.

1. When complete, click **[!UICONTROL Save Config]**.

   For reference, a thumbnail of the uploaded image appears before each field. Don't worry if the thumbnail appears distorted. The proportion of the logo is correct on the invoice.

### Replace an image

1. Click **[!UICONTROL Choose File]** and choose a different logo file.

1. Select the **[!UICONTROL Delete Image]** checkbox for the image you want to replace.

1. Click **[!UICONTROL Save Config]**.

### Image formats

|Format| Requirements                             |
|--- |------------------------------------------|
|**_PDF_**||
|File format| JPG (JPEG), PNG, TIF (TIFF)              |
|Image size| Up to 1080 pixels wide x 270 pixels high |
|Resolution| 300 DPI recommended                      |
|**_HTML_**||
|File format| JPG (JPEG), PNG, GIF                     |
|Image size| Determined by theme.                     |
|Resolution| 72 or 96 DPI                             |

{style="table-layout:auto"}

## Add reference IDs

The Order ID and customer IP address can be included in the header of sales documents that accompany an order. By default, both the order ID and customer IP address appear in the header of invoices, shipment packing slips, and credit memos.

![Sales configuration - PDF print-outs](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_To change the order ID setting:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL PDF Print-outs]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Invoice** section.

1. Set **[!UICONTROL Display Order ID in Header]** according to your preference.

1. Repeat for the **[!UICONTROL Shipment]** and **[!UICONTROL Credit Memo]** sections.

1. When complete, click **[!UICONTROL Save Config]**.

**_To change the customer IP address setting:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Sales]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL General]** section.

   ![Sales configuration - general sales settings](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Hide Customer IP]** to your preference.

1. When complete, click **[!UICONTROL Save Config]**.
