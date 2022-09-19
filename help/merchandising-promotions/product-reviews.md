---
title: Product reviews
description: <placeholder>
---
# Product reviews

Product reviews help to build a sense of community, and are considered more credible than any advertising money can buy. In fact, some search engines give sites with product reviews a higher ranking than those without. For those who find your site by searching for a specific product, a product review is essentially the landing page of your store. Product reviews help people find your store, keep them engaged, and often lead to sales.

Commerce includes a native product reviews capability that you can manage from the Admin. You can also use an extension from the [Commerce Marketplace](../getting-started/commerce-marketplace.md) to use a hosted review management system.

>[!NOTE]
>
>Adobe Commerce and Magento Open Source releases 2.4.0 through 2.4.3 included the Yotpo vendor-developed extension. Starting with the 2.4.4 release, this extension is no longer bundled with the core release and must be installed and updated from the Commerce Marketplace. The Marketplace also provides access to current documentation provided by the extension developer.
><br><br>
>If you have the bundled extension enabled and configured, you must update your composer.json file as part of the 2.4.4 upgrade process and to manage extension updates going forward. See [Upgrade modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) in the _Upgrade Guide_ for more information.

## Product reviews on the storefront

When the native Product Reviews function is enabled, customers can write reviews for any product in your catalog. Reviews can be written from the product page by clicking:

- **Add Your Review** for products with existing reviews.

- **Be the first to review this product** for products with no existing reviews.

The Reviews tab lists all current reviews and the form that was used to submit a review.

Your configuration determines whether customers must open an account with your store before writing product reviews or if they can submit reviews as guests. Requiring reviewers to open an account prevents anonymous submissions and improves the quality of reviews.

![Example storefront - Add Your Review](./assets/storefront-review-this-product.png)<!-- zoom -->

The number of stars indicates the product's satisfaction rating. Visitors can click the link to read the reviews and write their own. As an incentive, customers can receive reward points for submitting a review. When a review is submitted, it is sent to the Admin for moderation. When approved, the review is published in your store.

![Example storefront - Reviews tab](./assets/storefront-reviews-tab.png)<!-- zoom -->

## Enable product review features

The Commerce Product Reviews function is enabled by default.

>[!NOTE]
>
>To set these fields to `No` and disable Commerce Product Reviews, you must clear the **Use system value** checkboxes.

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Catalog** and select **Catalog** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Product Reviews** section.

   ![Catalog configuration - Commerce product reviews](./assets/product-reviews-config.png)<!-- zoom -->

1. Set **Enabled** to `Yes`.

   This is the default setting that enables product reviews.

1. Set **Allow Guests to Write Reviews** to `Yes`.

   This is the default setting that determines if customers must open an account with your store to be able to write product reviews.

1. When complete, click **Save Config**.
