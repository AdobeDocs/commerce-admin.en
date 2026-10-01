---
title: Add gift registry search
description: Learn how to place a gift registry search box to help store vistors purchase products from customer registries.
exl-id: 8c5558d6-3641-4769-987e-8b217603d9fc
feature: Gift, Storefront, Search
TQID: https://experienceleague.adobe.com/YlSi1XDNBNDc4EUdmEuPI-8gxAhHhWbxUY2ge-2AEV0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
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
# Add gift registry search

{{ee-feature}}

The [Widget](../content-design/widgets.md) tool can be used to place a gift registry search box most anywhere in your store. You can specify the search options to be available to customers, such as name, email address, and gift registry ID. When the customer clicks the Search button, the results appear on the Gift Registry Search page. If the search returns no results, the customer can try again with other parameters.

![Example storefront - gift registry search](./assets/storefront-gift-registry-search.png){width="700" zoomable="yes"}

## Configure gift registry search

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Elements]_ > **[!UICONTROL Widgets]**.

1. In the upper-right corner, click **[!UICONTROL Add Widget]**.

1. Choose the **[!UICONTROL Settings]** tab and do the following:

   - Set **[!UICONTROL Type]** to `Gift Registry Search`.

   - Set **[!UICONTROL Design Theme]** to the theme that is used by the store.

   - Click **[!UICONTROL Continue]**.

   ![Gift registry - search settings](./assets/widget-gift-registry-search-settings.png){width="700" zoomable="yes"}

1. In the _[!UICONTROL Storefront Properties]_ section, do the following:

   - Enter a **[!UICONTROL Widget Title]** for internal reference.

   - Set **[!UICONTROL Assign to Store Views]** to the store views where Gift Registry Search is to be available.

   - Set **[!UICONTROL Sort Order]** to determine the order that the Gift Registry Search block appears when there are other blocks assigned to the same location on the page.

   ![Gift registry - storefront properties](./assets/widget-gift-registry-search-storefront-properties.png){width="700" zoomable="yes"}

1. In the **[!UICONTROL Layout Updates]** section, click **[!UICONTROL Add Layout Update]**.

1. To determine where the Gift Registry Search appears in the store, do the following:

   - Set **[!UICONTROL Display On]** to the pages in your store where you want Gift Registry Search block to appear.

   - If applicable, choose the **[!UICONTROL Categories]** where you want it to appear.

   - Set **[!UICONTROL Container]** to the location on the page to place the Gift Registry Search block.

   ![Gift registry - layout updates](./assets/widget-gift-registry-search-layout-updates.png){width="500" zoomable="yes"}

1. In the left panel, choose **[!UICONTROL Widget Options]**.

1. To determine how visitors to your site can search for gift registries, select as many of the following that apply:

   - [!UICONTROL All Forms]
   - [!UICONTROL Registrant Name Search]
   - [!UICONTROL Registrant Email Search]
   - [!UICONTROL Gift Registry ID Search]

   ![Gift registry - widget options](./assets/widget-gift-registry-search-widget-options.png){width="700" zoomable="yes"}

1. When complete, click **[!UICONTROL Save]**.

1. When prompted to refresh the page cache, click the link in the message at the top of the workspace and follow the instructions.

## Field descriptions

### [!UICONTROL Settings]

|Field|Description|
|--- |--- |
|[!UICONTROL Type]|Identifies `Gift Registry Search` as the type of Widget.|
|[!UICONTROL Design Theme]|The theme that is used by the store where the Gift Registry Search is to appear.|

{style="table-layout:auto"}

### [!UICONTROL Storefront Properties]

|Field|Description|
|--- |--- |
|[!UICONTROL Widget Title]|A name for internal reference.|
|[!UICONTROL Assign to Store Views]|Identifies the store views where the Gift Registry Search is to be available.|
|[!UICONTROL Sort Order]|Indicates the order that Gift Registry Search block appears if there are other blocks assigned to appear in the same location.|

{style="table-layout:auto"}

### [!UICONTROL Layout Updates]

|Field|Description|
|--- |--- |
|[!UICONTROL Display On]|Indicate the specific pages, or types of pages where Gift Registry Search block appears.|
|[!UICONTROL Categories]|If applicable, identifies the category pages where Gift Registry Search appears.|
|[!UICONTROL Container]|Indicates the page layout block where Gift Registry Search is placed. The options vary by template and theme.|

{style="table-layout:auto"}

### [!UICONTROL Widget Options]

|Field|Description|
|--- |--- |
|[!UICONTROL Quick Search Form Types]|Determines the types of searches that can be performed with Gift Registry Search. Options: `All Forms` / `Registrant Name Search` /` Registrant Email Search` / `Gift Registry ID Search`|

{style="table-layout:auto"}
