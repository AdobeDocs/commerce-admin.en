---
title: Browser capabilities detection
description: Learn how to configure browser capabilities detection and display a notice if the customer's browser settings need to be changed.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/zPxdplYIYblw6-tsDvxEmvKfAx-2M6opb6qjX7YL1I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
---
# Browser capabilities detection

Like most websites and applications on the Internet, Adobe Commerce and Magento Open Source require that the visitor's browser allow both cookies and JavaScript for full operations. However, occasionally a user's browser is set to the highest privacy setting that prevents both cookies and JavaScript. Your store can be configured to test the capabilities of each visitor's browser and display a notice if the settings need to be changed.

- If the browser's privacy settings disallow cookies, you can configure the system to automatically redirect them to the [Enable Cookies](../content-design/pages.md#enable-cookies) page, which explains how to make the recommended settings with most browsers.
- If the browser's privacy settings disallow JavaScript, you can configure the system to display the following message above the header of every page.

For technical information, refer to [Supported browsers](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) in the _Installation Guide_.

## Configure browser capabilities detection

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the panel on the left under _[!UICONTROL General]_, choose **[!UICONTROL Web]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Browser Capabilities Detection]** section and do the following:

   - To display instructions that explain how to configure the browser to allow cookies, set **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** to `Yes`.

   - To display a banner above the header when JavaScript is disabled in the user's browser, set **[!UICONTROL Show Notice if JavaScript is Disabled]** to `Yes`.

   - To display a banner above the header when Local Storage is disabled in the user's browser, set **[!UICONTROL Show Notice if Local Storage is Disabled]** to `Yes`.

    ![General configuration - web browser capabilities detection](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. When complete, click **[!UICONTROL Save Config]**.
