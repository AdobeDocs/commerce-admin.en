# Recommendation Types

[!DNL Product Recommendations] provides a large set of recommendations that you can deploy to various pages on your site. All recommendation types are data-driven. They are based on behavioral data, product attribute data, and metrics. For easy reference, recommendation types are grouped as follows:

- [Personalized](#personalized)
- [Cross-sells and up-sells](#crossup)
- [Popularity](#popularity)
- [High-performing](#highperf)

As a best practice, Adobe recommends the following guidelines when using recommendations:

- Diversify your recommendation types. Customers start ignoring recommendations if they suggest the same products over and over again.

- Do not deploy the same recommendations to your cart page and order confirmation page. Consider using `Most Added to Cart` for the cart page and `Bought This, Bought That` for the order confirmation page.

- Keep your site tidy. Do not deploy more than three recommendation units on the same page.

- If your store sells clothing, the `More like this` recommendation can suggest gender-specific products that do not match the gender of the product being viewed. Consider using this recommendation type only for non-clothing categories.

>[!NOTE]
>
>For more information about the events described in this article, see [storefront events](https://developer.adobe.com/commerce/services/shared-services/storefront-events/#product-recommendations){target="_blank"} in the developer documentation.

## Data requirements and behavior

Product Recommendations is a data-driven system that relies on behavioral data collected from your storefront. The quality and quantity of recommendations depend on the amount of event data available.

>[!IMPORTANT]
>
>Most recommendation types require sufficient behavioral data (such as product views, add-to-cart actions, and purchases) to generate meaningful results. The system typically needs several days of active shopper activity to build accurate recommendations. See [readiness indicators](create.md#readiness-indicators) to learn how site traffic helps to populate the various recommendation types.

### What happens with insufficient data

When there is not enough event data to generate recommendations, the system can:

- Return empty results for the recommendation unit.
- Trigger [backup recommendations](/help/optimizer/setup/events/overview.md#backup-recommendations), such as showing `Most viewed` products when personalized recommendations are not yet available.
- Display fewer products than [configured](create.md) in the recommendation unit.

## Personalized {#personalized}

These recommendation types recommend products based on the specific shopper's behavioral history on your site. For example, if a shopper previously browsed for a jacket or purchased a jacket on your site, these recommendations continue from their previous activity and recommend other jackets or similar products.

>[!NOTE]
>
>Personalized recommendations require shoppers to have an established behavioral history. New visitors or shoppers without sufficient interaction history will see [backup recommendations](/help/optimizer/setup/events/overview.md#backup-recommendations), such as Most viewed products until they generate enough behavioral signals on your site.

|Type|Description|
|---|---|
|Recommended for you|Recommends products based on each shopper's current and previous onsite behavior. Displays highly relevant recommendations based on the shopper's browsing and purchase history. This recommendation type is effective on the home page where most shoppers begin their journey on a site. For first-time shoppers on your site who have not generated any signal to personalize their experience, Adobe Commerce shows products based on the Most viewed recommendation type. When the shopper starts to interact with the products on the site, however, recommended products adjust in real time to their behavior.<br/><br/>**Where used:**<br/>- Home page<br/>- Category<br/><br/>**Suggested labels:**<br/> - Just for you<br/>- Recommended for you<br/>- Inspired by your shopping trends|
|Recently viewed|Displays products most recently viewed by the shopper, based on browser history. Any deleted products are removed by the recommendation unit. The recommendation unit is not displayed if there is no browser history, or not enough history when filter rules are applied. If the results contain fewer products than are configured, the recommendation unit displays only the products returned.<br/><br/>**Where used:**<br/>-  Home page<br/>-  Category<br/>-  Product detail<br/>-  Cart<br/>-  Confirmation<br/><br/>**Suggested labels:**<br/>-  Recently viewed<br/>-  Take another look|

## Cross-sells and up-sells {#crossup}

These recommendation types are social-proof driven to help shoppers find what others liked or product-driven to help them find other similar products. The recommended products often complement the selected product.

>[!NOTE]
>
>The "viewed this, viewed that," "viewed this, bought that," and "bought this, bought that" recommendation types do not use a simple-occurrence metric but rather a more sophisticated collaborative-filtering algorithm that looks for *interesting similarities* that are not skewed towards popular products. The data used to inform these recommendation types is based on the shopper's aggregate behavior derived from multiple sessions on your site. The data is not based on shopper behavior derived from a single in-session occurrence on your site. These recommendation types help shoppers find those adjacent products that might not be obvious to pair with the currently viewed product.
>
>These recommendation types require substantial cross-product interaction data to identify meaningful correlations. Stores with limited product catalog diversity or low traffic can show fewer recommendations until sufficient behavioral patterns emerge.

|Type|Description|
|---|---|
|Viewed this, viewed that|Recommends products that shoppers view disproportionately more often with the currently viewed product.<br/><br/>**Where used:**<br/>- Product detail<br/>- Cart<br/>- Confirmation<br/><br/>**Suggested labels:**<br/>- Customers who viewed this product also viewed (PDP)|
|Viewed this, bought that|Recommends products that shoppers tend to buy disproportionately more often after viewing the current product. This type helps guide shoppers to discover products that they might not have otherwise noticed.<br/><br/>**Where used:**<br/>- Product detail<br/>- Cart<br/>- Confirmation<br/><br/>**Suggested labels:**<br/>- Customers who viewed this ultimately bought<br/>- Customers ultimately purchased<br/>- What do others buy after viewing this product?|
|Bought this, bought that|Recommends products that shoppers buy disproportionately more often with the currently viewed product. This type displays highly relevant products shoppers can add to their cart by aggregating what other shoppers have bought with the current product.<br/><br/>**Where used:**<br/>- Product detail<br/>- Cart<br/>- Confirmation<br/><br/>**Suggested labels:**<br/>- Get everything that you need<br/>- Don't forget these<br/>- Frequently bought together|
|More like this|Recommends products based on similar metadata such as name, description, category assignment, and attributes. By evaluating the attributes for the products being viewed, this type recommends similar products in the same category. For example, if a shopper is browsing yoga mats, other products in the equipment category are recommended. Because this recommendation type does not distinguish genders, it is not recommended for apparel, fashion, or other gender-specific verticals.<br/><br/>**Where used:**<br/>- Product detail<br/>- Cart<br/>- Confirmation<br/><br/>**Suggested labels:**<br/> - More products like this<br/>- Similar to this|
|Visual similarity|Recommends similar looking products to the product being viewed. This recommendation type is most useful where images and visual aspects of the products are important parts of the shopping experience.<br/><br/>**Where used:**<br>- Product detail<br/><br/>**Suggested labels:**<br/> -You may also like<br/> -We found other products you might like<br/> -Inspired by this style|

## Popularity {#popularity}

These recommendation types recommend products that are the most popular or trending within the last seven days.

>[!NOTE]
>
>Popularity-based recommendations require sufficient event data from your storefront. If your store is new or has low traffic, these recommendation types can return limited results or no results until adequate behavioral data has been collected. To ensure optimal performance, monitor your [data readiness indicator](/help/optimizer/manage-results/recommendation-performance.md).

|Type|Description|
|---|---|
|Most viewed|Recommends products that were viewed the most by counting the number of sessions where a view action occurred within the last seven days.<br/><br/>**Where used:**<br/>- Home page<br/>- Category<br/>- Product detail<br/>- Cart<br/>- Confirmation<br/><br/>**Suggested labels:**<br/>- Most popular<br/>- Trending<br/>- Popular right now<br/>- Recently popular<br/>- Popular products inspired by this product (PDP)<br/>- Top sellers|
|Most purchased|Recommends products most frequently purchased by shoppers within the last seven days.<br/><br/>**Where used:**<br/>- Home page<br/>- Category<br/>- Product detail<br/>- Cart<br/>- Confirmation<br/><br/>**Suggested labels:**<br/> - Most popular<br/>- Trending<br/>- Popular right now<br/>- Recently popular<br/>- Popular products inspired by this product (PDP)<br/>- Top sellers|
|Most added to cart|Recommends products most frequently added to carts by shoppers within the last seven days. This recommendation type can be used on all pages.<br/><br/>**Where used:**<br/>- Home page<br/>- Category<br/>- Product detail<br/>- Cart<br/>- Confirmation<br/><br/>**Suggested labels:**<br/> - Most popular<br/>- Trending<br/>- Popular right now<br/>- Recently popular<br/>- Popular products inspired by this product (PDP)<br/>- Top sellers|
|Trending|Recommends products based on the recent momentum of a product's popularity across your site within the last seven days.<br/><br/>Adobe AI aggregates browsing and purchase data across your site to determine and rank which products are the most recently popular with your shoppers. Because Trending analyzes recent product momentum, it is an effective recommendation type for catalogs that have a high turnover. If your catalog is more static, it might not be as useful unless the shopping patterns of your audience are highly variable.<br/><br/>When used on the home page, Trending recommends products that are recently popular across the entire site. Trending does not display products that are consistently popular, but rather those that have recently become popular. For example, if you have an email marketing campaign promoting certain products, the popularity increase generated by the email increases the likelihood that the promoted products classify as trending.<br/><br/>**Where used:**<br/>- Home page<br/>- Category<br/>- Product detail<br/>- Cart<br/>- Confirmation<br/><br/>**Suggested labels:**<br/>- Trending<br/>- Trending now<br/>- Recently trending<br/>- Hot products<br/>- Trending related products (PDP)|

## High performing {#highperf}

These recommendation types recommend top performing products based on success criteria like add-to-cart or conversion rates.

>[!NOTE]
>
>High-performing recommendation types rely on conversion data (purchases and add-to-cart actions). New stores or stores with low conversion volumes need to collect data over 7-14 days before these recommendations become effective.

|Type|Description|
|---|---|
|View to purchase conversion|Recommends products with the highest view-to-purchase conversion rate. Of all the shopper sessions that registered a product view, what is the proportion that eventually registered a purchase by the shopper.<br/><br/>**Where used:**<br/>- Home page<br/>- Category<br/>- Product detail<br/>- Cart<br/>- Confirmation<br/><br/>**Suggested labels:**<br/>- Top sellers<br/>- Popular products<br/>- You might be interested in|
|View to cart conversion|Recommends products with the highest view-to-cart conversion rate. Of all the shopper sessions that registered a product view, what is the proportion that eventually registered an add to cart by the shopper.<br/><br/>**Where used:**<br/>- Home page<br/>- Category<br/>- Product detail<br/>- Cart<br/>- Confirmation<br/><br/>**Suggested labels:**<br/> - Top sellers<br/>- Popular products<br/>- You might be interested in|
