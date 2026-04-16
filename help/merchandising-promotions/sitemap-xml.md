---
title: Site maps
description: Learn how to configure a site map to index all pages and images of your Commerce sites.
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
---
# Site maps

>[!TIP]
>
>For Adobe Commerce as a Cloud Service, see the [SEO guidelines](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/) in the Commerce Storefront documentation

A site map improves the way that your store is indexed by search engines, and is designed to find pages that might be overlooked by web crawlers. A site map can be configured to index all pages and images.

When enabled, Commerce creates a file called `sitemap.xml` that is saved to your installation in the location that you specify. The configuration gives you the ability to set the frequency of the updates, and the priority for each type of content. Your site map should be updated as frequently as the content on your site changes, which might be daily, weekly, or monthly.

While your site is in development, you might include instructions in the `robots.txt` file for web crawlers to avoid indexing the site. Then before the launch, you can change the instructions to allow the site to be indexed.

For technical information, see [Add sitemap and robots.txt](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html) in the _Commerce on Cloud Infrastructure Guide_.

![Sitemap grid](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## Step 1. Configure the site map

Complete the [XML Sitemap configuration](#site-map-configuration) to determine what is included, and how frequently the site map is updated.

## Step 2. Generate the site map

1. On the _Admin_ menu, go to **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_ > **[!UICONTROL Site Map]**.

1. Click **[!UICONTROL Add Site Map]**.

   ![Site map grid](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. Enter the site map **[!UICONTROL Filename]**. For example: `sitemap.xml`

1. Enter the **[!UICONTROL Path]** to determine where the site map file is to reside on the server. Make sure that the path is writeable.

   - `/sitemap/` - Places the site map file in a directory called _sitemap_.

   - `/` - Places the site map file at the base path, or root of your Commerce installation.

   ![New site map](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. When complete, click **[!UICONTROL Save & Generate]**.

    It might take a few minutes for the site map to appear in the grid.

## Step 3. Configure and enable robots.txt (optional)

Complete the [search engine robots](seo-overview.md#search-engine-robots) configuration with instructions that direct search engines to crawl the parts of your site that you want to be indexed.

## Step 4. Submit your site map to search engines

You can submit your site map to different search engines by providing them the link to the `sitemap.xml` file in your Commerce installation. To copy the link, do the following:

1. In the _Site Map_ list, right-click the URL in the **[!UICONTROL Link for Google]** column.

1. On the menu, choose **[!UICONTROL Copy Link Address]**.

For more information, see the instructions for the specific search engine. Here are links to instructions for two top search engines:

- [Google](https://support.google.com/webmasters/answer/183669?hl=en)
- [Microsoft&reg; Bing](https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed)

## Step 5: Restore previous robot instructions (optional)

You can now restore either the original (default) restrictions.

## Manage sitemaps and robots.txt for multiple websites

If you have multiple websites, you can simplify the process of creating and submitting sitemaps. Simply [create](#site-map-configuration) one or more sitemaps that include URLs for all your verified stores and save the sitemaps to a single location. All sites must be verified in [Google Search Console](https://support.google.com/webmasters/answer/7451001).

To create sitemaps for a multistore instance, do the following:

1. Create a folder called `sitemaps` at the root of your website, then create subfolders for each domain:

       /sitemaps/domain_1/
       /sitemaps/domain_2/

1. On the _Admin_ sidebar, go to **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_ > **[!UICONTROL Site Map]**.

1. Create or edit the sitemap listings for each store and set the **[!UICONTROL Path]** to the one you created for the store:

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. If needed, update your robots.txt file.

   To make sure that the search engine spiders are properly directed to the new sitemaps, you can update or create the robots.txt file. Add the following lines at the top.

         Website Sitemap
         Sitemap: https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
         Sitemap: https://www.domain_2.com/sitemaps/domain_2/sitemap.xml

>[!NOTE]
>
>If your site uses the [Apache](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html) web server engine, you should update the [`.htaccess`](https://httpd.apache.org/docs/current/howto/htaccess.html) file in the root of your website to direct any other sitemap requests to the proper place.

## Column descriptions

|Column|Description|
|------|-----------|
|[!UICONTROL ID]|The sequential record number of the current site map.|
|[!UICONTROL Filename]|The file name of the site map.|
|[!UICONTROL Path]|The location where the site map resides on the server. For example: <br/>`/sitemap/` - Places the site map file in a directory called _sitemap_, one level below the root of the Commerce installation. <br/>`/` - Places the site map file at the base path, or root of the Commerce installation.|
|[!UICONTROL Link for Google]|The URL of the site map that is to be submitted to Google and other search engines.|
|[!UICONTROL Last Generated]|Indicates the date and time that the site map was last generated.|
|[!UICONTROL Store View]|The store view where the site map applies.|
|[!UICONTROL Generate]|Regenerates the site map.|

{style="table-layout:auto"}

## Site map configuration

Your site map should be updated as frequently as the content on your site changes, which could be on a daily, weekly, or monthly basis. The configuration lets you set the frequency and priority for each type of content.

### Step 1. Set the frequency and priority of content updates

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Catalog]** and choose **[!UICONTROL XML Sitemap]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Categories Options]** section and do the following:

   >[!NOTE]
   >
   >If needed, clear the **[!UICONTROL Use system value]** checkbox to change these settings.

   - Set **[!UICONTROL Frequency]** to one of the following:

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - For **[!UICONTROL Priority]**, enter a value between `0.0` and `1.0`. Zero has the lowest priority.

   ![XML sitemap - Categories options](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   For a detailed list of these options, see [Categories Options](../configuration-reference/catalog/xml-sitemap.md#categories-options) in the _Configuration Reference_.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Products Options]** section and complete the **[!UICONTROL Frequency]** and **[!UICONTROL Priority]** settings as needed.

   For a detailed list of these options, see [Products Options](../configuration-reference/catalog/xml-sitemap.md#products-options) in the _Configuration Reference_.

1. To determine the extent that images are included in the sitemap, set **[!UICONTROL Add Images into Sitemap]** to one of the following:

   - `None`
   - `Base Only`
   - `All`

   ![Catalog configuration - XML sitemap products](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL CMS Pages Options]** section and complete the **[!UICONTROL Frequency]** and **[!UICONTROL Priority]** settings as needed.

   ![Catalog configuration - XML sitemap CMS pages](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   For a detailed list of these options, see [CMS Pages Options](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options) in the _Configuration Reference_.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Store Url Options]** section and complete the **[!UICONTROL Frequency]** and **[!UICONTROL Priority]** settings as needed.

   ![Catalog configuration - XML sitemap store url](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   For a detailed list of these options, see [Store Url Options](../configuration-reference/catalog/xml-sitemap.md#store-url-options) in the _Configuration Reference_.

1. When complete, click **[!UICONTROL Save Config]**.

### Step 2. Complete the generation settings

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Generation Settings]** section.

   If needed, clear the **Use system value** checkbox to change these settings.

   ![Catalog configuration - XML sitemap generation settings](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   For a detailed list of these options, see [Generation Settings](../configuration-reference/catalog/xml-sitemap.md#generation-settings) in the _Configuration Reference_.

1. To generate a sitemap, set **[!UICONTROL Enabled]** to `Yes` and do the following:

   - Set **[!UICONTROL Start Time]** to the hour, minute, and second that you want the sitemap to be updated.

   - Set **[!UICONTROL Frequency]** to one of the following:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - For **[!UICONTROL Error Email Recipient]**, enter the email address of the person who is to receive notification if an error occurs during a sitemap update.

   - Set **[!UICONTROL Error Email Sender]** to the store contact who appears as the sender of the error notification.

   - Set **[!UICONTROL Error Email Template]** to the template used for the error notification.

### Step 3. Set the site map file limits

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Sitemap File Limits]** section.

   ![Catalog configuration - XML sitemap file limits](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   For a detailed list of these options, see [Sitemap File Limits](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits) in the _Configuration Reference_.

1. For **[!UICONTROL Maximum No of URLs per File]**, enter the maximum number of URLs that can be included in the sitemap.

   By default, the limit is 50,000.

1. For **[!UICONTROL Maximum File Size]**, enter the largest size in bytes that is allocated for the sitemap.

   The default size is 10,485,760 bytes.

### Step 4. Set the search engine submission settings

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Search Engine Submission Settings]** section.

   ![Catalog configuration - XML sitemap search engine submission settings](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. If using a `robots.txt` file to provide instructions to search engines that crawl your site, set **[!UICONTROL Enable Submission to Robots.txt]** to `Yes`.

1. When complete, click **[!UICONTROL Save Config]**.
