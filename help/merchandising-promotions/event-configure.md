---
title: Configure events
description: <placeholder>
---
# Configure events

{{ee-feature}}

Before you can create an event, you must complete the basic configuration to enable events and set up the event block in the sidebar.

## Enable and configure events

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Catalog** and choose **Catalog** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Catalog Events** section and do the following:

    ![Catalog configuration - catalog events](../configuration-reference/catalog/assets/catalog-events.png)<!-- zoom -->

    - Set **Enable Catalog Events Functionality** to `Yes`.

    - Set **Enable Catalog Event Widget on Storefront** to `Yes`.

    - Enter the **Number of Events to be Displayed in the Event Slider Sidebar Widget**. By default, this value is set to `5`. If you want to display only one event in the slider at a time, enter `1`.

    - Enter the number of **Events to Scroll per Click in Event Slider Sidebar Widget**. By default, this value is set to `2`. If you want the slider to display the next event in sequence when clicked, enter `1`.

1. When complete, click **Save Config**.


## Restricting access

Access to a private sale, event, or site can be limited to registered customers who log in, or extended to non-registered customers who must register before gaining access.

![General configuration - website restrictions](../configuration-reference/general/assets/general-website-restrictions.png)<!-- zoom -->

## Set up exclusive access

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **General** and choose **General** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Website Restrictions** section and do the following:.

   - Set **Access Restriction** to `Yes`.

   - Set **Restriction Mode** to one of the following:

      - `Website Closed`
      - `Private Sales: Login Only`
      - `Private Sales: Login and Register`

   - Set **Startup Page** to one of the following:

        |To login form (302 Found)|Users are redirected to the login form before gaining access to the site.|
        |To landing page (302 Found)|Users are redirected to the specified landing page until they log in. <br/>**Important!** Be sure to include a link to the login page from the landing page so customers can log in to access the site.|

   - Choose the **Landing Page** that appears before customers log in to the private sale site.

   - To let search engine bots and spiders know that the landing page is correct and there are no other pages on the site to index, set **HTTP Response** to `200 OK`. In all other cases set to `503 Service Unavailable`.

   >[!NOTE]
   >
   >Applicable only if restriction mode is set to "Website Closed". The landing page is rendered as raw HTML.

   - If you want the fields in the customer login and forgot password forms to be filled automatically from previous entries, set **Enable Autocomplete on login/forgot password forms** to `Yes`.

1. When complete, click **Save Config**.

## Restrict access

Access to a private sale, event, or site can be limited to registered customers who log in, or extended to non-registered customers who must register before gaining access.

![General configuration - website restrictions](../configuration-reference/general/assets/general-website-restrictions.png)<!-- zoom -->

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **General** and choose **General** underneath.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Website Restrictions** section.

1. Set **Access Restriction** to `Yes`.

1. Set **Restriction Mode** to one of the following:

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Set **Startup Page** to one of the following:

   - `To login form (302 Found)` - Users are redirected to the login form before gaining access to the site.

   - `To landing page (302 Found)` - Users are redirected to the specified landing page until they log in. 

      >[!IMPORTANT]
      >
      >Be sure to include a link to the login page from the landing page so customers can log in to access the site.

1. Choose the **Landing Page** that appears before customers log in to the private sale site.

1. To let search engine bots and spiders know that the landing page is correct and there are no other pages on the site to index, set **HTTP Response** to `200 OK`.

   In all other cases set to `503 Service Unavailable`.

   >[!NOTE]
   >
   >Applicable only if restriction mode is set to _Website Closed_. The landing page is rendered as raw HTML.

1. If you want the fields in the customer login and forgot password forms to be filled automatically from previous entries, set **Enable Autocomplete on login/forgot password forms** to `Yes`.

1. When complete, click **Save Config**.

## Restrict sales

By default, products that appear in upcoming or closed events are not available for general sale and the _Add to Cart_ button does not appear on the product list or product page.

To restore the _Add to Cart_ button for a closed event, the event must be deleted (see [Update events](event-create.md#update-events)). However, if a product is associated with another category that has no selling restrictions, the button is available on the product page. Similarly, the ticker block does not appear on the product page if the product is associated with another category that has no selling restrictions.
