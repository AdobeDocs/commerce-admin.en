---
title: Data Management Dashboard
description: Learn how to access insights about data streams for Catalog Service, Live Search, Product Recommendations.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
---
# Data Management Dashboard

The Data Management Dashboard provides insight into data streams for Adobe Commerce SaaS products. Users of [!DNL Live Search], [!DNL Product Recommendations], and [!DNL Catalog Service] can view product sync statuses and resync data from a single dashboard.

The Data Management Dashboard is located at *System* > Data Transfer > *Data Management Dashboard*.

![Data Management Dashboard](assets/data-management-dashboard.png)

## Settings

The **[!UICONTROL Settings]** button on the right side of the page opens the dialog where you can resynchronize the catalog data.

Resynching catalog data forces the service to refetch data from the Commerce database. This action is usually used during the first-time onboarding when the catalog sync has not run for a couple of hours.

## Sync status

The _[!UICONTROL Sync]_ status panel reports the number of products that have been synced within the last three hours. If you make infrequent updates to your catalog, this value is frequently zero. Click **[!UICONTROL Refresh]** to refresh the count.

## Product count

The product count panel reflects the total number of catalog products available to the service.

The [!DNL Product Recommendations] and [!DNL Live Search] dashboards display the total number of _displayable_ products. [!DNL Catalog Service] does not filter products by displayable, so if you have both [!DNL Catalog Service] and [!DNL Live Search] or [!DNL Product Recommendations] installed, it is possible for the two dashboards to show two different values for the product count.

## Synced products

The Synced Products table provides details about the products in the index. By default, this table is sorted by 'Last Updated'.

To find a specific product, use the **[!UICONTROL Search by SKU]** field .
To control what columns are displayed, click **[!UICONTROL Customize Table]** on the right of the table.
