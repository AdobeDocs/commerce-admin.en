---
title: Create Compelling, Personalized Experiences at Scale
description: Learn which features in Adobe [!DNL Commerce] allow you to create a personalized experience for your shoppers.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
---
# Create Compelling, Personalized Experiences at Scale

Adobe [!DNL Commerce] gives you a powerful toolkit to personalize every customer touchpoint, boosting shopper engagement, conversion, and revenue.

In this article, you learn:

- What is personalization? 
- What data do I need to achieve personalization? 
- How does Adobe [!DNL Commerce] unlock personalization? 
- Available personalization use-cases 

## What is personalization?

Personalization means tailoring aspects of each customer's buying experience to meet their unique needs, context, and preferences. Personalization is not limited to content on the site, or recommending best-fit products, but rather encompasses all touchpoints across the customer journey, including: 

- **Campaigns and Communications** - Delivering relevant and consistent messaging via campaigns and communications 
- **Product Discovery** - Showing the right products to the right customers in just the right moments 
- **Promotions and Offers** - Targeting promotions and offers to drive each customer to convert 
- **Content Experiences** - Tailoring site content to feel hyper-relevant to each customer and their journey 

![Types of Personalization](assets/types-personalization.png){width="700" zoomable="yes"}

While these types of personalized experiences can seem achievable for a small subset of customers, personalizing at scale for thousands or millions of customers across every touchpoint and channel, all in real-time can feel impossible. In the following sections, you learn how Adobe [!DNL Commerce] and Adobe Experience Cloud can help. 

## What data do I need to achieve personalization? 

Effective personalization requires context or signals that provide information about customers that can then be used to modify their experience. The following table provides the various data types and the role that Adobe [!DNL Commerce] plays in supporting the gathering and activating of that data.  

|Data Types|Storefront Data (Behavioral Events)|Back office Data (Server-Side Events)|Customer Profile and Segment Data|
|---|---|---|---|
|**Definition**|Clicks or actions customers take on your site.|Information on the lifecycle and details of each order (past and current).|Who your shoppers are and what segments that they qualify for.| 
|**Events Captured by Adobe Commerce**|[pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#removefromrequisitionlist)|**Order Status**:<br>[orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCancelled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**Order History**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU, Name, Price Quantity, Discount<br>- Product Category<br>- Payment Amount, Type, Currency<br>- Shipping Method and Amount<br>- Refund ID, Amount, Currency<br>- Return Reason, Condition, Resolution<br>- Address<br>- Email|[**Profile record**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord): (Name, Gender, Address, Loyalty Status, Phone Number, Email Address)<br>**Account Status**:<br>[accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountdeleted)| 

With all of this rich, first-party [!DNL Commerce] data, you are ready to start targeting and personalizing each shopper's experience. Let's explore how Adobe [!DNL Commerce] and Adobe Experience Cloud help you create personalized experiences and the use-cases you can activate. 

## How does Adobe [!DNL Commerce] empower personalization?

Adobe [!DNL Commerce] Data Sharing enables you to collect and share the data types above to other Adobe Experience Cloud products to power unified customer profiles and audiences, personalized campaigns, and rich analytics and insights.  

![How data flows to the Experience Platform edge](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce] Data Sharing includes two key components:

1. [Data Connection](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview): Share storefront, back office, and customer profile data from Adobe [!DNL Commerce] to the Adobe Experience Platform edge network for use across Adobe Experience Cloud applications, including: 

    - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview): Stitch customer data from across sources (ERP, CRM, POS) into unified profiles and create rules-based or AI-based segments. 
    - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started): Launch personalized omni-channel journeys, including email campaigns, SMS, push notifications, and more.  
    - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) and [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview): Gain insights into the customer and the business.
    - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro): Test and optimize content, recommended products, offers, navigation, and more. 

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation): Use [!DNL Real-Time CDP] audiences to personalize dynamic content blocks, promotions, and related product rules on your Adobe [!DNL Commerce] site.

### Out-of-the-box Personalization: Get started with native Adobe [!DNL Commerce] features 

Adobe [!DNL Commerce] delivers powerful personalization with its native out-of-the-box capabilities. The following table describes [!DNL Commerce] features you can activate immediately to get started on your personalization journey.  

- **Personalized Product Discovery**

    - [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview): Personalize and optimize search results based on a shopper's onsite behavioral actions and affinities with AI-powered search. 
    - [Intelligent Category Merchandising](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch): AI-driven product ranking on category pages based on a shopper's onsite behavioral actions and affinities. 
    - [Product Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview): AI-powered product recommendations based on shopper behavior, trends, and affinities. 
    - [Related Product Rules](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules): Define custom rules to display products from your catalog to drive cross- and up-sell. 

- **Personalized Site Content**

    - [Dynamic Content Blocks](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks): Display personalized content blocks (for example, banners) based on customer segments in Adobe Commerce. 

- **Personalized Offers and Promotions**

    - [Cart Price Rules](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart): Apply discounts to items in the shopping cart based on a set of conditions, including customer segments in Adobe Commerce. 

- **Insights and Measurement**

    - [Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started): Understand how your personalization strategies are working and improve over time.  

## Top personalization use-cases

Adobe [!DNL Commerce] customers are using out-of-the-box capabilities and sharing data to Adobe Experience Cloud for a variety of use-cases. The following sections highlight those top use-cases and how they are implemented using Adobe [!DNL Commerce] Only or [!DNL Commerce] plus Experience Cloud apps.

### Personalized campaigns and communications

|Use-Case|Solution|
|---|---|
|**Abandoned Cart and Browse** - Deliver a personalized re-engagement email or notification when a customer abandons their cart or browsing session after demonstrating high engagement|**Adobe [!DNL Commerce] Only**:<br>[Email Reminders](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] with Adobe Journey Optimizer**:<br>[!DNL Commerce] data serves as the trigger for an omni-channel abandonment journey. Personalize that journey based on customer attributes, what they abandoned, other shopping behaviors, and past purchases.<br>Commerce with Adobe Journey Optimizer and Real-Time CDP: Tailor abandonment campaigns based on unified customer profiles and centrally managed audiences, for example creating a high abandonment rate audience.|
|**Centralized Audience Creation** - Create rules-based or AI-powered audiences based on onsite behavior, past-purchases, profile attributes, category affinities, loyalty status, customer value and more|**Adobe [!DNL Commerce] Only**:<br>Gather customer profile information when [!DNL Commerce] customers create accounts. Create rules-based [customer segments](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) and customer groups to personalize content and promotions.<br>**Adobe [!DNL Commerce] with Adobe Real-Time CDP**:<br> [Unified profiles](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) from across data sources and channels; rules-based or AI-powered audiences.|
|**Personalized Email/SMS Offer Based on Shopper Behavior** - Send personalized offers to customers via targeted email based on past purchases and shopper behavior for example, send offer for products or categories customers have viewed or engaged with.|**Adobe [!DNL Commerce] Only**:<br>Export data for use with marketing automation solutions.<br>**Adobe [!DNL Commerce] with Adobe Journey Optimizer and Real-Time CDP**:<br>[!DNL Commerce] data serves as the trigger for email or SMS offers and provides signals (shopper behaviors) to personalize based upon. Real-Time CDP is not required, but generally these offers and campaigns are created around audiences, which would be created and managed within Real-Time CDP.|
|**Cross or Upsell Compatible Products/Brands** - If a customer purchases one product or brand that is compatible or indicates high affinity towards another product or brand, send a campaign (email/SMS) to drive cross-sell conversion.|**Adobe [!DNL Commerce] Only**:<br>Use Adobe [!DNL Commerce] [Product Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) to recommend specific products on the site. You can also use [Related Product Rules](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) to suggest other products.<br>**[!DNL Commerce] with Target**:<br>Adobe Target also has a built-in product recommendation engine with powerful capabilities such as category affinity. This can be used for cross or upsell.<br>**[!DNL Commerce] with Adobe Journey Optimizer**:<br>Use Target or [!DNL Commerce] to determine products to recommend, then deliver via Adobe Journey Optimizer.|

### Personalized site experiences

|Use-Case|Solution|
|---|---|
|**Personalized Site Content** - Personalize site banners and other page content based on shopper actions, such as product browsing and category affinities. Deploy best-fit content based on results of A/B tests or business goals.|**Adobe [!DNL Commerce] Only**:<br>Deploy segment-specific [dynamic content blocks](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks).<br>**[!DNL Commerce] with Real-Time CDP**:<br>Use [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) to deploy audience-specific dynamic content blocks that respond to real-time actions and unified customer profile data, while centrally managing profiles and audiences in Real-Time CDP.<br>**[!DNL Commerce] with Target**:<br>Personalize every part of the site experience, including content, navigation items, full page layouts and more using Adobe [!DNL Commerce] data in Adobe Target. A/B test content, automatically select and deploy winning content for each customer.<br>**[!DNL Commerce] with AEM Assets**:<br>Store all of your content in Adobe Experience Manager Assets. Natively access that content from within Adobe Commerce. Use GenAI to create content variations to personalize for different segments or audiences.|
|**Personalized Onsite Offer Based on Behavior** - Personalize promotions based on shopper actions, such as product browsing and category affinities. Deploy the next best offer based on results of A/B tests or business goals.|**Adobe [!DNL Commerce] Only**:<br>Deploy segment-specific catalog and [cart price rules](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] with Real-Time CDP**:<br>Use [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) to deploy audience-specific offers, while centrally managing profiles/audiences in Real-Time CDP.<br>Commerce with Target: Use offer decisioning to determine which offer to deploy, A/B test or set business goals to guide offers deployed in Adobe Commerce.|

### Analytics and insights

|Use-Case|Solution|
|---|---|
|**Customer Behavior by Channel** - Understand the nuances of how customers engage in each channel (web, in-person, app, other) to impact marketing strategies for each channel; understand the shopper funnel and weaknesses in the customer experience.|**Adobe [!DNL Commerce] Only**:<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) provides rich analytics on the digital [!DNL Commerce] channel, but not across channels or broader pieces of the customer journey.<br>**Adobe [!DNL Commerce] with Customer Journey Analytics**:<br>[!DNL Commerce] data feeds data dashboards for full rich detail on all stages of the customer experience (across channels). Understand every touchpoint and the broader funnel to identify weak points in the customer journey where customers may fall off.|
|**Purchase Trends** - Understand purchase behaviors over a specific time frame (for example, shopper basket analysis, product analysis) to identify trends, seasonality, and optimize marketing based on historical purchase patterns.|**Adobe [!DNL Commerce] Only**:<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) provides rich analytics on the digital [!DNL Commerce] channel, but not across channels or broader pieces of the customer journey.<br>**Adobe [!DNL Commerce] with Customer Journey Analytics**:<br>[!DNL Commerce] data feeds data dashboards for full rich detail on all stages of the customer experience (across channels). Understand every touchpoint and the broader funnel to identify weak points in the customer journey where customers may fall off.|

## Example Use-Case

In the following example, you learn about the parts needed to create an abandoned cart and browse email.

### Abandoned Cart and Browse 

Learn how to deliver a personalized re-engagement email or notification if a cart or browser session has been abandoned. You will use data generated from customers that have viewed a number of products and categories, engaged with a product, or spent time on a page.

#### What data should I consider using?

To build an abandoned cart or browse email or notification, you need data from storefront and back office events.

#### Relevant Storefront Events:  

- [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#pageview)
- [productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtocart)
- [openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#opencart)
- [startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#startcheckout)
- [completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#completecheckout)

#### Relevant Back office Events:  

- [orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderplaced)
- [Order history](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/connect-data#send-historical-order-data)

#### What can I do with just Adobe Commerce? 

Adobe [!DNL Commerce] enables you to set up rules-based email reminders, which can serve as cart or browse abandonment emails. Learn how here.  

#### What can I do with Adobe [!DNL Commerce] and Experience Cloud? 

- **Adobe [!DNL Commerce] with Adobe Journey Optimizer** - Using Adobe [!DNL Commerce] with Adobe Journey Optimizer lets you use [!DNL Commerce] data as the trigger for an omni-channel abandonment journey. You can personalize that journey based on customer attributes, items they abandoned, other shopping behaviors, and past purchase behaviors.  

- **Adobe Commerce, Adobe Journey Optimizer, and Adobe Real-Time CDP** - Adding Real-Time CDP would allow you to further refine abandonment campaigns based on unified customer profiles and centrally managed rules-based or AI-powered audiences. For example, you could create:  

    - A "strong converters" audience that has a low abandonment rate
    - A "high consideration" audience that has revisited certain categories multiple times
    - A "high potential" audience that has high spend and loyalty but has recently abandoned 

#### What have other customers achieved?

Adobe [!DNL Commerce] customers have achieved significant business impacts from implementing personalized abandonment campaigns using Adobe [!DNL Commerce], Adobe [!DNL Journey Optimizer], and Adobe [!DNL Real-Time CDP].

A global, multi-brand apparel retailers achieved:

- 1.9x conversion on click from new campaigns
- 57% increase in revenue flowing from omni-channel abandonment journeys
- 41% increase in conversion rate of re-engagement campaigns
- 1000+ new shoppers engaged per week

A global beverage company achieved:

- 36% re-engagement email open rates
- 21% lift in clickthrough rates
- 8.5% lift in conversion rate
- 89% of re-engaged abandoners convert

#### Ready to implement?

Learn how you can use Adobe Journey Optimizer to [send an abandoned cart email](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/using-ajo).
