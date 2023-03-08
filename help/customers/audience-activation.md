---
title: Audience Activation
description: Learn how to activate audiences in Adobe Commerce.
---
# Audience Activation in Adobe Commerce

The Audience Activation extension lets you activate Real-Time CDP audiences in Adobe Commerce to create unique offers in the cart such as "buy 2 get 1 free", display hero banners geared toward that customer, and modify product pricing through various offers. The audiences built within Real-Time CDP are based on data from various enterprise systems, such as Enterprise Resource Planning (ERP), Customer Relationship Management (CRM), point of sale, and marketing systems. Because customer segment information is constantly refreshed, customers can become associated and disassociated from a segment as they shop in your store.

You can activate audiences in a Luma storefront or [headless](#headless-support) storefront. In a Luma storefront, audience information (segment membership) is stored in a cookie on the Commerce side. In a headless storefront, audience information is passed in the GraphQL API header as a parameter named: `aep-segments-membership`.

## Storefront implementation

The following tasks apply to both Luma and headless storefront implementations. To activate audiences in Adobe Commerce, you must:

- [Install Adobe Commerce on cloud infrastructure, version 2.4.4 or higher](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html)
- [Activate](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce as a destination in Experience Platform
- [Install](#install-the-extension) the Audience Activation extension in the Admin
- [Configure](#configure-the-extension) the Audience Activation extension in the Admin to activate Real-Time CDP audiences in Commerce

### Install the extension

You can install the Audience Activation extension from the [marketplace](https://marketplace.magento.com/magento-experience-platform-audiences.html) or you can run the following command:

   ```bash
   composer require magento/audiences
   ```

### Configure the extension

After you install the Audience Activation extension, you need to log into your Commerce Admin and complete the following:

1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Services]_ > **[!UICONTROL Commerce Services Connector]**, [sign in](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) to your Adobe account, and select your organization ID.
1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Services]_ > **[!UICONTROL Real-Time CDP Audiences]** and in the **[!UICONTROL Datastream ID]** field paste the ID of the datastream ID that you created when you [activated](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce as a destination in Experience Platform.
1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**. Expand **[!UICONTROL Services]** and select **[!UICONTROL Real-Time CDP Audiences]**. Then, enter the configuration credentials found in the [developer console](https://developer.adobe.com/console/home).

    ![Real-Time CDP Audience Admin Configuration](./assets/rtcdp-admin-config.png)

1. Click **Save Config**.

With audiences activated to your Adobe Commerce instance, you can:

- [Create](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) a cart price rule informed by audiences
- [Create](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) a dynamic block informed by audiences

## Real-Time CDP audiences dashboard

You can view all audiences that are available in your Adobe Commerce instance using the **Real-Time CDP Audiences** dashboard. With this dashboard, you can see which audiences are active and where they are deployed on your site. Any new or modified audiences you [configure or create](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html) in Experience Platform appears in this dashboard.

To access the **Real-Time CDP Audiences** dashboard, go to the _Admin_ sidebar, then go to **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**. The **Real-Time CDP Audiences** dashboard appears:

![Real-Time CDP Audiences Dashboard](./assets/audience-library.png)

|Column|Description|
|--- |--- |
|[!UICONTROL Audience]|Name given to the audience in Real-Time CDP.|
|[!UICONTROL Last Modified]|Indicates when the audience was modified in Real-Time CDP.|
|[!UICONTROL Origin]|Indicates from where the audience was imported.|

{style="table-layout:auto"}

## Headless support

You can activate audiences in a headless Adobe Commerce instance, such as AEM, PWA, and so on. A headless storefront communicates to the Experience Platform via the [Commerce Integration Framework (CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). The framework provides a server-side API that is implemented using GraphQL. Audience information, like which segment a shopper belongs to, is passed to Commerce via a GraphQL header parameter named: `aep-segments-membership`.

The overall architecture is as follows:

![Sending Data from Headless Storefront to Backend](./assets/aem-commerce-architecture.png)

After you [install](#install-the-extension) and [configure](#configure-the-extension) the extension, the AEP Web SDK contains the audience information in the form of segment membership.

To capture those segment memberships from the SDK, see this [code snippet](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

Once retrieved, you can then pass those segments to Commerce within the GraphQL header. For example:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```
