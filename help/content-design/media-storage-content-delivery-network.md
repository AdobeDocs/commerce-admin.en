---
title: Use a content delivery network
description: Learn how to use a Content Delivery Network (CDN) to store media files.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/c-Aw3S5unZlMdDG1k080D4CIMcILglNa4ymZxPt6HBk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Use a content delivery network

A content delivery network (CDN) can be used to store media files. Adobe Commerce on cloud infrastructure includes the Fastly CDN (see [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) in the _Commerce on Cloud Infrastructure Guide_). A Commerce instance that is installed _on premise_ does not include an integration with any specific CDN, you can use the CDN of your choice. 

After configuring the CDN, you must complete the configuration from the Admin. The changes can be made at either the global or website level. When a CDN is used for media storage, all paths to media on Commerce store pages are changed to the CDN paths that are specified in the configuration.

## CDN workflow

1. **Browser requests media** - A page from the store opens in the customer's browser, and the browser requests the media that is specified in the HTML.
1. **Request sent to CDN; images found and served** - The request is sent first to the CDN. If the CDN has the images in storage, it serves the media files to the customer's browser.
1. **Media not found, request sent to [!DNL Commerce] web server** - If the CDN does not have the media files, the request is sent to the [!DNL Commerce] web server. If the media files are found in the file system, the web server sends them to the customer's browser.

>[!IMPORTANT]
>
>For security, when a CDN is used as media storage, JavaScript may not function properly if the CDN is located outside of your subdomain.

## Configure a content delivery network

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel under _[!UICONTROL General]_, choose **[!UICONTROL Web]**.

1. In the upper-left corner, set **[!UICONTROL Store View]** as needed.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Base URLs]** section and do the following:

    ![General configuration - web base URLs](./assets/web-base-urls.png){width="600" zoomable="yes"}

    - Update the **[!UICONTROL Base URL for Static View Files]** with the URL of the location on the CDN where static view files are stored.

    - Update the **[!UICONTROL Base URL for User Media Files]** with the URL of the JavaScript files on the CDN.

        Both these fields can be left blank, or can start with the placeholder: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Base URLs (Secure)]** section and do the following:

    ![General configuration - web base URLs (secure)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

    - Update the **[!UICONTROL Secure Base URL for Static View Files]** with the URL of the location on the CDN where static view files are stored.

    - Update the **[!UICONTROL Secure Base URL for User Media Files]** with the URL of the JavaScript files on the CDN.

      Both these fields can be left blank, or can start with the placeholder: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. When complete, click **[!UICONTROL Save Config]**.
