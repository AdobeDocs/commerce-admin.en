---
title: Customer reports
description: Customer reports available in Adobe Commerce and Magento Open Source provide insight into customer activity during a specified time period or date range.
exl-id: 7bee414b-b605-4aed-9749-78bb8056a6a4
feature: Customers, Reporting
TQID: https://experienceleague.adobe.com/i6BKd2v1P3eT8BkNn4poW5BhsrH8bG86kNN58v-TRIQ
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
subfeature_v2:
  - id: a0ba824e-0c31-421c-9b6f-aa500e5c18a1
    internal-label: Customer reports
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
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Customer reports

Customer reports provide insight into customer activity during a specified time period or date range.

## [!UICONTROL Order Total Report]

The [!UICONTROL Order Total Report] shows customer orders for a specified time interval or date range. The report includes the number of orders per customer, average order amount, and total amount.

On the _Admin_ sidebar, go to **[!UICONTROL Reports]** > _[!UICONTROL Customers]_ > **[!UICONTROL Order Total]**.

![Order Total Report](./assets/customers-order-total.png){width="600"}

### Workspace controls

|Control|Description|
|--- |--- |
|[!UICONTROL From / To]| Used to define a search for the orders based on the start and end date.|
|[!UICONTROL Show By]|Defines the granularity of the order record splitting. Options: `Month` / `Day` / `Year` |
|[!UICONTROL Refresh]|Updates the grid to the specified filters.|
|[!UICONTROL Export]|Exports the selected records as a CSV or Excel XML file.|
|[!UICONTROL Scope]| Used to set the site or store for which the report is generated.|

{style="table-layout:auto"}

### Column descriptions

|Column|Description|
|--- |--- |
|[!UICONTROL Interval]|The order total interval, by `Month` / `Day` / `Year`.|
|[!UICONTROL Customer]|The name of the customer who placed the orders.|
|[!UICONTROL Orders]|The number of orders for the specified interval.|
|[!UICONTROL Average]|Average order amount. This amount is always calculated for product prices **excluding tax** even if catalog product prices, order subtotal and order total include tax. As a result, the amount shown in the report is different than the amount shown in order details in cases where order totals include tax.|
|[!UICONTROL Total]|The sum of all orders for the period. This amount is always calculated for product prices **excluding tax** even if catalog product prices, order subtotal and order total include tax. As a result, the total shown in the report is different than the amount shown in order details in cases where order totals include tax.|

{style="table-layout:auto"}

## [!UICONTROL Order Count Report]

The [!UICONTROL Order Count Report] shows the number of orders per customer for a specified time interval or date range. The report includes the number of orders per customer, average order amount, and total amount.

On the _Admin_ sidebar, go to **[!UICONTROL Reports]** > _[!UICONTROL Customers]_ > **[!UICONTROL Order Count]**.

![Order Count Report](./assets/customer-order-count.png){width="600"}

### Workspace controls

|Control|Description|
|--- |--- |
|[!UICONTROL From / To]| Used to define a search for the orders based on the start and end date.|
|[!UICONTROL Show By]|Defines the granularity of the order record splitting. Options: `Month` / `Day` / `Year` |
|[!UICONTROL Refresh]|Updates the grid to the specified filters.|
|[!UICONTROL Export]|Exports the selected records as a CSV or Excel XML file.|
|[!UICONTROL Scope]| Used to set the site or store for which the report is generated.|

{style="table-layout:auto"}

### Column descriptions

|Column|Description|
|--- |--- |
|[!UICONTROL Interval]|The order count interval, by `Month` / `Day` / `Year`.|
|[!UICONTROL Customer]|The customer who placed the order.|
|[!UICONTROL Orders]|The number of orders for the specified interval.|
|[!UICONTROL Average]|Average order amount. This amount is always calculated for product prices **excluding tax** even if catalog product prices, order subtotal and order total include tax. As a result, the amount shown in the report is different than the amount shown in order details in cases where order totals include tax.|
|[!UICONTROL Total]|The sum of all orders for the period. This amount is always calculated for product prices **excluding tax** even if catalog product prices, order subtotal and order total include tax. As a result, the total shown in the report is different than the amount shown in order details in cases where order totals include tas.|

{style="table-layout:auto"}

## [!UICONTROL New Accounts Report]

The [!UICONTROL New Accounts Report] shows the number of new customer accounts opened during a specified time interval or date range.

On the _Admin_ sidebar, go to **[!UICONTROL Reports]** > _[!UICONTROL Customers]_ > **[!UICONTROL New]**.

![New Accounts Report](./assets/customers-new-accounts.png){width="600"}

### Workspace controls

|Control|Description|
|--- |--- |
|[!UICONTROL From / To]|Used to define a search for the new accounts based on the start and end date.|
|[!UICONTROL Show By]|Defines the granularity of the order record splitting. Options: Month / Day / Year |
|[!UICONTROL Refresh]|Updates the grid to the specified filters.|
|[!UICONTROL Export]|Exports the selected records as a CSV or Excel XML file.|
|[!UICONTROL Scope]|Used to set the site or store for which the report is generated.|

{style="table-layout:auto"}

### Column descriptions

|Column|Description|
|--- |--- |
|[!UICONTROL Interval]|New account creation interval, by Month / Day / Year.|
|[!UICONTROL New Accounts]|The number of new accounts created in a certain interval.|

{style="table-layout:auto"}

## [!UICONTROL Customer Wish List Report]

[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."}

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)

The [!UICONTROL Customer Wish List Report] provides information about customer wish lists.

On the _Admin_ sidebar, go to **[!UICONTROL Reports]** > _[!UICONTROL Customers]_ > **[!UICONTROL Wish Lists]**.

![Wish List Report](./assets/customer-wish-list.png){width="600"}

### Workspace controls

|Control|Description|
|--- |--- |
|[!UICONTROL Scope]|Used to set the site or store for which the report is generated.|
|[!UICONTROL Search]| Initiates a search by the specified parameters.|
|[!UICONTROL Reset Filter]| Initiates a reset of all search parameters.|
|[!UICONTROL Per Page]| Sets the number of records displayed in a single page. |
|[!UICONTROL Export]|Exports the selected records as a CSV or Excel XML file.|
|[!UICONTROL From / To]|Used to define a search for the wish lists based on the start and end date.|
|[!UICONTROL Wishlist]| Initiates a wish list search by name.|
|[!UICONTROL Status]| The status of the wish list. Options: `Private` / `Public` |
|[!UICONTROL Comment]| Initiates a search by text in the wish list comments.|

{style="table-layout:auto"}

### Column descriptions

|Column|Description|
|--- |--- |
|[!UICONTROL Added]| Date the wish list was created.|
|[!UICONTROL Customer]| First and last name of the customer who created the wish list.|
|[!UICONTROL Wishlist]| Name of the wish list.|
|[!UICONTROL Status]| The status of the wish list. Options: `Private` / `Public` |
|[!UICONTROL Product]| Name of the product added to the wish list.|
|[!UICONTROL SKU]| SKU of the product added to the wish list.|
|[!UICONTROL Comment]| The comment text that was entered when the wish list was created.|

{style="table-layout:auto"}

## [!UICONTROL Customer Segment Report]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)

The [!UICONTROL Customer Segment Report] provides information about the number of customers in each segment.

On the _Admin_ sidebar, go to **[!UICONTROL Reports]** > _[!UICONTROL Customers]_ > **[!UICONTROL Segments]**.

![Segments Report](./assets/customers-segments.png){width="600"}

### Workspace controls

|Control|Description|
|--- |--- |
|[!UICONTROL Search]| Initiates a search by the specified parameters.|
|[!UICONTROL Reset Filter]| Initiates a reset of all search parameters.|
|[!UICONTROL Action]| Initiates the display of segments by parameters. Options: `Action` / `View Combined Report`|
|[!UICONTROL Per Page]| Sets the number of records displayed in a single page.|

{style="table-layout:auto"}

### Column descriptions

|Column|Description|
|--- |--- |
|[!UICONTROL ID]|A unique numeric identifier that is assigned to each segment.|
|[!UICONTROL Segment]|Segment name.|
|[!UICONTROL Status]|Segment status. Options: `Active` / `Inactive`|
|[!UICONTROL Website]|Website to which the segment is assigned.|
|[!UICONTROL Customers]|Number of customers assigned to the segment.|

{style="table-layout:auto"}
