---
title: AEM Assets Integration
description: Integrate Adobe Experience Manager (AEM) Assets with your [!DNL Commerce] instance to access to countless media assets for use in your store.
feature: CMS, Media, Configuration, Integration
---
# AEM Assets Integration

Streamline the process of managing and delivering product images by integrating Adobe Experience Manager (AEM) Assets with your Commerce instance.

**Prerequisites**

- Adobe Commerce must be integrated with the Admin Console with an assigned Organization ID.
- Adobe Commerce and Experience Manger Assets or Assets Essentials must be assigned as a product to the user configuring the integration.

## Integrate [!DNL Commerce] and AEM Assets

Configuring the AEM Assets integration for Adobe Commerce is a two-step process:

1. [Generate an API key](#create-an-adobe-developer-integration) to generate an API Key
1. [Configure the AEM Assets integration in the Commerce Admin](#configure-the-aem-assets-integration)

### Generate an API key


### Configure the AEM Assets integration

To set the system configuration in your [!DNL Commerce] Admin, use the _API Key_ and _Client secret_ generated in the [previous section][create-integration].

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL System]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** and do the following:

   - Set **[!UICONTROL Enabled Adobe Stock]** to `Yes`.

   - Enter your **[!UICONTROL API Key (Client ID)]**.

   - Enter your **[!UICONTROL Client Secret]**.

   - Click **[!UICONTROL Test Connection]** to validate your keys.

   ![Advanced configuration - AEM Assets integration](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Give the validation a few seconds. If your credentials are valid, you should see a green _Connection Successful!_ message.

1. When complete, click **[!UICONTROL Save Config]**.

