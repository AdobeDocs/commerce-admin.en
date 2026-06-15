---
title: Use a widget to position a block
description: Learn how to use a static block widget to place an existing content nearly anywhere within your store.
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/LZt31t9uNhrCglxO5L8E0XfVsFrwEKcv2H-TcKF46Ng
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
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Use a widget to position a block

The _CMS Static Block_ [widget](widgets.md) gives you the ability to place an existing [content block](blocks.md) nearly anywhere in your store.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Step 1: Choose the widget type

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Elements]_ > **[!UICONTROL Widgets]**.

1. In the upper-right corner, click **[!UICONTROL Add Widget]**.

1. In the _Settings_ section, set **[!UICONTROL Type]** to `CMS Static Block` and click **[!UICONTROL Continue]**.

1. Verify that the **[!UICONTROL Design Theme]** is set to the current theme and click **[!UICONTROL Continue]**.

   ![Widget settings](./assets/widget-settings.png){width="600" zoomable="yes"}

1. In the _[!UICONTROL Storefront Properties]_ section, do the following:

   - For **[!UICONTROL Widget Title]**, enter a descriptive title for the widget.

      This title is visible only from the _Admin_.

   - For **[!UICONTROL Assign to Store Views]**, select the store views where the widget is visible.

      You can select a specific store view, or `All Store Views`. To select multiple views, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

   - (Optional) For **[!UICONTROL Sort Order]**, enter a number to determine the order this item appears with others in the same part of the page. (`0` = first, `1` = second, `3` = third, and so on.)

      ![Storefront properties](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## Step 2: Complete the widget layout updates

1. In the _[!UICONTROL Layout Updates]_ section, click **[!UICONTROL Add Layout Update]**.

1. Set **[!UICONTROL Display On]** to the category, product, or page where you want the block to appear.

1. To place the block on a specific page, do the following:

   - Choose the **[!UICONTROL Page]** where you want the block to appear.

   - Choose the **[!UICONTROL Block Reference]** that identifies the place where the block is displayed on the page.

   - Accept the default setting for **[!UICONTROL Template]**, which is set to `CMS Static Block Default Template`.

      ![Layout updates](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### Layout update options

|Field|Description|
|--- |--- |
|**_[!UICONTROL Categories]_**||
|[!UICONTROL Anchor Categories]|Displays the widget on the anchor category page.<br/>**[!UICONTROL Categories]** - Categories where the anchor is displayed. Options: `All` / `Specific Categories`<br/>**[!UICONTROL Container]** - Set the container to the part of the page layout where you want to display the widget.<br/>**[!UICONTROL Template]** - Determines the theme of the layout.|
|[!UICONTROL Non-Anchor Categories]|Displays the widget on the non-anchor category page.<br/>**[!UICONTROL Categories]** - Categories where the anchor is displayed. Options: `All` / `Specific Categories`<br/>**[!UICONTROL Container]** - Set the container to the part of the page layout where you want to display the widget.<br/>**[!UICONTROL Template]** - Determines the theme of the layout.|
|**_[!UICONTROL Products]_**||
|All Product Types|Displays the widget on either a specific type of product page, or on all product pages. <br/>**[!UICONTROL Products]** - Products for which the widget is displayed. Options: `All` /` Specific Products`<br/>**[!UICONTROL Container]** - Set the container to the part of the page layout where you want to display the widget.<br/>**[!UICONTROL Template]** - Determines the theme of the layout.|
|**_[!UICONTROL Generic Pages]_**||
|[!UICONTROL All Pages]|Displays the widget on all pages. <br/>**[!UICONTROL Container]** - Set the container to the part of the page layout where you want to display the widget.<br/>**[!UICONTROL Template]** - Determines the theme of the layout.|
|[!UICONTROL Specified Page]|Displays the widget on a specific page. Options:<br/>**[!UICONTROL Page]** - Pages for which the widget is displayed.<br/>**[!UICONTROL Container]** - Set the container to the part of the page layout where you want to display the widget.<br/>**Template** - Determines the theme of the layout.|
|[!UICONTROL Page Layouts]|Displays the widget on pages with a certain layout. <br/>**[!UICONTROL Page]** - Pages for which the widget is displayed.<br/>**[!UICONTROL Container]** - Set the container to the part of the page layout where you want to display the widget.<br/>**[!UICONTROL Template]** - Determines the theme of the layout.|

{style="table-layout:auto"}

## Step 3: Place the block

1. In the left panel, select **[!UICONTROL Widget Options]**.

1. Click **[!UICONTROL Select Block…]** and choose the block that you want to place from the list.

1. When complete, click **[!UICONTROL Save]**.

   The app now appears in the list.

1. When prompted, follow the instructions at the top of the page to update the index and page cache.

1. Return to your storefront to verify that the block appears in the correct location.

   To move the block, you can reopen the widget or try a different page or block reference.
