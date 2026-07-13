---
title: Wish lists
description: Learn about wish lists and how they can add to the shopping experience and promote more sales.
exl-id: 42c73566-0e32-4639-9fa2-d504fa161ebc
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/neTWJnIbZcaAAMQiX-SV82fTyvOGEeNLhBfxDUh4Ulk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Wish lists

A wish list is a list of products that a registered customer can share with friends, or save to transfer to the cart later. When wish lists are enabled, the Add to Wishlist link appears on the category and product pages of each product in the store. Depending on the theme, it might be a text link or a graphic image.

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce supports the use of multiple wish lists per customer account.

![Magento Open Source](../assets/open-source.svg) Magento Open Source supports the use of a single wish list per customer account.

Shared wish lists are sent from a store email address, but the body of the message contains a personalized note from the customer. You can customize the email template that is used when wish lists are shared and choose the store contact that appears as the sender.

Wish lists can be updated from the dashboard of the [customer account](../customers/account-dashboard.md). Items can be added or transferred between the wish list and cart by the customer or by the store administrator.

![Example storefront - My Wish List](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

When a product with multiple options is added to a wish list, any options that have been selected by the customer are included in the wish list item description. For example, if the customer adds the same pair of shoes in three different colors, each pair appears as a separate wish list item. However, if the customer adds the same product to the wish list multiple times, the product appears only once, but with the quantity selected from product page.

## Wish list assistance in the Admin

Customers can [manage their wish lists](wishlist-storefront.md) by logging in to their accounts on the storefront. As a store administrator, you can also manage customer wish lists from the Admin.

**_To update wish list items from the Admin:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Find the customer in the list and click **[!UICONTROL Edit]** in the _[!UICONTROL Action]_ column.

1. In the left panel, choose **[!UICONTROL Wish List]** and find the item to be edited in the list.

   Any options selected for the product appear below the product name.

   ![Commerce Admin - customer wish list](./assets/customer-wishlist-edit-admin.png){width="600" zoomable="yes"}

1. To edit the product options, do the following:

   - In the **[!UICONTROL Action]** column, click **[!UICONTROL Configure]**.

   - On the product page, update the options and **[!UICONTROL Quantity]** as needed.

   - Click **[!UICONTROL OK]**.

1. When complete, click **[!UICONTROL Save Customer]** or **[!UICONTROL Save and Continue Edit]**.
