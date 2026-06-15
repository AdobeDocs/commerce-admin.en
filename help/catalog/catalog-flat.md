---
title: Flat catalogs
description: Learn  about creating a flat catalog, where each row contains all the necessary data about a product or category.
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
TQID: https://experienceleague.adobe.com/7D7lHMHFVKh2J35S1Mpr5eudyLyicbpL4xqkvu-KatA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
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
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Flat catalogs

>[!IMPORTANT]
>
>Use of a flat catalog is no longer recommended as a best practice. Continued use of this feature is known to cause performance degradation and other indexing issues. A detailed description and solution is available in the [Help Center](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html).<br/><br/>Affected versions include: <br/>- Adobe Commerce on cloud infrastructure, 2.3.x and above<br/>- Adobe Commerce (On-Premise), 2.3.x and above<br/>- Magento Open Source, 2.3.x and above <br/><br/>On any release version, some extensions only work with flat tables, thus creating a risk if you disable flat tables. If you know that you have some extensions that use Flat Catalog indexers, you must be aware of this risk when setting those values to `No`.

Commerce typically stores catalog data in multiple tables, based on the Entity-Attribute-Value (EAV) model. Because product attributes are stored in many tables, SQL queries are sometimes long and complex.

In contrast, a flat catalog creates tables on the fly, where each row contains all the necessary data about a product or category. A flat catalog is updated automatically—either every minute, or according to your cron job. Flat catalog indexing can also speed up the processing of catalog and cart price rules. A catalog with as many as 500,000 SKUs can be indexed quickly as a flat catalog.

>[!NOTE]
>
>Before you enable a flat catalog for a live store, make sure to test the configuration in a development environment.

## Step 1: Enable the flat catalog

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. Expand the _Storefront_ section and do the following:

   - Set **[!UICONTROL Use Flat Catalog Category]** to `Yes`. (If necessary, deselect the **[!UICONTROL Use system value]** checkbox.)

   - Set **[!UICONTROL Use Flat Catalog Product]** to `Yes`.

   ![Flat catalog configuration](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. When complete, click **[!UICONTROL Save Config]**.

1. When prompted to update the cache, click **[!UICONTROL Cache Management]** in the system message and follow the instructions to refresh the cache.

## Step 2: Verify the results

There are two methods that you can use to verify the results.

### Method 1: Verify the results for a single product

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Open a product in edit mode.

1. For **[!UICONTROL Name]**, add the text `_TEST` to the end of the product name.

1. Click **[!UICONTROL Save]**.

1. On a new browser tab, navigate to the home page of your store and do the following:

   - Search for the product you edited.

   - Use the navigation to browse to the product under its assigned category.

      If necessary, refresh the page to see the results. The change appears within the minute or according to your [Cron](../systems/cron.md) schedule.

   ![Storefront with Flat Catalog](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### Method 2: Verify the results for a category

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. In the upper-left corner, verify that **[!UICONTROL Store View]** is set to `All Store Views`.

   If prompted, click **[!UICONTROL OK]** to confirm.

1. In the category tree, select an existing category, click **[!UICONTROL Add Subcategory]**, and do the following:

   - For **[!UICONTROL Category Name]**, enter `Test Category`.

   - When complete, click **[!UICONTROL Save]**.

      ![Test subcategory](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Products in Category]** section and click **[!UICONTROL Reset Filter]** to display all products.

   - Select the checkbox of several products to be added to the new category.

   - click **[!UICONTROL Save]**.

   ![Test category products](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. On a new browser tab, navigate to the home page of your store and use the store navigation to browse to the category you created.

   If necessary, refresh the page to see the results. The change appears within the minute or according to your cron schedule.

## Step 3: Remove the test data

Do the following to remove the test data and restore the original product name and catalog configuration.

### Remove the test category

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. In the category tree, select the test subcategory that you created.

1. In the upper-right corner, click **[!UICONTROL Delete]**.

1. When prompted to confirm, click **[!UICONTROL OK]**.

   This category removal does not remove the products that are assigned to the category.

### Restore the original product name

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Open the test product in edit mode.

1. Remove the `_TEST` text that you added to the **[!UICONTROL Product Name]**.

1. In the upper-right corner, click **[!UICONTROL Save]**.

### Restore the original catalog configuration

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL Catalog]** underneath.

1. Expand the _Storefront_ section and do the following:

   - Set **[!UICONTROL Use Flat Catalog Category]** to `No`.

   - Set **[!UICONTROL Use Flat Catalog Product]** to `No`.

1. When complete, click **[!UICONTROL Save Config]**.

1. When prompted, refresh the cache.
