---
title: Gift card product
description: <placeholder>
---
# Gift card product

{{ee-feature}}

Each gift card has a unique code, which can be redeemed by only one customer during checkout. A [code pool](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html#step-3-establish-the-gift-card-code-pool) must be established before gift cards can be sold. See [Gift Card Workflow](https://docs.magento.com/user-guide/catalog/product-gift-card-workflow.html) for information about how gift cards are redeemed in the shopping cart.

![Gift card product page](./assets/storefront-giftcard-product-page.png)<!-- zoom -->

There are three kinds of gift card products:

- **Virtual** - A virtual gift card is sent to the recipient's email address, which is required during the purchase of the gift card. A shipping address is not necessary.

- **Physical** - A physical gift card is shipped to recipient's address, which is required during the purchase of the gift card.

- **Combined** - A [combined gift card](https://docs.magento.com/user-guide/catalog/product-gift-card-workflow.html) is shipped and emailed to the recipient. The recipient's email and shipping address is required during the purchase of the gift card.

## Create a gift card product

The following instructions demonstrate the process of creating a gift card using a [product template](attribute-sets.md), required fields, and basic settings. Each required field is marked with a red asterisk (`*`). When you finish the basics, you can complete the other product settings as needed.

## Step 1: Choose the product type

1. On the _Admin_ sidebar, go to **Catalog** > **Products**.

1. In the upper-right corner on the _Add Product_ ( ![Menu arrow](../assets/icon-menu-down-arrow-red.png)<!-- {: width="25px"} --> ) menu, choose **Gift Card**.

   ![Add Gift Card](./assets/product-add-gift-card.png)<!-- zoom -->

## Step 2: Choose the attribute set

You can use the default `Gift Card` attribute set or choose another. To choose the attribute set that is used as a template for the product, do one of the following:

- For **Search**, enter the name of the attribute set.
- In the list, choose the attribute set that you want to use.

![Choose Attribute Set](./assets/product-create-choose-attribute-set-gift-card.png)<!-- zoom -->

## Step 3: Complete the required settings

1. Enter a **Product Name** for the gift card.

   You might also indicate the type of gift card in the name. For example, _Luma Virtual Gift Card_.

1. Enter a **SKU** for the product.

   By default, the Product Name is used as the default SKU.

1. Set **Card Type** to one of the following:

   - `Virtual` - Virtual gift cards are delivered by email to the recipient.
   - `Physical` - Physical gift cards can be mass produced in advance and embossed with unique codes.
   - `Combined` - A combined gift card has the characteristics of both a virtual and physical gift card.

   ![Gift Card Type](./assets/product-create-gift-card-type.png)<!-- zoom -->

1. To offer the customer a choice of fixed amounts, click **Add Amount** and enter the first fixed value of the card as a decimal.

   Repeat this step to enter the selection of fixed amounts.

   ![Gift Card Amounts](./assets/product-create-gift-card-amounts.png)<!-- zoom -->

1. To give customers the ability to set the value of the gift card, do the following:

   - Set **Open Amount** to `Yes`.

   - To define the range of minimum and maximum acceptable values, enter the **Open Amount From** and **To** values.

   You can create gift cards with fixed pricing, open amount pricing, or both.

## Step 4: Complete the basic settings

1. For a physical or combined gift card, enter the **Quantity** in stock.

1. If the gift card that is to be shipped, enter the **Weight** of the package.

1. In the **Categories** field, choose `Gift Card`.

There might be additional individual attributes that describe the product. The selection varies attribute set, and you can complete them later.

## Step 5: Complete the gift card information

The _Gift Card Information_ section of the product settings can be used to override the [gift card configuration](https://docs.magento.com/user-guide/configuration/sales/gift-cards.html) settings that determine how the card is managed.

1. Scroll down to the _Gift Card Information_ section.

   The default settings in this section are determined by the system configuration.

   ![Gift Card Information](./assets/product-gift-card-information.png)<!-- zoom -->

1. Change additional fields according to how you want the gift card to function:

   - **Treat Balance as Store Credit** - Determines if the gift card holder can redeem the balance as store credit.

   - **Lifetime (days)** - Determines the number of days after purchase until the gift card expires. If you do not want to set a limit for the lifetime of the card, leave this field blank.

   - **Allow Message** - Determines if the purchaser of the gift card can enter a message for to the recipient. A gift message can be included for both virtual (emailed) and physical (shipped) gift cards.

   - **Email Template** - Determines the email template that is used for the notification sent to the recipient of a gift card.

## Step 6: Complete the product information

Complete the information in the following sections as needed:

- [Content](product-content.md)
- [Images and Videos](product-images-and-video.md)
- [Related Products, Up-Sells, and Cross-Sells](related-products-up-sells-cross-sells.md)
- [Search Engine Optimization](product-search-engine-optimization.md)
- [Customizable Options](settings-advanced-custom-options.md)
- [Products in Websites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Gift Options](product-gift-options.md)

## Step 7: Publish the product

1. If you are ready to publish the product in the catalog, set the **Enable Product** switch to `Yes`.

1. Do one of the following:

   **Method 1:** Save and Preview

   - In the upper-right corner, click **Save**.

   - To view the product in your store, choose **Customer View** on the _Admin_ ( ![Menu arrow](../assets/icon-menu-down-arrow-black.png) ) menu,

   ![Customer View](./assets/admin-customer-view.png)<!-- zoom -->

   **Method 2:** Save and Close

   On the _Save_ ( ![Menu arrow](../assets/icon-menu-down-arrow-red.png)<!-- {: width="25px"} --> ) menu, choose **Save & Close**.

   ![Save & Close](./assets/product-edit-save-close.png)<!-- zoom -->

## Things to remember

- A _code pool_ of unique numbers must be generated before a gift card can be offered for sale.

- The three types of gift cards are Virtual, Physical, and Combined.

- Gift cards can be set to `Redeemable` or `Non-Redeemable`.

- The lifetime of a gift card can be unlimited or set to a number of days.

- The value of a gift card can be set to a fixed amount or set to an open amount with a minimum and maximum value.

- A gift card account for the customer can be created when the order is placed or at the time of invoice.
