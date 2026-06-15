---
title: Automatic redirects
description: Learn how to configure automatic redirects to be generated whenever the URL key of a product or category changes in your Commerce store.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/Vscg-TDdLnzKjdi-SMwrcpR-QDPvlHpPzgmcLe63-4Q
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
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Automatic redirects

Your store can be configured to automatically generate a permanent redirect whenever the URL key of a product or category changes. In the Search Engine Optimization section, the checkbox below the URL key indicates if permanent redirects are enabled. If your store is already configured to automatically redirect catalog URLs, a redirect is a simple update to the URL key. The process to create an automatic redirect is the same for both products and categories.

>[!NOTE]
>
>When automatic redirects are enabled and you save a category, all product and category rewrites are generated in real time and stored in database tables by default. This could result in significant performance issues for categories with many assigned products. The solution is to change this default and skip the generation of category/products URL rewrites for products on category save. In this case, product rewrites are generated only for the canonical product URL.

## Set up automatic redirects

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Search Engine Optimization]** section.

   ![Catalog configuration - search engine optimization](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** to `Yes`.

1. When complete, click **[!UICONTROL Save Config]**.


>[!NOTE]
>
> URL rewrites can be generated for the store view or website scope. Set the URL rewrite scope from the Admin at **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]** **[!UICONTROL Catalog]** > **[!UICONTROL Catalog]** > **[!UICONTROL Search Engine Optimization]**. Select the scope in the _[!UICONTROL Product URL Rewrite Scope]_ field.

## Automatically redirect product URLs

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Find the product in the list and click to open the record.

1. Expand ![Expansion selector ](../assets/icon-display-expand.png) the **[!UICONTROL Search Engine Optimization]** section.

   ![Product search engine optimization - permanent redirect](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. For **[!UICONTROL URL Key]**, do the following:

   - Make sure that the **[!UICONTROL Create Permanent Redirect for old URL]** checkbox is selected. If not, follow the instructions to [enable automatic redirects](url-rewrite.md#configure-url-rewrites).

   - Update the **[!UICONTROL URL Key]** as needed, using all lowercase characters and non-trailing hyphens between these characters instead of spaces.

1. When complete, click **[!UICONTROL Save]**.

1. When prompted to refresh the cache, follow the links in the message at the top of the workspace.

   The permanent redirect is now in effect for the product and any associated category URLs.

## Automatically redirect category URLs

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Find the category in the tree and click to open the record.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Search Engine Optimization]** section.

1. For **[!UICONTROL URL Key]**, do the following:

   - Make sure that the **[!UICONTROL Create Permanent Redirect for old URL]** checkbox is selected. If not, follow the instructions to [enable automatic redirects](url-rewrite.md#configure-url-rewrites).

   - Update the **[!UICONTROL URL Key]** as needed, using all lowercase characters and non-trailing hyphens between these characters instead of spaces.

1. When complete, click **[!UICONTROL Save]**.

1. When prompted to refresh the cache, follow the links in the message at the top of the workspace.

   The permanent redirect is now in effect for the category and any associated product URLs.

## Skip generation of product URL rewrites for category save {#skip-rewrite}

>[!WARNING]
>
>Turning off automatic generation of category/products URL rewrites results in permanent removal of all existing category/product type URL rewrites, which cannot be restored. This could potentially cause unresolved category/product type URL conflicts that require a manual update of the URL key to resolve.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Search Engine Optimization]** section.

1. Set **[!UICONTROL Generate "category/product" URL Rewrites]** to `No`.

1. In the confirmation dialog, click **[!UICONTROL OK]** to confirm the change and the removal of existing URL rewrites.

   ![Turn off category/product URL rewrites - confirm](./assets/seo-rewrite-off.png){width="350"}

1. When complete, click **[!UICONTROL Save Config]**.
