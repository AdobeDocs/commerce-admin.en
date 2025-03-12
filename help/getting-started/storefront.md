---
title: What is the storefront?
description: Learn about the pages and functional elements that your store can provide to support the shopping experience for your customers.
exl-id: 1c64888f-2bc0-4e2e-b7da-0e7182ea67e0
feature: Storefront
---
# What is the storefront?

Within your Adobe Commerce or Magento Open Source implementation, the storefront is the external, public-facing part of your store. It provides the content and functional components that your customers use to shop and purchase.

The path customers take to a sale is sometimes called the _path to purchase_, and your storefront includes the components for customers to complete this path. The following sections provide an overview of the basic page types that provide strategic value---the places customers usually visit while shopping in your store. As you review them, consider different store features that can be used at each stage of the customer journey.

## Commerce Storefront

With the introduction of the [!DNL **Commerce Storefront powered by Edge Delivery Services**], Adobe offers a high-performance, scalable, and reliable storefront that leverages cutting-edge technology to deliver superior speed and user experience.

- **Enhanced performance**: Hosting storefronts on Edge Delivery Services ensures faster load times and improved site performance, which can lead to higher conversion rates and better SEO rankings.

- **Scalability**: The architecture supports seamless scaling to handle increased traffic and larger product catalogs without compromising performance.

- **Flexibility**: The storefront is highly customizable, allowing businesses to tailor the shopping experience to their unique needs.

- **Improved user experience**: Features such as advanced caching, real-time updates, and personalized content delivery contribute to a smoother and more engaging shopping experience.

### Key features

The Commerce Storefront powered by Edge Delivery Services offers several key features that benefit both merchants and developers. These features enable businesses to create engaging shopping experiences while maintaining the flexibility to customize and scale their storefronts according to their needs.

For more detailed information and guidance on setting up and optimizing your Commerce Storefront, see the [Adobe Commerce Storefront Documentation](https://experienceleague.adobe.com/en/docs/commerce).

>[!BEGINTABS]

>[!TAB Merchants]

The Commerce Storefront powered by Edge Delivery Services provides an intuitive document-based authoring experience that makes it easy for merchants to create and manage content. Using familiar tools like Microsoft Word or Google Docs, merchants can create rich content while maintaining version control and collaborating with team members.

- **Simplified content creation**: Create and edit content using familiar document-based authoring tools, like Microsift Word or Google Docs.
- **Real-time preview**: See changes instantly with live preview capabilities before publishing.
- **Version control**: Track content changes and easily roll back to previous versions.
- **Collaborative workflow**: Multiple team members can work on content simultaneously with built-in review processes.
- **Content reuse**: Create content blocks that can be reused across multiple pages to maintain consistency.

>[!TAB Developers]

Headless implementation enables developers to decouple the frontend presentation layer from the backend commerce functionality, allowing for flexible, custom storefronts built with modern technologies while leveraging Commerce's robust backend services.

- **API-first architecture**: Build custom frontend experiences using modern frameworks while leveraging Commerce backend services.
- **Composable components**: Create and deploy modular, reusable components that can be assembled into different page layouts.
- **Extensible platform**: Add custom functionality through APIs and webhooks without modifying core code.
- **Modern development tools**: Use industry-standard development tools and workflows for faster implementation and deployment.

>[!ENDTABS]

>[!NOTE]
>
>While the Commerce Storefront offers numerous advantages, Adobe continues to support the original Luma-based storefront. Businesses currently using Luma can continue to operate without disruption and have the option to transition to the new storefront at their own pace. The remaining sections on this page are based on Luma examples.

## Home page

Did you know that most people spend only a few seconds on a page before they decide to stay or go somewhere else? It is not long to make an impression. Studies show that people also love photographs, especially of other people. Whatever design you choose, everything on your home page should move visitors along toward the next step in the sales process. The idea is to guide their attention in a cohesive flow from one point of interest to the next.

![Example storefront home page](./assets/storefront-homepage-full.png){width="700"}

## Catalog page

Catalog page listings typically have small product images and brief descriptions, and can be formatted as a list or as a grid. You can add blocks, videos, and keyword-rich descriptions, and also create special designs for a promotion or season. You might create a special category to feature a lifestyle or brand that is a curated collection of products from different categories.

The initial product description usually gives shoppers enough information to merit a closer look. People who know what they want can add the product to their carts and go. Customers who shop while logged in to their accounts enjoy a personalized shopping experience.

![Collection page on the storefront](./assets/storefront-collection-page.png){width="700"}

## Search results

Did you know that people who use search are nearly twice as likely to make a purchase as people who rely on navigation alone? You might consider these shoppers to be _pre-qualified_.

### [!DNL Live Search]

With [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview) for Adobe Commerce, your store delivers a fast, super-relevant, and intuitive search experience, and is available for Adobe Commerce at no additional charge.

![Live Search example - search as you type](./assets/storefront-search-as-you-type.png){width="700"}

### Standard catalog search

With [standard catalog search](../catalog/search.md), your store includes a Search box in the upper-right corner, and a link to Advanced Search in the footer. All search terms that shoppers submit are saved, so you can see exactly what they're looking for. You can offer suggestions, and enter synonyms and common misspellings. Then, display a specific page when a search term is entered.

![Example of standard catalog search results](./assets/storefront-search-results-page-full.png){width="700"}

## Product page

The product page has a lot going on! The first thing that catches your eye on the product page is the main image with a high-resolution zoom and thumbnail gallery. In addition to the price and availability, there is a tabbed section with more information and a list of related products.

![Example storefront product page](./assets/storefront-product-page-full-m.png){width="700"}

## Shopping cart

The cart shows the order total, including any discount coupons, estimated shipping, and tax. These features make it a great place to display trust badges and seals. You can also use the cart page as an opportunity for one final offer. For example, you can set up cross-sell items that appear as impulse purchase options when specific products are in the cart.

![Example storefront shopping cart page](./assets/storefront-cart-full.png){width="700"}

## Checkout page

The checkout process consists of two steps:

1. Shipping Information

   The first step of the checkout process is for the customer to complete the shipping address information, and to choose the shipping method. If the customer has an account, the shipping address is entered automatically, but can be changed if needed.
   If a guest customer enters an email address that is recognized as previously registered, the sign-in prompt is displayed if the [!UICONTROL Enable Guest Checkout Login] field in the store configuration is set to `Yes` (see [[!UICONTROL Checkout Options]](../configuration-reference/sales/checkout.md#checkout-options) in the _Configuration Reference Guide_). However, this setting can expose customer information to unauthenticated users.

   ![Example storefront checkout page](./assets/storefront-checkout-shipping-full.png){width="700"}

1. Review and Payment Information

   The second step of the checkout process is for the customer to choose the payment method and optionally apply a discount code.

   >[!NOTE]
   >
   >Although [!DNL Commerce] allows configuring multiple coupon codes, a customer may apply only one coupon code to the cart. (See the [Coupon codes](../merchandising-promotions/price-rules-cart-coupon.md#coupon-codes) for more information.)

   ![Example storefront checkout page](./assets/storefront-checkout-payment-full.png){width="700"}

The progress bar at the top of the page follows each step of the checkout process, and the _Order Summary_ shows the information that was entered up to this point.

>[!NOTE]
>
>The exception to a two-step checkout applies to virtual and/or downloadable products. If there are only these types of products in the shopping cart, checkout is automatically transformed to a one-step procedure, because shipping information is not required.
