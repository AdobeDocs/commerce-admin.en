---
title: '[!DNL Google Analytics]'
description: Learn how you can use [!DNL Google Analytics] to gather useful metrics for your Commerce sites.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
---
# [!DNL Google Analytics]

[!DNL Google Analytics] gives you the ability to define additional custom dimensions and metrics for tracking, with support for offline and mobile app interactions, and access to ongoing updates. [!DNL Google Analytics] 4 is Google's next-generation measurement solution, and is replacing [!DNL Universal Analytics]. On July 1, 2023, standard Universal Analytics properties will stop processing new hits.

>[!NOTE]
>
>If your business is subject to privacy regulations such as the [General Data Protection Regulation](../getting-started/compliance-gdpr.md) and/or the [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), see [Google Privacy Settings](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>If you enable the [Cookie Restriction Mode](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] does not collect data about visitors unless they have accepted cookies.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### Step 1: Set up [!UICONTROL Google Analytics] 4

If you do not already have a [!DNL Google Analytics] 4 setup for your site, follow one of these methods:

- [Set up Analytics data collection for the first time](https://support.google.com/analytics/answer/9304153)
- [Add Google Analytics 4 to a site with [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### Step 2: Complete the Commerce configuration

1. Log in to the Admin for your Commerce store.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Google API]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Google GTag]** section.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Google Analytics4]** subsection and do the following:

   - Set **[!UICONTROL Enable]** to `Yes`.

   - Leave the **[!UICONTROL Account type]** as `Google Analytics4`.

   - Enter your **[!UICONTROL Measurement ID]**. To learn more, see [Google Analytics Help](https://support.google.com/analytics/answer/9539598).

   - If you want to conduct A/B testing and other performance tests on your content, set **Content Experiments** to `Yes`.

   ![Sales configuration - Google API for Google Analytics 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

1. When complete, click **[!UICONTROL Save Config]**.

## Google Universal Analytics

>[!IMPORTANT]
>
>On July 1, 2023, standard Universal Analytics properties will no longer process data. If you still rely on [!DNL Universal Analytics], it is recommended that you [prepare to use Google Analytics 4](https://support.google.com/analytics/answer/10759417) going forward.

### Step 1: Set up Google Universal Analytics

Visit the Google website, and sign up for a [Google Universal Analytics][1] account.

### Step 2: Complete the Commerce configuration

1. Log in to the Admin for your Commerce store.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Google API]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Google Analytics]** section and do the following:

   - Set **[!UICONTROL Enable]** to `Yes`.

   - Enter your [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - If you want to conduct A/B testing and other performance tests on your content, set **[!UICONTROL Content Experiments]** to `Yes`.

   ![Sales configuration - Google API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png)<!-- zoom -->

1. When complete, click **[!UICONTROL Save Config]**.

## Enhanced Ecommerce

Enhanced Ecommerce is a plugin for [!DNL Google Universal Analytics] that gives you insight into the shopping and purchasing behavior of your customers. You can use Enhanced Ecommerce to produce reports about key customer activities, such as when customers add items the cart, begin the checkout process, or complete a purchase. You can also identify and analyze patterns of shoppers who abandon their carts without making a purchase.

The following instructions show how to configure [!DNL Google Tag Manager] with [!DNL Universal Analytics] to produce Enhanced Ecommerce data and reports.

![Example storefront in debug mode - Google tags fired in shopping cart](./assets/storefront-google-tags-fired-checkout.png)<!-- zoom -->

### Step 1. Sign up for Google accounts

1. Sign up for a [Google Tag Manager](google-tag-manager.md) account, and complete the Commerce configuration.

1. Sign up for a new [Google Universal Analytics][1] account.

### Step 2. Configure Enhanced Ecommerce

1. Sign in to your Google Universal Analytics account.

1. Create a property for Enhanced Ecommerce analytics with the following settings:

   - Status: ON
   - Related Products: ON
   - Enable Enhanced Ecommerce Reporting: ON
   - Checkout Labeling: (not required)

1. When complete, click **[!UICONTROL Submit]**.

   ![Google Universal Analytics - enable Enhanced Ecommerce](./assets/google-universal-analytics-ecommerce-setup1.png)<!-- zoom -->

### Step 3. Create tags and triggers

1. Sign in to your [!DNL Google Tag Manager] account and create the following triggers:

    |Name|Event Type|Filter|
    |--- |--- |--- |
    |`addToCart`|Custom Event||
    |`checkout`|Custom Event||
    |`checkout only`|Page View|Page URL matches RegEx /checkout/.*|
    |`checkoutOption`|Custom Event||
    |`gtm.dom`|Custom Event||
    |`productClick`|Custom Event||
    |`promotionClick`|Custom Event||
    |`removeFromCart`|Custom Event||

>[!NOTE]
>
>The [!UICONTROL Checkout] event is triggered for the built into Commerce basic payment methods only (such as `Check / Money Order` and `Cash On Delivery Payment`). This event is not executed for `PayPal checkout` and other external payment methods, which use redirection to the checkout from external resources.

1. Create the following Universal Analytics tags with the same basic configuration.

   - Universal Analytics Tags

      |Name|Type|Firing triggers|
      |--- |--- |--- |
      |`Add to cart tracking`|Universal Analytics|addToCart|
      |`Checkout option tracking`|Universal Analytics|checkoutOption|
      |`Checkout tracking`|Universal Analytics|checkout|
      |`Pageview tracking`|Universal Analytics|gtm.dom|
      |`Product click tracking`|Universal Analytics|productClick|
      |`Promo click tracking`|Universal Analytics|promotionClick|
      |`Remove from cart tracking`|Universal Analytics|removeFromCart|

   - Basic Tag Configuration

      |Setting|Value|
      |--- |--- |
      |[!UICONTROL Product]|Google Analytics|
      |[!UICONTROL Tag Type]|Universal Analytics|
      |[!UICONTROL Tracking ID]|UA-XXX (The tracking ID from your Universal Analytics account.)|
      |[!UICONTROL Enable Enhanced Ecommerce Features]|True|
      |[!UICONTROL Use data layer]|True|
      |[!UICONTROL Use Debug version]|True|

1. Complete the individual tracking configurations.

   - Enter the following **[!UICONTROL Add to Cart]** tracking settings:

      |Setting|Value|
      |--- |--- |
      |[!UICONTROL Track Type]|Event|
      |[!UICONTROL Category]|Ecommerce|
      |[!UICONTROL Action]|Add to Cart|
      |[!UICONTROL Trigger]|addToCart|

   - Enter the following **[!UICONTROL Checkout option]** tracking settings:

      |Setting|Value|
      |--- |--- |
      |[!UICONTROL Track Type]|Event|
      |[!UICONTROL Category]|Ecommerce|
      |[!UICONTROL Action]|Checkout Option|
      |[!UICONTROL Trigger]|checkoutOption|

   - Enter the following **[!UICONTROL PageView]** tracking settings:

      |Setting|Value|
      |--- |--- |
      |[!UICONTROL Track Type]|PageView|
      |[!UICONTROL Trigger]|gtm.dom|

   - Complete the following **[!UICONTROL Product Click]** tracking configuration:

      |Setting|Value|
      |--- |--- |
      |[!UICONTROL Track Type]|Event|
      |[!UICONTROL Category]|Ecommerce|
      |[!UICONTROL Action]|Product Click|
      |[!UICONTROL Trigger]|productClick|

   - Complete the following **[!UICONTROL Promotion Click]** tracking configuration:

      |Setting|Value|
      |--- |--- |
      |[!UICONTROL Track Type]|Event|
      |[!UICONTROL Category]|Ecommerce|
      |[!UICONTROL Action]|Promotion Click|
      |[!UICONTROL Trigger]|promotionClick|

   - Complete the following **[!UICONTROL Remove from Cart]** tracking configuration:

      |Setting|Value|
      |--- |--- |
      |[!UICONTROL Track Type]|Event|
      |[!UICONTROL Category]|Ecommerce|
      |[!UICONTROL Action]|Remove from Cart|
      |[!UICONTROL Trigger]|removeFromCart|

1. When complete, click **[!UICONTROL Preview]** and verify that the tags work correctly.

1. After verifying the settings, click **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en
