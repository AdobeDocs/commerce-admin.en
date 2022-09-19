---
title: Newsletters and subscriptions
description: <placeholder>
---
# Newsletters and subscriptions

Publishing a regular newsletter is considered to be one of the most powerful and affordable marketing tools available. Commerce gives you the ability to publish and distribute newsletters to customers who have subscribed, plus tools to produce your newsletter, build and manage your list of subscribers, develop content, and drive traffics to your store. You can also use [Page Hierarchy](../content-design/page-hierarchy.md) to create an archive of past issues.

>[!NOTE]
>
>You can add capabilities by integrating your Commerce instance with a third-party newsletter service provider and by adding extensions. To learn more, see [Commerce Marketplace](../getting-started/commerce-marketplace.md).

The first step in creating newsletters is to configure the newsletter settings for your site. You can require customers to click a confirmation link that is sent by email to confirm the subscription. This double opt-in method requires customers to confirm twice that they want to receive your newsletter and reduces the possibility that it might be considered to be spam.

## Enable newsletters

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Customers** and choose **Newsletter**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **General Options** section.

1. To enable newsletters for the store view scope, set **Enabled** to `Yes`.

After enabling the newsletter function the **Subscription Options** section appears.

## Configure the subscription options

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Customers** and choose **Newsletter**.

1. If needed, [change the configuration scope](../getting-started/websites-stores-views.md#scope-settings) to apply the newsletter configuration changes to a specific site/store view.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Subscription Options** section and do the following:

   ![Customers configuration - newsletter subscriptions](../configuration-reference/customers/assets/newsletter-subscription-options.png)<!-- zoom -->

   - Confirm the email template and sender of the each of the following email messages that are sent to subscribers:

      - Success email
      - Confirmation email
      - Unsubscribe email

   - To use the double opt-in process to confirm subscriptions, set **Need to Confirm** to `Yes`.

   - To allow people who do not have an account with your store to subscribe to the newsletter, set **Allow Guest Subscription** to `Yes`.

1. When complete, click **Save Config**.
