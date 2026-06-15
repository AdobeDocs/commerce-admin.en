---
title: Orders and returns widget
description: Learn how to use the orders and returns widget to give customers the ability to check the status of their orders, print invoices, and track shipments.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/jWpFWPBwvKr5EnMXdV5-3zAqagGuzPrvOL6-gMiEw-M
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
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
# Orders and returns widget

The _Orders and Returns_ widget gives guests the ability to check the status of their orders, print invoices, and track shipments. When the widget is added to the storefront, it is visible only for guests and for customers who are not logged in to their accounts. Guests can find orders by providing the Order ID, Billing Last Name, and either the Email Address or ZIP Code.

![Orders and Returns widget in the sidebar on the storefront](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## The orders and returns widget on the storefront

1. The customer can use the **[!UICONTROL Find Order By]** option to choose one of the following parameters to be used to find the order:

   - Email Address
   - ZIP Code

1. The customer enters the **[!UICONTROL Order ID]** and **[!UICONTROL Billing Last Name]**.

1. Enters either the billing **[!UICONTROL Email Address]** or **[!UICONTROL ZIP Code]** that is associated with the order.

1. Clicks **[!UICONTROL Search]** to retrieve the order.

   ![Order information displayed in the storefront](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## Set up the Orders and Returns widget

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Elements]_ > **[!UICONTROL Widgets]**.

1. In the upper-right corner, click **[!UICONTROL Add Widget]**.

1. In the _[!UICONTROL Settings]_ section, do the following:

   - Set **[!UICONTROL Type]** to `Orders and Returns`.

   - Choose the **[!UICONTROL Design Theme]** that is used by the store.

1. Click **[!UICONTROL Continue]**.

1. In the _[!UICONTROL Storefront Properties]_ section, do the following:

   - For **[!UICONTROL Widget Title]**, enter a descriptive title for the widget.

      This title is visible only from the Admin.

   - For **[!UICONTROL Assign to Store Views]**, select the store views where the widget is visible.

      You can select a specific store view, or `All Store Views`. To select multiple views, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

   - (Optional) For **[!UICONTROL Sort Order]**, enter a number to determine the order this item appears with others in the same part of the page. (`0` = first, `1` = second, `3` = third, and so on.)

1. In the _[!UICONTROL Layout Updates]_ section, click **[!UICONTROL Add Layout Update]** and do the following:

   - Set **[!UICONTROL Display On]** to the type of page where you want the widget to appear.

   - To determine where the widget is displayed on the page, complete the rest of the layout update information.

1. When complete, click **[!UICONTROL Save]**.

1. When prompted to refresh the cache, click the link in the message at the top of the page and follow the instructions.
