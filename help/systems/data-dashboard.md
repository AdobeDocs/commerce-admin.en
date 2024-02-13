---
title: Data Management Dashboard
description: Learn about the Data Management Dashboard
feature: Products, Customers, Data Import/Export
---
# Data Management Dashboard

The Data Management Dashboard provides insight into data streams for Adobe Commerce SaaS products. Users of [!DNL Live Search], [!DNL Product Recommendations], and [!DNL Catalog Service] can view product sync statuses and resync data from a single dashboard.

The Data Management Dashboard is located at *System* > Data Transfer > *Data Management Dashboard*.

![Data Management Dashboard](assets/data-management-dashboard.png)

## Settings

The Settings button on the right side of the page opens the [[!DNL Catalog Sync]](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) settings dialog.

Normally, the [!DNL Catalog Sync] process runs automatically, once an hour.

Resyncing catalog data forces the service to refetch data from the Commerce database, ensuring that the latest changes are reflected in the service and on your site. Use this button if you have made several product changes and you need to have those changes updated before the normal automatic sync process. 

## Sync status

The _[!UICONTROL Sync]_ status panel reports the number of products that have been synced within the last three hours. If you make infrequent updates to your catalog, this value is frequently zero. Click **[!UICONTROL Refresh]** to refresh the count.

## Product count

The product count panel reflects the total number of catalog products available to the service.

The [!DNL Catalog Service] dashboard reflects the total number of products in the catalog available to the service. This is generally all products in the Commerce database. 

The Product Recommendations and Live Search dashboards display the total number of [_searchable_](https://experienceleague.adobe.com/docs/commerce-admin/catalog/catalog/search/search.html) products. If some products are not set to be searchable, this would account for the difference in product totals between [!DNL Product Recommendations] and [!DNL Live Search], and [!DNL Catalog Service].

## Synced products

The Synced Catalog Products table provides details about the products in the index. By default, this table is sorted by 'Last Updated'.

To find a specific product, use the**[!UICONTROL Search by SKU]** field .
To control what columns are displayed, click **[!UICONTROL Customize Table]** on the right of the table.
