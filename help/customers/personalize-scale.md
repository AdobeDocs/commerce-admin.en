---
title: Personalization at scale
description: Learn which features in Adobe Commerce allow you to create a personalized experience for your shoppers.
feature: Customers, Storefront, Personalization
---
# Personalization at scale

​Personalization at scale allows businesses the ability to personalize the shopping experience for every customer touchpoint based on immediate context and previously observed behavior. The goal is to present the most relevant and personalized experience possible every time.

To understand the benefits of delivering a personalized shopping experience, download the [_Getting Started with Personalization at Scale_](https://business.adobe.com/resources/reports/getting-started-with-personalization-at-scale.html) report.

Creating a personalized shopping experience requires you to learn about the type of data needed to understand the customer context. From there, you learn about Adobe Commerce features that use that data to unlock the customer insights you need to create the personalized shopping experience.

The following image illustrates the concepts involved in personalizing the shopping experience:

![Building a personalization pipeline](assets/personalization-journey.png){width="700" zoomable="yes"}

This article discusses each of the above concepts in more detail.

## How do you personalize the shopping experience

Successful personalization starts with customer context. In this section, you learn about the data types that are available to help you build the customer context.

### Behavioral data

Behavioral data answers the question: How do shoppers interact with your site? For example:

- What products and categories are my shoppers most interested in?
- What kind of search queriers are my shoppers most engaged in?
- What is the order life cycle like? Are my shoppers returning products?
- Are my shoppers adding products to the cart and then abandoning it?
- Are my shoppers using a desktop or mobile browser?

While this list is not exhaustive, it helps us shed light on the diverse domains where behavioral information can be captured

### Customer profile data

Customer profile data answers the question: Who are your shoppers? For example, what is their:

- Name
- Gender
- Address
- Loyalty status
- Phone number
- Email address

### Segment data

Segment data answers the question: Which segments do your shoppers qualify for. For example, are they:

- Eligible for upgrades
- Cross-channel shoppers
- Prospects for new products
- Gold, silver, or bronze loyalty members

The above data forms the foundation of the Commerce customer context, which helps you know what products your customers are viewing and ultimately purchasing. You can then target their interests and personalize their experience.

In the next two sections, you learn how you can use this data in [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) and in [native Commerce features](#using-commerce-data-in-native-commerce-features) to personalize the shopping experience.

## Using Commerce data in Adobe Experience Platform

The Adobe Experience Platform provides a suite of technologies, that when hydrated with data from your Commerce store, can distribute that data through the Edge Network to other Adobe DX products to unlock insights into your shopper's buying behavior. With these deep insights, you can create a more personalized shopping experience across all channels.

![How data flows to the Experience Platform edge](assets/commerce-edge.png){width="700" zoomable="yes"}

To learn more about how you can send your Commerce data to the Experience Platform, see [Data Connection](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/overview.html).

In the following section, you learn how you can use native Commerce features, such as Product Recommendations and Live Search to create that personalized shopping experience. You will also learn about a feature called [!DNL Audience Activation], which uses data from a product available in the Experience Platform called Real-Time CDP. While Real-Time CDP is not native to Commerce, its information can be ingested into Commerce through the [[!DNL Audience Activation]](https://experienceleague.adobe.com/docs/commerce-admin/customers/audience-activation.html) extension.

## Using Commerce data in native Commerce features

Sitting on top of the customer context data in Commerce is the experience layer. This layer is composed of the Commerce features that can act on the context data and is divided into four main pillars:

- Product discovery
- Site content
- Offers and campaigns
- Measurement

The following sections describe each of the pillars in the experience layer in more detail and provides the list of available Commerce features you can use to turn the context data into actionable insights.

### Product discovery

The product discovery pillar contains merchandising services that are [deployed as SaaS](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html). These are features that allow you to use behavioral data, product attributes, and inventory levels to automatically personalize product discovery across search results, product recommendations, and browsing pages. These features all use [Adobe Sensei AI](https://business.adobe.com/products/sensei/adobe-sensei.html).

#### Commerce features to use

You can use the following Commerce features to assist in product discovery.

- **Product Recommendations** - Displays AI-fueled product recommendations based on shopper behavior, trends, product similarity and more. When combined with your Adobe Commerce catalog, product recommendations deliver a highly engaging, relevant, and personalized experience. [Learn more](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html).

- **Live Search** - Uses AI ranking algorithms to personalize and optimize search results based on a shopper's on-site behavioral actions, boosting search relevance and conversion. [Learn more](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html).

- **Category Merchandising** - Accessed from the Live Search Admin, category merchandising uses AI to automatically rerank the sequence of products on each category page to boost relevance and conversion for every shopper. You can create and manage AI-powered rules to automatically rerank product sequencing on category pages according to shopper actions and affinities. [Learn more](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/category-merch.html).

### Site content

The site content pillar refers to the ability to deploy personalized dynamic content blocks based on the current customer browsing your site.

#### Commerce features to use

You can use the following Commerce features to assist in personalizing site content.

- **Dynamic blocks informed by native Commerce features** - Allows you to deliver personalized site content based on logic configured in price rules and customer segments. [Learn more](https://experienceleague.adobe.com/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks.html).

- **Dynamic blocks informed by Real-Time CDP audiences** - Enables merchants to deliver personalized site content based on audiences configured in Real-Time CDP. [Learn more](https://experienceleague.adobe.com/docs/commerce-admin/customers/audience-activation.html).

### Offers and campaigns

The offers and campaigns pillar lets you deploy personalized promotional content based on segment data.

#### Commerce features to use

You can use the following Commerce features to assist in creating personalized offers and campaigns.

- **Cart price rules** - Lets you apply discounts to items in the shopping cart based on a set of conditions. [Learn more](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

- **Dynamic blocks informed by native Commerce features** - Allows you to display personalized banner promotions based on customer segments configured natively in Commerce. [Learn more](https://experienceleague.adobe.com/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks.html).

- **Dynamic blocks informed by Real-Time CDP audiences** - Allows you to display personalized promotions based on audiences configured in Real-Time CDP. [Learn more](https://experienceleague.adobe.com/docs/commerce-admin/customers/audience-activation.html).

### Measurement

The measurement pillar uses data intelligence to better understand your business including revenue, channel and merchandise performance, promotions, and so on.

#### Commerce features to use

You can use the following Commerce feature to assist in measuring the success of any personalization at scale implementation.

- **Adobe Commerce Intelligence** - (Formerly known as Magento Business Intelligence) is a cloud platform that provides best practice insights to help you make data-driven decisions and take clear and informed actions. Adobe Commerce Intelligence can analyze your data to help you answer questions about order growth, customer behavior, and the effectiveness of promotional strategies. [Learn more](https://experienceleague.adobe.com/docs/commerce-business-intelligence/mbi/getting-started.html).
