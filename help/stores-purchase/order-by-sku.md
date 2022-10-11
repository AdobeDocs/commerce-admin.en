---
title: Order by SKU
description: <Add description here>
---
# Order by SKU

{{ee-feature}}

Order by SKU is a [widget](../content-design/widgets.md) that can be displayed in the store as a convenience for all shoppers, or made available to only those in specific customer groups. Shoppers can either enter the SKU and quantity information directly into the Order by SKU block, or upload a csv file from their customer account. Regardless of the configuration, Order by SKU is always available to store administrators.

![Order by SKU in the Storefront](./assets/storefront-order-by-sku.png)<!-- zoom -->

## Configure order by SKU

1. On the _Admin_ sidebar, click **Stores**.

1. In the _Settings_ section, choose **Configuration**.

1. In the _Sales_ section in the left panel, choose **Sales**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the _Order by SKU Settings_ section.

1. Set **Enable Order by SKU on my Account in Storefront** to one of the following:

    - **Yes, for Everyone** – The Order by SKU block is available in the store for every shopper.
    - **Yes, for Specified Customer Groups** – Order by SKU is available only to members of a specific customer group, such as `Wholesale`.
    - **No** – The Order by SKU block does not appear in the storefront, and the Order by SKU page is not available in the  customer account.

      ![Order by SKU Settings](../configuration-reference/sales/assets/sales-order-by-sku-settings.png)<!-- zoom -->

1. Click **Save Config**.

To enable the **Order by SKU** function, disable the **Quick Order** function:

1. Go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel under _General_, choose **B2B Features**

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **B2B Features** section.

1. Set **Enable Quick Order** to `No`.

   The **Quick Order** feature allows customers and guests to quickly place orders based on SKU or product name.

## Order by SKU storefront experience

When the functionality is configured for the store, customers can order by SKU from any page that includes the _Order by SKU_ widget or from their account dashboard.

### Order by SKU from the page block

1. In the _Order by SKU_ block, the customer enters the **SKU** and **Qty** of the item to be ordered.

1. To add another item, clicks **Add Row** and repeat the process.

1. Clicks **Add to Cart**.

### Order by SKU from a customer account

1. From the storefront, the customer logs in to their account.

1. In the panel on the left, chooses **Order by SKU**.

1. Adds individual items according to preference:

   **Adds each item by SKU**:

      - Enters the **SKU** and **Qty** of the item to be ordered.

      - To add additional items as needed, clicks _Add Row_ ![Plus sign button](../assets/button-add-item.png) and repeats for as many items as necessary.

   **Uploads a CSV file of multiple items**:

      - Prepares a CSV file that includes columns for SKU and Qty.

      - To upload the CSV file, clicks **Choose File** and select the file to upload.

      - Clicks **Add to Cart**.
