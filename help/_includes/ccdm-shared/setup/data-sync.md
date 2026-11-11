# Catalog sync

The **Data Sync** page displays an overview of the synchronization status for product data transferred from your data source (your existing Commerce catalog, Product Information Management (PIM) system, Enterprise Resource Planning (ERP) system, and so on) into the Merchandising Services data layer.

The **Data Sync** page provides valuable insights into the availability of product data for your storefront, ensuring that it can be promptly displayed to your shoppers.

## Access the Data Sync workspace

How you open the *Data Sync* workspace depends on the product you use:

- **Adobe Commerce Admin** (Adobe Commerce as a Cloud Service)—Select *Stores* > **Catalog Sync**.
- **Adobe Commerce Optimizer Studio**—Select *Store setup* > **Data Sync**.

![Data Sync](/help/assets/ccdm-shared/setup/data-sync.png)

The **Data Sync** page contains the following fields:

| Field | Description |
| --- | --- |
| Catalog source | Specific locale for the synced data. |
| [!DNL Catalog Service] | Displays the latest sync update, the total products received, a search field, and a table of the synced products for [!DNL Catalog Service]. |
| Product Discovery | Displays the latest sync update, the total products received, a search field, and a table of the synced products for Search. |
| Recommendations | Displays the latest sync update, the total products received, a search field, and a table of the synced products for Recommendations. |
| Products received in the last 3 hours | Displays the number of products that have been transferred from the catalog source to the Merchandising Services data layer within the last three hours. If you make infrequent updates to your catalog, this value is frequently zero. |
| Total products in catalog | Reflects the total number of catalog products available in the Merchandising Services data layer. |
| Synced products | Provides details about the products synced to the Merchandising Services data layer. By default, this table is sorted by 'Last Updated'. To find a specific product, use the **[!UICONTROL Search by Name or SKU]** field. |

## List of synced products

To see the details of a synced product in JSON format, click on the code icon ![Code link](/help/assets/ccdm-shared/setup/data-sync-details.png) on the row of the product from the synced products table.

![Synced Product Details](/help/assets/ccdm-shared/setup/synced-products.png)

## Resync catalog data

If you do not see specific products on the **Data Sync** page, you need to initiate a resync from your upstream system. However, keep in mind that a resync can increase the load on hardware resources. Nevertheless, resyncing your catalog might be necessary in the following scenarios:

- When significant changes are made to your product catalog, such as adding new products, updating product details, or modifying categories

- If you notice any discrepancies or performance issues in displaying product data on your storefronts

>[!IMPORTANT]
>
>The time it takes to complete the sync varies based on your catalog size and the volume of data updated.

## Verify that data synchronization is working

For projects that use Adobe Commerce as the upstream data source, you can monitor the data export process and initiate resync operations from the Data Feed Sync Status page. For details, see [Data Feed Sync Status monitoring](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/data-transfer/data-sync/data-feed-sync-status).
