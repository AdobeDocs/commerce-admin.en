---
title: Configure wish lists
description: <Add description here>
---
# Configure wish lists

The wish list configuration enables wish lists and determines the email template and sender of email messages that are used when a wish list is shared.

## Enable wish list functionality

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Customers** and choose **Wish List**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **General Options** section and do the following:

    ![Customers configuration - wish list general settings](../configuration-reference/customers/assets/wishlist-general-options.png)<!-- zoom -->

    - Set the **Enabled** field to `Yes`. This activates the wish list module for the store.

    - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) Set the **Enable Multiple Wish Lists** field to `Yes`. This allows customers to create and maintain multiple wish lists.

    - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) sTo limit the number of wish lists customers can have associated with their account, enter value for **Number of Multiple Wish Lists**.

    - Set the **Show in Sidebar** field to `Yes`. This displays the wish lists in the sidebar.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Share Options** section. Then, do the following:

    ![Customers configuration - wish list share options](../configuration-reference/customers/assets/wishlist-share-options.png)<!-- zoom -->

    - Set the **Email Sender** to the store contact that should appear as the sender of the message. Options: General Contact, Sales Representative, Customer Support, Custom Email.

    - Set the **Email Template** to be used when a customer shares a wish list.

    - To limit the total number of emails a customer can send, enter a **Max Emails Allowed to be Sent** value. The default is 10 and the maximum allowed is 10,000.

    - To limit the size of the message, enter value for **Email Text Length Limit**. The default is 255.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **My Wish List Link** section and set **Display Wish List Summary** to one of the following:

    - `Display number of items in wish list`
    - `Display item quantities`

    ![Customers configuration - wish list display](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png)<!-- zoom -->

1. When complete, click **Save Config**.

## Add wish list search

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only)

Any public wish list can be found using the Wish List Search [widget](../content-design/widgets.md). The widget enables a customer to search by the name or email address of the wish list owner. Store customers can find wish lists that belong to other customers, view them and order products from them, or add the products to their own wish lists. If an item is purchased from a public wish list by another customer, it is not removed from the original wish list. The Wish List Search widget can be added to any page of your store to make it easy for customers to find the wish lists of friends and family members.

![Example storefront - wish list search](./assets/storefront-wishlist-search.png)<!-- zoom -->

### Add a wish list search widget

1. On the _Admin_ sidebar, go to **Content** > _Elements_ > **Widgets**.

1. In the upper-right corner, click **Add Widget**.

1. In the _Settings_ tab, do the following:

   - Set **Type** to `Wish List Search`.

   - Set **Design Theme** to the theme of the store where the wish list is added.

   - Click Continue.

1. Complete the _Storefront Properties_:

   - Enter the **Widget Title**.

   - Set **Assign to Store Views** to the view or website where the widget is to be used.

   - For **Sort Order**, enter a number to determine the placement of the widget within its container.

     `0` = first (default), `1` = second, `2` = third, and so on.

1. In the _Layout Updates_ section, click **Add Layout Update** and set **Display on** to one of the following:

   - _Categories_

      - Anchor Categories
      - Non-Anchor Categories

   - _Products_

      - All Product Type
      - Simple Product
      - Virtual Product
      - Bundle Product
      - Configurable Product
      - Downloadable Product
      - Gift Card
      - Grouped Product

   - _Generic Page_

      - All Pages
      - Specified Page
      - Page Layouts

1. In the **Container** list, choose the area of the page layout where it is to be placed.

    ![Wish list search widget - layout](./assets/widget-wishlist-search-layout-update.png)<!-- zoom -->

1. In the left panel, choose **Widget Options**.

1. Set **Quick Search Form Types** to one of the following:

   - `All Forms` - Customers can search by all available parameters.
   - `Owner Name` - Customers can search for wish lists by owner name.
   - `Owner Email` - Customers can search for wish lists by owner email address.

   >[!NOTE]
   >
   >Shipping addresses are not included in wish lists.

1. Configure any remaining widget properties as needed, following the standard [instructions](../content-design/widget-create.md).

1. When complete, click **Save**.

1. When prompted, refresh all invalid caches.

### Find a customer wish list 

1. From the Wish List Search widget, select a search option.

1. Enter the customer's name or email address and click **Search**.

   The **Wish List Search** page opens and any matching wishlists are displayed in the search results section.

   >[!NOTE]
   >
   >Only public wishlists are displayed in search results---customers' private wishlists are not publicly viewable.

1. To view the list of customer wishes, click **View**.

   The owner name and the date of the last update is displayed for each wishlist.

1. To add a product to your cart, select the checkbox below the product and click **Add to Cart**.

   You can also add items you like from another customer's wishlist to your own.
