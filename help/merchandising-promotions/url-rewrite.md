---
title: URL rewrites
description: Learn about URL rewrites and using the Commerce URL rewrite tool to change URLs that are associated with a product, category, or CMS page.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
---
# URL rewrites

>[!TIP]
>
>For Adobe Commerce as a Cloud Service, see the [SEO guidelines](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/) in the Commerce Storefront documentation

The URL Rewrites tool lets you change any URL that is associated with a product, category, or CMS page. When you create a URL rewrite, Commerce automatically creates a permanent redirect (301) so that any links pointing to the old URL are redirected to the new address.

>[!NOTE]
>
>To update URL rewrites for multiple or all products simultaneously, refer to [Multiple URL rewrites](url-rewrite-product.md#multiple-url-rewrites).

>[!BEGINSHADEBOX "Understanding rewrites and redirects"]

The terms _rewrite_ and _redirect_ are often used interchangeably, but they are different operations:

* **URL Rewrite** — A server-side process that internally maps one URL to another without changing what appears in the browser's address bar. When a visitor requests a URL, the server processes it as a different URL behind the scenes, but the browser continues to display the original URL.

* **URL Redirect** — Sends an HTTP response to the browser instructing it to navigate to a different URL. The browser's address bar updates to show the new URL. Redirects can be temporary (302) or permanent (301).

>[!ENDSHADEBOX]

## How the Rewrites tool works

In Adobe Commerce, the URL Rewrites tool creates permanent redirects (301) by default to preserve SEO value when you change the URL key of a product, category, or page. This behavior ensures that existing links continue to work and search engine rankings are maintained.

By default, [automatic URL redirects](url-redirect-product-automatic.md) are enabled for your store and the **Create Permanent Redirect for old URL** checkbox is selected under the URL key field of each product.

{{url-rewrite-skip}}

![Search engine optimization - create permanent URL redirect](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

{{url-rewrite-params}}

## URL rewrites demo

Watch this video to learn about managing URL rewrites:

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)

## Create URL rewrites

Use the URL Rewrites tool to create product and category redirects, and custom redirects for any page in your store. When the URL rewrite configuration is applied, any existing links that point to the previous URL are seamlessly redirected to the new address.

You can create URL rewrites to:

* Add high-value keywords to improve the way the product is indexed by search engines.

* Add additional URLs for a temporary seasonal change, or permanent change.

* Add a valid path for a page, including CMS content pages. For example, the system always references products and categories by their ID internally, and you want to create a more user- or SEO-friendly URL path.

The URL rewrites you create can redirect to existing categories or custom pages without changing your site structure, making it easy to create memorable URLs for marketing campaigns.

![URL rewrites grid](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce offers these URL rewrite types:

* [Product Rewrites](url-rewrite-product.md)
* [Category Rewrites](url-rewrite-category.md)
* [CMS Page Rewrites](url-rewrite-cms-page.md)
* [Custom Rewrites](url-rewrite-custom.md)

### Use cases and examples

URL rewrites are commonly used in these scenarios:

#### Internal system URL vs. SEO-friendly URL

Commerce uses ID-based URLs internally, but you can create SEO-friendly URLs for customers:

**System URL (internal):**

    http://www.example.com/catalog/category/id/6

**Customer-facing URL:**

    http://www.example.com/peripherals/keyboard.html

#### Product rebranding or URL optimization

When you rename a product or want to improve its URL for SEO, create a redirect to preserve existing links:

**Original URL:**

    http://www.example.com/peripherals/keyboard.html

**New optimized URL:**

    http://www.example.com/ergonomic-keyboard.html

The Rewrites tool automatically creates a 301 redirect from the old URL to the new one, so customers and search engines are seamlessly directed to the correct page.

#### Promotional landing pages

Create temporary or permanent custom URLs for marketing campaigns:

**Promotional URLs:**

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

## Additional URL management configuration

The following sections describe how to configure Web Server Rewrites and canonical URLs for Commerce.

### Configure Web Server Rewrites

>[!NOTE]
>
>This section describes web server-level URL rewriting, which is different from the URL Rewrite tool capability. Web server rewrites handle technical URL formatting (like removing `index.php`), while the URL Rewrite tool manages redirects for content changes.

Enabling Web Server Rewrites is part of the initial Commerce setup and is typically configured during installation. When enabled, the web server (Apache or Nginx) automatically removes the file name `index.php` from URLs, creating cleaner, more SEO-friendly addresses.
The following example shows how URLs appear with and without web server rewrites enabled:

**URL without a Web Server Rewrite**

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

**URL with Web Server Rewrite**

    http://www.yourdomain.com/magento/storeview/url-identifier

#### Enable or disable Web Server Rewrites:

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel where **[!UICONTROL General]** is expanded, choose **[!UICONTROL Web]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Search Engine Optimization]** section.

   ![General configuration - web search engine optimization](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Use Web Server Rewrites]** to your preference.

1. When complete, click **[!UICONTROL Save Config]**.

### Specify canonical URLs

For SEO purposes, it is a good idea that each of your web pages has only one, distinct URL.

If you have a single page accessible by multiple URLs, or different pages with similar content, Google sees these as duplicate versions of the same page. Google chooses one URL as the canonical version and crawls that, and all other URLs are considered duplicate URLs and are crawled less often.

If you don't explicitly tell Google which URL is canonical, it makes the choice for you, or might consider them both of equal weight. This could lead to unwanted behavior, and runs the risk of an ineffective crawl budget and low distributed backlinks.

Depending on how you set up your website, there may be multiple versions of your site in the index, including:

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

To specify a canonical page, see [Google Search Central documentation](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).
