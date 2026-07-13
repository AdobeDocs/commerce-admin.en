---
title: Customers now online
description: The _Now Online_ option on the [!UICONTROL Customers ]menu lists all customers and visitors who are currently online in your store.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
TQID: https://experienceleague.adobe.com/jtyDgy3jFmn0XymAYcpc2AOLLWSTDw-3OGkvG9a1SDc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
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
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Customers now online

The **[!UICONTROL Now Online]** option on the [!DNL Customers] menu lists all customers and visitors who are currently online in your store. The interval of time that customers are shown as currently online is set in the configuration, and determines how long the [!DNL Customer's] activity is visible from the Admin. By default, the interval is 15 minutes. The session ends if the keyboard is not used during this time and customers must sign into their accounts again to continue shopping. It is important to note that the contents of the carts are saved for later access.

![Online Customers](assets/customers-now-online.png){width="700" zoomable="yes"}

The online status of customers is updated only upon customer login, registration, or any other state-changing event. It includes cart-related events, such as adding, removing, and modifying products.

>[!NOTE]
>
>Page visits alone do not update the customer's online status. To collect such information, it is recommended to [set up Google Analytics](../merchandising-promotions/google-analytics.md) (alone or with [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) or use other analytics software with Adobe Commerce.

## See all customers currently online

On the _Admin_ sidebar, go to **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>For information about helping an online customer complete a purchase, see [Shopping assistance](../stores-purchase/introduction.md#shopping-assistance).

## Configure the time interval

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Customers]** and choose **[!UICONTROL Customer Configuration]**.

1. Expand the **[!UICONTROL Online Customers Options]** section and do the following:

      ![Online Customer options](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

      - For **[!UICONTROL Online Minutes Interval]**, enter the number of minutes for the customer session to be visible from the Admin. Leave the field empty to accept the default interval of 15 minutes.

      - For **[!UICONTROL Customer Data Lifetime]**, enter the number of minutes before any unsaved data entered by the customer expires.

1. When complete, click **[!UICONTROL Save Config]**.

## Column descriptions

|Column|Description|
| --- | --- |
| **[!UICONTROL ID]** | The customer ID of a registered customer. |
| **[!UICONTROL First Name]** | The first name of a registered customer. |
| **[!UICONTROL Last Name]** | The last name of a registered customer. |
| **[!UICONTROL Email]** | The email address of a registered customer. |
| **[!UICONTROL Last Activity]** | The date and time of the customer's last activity in your store. |
| **[!UICONTROL Type]** | Options: `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | The last URL that the customer visited. |
| **[!UICONTROL Company]** | The name of the company to which the user belongs. |

{style="table-layout:auto"}
