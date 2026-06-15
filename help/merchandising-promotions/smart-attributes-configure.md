---
title: Configure smart attributes for Visual Merchandiser
description: Learn how to configure the smart attributes used by the Visual Merchandiser.
exl-id: 7bbbca40-d991-4393-b99c-5bef2e711071
feature: Merchandising, Products, Configuration, Attributes
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/-6tbdpZ7L6nS1sIOXdk5Faxpkkt9qzqWhIjqp9MwgiM
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
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Configure smart attributes for Visual Merchandiser

{{ee-feature}}

The Visual Merchandiser configuration determines the attributes that can be used in the merchandising window and the minimum stock threshold. The configuration also identifies the attribute used for color and the order of color values.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Visual Merchandiser]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL General Options]** section.

   ![Catalog configuration - visual merchandiser](../configuration-reference/catalog/assets/catalog-visual-merchandiser-general-options.png){width="600" zoomable="yes"}
   
1. In the **[!UICONTROL Attributes for Category Rules]** list, select each attribute that you want to make available for visual merchandising.
   
   To select multiple attributes, hold down the Ctrl key (PC) or the Command key (Mac) and click each item.

1. Enter the **[!UICONTROL Minimum Stock Threshold]** for a product to appear in the Visual Merchandiser window.

1. Enter the **[!UICONTROL Color Attribute Code]**.

   The default value is `color`. If your catalog uses a different attribute, enter the attribute name in lowercase.

1. For **[!UICONTROL Color Order]**, enter each color value on a separate line and in sequence to determine the priority of each color.

1. When complete, click **[!UICONTROL Save Config]**.
