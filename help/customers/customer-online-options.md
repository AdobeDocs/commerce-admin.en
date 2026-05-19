---
title: Customer session lifetime
description: The customer session lifetime determines the lifetime of a customer shopping session.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
TQID: https://experienceleague.adobe.com/cJ8Rv5zMkTvZMfrl-nj-3xy3guSPDlxa7HZ-ZG7kLFw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
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
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Customer session lifetime

The lifetime of a customer shopping session is determined by several factors, including the length of the server session, the use of a [persistent cart](../stores-purchase/cart-persistent.md), and the lifetime of information that is stored in the browser. Although these are related to the same customer experience, they are separate processes with different expiration events and lifetimes.

|Process|Description|
| --- | --- |
| Session | Information that is stored on the server, such as the contents of the shopping cart. If the server session expires before the cookie expires, customers might lose the cart contents and reduce security risk. |
| Session Cookie | Information that is stored in the browser as a number or string of characters. If the session cookie expires before the server session, the customer is logged out. The session cookie is deleted when the customer closes the browser window. By default, the cookie lifetime is set to 3600 seconds, or one hour. If there is no keyboard activity during that time, the current session ends, and customers must log back into their accounts to continue shopping. |

{style="table-layout:auto"}

If [Persistent Cart](../stores-purchase/cart-persistent.md) is enabled, the cart contents are saved for the next time customers sign into their accounts. When using a persistent cart, it is recommended that you set the lifetime of the server session and the session cookie to a long time period.

On the server, the length of the session is controlled by the `php.ini` file and several variables. Currently, Adobe Commerce does not have an Admin configuration setting that controls the length of the server session.

## Configure the cookie lifetime

1. On the _Admin_ sidebar, go to [!UICONTROL **Stores**] > _[!UICONTROL Settings]_ > [!UICONTROL **Configuration**].

1. If you have multiple stores, set the **[!UICONTROL Store View]** chooser in the upper-right corner to the store where the configuration applies.

1. In the left panel under **[!UICONTROL General]**, choose **[!UICONTROL Web]**.

1. Expand the **[!UICONTROL Default Cookie Settings]** section.

   ![Default Cookie Settings](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. To change the default, clear the **[!UICONTROL Use system value]** checkbox and enter the new value in seconds.

1. When complete, click **[!UICONTROL Save Config]**.

## Configure _Remember Me_ functionality

To make login easier, the **[!UICONTROL Remember Me]** function allows user account holders to avoid entering their credentials every time they enter the storefront. For security reasons, the persistence feature is disabled by default.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Customers]** and choose **[!UICONTROL Persistent Shopping Cart]**.

1. Expand the **[!UICONTROL General Options]** section.

1. For **[!UICONTROL Enable Persistence]**, set to `Yes`. (Clear the **[!UICONTROL Use system value]** checkbox to allow changing the default setting.)

1. For **[!UICONTROL Enable "Remember Me"]**, set to `Yes` or `No` according to your requirements.

1. When complete, click **[!UICONTROL Save Config]**.
