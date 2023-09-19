---
title: United States Postal Service (USPS)
description: Learn how to set up USPS as a shipping carrier for your store.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
---
# United States Postal Service (USPS)

The United States Postal Service is the independent postal service of United States government, offering domestic and international shipping services by land and air.

## Step 1: Open a USPS shipping account

Open a [USPS Web Tools][1] account. After you complete the registration process, you will receive your User ID and a URL to the USPS test server.

You can also open a [USPS Web Tools][1] account. After you complete the registration process, you will receive your User ID and a URL to the USPS test server. To learn more about USPS Web Tools, see their [Technical Documentation][2].

## Step 2: Enable USPS for your store

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Sales]** and choose **[!UICONTROL Delivery Methods]**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL USPS]** section.

   >[!NOTE]
   >
   >If necessary, first deselect the **[!UICONTROL Use system value]** checkbox to change the following settings as described.

1. Set **[!UICONTROL Enabled for Checkout]** to `Yes`.

1. If needed, enter the **[!UICONTROL Gateway URL]** to access USPS shipping rates.

   >[!IMPORTANT]
   >
   >Effective June 24, 2021, USPS Web Tools will remove support for all unsecure HTTP endpoints. After this change, all Web Tools API requests that to an unsecure HTTP endpoint will fail. Make sure that your **[!UICONTROL Gateway URL]** uses the secure HTTPS endpoint.

   The field is preset by default, and normally does not need to be changed.

1. Enter a **[!UICONTROL Title]** for this shipping method that appears during checkout.

1. Enter the **[!UICONTROL User ID]** and **[!UICONTROL Password]** for your USPS account.

1. Set **[!UICONTROL Mode]** to one of the following:

   - `Development` - Runs USPS in a test environment. After running USPS in a development environment, make sure to return later and set Mode to `Live`.
   - `Live` - Runs USPS in a live production environment.

## Step 3: Complete the packaging description

1. To determine how the order is managed if sent as multiple packages, set **[!UICONTROL Packages Request Type]** to one of the following:

   - `Divide to Equal Weight` - (One Request) The shipment of multiple packages can be submitted as one request if the packages are divided by equal weight.
   - `Use Origin Weight` - (Multiple Requests) Multiple packages must be submitted as separate requests if using origin weight as the basis of calculating the shipping cost.

1. Set **[!UICONTROL Container]** to the type of packaging normally used to ship products ordered for your store.

1. Set the **[!UICONTROL Size]** of the typical package shipped from your store.

1. Set **[!UICONTROL Machinable]** to one of the following:

   - `Yes` - If your typical package can be processed by a machine.
   - `No` - If your typical package must be processed manually.

1. Enter the **[!UICONTROL Maximum Package Weight]** according to carrier requirements.

   ![USPS Packaging Settings](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## Step 4: Set up handling fees

The handling fee is optional, and appears as an extra charge that is added to the DHL shipping cost. If you want to include a handling fee, do the following:

1. Set **[!UICONTROL Calculate Handling Fee]** to one of the following methods:

   - `Fixed`
   - `Percent`

1. To determine how the handling fee is applied, set **[!UICONTROL Handling Applied]** to one of the following:

   - `Per Order`
   - `Per Package`

1. Enter the amount of the **[!UICONTROL Handling Fee]** to be charged.

   To enter a percentage, use the decimal format. For example, enter `0.25` for 25%.

   ![USPS Handling Fee](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## Step 5: Specify allowed methods and applicable countries

1. For **[!UICONTROL Allowed Methods]**, choose each USPS shipping method to be available to your customers.

   The methods appear under USPS during checkout. To select multiple methods, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

1. If you want to provide a [Free Shipping](shipping-free.md) option through USPS, set the free shipping options:

   - Set **[!UICONTROL Free Method]** to the method you want to use for free shipping. If you don't want to offer free shipping through USPS, choose `None`.

   - To require a minimum order amount that qualifies an order for free shipping with USPS, set **[!UICONTROL Enable Free Shipping Threshold]** to `Enable`. Then, enter the minimum value in **[!UICONTROL Free Shipping Amount Threshold]**.

1. If needed, change the **[!UICONTROL Displayed Error Message]**.

   This text box is preset with a default message, but you can enter a different message that you want to appear if USPS becomes unavailable.

   ![USPS Allowed Methods](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Ship to Applicable Countries]** to one of the following:

   - `All Allowed Countries` - Customers from all [countries](../getting-started/store-details.md#country-options) specified in your store configuration can use this delivery method.
   - `Specific Countries` - When you choose this option, the _Ship to Specific Countries_ list appears. Select each country in the list where this delivery method can be used.

   ![USPS Applicable Countries](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. Set **[!UICONTROL Show Method if Not Applicable]** to one of the following:

   - `Yes` - Lists all available USPS shipping methods during checkout, including methods that don't apply to the shipment.
   - `No` - Lists only the USPS shipping methods that are applicable to the shipment.

1. To create a log file with the details of USPS shipments made from your store, set **[!UICONTROL Debug]** to `Yes`.

1. For **[!UICONTROL Sort Order]**, enter a number to determine the sequence in which USPS appears when listed with other delivery methods during checkout.

   `0` = first, `1` = second, `2` = third, and so on.

1. Click **[!UICONTROL Save Config]**.


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
