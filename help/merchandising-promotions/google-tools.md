---
title: Google site tools
description: Learn about the Google tools integrations that you can use to optimize your content, analyze your traffic, and connect your catalog to shopping aggregators and marketplaces.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
---
# Google site tools

Your store configuration is integrated with the following Google tools to help optimize your content, analyze your traffic, and connect your catalog to shopping aggregators and marketplaces.

- [Google Analytics](google-analytics.md) - Use _Google Universal Analytics_ to define additional custom dimensions and metrics for tracking, with support for offline and mobile app interactions, and access to ongoing updates.

- [Google Content Experiments](google-content-experiments.md) - Set up an A/B test for products, categories, or content pages using Google Analytics Content Experiments.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) Use Google Tag Manager to manage the many tags related to marketing campaign events.

- [Google AdWords](google-adwords.md) - Create a Google AdWords campaign and track conversions for your store.

{{gtag-api-note}}

## Google privacy settings

If your business is required to comply with privacy regulations such as the [GDPR](../getting-started/compliance-gdpr.md) or [CCPA](../getting-started/compliance-ccpa.md), change the default settings of the Google tools to meet privacy requirements. Follow these steps to ensure that your use of customer data remains in compliance.

### Step 1: Update Google settings

1. [Sign in][1]{: target="_blank"} to your company's Google Analytics account.

1. At the bottom of the left sidebar, choose **[!UICONTROL Admin]**, and then navigate to the account that you want to edit (if applicable).

1. In the **[!UICONTROL Account]** column, click **[!UICONTROL Account Settings]**.

1. Turn off data sharing in order to meet privacy regulation requirements.

   The default Google Analytics settings share your company data with Google and other parties, To turn off data sharing, clear the selection checkbox for the following settings:

   - Google products & services
   - Benchmarking
   - Technical support
   - Account specialists

1. Accept the _Data Processing Amendment_.

   The Google Ads Data Processing Terms describe how Google processes data, and the measures it takes to ensure data security for business that are subject to the GDPR. A record of your legal entities and contact information is also maintained with the amendment. To [learn more][2]{: target="_blank"}, click the link in the message at the top of the page.

   - Scroll down the page to **[!UICONTROL Data Processing Amendment]**.
   - Click **[!UICONTROL Review Amendment]** to read the _Google Ads Data Processing Terms_.
   - Click **[!UICONTROL Accept]**.
   - Click **[!UICONTROL Save]**.

1. Complete the _DPA Administration_ details.

   - Click **[!UICONTROL Manage DPA Details]** to open a DPA administration page where you can edit contacts and your organization's legal entities.

   - In the **[!UICONTROL Legal Entities]** section, click the _Edit_ ( ![Google edit icon](./assets/google-icon-edit.png) ) icon and add one or more registered names for your organization. When complete, click **[!UICONTROL Save]**.

   - In the **Contacts** section, click the _Add_ ( ![Google add icon](./assets/google-icon-add.png) ) icon and enter the information for the first contact. Next, select the checkbox of each applicable role and click **[!UICONTROL Add]**.

      - Primary Contact - (Notification Email Address) The contact to whom notices are sent.
      - Data Protection Officer - (If applicable) The person who is designated to facilitate privacy regulation compliance.
      - European Economic Area (EEA) Representative - (If applicable) The person who represents customers outside of the EU regarding their GDPR obligations.

      Repeat to add another contact, if applicable.

### Step 2: Modify your Google JS libraries

Google supports three JavaScript libraries to measure website usage, depending on the Google product: `gtag.js`, `analytics.js`, and `ga.js`. To meet privacy requirements, the standard code can be modified as follows:

#### Anonymize IP addresses

To anonymize the IP addresses used by **_Google Universal Analytics_**, add the following snippet to the `analytics.js` library on your web server:

   analytics.js

   ```
   : `ga('set', 'anonymizeIp', true);`
   ```

   To learn more, see the [Analytics.js Field Reference][3]{: target="_blank"} in Google Help.

   If you use the legacy `ga.js` library, add the following snippet:
   
   ga.js
   
   ```
   : `ga('set', 'anonymizeIp', true);`
   ```

To anonymize the IP addresses used by **_Google Tag Manager_**, set the `anonymize_ip` parameter to `true` in the `gtag.js` library on your web server.

   gtag.js

   ```
   : `gtag('event', 'your_event', { 'anonymize_ip': true })`
   ```

   To learn more, see [IP Anonymization in Analytics][4] in Google Help.

#### Force SSL

To force all Google data to be transmitted over a secure socket layer (SSL), add the following snippet to the `analytics.js` library on your web server.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Step 3: Update your privacy policy

Update your [privacy policy](../getting-started/privacy-policy.md ) to state that your company:

- Uses Google Analytics
- Masks IP addresses to hide personal information
- Has turned off Google Data Sharing
- Does not use other Google services with Google Analytics cookies

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
