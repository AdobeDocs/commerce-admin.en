---
title: Data Management Dashboard
description: Learn how to access insights about data streams for Catalog Service, Live Search, Product Recommendations.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
---
# Data Management Dashboard



What is the Data Management Dashboard?
The Data Management Dashboard offers an overview of the synchronization status for product data transferred from Commerce Foundation to Commerce SaaS Services. Users of Product Recommendations, Live Search, and/or Catalog Service can conveniently monitor product sync statuses and initiate data resynchronization from a unified dashboard. This feature provides valuable insights into the availability of product data for your storefront, ensuring it can be promptly displayed to your shoppers.




Who is this for?
The Data Management Dashboards are available for all Commerce merchants using at least one of Commerce SaaS Services:  Product Recommendations, Live Search, and/or Catalog Service. Commerce SaaS Services are available at no additional cost for Commerce merchants with an active license. 



Using the Data Management Dashboard
The Data Management Dashboard is located at System > Data Transfer > Data Management Dashboard.

Once you get to this page you will see 3 taps, one for each SaaS service. 

Which data can you see?
For each SaaS service you will see:





The Sync status panel reports the number of products that have been transferred from Commerce Foundation to any of the SaaS services within the last three hours. If you make infrequent updates to your catalog, this value is frequently zero.

If there is a synchronization process in progress, you can click the Refresh button to get an updated count.


Guidance
Once you've updated products on Commerce Foundation, you should observe data transferring to SaaS services according to your system configuration. As the process initiates, the synced products count will indicate the number of products sent to SaaS services. Please note that the time taken to complete the transfer will vary based on your catalog size and the volume of updated data.

When the number of Products processed matches the number of updated products, it signifies that the transfer has been completed.

Products in SaaS service panel


The product count panel reflects the total number of catalog products available to the service (tap) you are looking at.

Guidance
The Product Recommendations and Live Search dashboards display the total number of displayable products (add a link to displayable products description). Catalog Service does not filter products by displayable, so if you have both Catalog Service and Live Search or Product Recommendations installed, it is possible for the two panels to show two different values for the product count.

List of synced products


The Synced Products table provides details about the products in the Commerce index. By default, this table is sorted by 'Last Updated' to help you identify which products were recently updated.

To find a specific product, use the Search by SKU field.



To control what columns are displayed, click Customize Table on the right of the table.



You will be able to choose the columns you want to display



To see details of a product you can click on the product from the table, a lightbox will be displayed showing the selected product data:



Which actions can I do?
Resync catalog data
You should implement a regular schedule (add link to doc on how to set up a data sync) for syncing catalog data to ensure that your Commerce SaaS Services are always up-to-date with the latest product information. During certain crucial circumstances, there's an option to manually initiate a catalog data resynchronization from Commerce Foundation to SaaS Services. While we don't advise frequent use of this tool, it offers flexibility in the following scenarios if required:

Whenever significant changes are made to your product catalog, such as adding new products, updating product details, or modifying categories, it's prudent to trigger a resynchronization to reflect these changes in your Commerce SaaS Services.
If you notice any discrepancies or performance issues in displaying product data on your storefronts, consider resyncing catalog data as a troubleshooting measure to ensure smooth operations.

Following any updates or changes to integrations between Commerce Foundation and SaaS Services, it's advisable to perform a resynchronization to maintain data consistency and integrity across platforms.

When deploying customizations or configurations that impact product data management or synchronization processes, initiate a resynchronization to ensure that all changes are accurately reflected in your Commerce SaaS Services.

By adhering to these guidelines and proactively resyncing catalog data as needed, you can maintain data consistency, accuracy, and reliability across your Adobe Commerce ecosystem.

To resync catalog data use the Settings button on the right side of the page, it will open the dialog where you can resynchronize the catalog data.





Resynching catalog data forces the service to refetch data from the Commerce database to SaaS services. This action is usually used during the first-time onboarding when the catalog sync has not run for a couple of hours.












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
