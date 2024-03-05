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

### Storefront data

Storefront data, also called behavioral or browser data, answers the question: How do shoppers interact with your site? For example

- What products and categories are my shoppers most interested in?
- What kind of search queriers are my shoppers most engaged in?
- Are my shoppers adding products to the cart and then abandoning it?
- Are my shoppers using a desktop or mobile browser?

The following storefront events capture data that can help you answer these questions:

- View page
- Search request
- Search response
- View category
- View product page
- Add to cart
- View cart
- Sign in
- Sign out
- Start checkout
- Complete checkout
- Create requisition list
- Add to requisition list
- Remove from requisition list
- Quote accepted

### Back office data

Back office data, also called server-side data, answers the question: What is the order life cycle for my shoppers? For example:

- Are there products that are purchased more frequently based on season?
- Are my shoppers returning products?
- How can I calculate lifetime customer value?

The following back office events capture data that can help you answer these questions:

- Order placed
- Order returned
- Order shipped
- Order canceled
- Order history (past five years of transactions)

### Customer profile and segment data

Customer profile data answers the question: Who are your shoppers? Which segments do your shoppers qualify for? For example:

- Name
- Gender
- Address
- Loyalty status
- Phone number
- Email address
- Loyalty status
- Phone number
- Email address
- Eligibility for upgrades
- Cross-channel shoppers
- Prospects for new products
- Gold, silver, or bronze loyalty members

The following profile events capture data that can help you answer these questions:

- Profile record
- Account created
- Account updated
- Account deleted

The above data forms the foundation of the Commerce customer and order context, which helps you know what products your customers are viewing and ultimately purchasing. You can then target their interests and personalize their experience. In the next section, you learn what types of personalized experiences you can engage in with  your shoppers.

## Types of personalized experiences

The customer and order context data in Commerce fuels the following types of personalized experiences:

|Experience|Description|
|---|---|
|**Product discovery**|Contains merchandising services that are [deployed as SaaS](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html). These are features that allow you to use behavioral data, product attributes, and inventory levels to automatically personalize product discovery across search results, product recommendations, and browsing pages. These features all use [Adobe Sensei AI](https://business.adobe.com/products/sensei/adobe-sensei.html).|
|**Site content**|Refers to the ability to deploy personalized dynamic content blocks based on the current customer browsing your site.|
|**Offers and campaigns**|Lets you deploy personalized promotional content based on segment data.|
|**Measurement**|Uses data intelligence to better understand your business including revenue, channel and merchandise performance, promotions, and so on.|

In the next two sections, you learn how you can use this data to create personalized experiences in [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) and in [native Commerce features](#using-commerce-data-in-native-commerce-features).

## Using Commerce data in Adobe Experience Platform

To create a personalized experience for your shoppers across all channels, send your Commerce data to the Experience Platform Edge Network using the [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/overview.html) extension.

![How data flows to the Experience Platform edge](assets/commerce-edge.png){width="700" zoomable="yes"}

In the above image, your storefront, back office, and customer profile data is sent to the Experience Platform edge using an SDK, API, and a source connector. You do not need to fully understand how those pieces work as the extension handles the data sharing complexity for you. When the event data is at the edge, you can pull that data into other Experience Platform applications.

The following table highlights some of the Experience Platform applications available and how those applications use your Commerce data.

|Experience|Application|How Commerce Data is Used|
|---|---|---|
|**Site content**|[Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview.html)|Adobe Commerce data fuels unified customer profiles, with Real-Time CDP stitching data from across sources (ERP, CRM, CMS, POS) into singular profiles. Real-Time CDP can also create both rules-based and AI-based segments to then use across your marketing solution set. You can also use Real-Time CDP audiences to personalize content blocks, promotions, and related product rules. See [[!DNL Audience Activation]](../customers/audience-activation.md) to learn more.​|
||[Adobe [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/introduction/intro.html)|Adobe Commerce data can be activated in Adobe [!DNL Target] for testing, optimization, and creating dynamic landing pages. You can personalize the order that content is shown on a page, such as descriptions, specifications, reviews, and recommended products based on the Commerce data sent.|
|**Offers and campaigns**|[Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/docs/journey-optimizer/using/get-started/get-started.html)|Adobe Commerce behavioral and back office data can serve as a trigger for personalized omni-channel journeys, including email campaigns, SMS, push notifications and more.​|
|**Measurement**|[Adobe [!DNL Analytics]](https://experienceleague.adobe.com/docs/analytics/analyze/admin-overview/analytics-overview.html) and [Customer [!DNL Journey Analytics]](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html)|Commerce sends both storefront and back-office data to Customer [!DNL Journey Analytics] (and only storefront data to Adobe [!DNL Analytics]) to allow for richer analysis beyond basic metrics in Adobe Commerce Intelligence, such as revenue, merchandise, and promotions.​|


To learn more about how you can send your Commerce data to the Experience Platform, see [Data Connection](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/overview.html).

## Using Commerce data in native Commerce features

In the following section, you learn how you can use native Commerce features, such as Product Recommendations and Live Search to create a personalized shopping experience. You will also learn about a feature called [!DNL Audience Activation], which uses data from a product available in the Experience Platform called Real-Time CDP, as mentioned [previously](#using-commerce-data-in-adobe-experience-platform). While Real-Time CDP is not native to Commerce, its information can be ingested into Commerce through the [[!DNL Audience Activation]](../customers/audience-activation.md) extension.

The following table highlights the Commerce features available to turn the Commerce customer and order context data into actionable insights.

|Experience|Feature|Description|
|---|---|---|
|**Product discovery**|[Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)|Uses AI ranking algorithms to personalize and optimize search results based on a shopper's on-site behavioral actions, boosting search relevance and conversion.|
||[Product Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)|Displays AI-fueled product recommendations based on shopper behavior, trends, product similarity and more. When combined with your Adobe Commerce catalog, product recommendations deliver a highly engaging, relevant, and personalized experience.|
||[Category Merchandising](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/category-merch.html)|Accessed from the Live Search Admin, category merchandising uses AI to automatically rerank the sequence of products on each category page to boost relevance and conversion for every shopper. You can create and manage AI-powered rules to automatically rerank product sequencing on category pages according to shopper actions and affinities.|
|**Site content**|[Dynamic blocks informed by native Commerce features](https://experienceleague.adobe.com/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks.html)|Allows you to deliver personalized site content based on logic configured in price rules and customer segments.|
||[Dynamic blocks informed by Real-Time CDP audiences](../customers/audience-activation.md)|Enables merchants to deliver personalized site content based on audiences configured in Real-Time CDP.|
|**Offers and campaigns**|[Cart price rules](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html)|Lets you apply discounts to items in the shopping cart based on a set of conditions.|
||[Dynamic blocks informed by native Commerce features](https://experienceleague.adobe.com/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks.html)|Allows you to display personalized banner promotions based on customer segments configured natively in Commerce.|
||[Dynamic blocks informed by Real-Time CDP audiences](../customers/audience-activation.md)|Allows you to display personalized promotions based on audiences configured in Real-Time CDP.|
|**Measurement**|[Adobe Commerce Intelligence](https://experienceleague.adobe.com/docs/commerce-business-intelligence/mbi/getting-started.html)|(Formerly known as Magento Business Intelligence) is a cloud platform that provides best practice insights to help you make data-driven decisions and take clear and informed actions. Adobe Commerce Intelligence can analyze your data to help you answer questions about order growth, customer behavior, and the effectiveness of promotional strategies.|
