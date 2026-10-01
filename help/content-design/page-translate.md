---
title: Translate a content page
description: Learn how to create a translated version of each page that is available from the specific store view.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/9jox-v5fCEhPsaex70yQod--qH-Xnp9dkgmuxJGTZd0
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
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# Translate a content page

If your store has multiple views in different [languages](../stores-purchase/store-localize.md), and you have set the locale for each view to a different language, the result is a partially translated site. The next step is to create a translated version of each page that is available from the specific store view. The [!UICONTROL Store View] column of the _[!UICONTROL Manage Pages]_ list shows each view that has a translated version of the page.

To translate a content page, you must create another page that has the same URL Key as the original, but is assigned to the specific store view. Then, update the page for the specific view with the translated text. The following example shows how to create a translated version of the _About Us_ page for the Spanish store view.

## Step 1: Copy the URL key for the page to be translated

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Elements]_ > **[!UICONTROL Pages]**.

1. In the grid, find the page to be translated and open in _edit_ mode.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Search Engine Optimization]** section and copy the **[!UICONTROL URL Key]** to the clipboard.

1. To return to the _[!UICONTROL Pages]_ grid, click **[!UICONTROL Back]** in the top button bar.

## Step 2: Add a page for the translated content

1. Click **[!UICONTROL Add New Page]**.

1. Enter the translated **[!UICONTROL Page Title]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Content]** section and complete the translated text for the page.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Search Engine Optimization]** section and do the following:

   - Paste the **[!UICONTROL URL Key]** that you copied from the original page.

   - Enter the translated text for the **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]**, and **[!UICONTROL Meta Description]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Page in Websites]** section and set **[!UICONTROL Store View]** to the store view where the page is to be available.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Design]** section and set the column **[!UICONTROL Layout]** of the page.

1. Click **[!UICONTROL Save]**.

1. When prompted, refresh any invalid [caches](../systems/cache-management.md).

## Step 3: Verify the translation

To verify the translation, go to the storefront and use the language chooser to change the store view.

Notice that there are still some elements on the page that should be translated, including the company footer links [block](block-add.md), the [welcome message](../getting-started/storefront-branding.md#change-the-welcome-message), and [product information](../stores-purchase/store-localize.md#localize-products).
