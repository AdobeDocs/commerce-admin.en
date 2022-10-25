---
title: Integrate Experience Platform Audiences in Commerce
description: Learn how to integrate Experience Platform Audiences in Commerce to inform cart price rules.
---
# Integrate Experience Platform Audiences in Commerce

>[!IMPORTANT]
>
>The Real-Time CDP extension is in beta and only available to a select number of customers.

The Real-Time CDP extension for Adobe Commerce lets you import Experience Platform Audiences into Adobe Commerce to dynamically personalize cart price rules. The Audiences built within Real-Time CDP are based on data from various enterprise systems, such as Enterprise Resource Planning (ERP), Customer Relationship Management (CRM), point of sale, and marketing systems.

>[!NOTE]
>
>Audiences in Experience Platform are referred to as segments in Adobe Commerce.

Using Experience Platform Audiences in Adobe Commerce requires that you:

- [Activate](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce as a destination in Experience Platform
- [Install](#install-the-extension) the Real-Time CDP extension in Adobe Commerce
- [Configure](#configure-the-extension) the Real-Time CDP extension in the Admin to import Experience Platform Audiences into Commerce
- [Create](#create-a-cart-price-rule) a cart price rule based on the imported Experience Platform Audiences

## Install the extension

To install the Experience Platform Audiences extension in Adobe Commerce, run the following command:

   ```bash
   composer require adobe/experience-platform-audiences
   ```

## Configure the extension

After you install the Real-Time CDP extension, you need to log into your Commerce Admin and complete the following:

On the _Admin_ sidebar, go to **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_ > **[!UICONTROL Email Reminder Rules]**.

1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Services]_ > **[!UICONTROL Commerce Services Connector]** and [sign in](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/saas.html?lang=en#organizationid) to your Adobe account and select your organization ID.
1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Services]_ > **[!UICONTROL Experience Platform Connector]** and in the **[!UICONTROL Datastream ID](https://experienceleague.adobe.com/docs/commerce-merchant-services/experience-platform-connector/fundamentals/connect-data.html)** field paste the ID of the datastream ID that you created when you [activated](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce as a destination in Experience Platform.
1. On the _Admin_ sidebar, go to **[!UICONTROL Store]** > _[!UICONTROL Configuration]_, select **[!UICONTROL Services]**, then **[!UICONTROL Experience Platform Audiences]** and enter the configuration credentials found in the [developer console](https://developer.adobe.com/console/home).

    ![Real-Time CDP Admin Configuration](./assets/rtcdp-admin-config.png)

1. Select **Save Config**.

## Create a cart price rule

You can create a cart price rule in Commerce using the Experience Platform Audiences you imported from Experience Platform.

1. On the _Admin_ sidebar, go to **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_ > **[!UICONTROL Cart Price Rules]** and select the **[!UICONTROL Add New Rule]** button. For this exercise, let's add a 50% discount rule.

1. Expand **[!UICONTROL Rule Information]** and fill in the fields as per your requirements.

   ![New Rule with Experience Platform Audience](./assets/rtcdp-new-rule.png)

1. Expand **[!UICONTROL Conditions]** and select the "+" icon and select **[!UICONTROL Experience Platform Audience]** from the dropdown menu.

   ![Select Experience Platform Audience Condition](./assets/rtcdp-conditions.png)

1. Select the "..." icon and select the **[!UICONTROL Open Chooser]** button. Locate the specific Experience Platform Audience that you want to use.

   ![Select Experience Platform Audience Identifier](./assets/rtcdp-conditions-chooser.png)

1. Expand **[!UICONTROL Actions]** and add a value in the **[!UICONTROL Discount Amount]** field.

   ![New Action with Experience Platform Audience](./assets/rtcdp-actions.png)

1. Select **[!UICONTROL Save]** to save the new cart price rule.

1. Clean the cache.

## Headless support

You can use Experience Platform Audiences in a headless Adobe Commerce instance.

>[!IMPORTANT]
>
>Documentation not yet available.

<!--### Prerequisits

- GraphQL endpoint
- Others?
- Configure Admin as above (it's the same for headless)

Do we have a list of GraphQL Queries/Mutations? Or an example of a call to the endpoint?
What headers are needed?

You need the AEP Web SDK (alloy.js). This returns segment membership. It's cookie based.

And then the change here is that when AEP segment memberships is passed in the header, you're sending the the discount values back.

how to get frontend to implement integration between aep segments and what you belong to, then pass that in header to commerce.-->

## AEM support

You can use Experience Platform Audiences in an AEM-Commerce storefront.

>[!IMPORTANT]
>
>Documentation not yet available.
