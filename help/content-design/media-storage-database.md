---
title: Use a media database
description: Learn how to use a media database to store your [!DNL Commerce] media files.
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/QUhPGliOg0grz9UcLAcWWiPd5Zh4pIvB-n-QeORilfg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Use a media database

>[!IMPORTANT]
>
>The database media storage method is deprecated as of Adobe Commerce and Magento Open Source 2.4.3.

By default, all images, compiled CSS files, and compiled JavaScript files of the [!DNL Commerce] instance are stored in the file system on the web server. You can choose to store these files in a database on a database server. One advantage of this approach is the option of automatic synchronization and reverse synchronization between the web server file system and the database. You can use the default database to store media or create one. To be able to use a newly created database as media storage, you must add information about it and its access credentials to the `env.php` file.

## Database workflow

1. **Browser requests media** - A page from the store opens in the customer's browser, and the browser requests the media that is specified in the HTML.

1. **System looks for media in file system** - The system searches for the media in the file system and if found, passes it to the browser.

1. **System locates media in database** - If the media is not found in the file system, a request for the media is sent to the database that is specified in the configuration.

1. **System locates media in database** - A PHP script transfers the files from the database to the file system, and sent to the customer's browser. The browser request for media triggers the script to run as follows:

    - If web server [rewrites](../merchandising-promotions/url-rewrite.md) are enabled for [!DNL Commerce] and supported by the server, the PHP script runs only when the requested media is not found in the file system.
    - If web server rewrites are disabled for [!DNL Commerce], or not supported by the server, the PHP script runs anyway, even if the required media is available in the file system.

## Use a database for media storage

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL System]**.

1. In the upper-left corner, set **[!UICONTROL Store View]** to `Default Config` to apply the configuration at the global level.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Storage Configuration for Media]** section and do the following:

    ![Advanced configuration - storage configuration for media](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

    - Set **[!UICONTROL Media Storage]** to `Database`.

    - Set **[!UICONTROL Select Media Database]** to the database you want to use.

    - To transfer the existing media to the newly selected database, click **[!UICONTROL Synchronize]**.

    - Enter the **[!UICONTROL Environment Update Time]** in seconds.

1. When complete, click **[!UICONTROL Save Config]**.
