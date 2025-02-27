---
title: FedEx
description: Learn how to set up FedEx as a shipping carrier for your store.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
---
# FedEx

FedEx is one of the world's largest shipping service companies, providing air, freight, and ground shipping services with several levels of priorities.

![FedEx Shipping Options at Checkout](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx can use [dimensional weight](carriers.md#dimensional-weight) to determine some shipping rates. However, Adobe Commerce and Magento Open Source support only weight-based shipping cost calculation.

## Step 1: Register for FedEx Web Services Production

A FedEx merchant account and registration for FedEx Web Services Production Access is required. After creating a FedEx account, read through the production account information page, then click the _Obtain Production Key_ link at the bottom of the page to register and obtain a key.

>[!NOTE]
>
>Make sure to copy or write down the authentication key. It is required to set up FedEx in your Commerce shipping settings.

## Step 2: Enable FedEx for Your Store

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Delivery Methods]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL FedEx]** section.

1. Set **[!UICONTROL Enabled for Checkout]** to `Yes`.

1. For **[!UICONTROL Title]**, enter a title that identifies the FedEx shipping method during checkout.

1. Enter the following information from your FedEx account:

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. If you have set up a FedEx sandbox and want to work in the testing environment, set **[!UICONTROL Sandbox Mode]** to `Yes`.

   >[!NOTE]
   >
   >Remember to set Sandbox Mode to `No` when you are ready to offer FedEx as a shipping method to your customers.

   ![FedEx Account Settings](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Step 3: Package description and handling fees

1. Set **[!UICONTROL Pickup Type]** to the pickup method used for shipments.

   - `DropOff at Fedex Location` - (Default) Indicates that you drop off shipments at your local FedEx station.
   - `Contact Fedex to Schedule` - Indicates that you contact FedEx to request a pickup.
   - `Use Scheduled Pickup` - Indicates that the shipment is picked up as part of a regular scheduled pickup. 
   - `On Call` - Indicates that the pickup is scheduled by calling FedEx. 
   - `Package Return Program` - Indicates that the shipment is picked up by the FedEx Ground Package Returns Program.
   - `Regular Stop` - Indicates that the shipment is picked up at the regular pickup schedule.
   - `Tag` - Indicates that the shipment pickup is specific to an Express tag or Ground call tag pickup request. This is applicable only for a return shipping label. 

1. For **[!UICONTROL Packages Request Type]**, select the request type that best describes your preference when splitting an order into multiple shipments:

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. For **[!UICONTROL Packaging]**, select the type of FedEx packaging that you typically use to ship products from your store.

1. Set **[!UICONTROL Weight Unit]** to the unit of measurement that is used in your locale.

   - `Pounds`
   - `Kilograms`

1. Enter the **[!UICONTROL Maximum Package Weight]** allowed for FedEx shipments.

   The default FedEx maximum weight is 150 lbs. Consult your shipping carrier for more information. The default value is recommended, unless you have made special arrangements with FedEx. See [Dimensional weight](carriers.md#dimensional-weight) for more information.

   ![FedEx Package Settings](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Configure the handling fee options according to your requirements.

   The handling fee is optional and is not visible during checkout. If you want to include a handling fee, do the following:

   - Set **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - For **[!UICONTROL Handling Applied]**, choose one of the following methods for managing handling fees:

      - `Per Order`
      - `Per Package`

   - Enter the **[!UICONTROL Handling Fee]** as either a `fixed` amount or `percentage`, depending on the method of calculation.

1. Set **[!UICONTROL Residential Delivery]** to one of the following, depending on whether you sell Business-to-Consumer (B2C) or Business-to-Business (B2B).

   - `Yes` - For B2C residential deliveries.
   - `No` - For B2B residential deliveries.

   ![FedEx Handling Fee Settings](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Step 4: Allowed methods and applicable countries

1. Set **[!UICONTROL Allowed Methods]** to each method of shipment that you want to offer.

   When choosing methods, consider your FedEx account, the frequency and size of your shipments, and if you allow international shipments. You can offer as many or as few methods as you want, such as:

   - Europe First Priority
   - Delivery day options: 1 Day Freight, 2 Day Freight, 2-Day, 2-Day AM, 3 Day Freight
   - Domestic options–Express Saver, Ground, First, Overnight, Home Delivery, Standard Overnight
   - International options–International Economy, Intl Economy Freight, International First, International Ground, International, Priority Intl
   - Priority options–Freight, Priority Overnight
   - Smart Post–If offering the Smart Post method (enter the **Hub ID**)
   - Freight options–Freight, National Freight

1. If you want to provide a [Free Shipping](shipping-free.md) option through FedEx, set the free shipping options.

   - Set **[!UICONTROL Free Method]** to the method you want to use for free shipping. If you do not want to offer free shipping through FedEx, choose `None`.

   - To require a minimum order amount that qualifies an order for free shipping with FedEx, set **[!UICONTROL Enable Free Shipping Threshold]** to `Enable`. Then, enter the minimum value in **[!UICONTROL Free Shipping Amount Threshold]**.

   This setting is similar to the one for the standard Free Shipping method, but appears in the FedEx section during checkout, so customers know which method is used for their order.

1. If needed, change the **[!UICONTROL Displayed Error Message]**.

   This text box is preset with a default message, but you can enter a different message that you want to appear if FedEx becomes unavailable.

   ![FedEx Allowed Delivery Methods](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Customers from all [countries](../getting-started/store-details.md#country-options) specified in your store configuration can use this delivery method.

   - `Specific Countries` - When you choose this option, the _Ship to Specific Countries_ list appears. Select each country in the list where this delivery method can be used.

1. If you want to keep a log of all communication between your store and the FedEx system, set **[!UICONTROL Debug]** to `Yes`.

1. Set **[!UICONTROL Show Method if Not Applicable]**:

    - `Yes` - Shows all FedEx shipping methods to customers, regardless of their availability.
    - `No` - Shows only the FedEx shipping methods that apply to the order.

1. For **[!UICONTROL Sort Order]**, enter a number to determine the sequence in which FedEx appears when listed with other delivery methods during checkout.

   `0` = first, `1` = second, `2` = third, and so on.

1. Click **[!UICONTROL Save Config]**.

   ![FedEx Applicable Countries](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Commerce always declares the full order price to FedEx when calculating shipping charges. This behavior cannot be changed.
