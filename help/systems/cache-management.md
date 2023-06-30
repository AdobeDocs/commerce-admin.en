---
title: Cache management
description: Learn how to use the cache management tools, which provide an easy way to improve the performance of your site.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
---
# Cache management

The Adobe Commerce and Magento Open Source cache management system provides an easy way to improve the performance of your site. Whenever a cache requires a refresh, a notice appears at the top of the workspace to guide you through the process. Follow the link to Cache Management and refresh the invalid caches.

![Save product attribute - update cache message](./assets/product-attribute-save-msg-update-cache.png){width="500"}

>[!NOTE]
>
>Multiple pages cache can be invalidated simultaneously and automatically **_without_** these entities editing. For example, when any product in the catalog is assigned to any category, or when any [!UICONTROL related product rule] is modified.

The _[!UICONTROL Cache Management]_ page shows the status of each primary cache and its associated tag. The large buttons in the upper-right corner can be used to flush the cache, or the all-inclusive Cache Storage. At the bottom of the page, there are additional buttons to flush the catalog product images cache and JavaScript/CSS cache.

After clearing a cache, always refresh your browser to make sure that you can see the most recent files. Clearing the Commerce cache does not clear your web browser cache. You may need to clear the browser cache to see updated content.

For additional technical information, see [Cache overview](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target="_blank"} in the _Commerce Frontend Development Guide_.

Access the _[!UICONTROL Cache Management]_ page by doing one of the following:

- Click the **[!UICONTROL Cache Management]** link in the message above the workspace.
- On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Tools]_ > **[!UICONTROL Cache Management]**.

![Cache management](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## Best Practices for caching

Reindexing and caching have different purposes in Commerce. [Indexes](index-management.md) track database information for increased search performance, faster data retrieval for storefronts, and more. Caches save loaded data, images, formats, and the like for increased performance loading and accessing the storefront.

- Always flush the cache after installing extensions/modules. You can install one or more extensions, then flush the cache.
- Flush the cache after installing Commerce. For fresh installs, you should also reindex.
- Flush the cache after upgrading from one version of Open Source or Commerce to another.
- When flushing caches, consider the type of cache and scheduling the flushing during non-peak times. For example, pick a time when few customers may access the site such as late night or early morning. Clearing some cache types during peak times cause result in a high load on the Admin and may result in a down site until completed.
- When [reindexing](index-management.md), you do not need to also perform a flush cache.

## Cache management role resources

Access to specific cache maintenance actions can be assigned to users by role, including options to view, toggle, and flush caches. Adobe recommends enabling flush actions only for administrator level users. Providing access to all Cache Management features can impact your storefront's performance.

![Role resources - cache management](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

For information about assigning resources to grant access for Admin user accounts, see [Role resources](permissions-user-roles.md#role-resources). The following resources control access to the cache management tools:

- [!UICONTROL Clean Cache Actions]

   - [!UICONTROL Flush Cache Storage]
   - [!UICONTROL Flush Magento Cache]

- [!UICONTROL Cache Type Management]

   - [!UICONTROL Toggle Cache Type]
   - [!UICONTROL Refresh Cache Type]

- [!UICONTROL Additional Cache Management]

   - [!UICONTROL Catalog Images Cache]
   - [!UICONTROL Flush Js/Css]
   - [!UICONTROL Flush Static Files]

## Refresh specific caches

1. For each cache to be refreshed, select the checkbox at the beginning of the row.

1. Set **[!UICONTROL Actions]** to `Refresh` and click **[!UICONTROL Submit]**.

## Perform mass action refresh

1. To select a group of caches, set **[!UICONTROL Mass Actions]** to one of the following:

   - `Select All`
   - `Select Visible`

1. Select the checkbox of each cache to be targeted by the action.

1. Set **[!UICONTROL Actions]** to `Refresh` and click **[!UICONTROL Submit]**.

## Flush the product image cache

1. Under _[!UICONTROL Additional Cache Management]_, click **[!UICONTROL Flush Catalog Images Cache]** to clear pre-generated product image files.

   The `Image cache was cleaned` message appears at the top of the workspace.

1. Clear the cache of your browser.

## Flush the JavaScript/CSS cache

1. Under _[!UICONTROL Additional Cache Management]_, click **[!UICONTROL Flush JavaScript/CSS Cache]** to clear any JavaScript and CSS files that have been merged into a single file.

   The `The JavaScript/CSS cache has been cleaned` message appears at the top of the workspace.

1. Clear the cache of your browser.

## Flush using the command line

Commerce provides additional flush cache options using the command line. These options may require developer support to complete. For complete details and command options, see [Manage the cache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-cache.html){:target="_blank"} in the _Configuration Guide_.

## Controls

|Control|Description|
|--- |--- |
|[!UICONTROL Mass Actions]|Selects the checkbox of multiple caches. Options: <br/>**[!UICONTROL Select All]** — Selects the checkbox of all caches. <br/>**Unselect All** — Clears the checkbox of all caches. <br/>**[!UICONTROL Select Visible]** — Selects the checkbox of all visible caches. <br/>**[!UICONTROL Unselect Visible]** — Clears the checkbox of all visible caches.|
|[!UICONTROL Actions]|Determines the action to be applied to all selected caches. Options: <br/>**[!UICONTROL Enable]** — Enables all selected caches. <br/>**[!UICONTROL Disable]** — Disables all selected caches. <br/>**[!UICONTROL Refresh]** — Refreshes all selected caches.|
|[!UICONTROL Submit]|Applies the action to all selected caches.|

{style="table-layout:auto"}

### Buttons

|Button|Description|
|--- |--- |
|[!UICONTROL Flush Magento Cache]|Removes all items in the default Commerce cache (`var/cache`), according to their associated Commerce tags.|
|[!UICONTROL Flush Cache Storage]|Removes all items from the cache, regardless of Commerce tag. If your system uses an alternate cache location, any cached files used by other applications are removed in the process.|
|[!UICONTROL Flush Catalog Images Cache]|Removes all automatically resized and watermarked catalog images that are stored in `media/catalog/product/cache`. If recently uploaded images are not reflected in the catalog, try flushing the catalog and refreshing your browser.|
|[!UICONTROL Flush JavaScript/CSS Cache]|Removes the merged copy of JavaScript and CSS files from the cache. If recent changes to the style sheet or JavaScript are not reflected in the store, try flushing the JavaScript/CSS cache and refreshing your browser.|
|[!UICONTROL Flush Static Files Cache]|Removes preprocessed view files and static files.|

{style="table-layout:auto"}

### Caches

| Cache | Description | Associated tag |
| ----- | ----------- | -------------- |
| [!UICONTROL Configuration] | Various XML configurations that were collected across modules and merged.<br>**[!UICONTROL System]** -  `config.xml`, `local.xml`<br>**[!UICONTROL Module]** -  `config.xml` | `CONFIG` |
| [!UICONTROL Layouts] | Layout building instructions. | `LAYOUT_GENERAL_CACHE_TAG` |
| [!UICONTROL Blocks HTML output] | Page blocks HTML. | `BLOCK_HTML` |
| [!UICONTROL Collections Data] | Collection data files.  | `COLLECTION_DATA` |
| [!UICONTROL Reflection Data ]| Clears API interface reflection data, that typically is generated during runtime. | `REFLECTION` |
| [!UICONTROL Database DDL operations] | Results of DDL queries, such as describing tables or indexes.  | `DB_DDL` |
| [!UICONTROL Compiled Config] | Results of code compilation. | `COMPILED_CONFIG` |
| [!UICONTROL EAV types and attributes] | Entity types declaration cache. | `EAV` |
| [!UICONTROL Customer Notification] | Temporary notifications that appear in the user interface. | `CUSTOMER_NOTIFICATION` |
| [!UICONTROL Integrations Configuration] | Integration configuration file. | `INTEGRATION` |
| [!UICONTROL Integrations API Configuration] | Integrations API configuration file. | `INTEGRATION_API_CONFIG` |
| [!UICONTROL Page Cache] | Full page caching. | `FPC` |
| [!UICONTROL Translations] | Translation files. | `TRANSLATE` |
| [!UICONTROL Web Services Configuration] | REST and SOAP configurations, generated WSDL file. | `WEBSERVICE` |
| [!UICONTROL Target Rule] | Target Rule Index | `TARGET_RULE` |

{style="table-layout:auto"}

## Full-page caching

Adobe Commerce and Magento Open Source use full-page caching on the server to quickly display category, product, and CMS pages. Full-page caching improves response time and reduces the load on the server. Without caching, each page might need to run blocks of code and retrieve information from the database. However, with full-page caching enabled, a fully generated page can be read directly from the cache.

>[!NOTE]
>
>It is recommended that [Varnish Cache](https://varnish-cache.org/){:target="_blank"} be used only in a production environment.

Cached content can be used to process the requests from similar types of visits. As a result, pages shown to a casual visitor might differ from those shown to a customer. For the purposes of caching, each visit is one of three types:

- `Non-sessioned` - During a non-sessioned visit, the shopper views pages, but does not interact with the store. The system caches the content of each page viewed and serves them to other non-sessioned shoppers.
- `Sessioned` - During a sessioned visit, shoppers who interact with the store — through activities such as comparing products or adding products to the shopping cart — are assigned a session ID. Cached pages that are generated during the session are used only by that shopper during the session.
- `Customer` - Customer sessions are created for those who have registered for an account with your store and shop while logged in to their accounts. During the session, customers can be presented with special offers, promotions, and prices that are based on their assigned customer group.

For technical information, see [Configure and Use Varnish](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target="_blank"} and [Use Redis for the Commerce page and default cache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target="_blank"} in the _Configuration Guide_.

**_To configure the full-page cache:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Advanced]** and choose **[!UICONTROL System]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Full Page Cache]** section.

   ![Advanced configuration - full page cache](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Caching Application]** to one of the following:

   - `Built-in Application`
   - `Varnish Caching`

1. To set the timeout for the page cache, enter the **[!UICONTROL TTL for public content]**. (The default value is `86400`)

1. If using Varnish, complete the **[!UICONTROL Varnish Configuration]** section as follows:

   - **[!UICONTROL Access list]** - Enter the IP addresses that can purge the Varnish configuration to generate a config file. Separate multiple entries with a comma. The default value is `localhost`.

   - **[!UICONTROL Backend host]** - Enter the IP address of the backend host that generates config files. The default value is `localhost`.

   - **[!UICONTROL Backend port]** - Identify the backend port that is used to generate config files. The default value is: `8080`.

   - **[!UICONTROL Grace period]** - Specify the number of seconds to use as a grace period to generate config files. See [Advanced Varnish configuration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) in the _Configuration Guide_.

   - To export the configuration as a `varnish.vcl` file, click the button for the version of Varnish that you use.

   ![Advance configuration - full page cache varnish](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. When complete, click **[!UICONTROL Save Config]**.
