---
title: Store and site structure
description: Learn about the website, store, and store view hierarchy.
exl-id: d745cbd0-151b-4f82-bb6c-fb6b9565a014
feature: Site Navigation, System
---
# Store and site structure

When Adobe Commerce or Magento Open Source is installed, a hierarchy that includes a main website, store, and store view is created. You can create additional websites, stores, and store views, as needed. For example, in addition to your main website, you might have additional websites with a different domain. Within each website, you can have multiple stores, and within each store, separate store views. Many installations have one website and one store, but with multiple store views to support different languages.

Before you begin, plan your store catalog hierarchy in advance because it is referred to throughout the configuration. Each store can have a separate [root category](../catalog/category-root.md), which makes it possible to have an entirely different set of main menu options for each store.

![Scope diagram](./assets/scope-multisite.svg){width="550"}

## Add stores

A single installation of Adobe Commerce or Magento Open Source can have multiple stores that share an Admin. Stores that are under the same website have the same IP address and domain, use the same security certificate, and share a single checkout process.

The important thing to understand is that the stores use the same code and share an Admin. Each store can have a separate catalog, or the stores can share a catalog. Each store can have a separate [root category](../catalog/category-root.md), which makes it possible to have a different main menu for each store. Stores can also have different branding, presentation, and content. Take some time to plan your store hierarchy with future growth in mind before you begin, because it is used throughout the configuration.

![Scope - multiple stores](./assets/scope-multistore.svg){width="550"}

Here are some examples of how URLs can be configured for multiple stores:

| URL | Description |
| --- | ----------- |
| `yourdomain.com/store1`<br>`yourdomain.com/store2` | Each store has a different path, but shares a domain. |
| `store1.yourdomain.com`<br>`store2.yourdomain.com` | Each store has a different subdomain of the primary domain. |

Multi-store installations of Adobe Commerce must be configured from the Admin and also from the command line of the server. The Adobe Commerce [Configuration Guide](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) provides detailed instructions for configuring the server environment.

### Step 1: Choose the store domain

The first step is to choose how you want to position the store. Should the stores share a domain, each have a subdomain, or have distinctly different domains? For each store, do one of the following:

- To place the store one level below the primary domain, you do not have to do anything.
- Set up a subdomain of your primary domain.
- Set up a different primary domain.

### Step 2: Create the store

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL All Stores]**.

1. Click **[!UICONTROL Create Store]** and set the options for the new store:

   - **[!UICONTROL Web Site]** — Choose a website that is to be the parent of the new store. If the installation has only one web site, accept the default (`Main Website`).

   - **[!UICONTROL Name]** — Enter a name for the new store. The name is for internal reference only.

   - **[!UICONTROL Code]** — Enter a code in lowercase characters to identify the store. For example: `mainstore`.

   - **[!UICONTROL Root Category]** — Set to the [root category](../catalog/category-root.md) that defines the category structure for the main menu of the new store. If you have already created a specific root category for the store, select it. Otherwise, select `Default Category`. You can come back later and update the setting.

   ![Create Store - store options](./assets/stores-all-store-information.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save Store]**.

### Step 3: Create a default store view

1. Click **[!UICONTROL Create Store View]** and set the store view options:

   - **[!UICONTROL Store]** — Set to the new store you created.

   - **[!UICONTROL Name]** — Enter a name for the view. For example, `English`.

   - **[!UICONTROL Code]** — Enter a code for the view in lowercase characters.

   - **[!UICONTROL Status]** — Set to `Enabled`.

   - **[!UICONTROL Sort Order]** — Enter a number to determine the store's position when listed with other stores.

1. Click **[!UICONTROL Save Store View]**.

   If you open your store in edit mode, you can see that it now has a default view.

   ![New store with default view](./assets/new-store-default-view.png){width="600" zoomable="yes"}

### Step 4: Configure the store URL

1. On the _Admin_ sidebar, click **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. Under _[!UICONTROL General]_ in the left panel on the left, choose **[!UICONTROL Web]**.

1. In the upper-left corner, set **[!UICONTROL Store View]** to the view that you created for the new store.

1. When prompted to confirm [scope](../getting-started/websites-stores-views.md#scope-settings) switching, click **[!UICONTROL OK]**.

   ![Choose the store view](./assets/create-store-config-view.png){width="600" zoomable="yes"}

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Base URLs]** section and enter the base URL for the store.

   If needed, clear the **[!UICONTROL Use system value]** checkbox to change the setting.

   ![General configuration - web base URLs](./assets/config-general-web-base-urls-clear-checkbox.png){width="600" zoomable="yes"}

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Secure Base URLs]** section and repeat the previous step if you want to configure the store [secure URL](store-urls.md).

1. Click **[!UICONTROL Save Config]**.

### Step 5: Configure the server

To configure your server to support multiple websites, see [Multiple websites or stores](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) in the _Configuration Guide_.

For help with configuring your web server, see the following resources:

- [Set up multiple websites with NGNX](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html)
- [Set up multiple websites with Apache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html)

For Adobe Commerce on cloud infrastructure, see [Set up multiple websites or stores](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html).

## Add websites

Multiple websites can be set up from a single Adobe Commerce or Magento Open Source installation with the same domain or different domains. By default, stores that are under the same website have the same IP address and domain, use the same security certificate, and share a single checkout process. If you want each store to have a dedicated checkout process under its own domain, each store must have a distinct IP address and separate security certificate.

Multi-site installations of Adobe Commerce or Magento Open Source must be configured from the Admin and also from the command line of the server. The Commerce [Configuration Guide](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) provides detailed instructions for configuring the server environment.

![Scope - websites](./assets/scope-multisite.svg){width="550"}

### Step 1: Create a website

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL All Stores]**.

1. In the upper-right corner, click **[!UICONTROL Create Website]**.

1. Set the **[!UICONTROL Web Site Information]** options:

   ![Create website - options](./assets/create-website-info.png){width="600" zoomable="yes"}

   - **[!UICONTROL Name]** — Enter the domain of the new website. For example, `domain.com`.

   - **[!UICONTROL Code]** — Enter a code that is used on the server to point to the domain.

      The code must begin with a lowercase (a-z) letter, and can include any combination of letters (a-z), numbers (0-9), and the underscore (_) symbol.

   - **[!UICONTROL Sort Order]** — _(Optional)_ Enter a number to determine the sequence in which this site is listed with other sites. To make this site appear at the top of the list, enter a zero (`0`).

1. Click **[!UICONTROL Save Web Site]**.

1. Set up each [store](#add-stores) and [store view](store-views.md) that is needed for the new website.

   You can then open the website in edit mode to set the default store.

### Step 2: Configure the store URL

To configure the [store URLs](store-urls.md), follow the instructions.

### Step 3: Configure the server

To configure your server to support multiple websites, see [Multiple websites or stores](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) in the _Configuration Guide_.

For help with configuring your web server, see the following tutorials:

- [Set up multiple websites with NGNX](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html)
- [Set up multiple websites with Apache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html)

For Adobe Commerce on cloud infrastructure, see [Set up multiple websites or stores](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html).
