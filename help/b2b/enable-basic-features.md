---
title: Enable Basic B2B Features
description: Learn about enabling the primary B2B features for your store.
---
# Enable Basic B2B Features

By default, all B2B features are initially disabled. However, they are always available from the Admin, regardless of whether they are enabled or disabled for the storefront. For a complete list of B2B configuration settings, see [B2B Configuration Reference](https://docs.magento.com/user-guide/configuration/general/b2b-features.html).

>[!IMPORTANT]
>
>When support for customer companies is enabled, shared catalogs, negotiable quotes, and default B2B payment methods become available. The Quick Order and Requisition Lists features can be enabled/disabled independently.

## Configure B2B features

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

   If you have a multi-site installation, set the **Store View** control in the upper-left corner to the website where the configuration applies.

1. In the left panel under _General_, choose **B2B Features** and enable the basic features:

   ![B2B configuration - general](./assets/b2b-features.png)<!--- zoom --->

   See [B2B Features](https://docs.magento.com/user-guide/configuration/general/b2b-features.html) in the _Configuration Reference_ for a full list of general B2B feature options and their functions.

   - To allow customers to manage their own company accounts, set **Enable Company** to `Yes`.

      This setting displays additional fields to enable Shared Catalogs and B2B Quotes, and a new section for configuring Default B2B Payment Methods.

   - To allow customers and guests to quickly place orders based on SKU or product name, set **Enable Quick Order** to `Yes`.

   - To allow customers to create and manage requisition lists from their account dashboard, set **Enable Requisition List** to `Yes`.

      You can also [configure the maximum number of lists](configure-requisition-lists.md) a customer can have for their account.

   ![B2B configuration - enable company settings](./assets/b2b-features-company-enabled.png)<!--- zoom --->

1. To make custom pricing available for different companies, set **Enable Shared Catalog** to `Yes`.

   Enabling shared catalogs also enables category permissions for all stores.

1. To give company buyers the ability to negotiate prices, set **Enable B2B Quote** to `Yes`.

1. To establish the default payment methods for B2B orders, set **Applicable Payment Methods** to one of the following:

   - `All Payment Methods`

   - `Specific Payment Methods`

      For the specific option, select the **Payment Methods** that you want to make available to your customers by holding down the Ctrl key (PC) or the Command key (Mac) as you click each option.

      The list of [payment methods](https://docs.magento.com/user-guide/configuration/sales/payment-methods.html) shows which are currently enabled or disabled in your store. In addition to the standard payment methods, the list also includes the following:

      - No Payment Information is Required
      - [Payment on Account](#configure-payment-on-account)
      - Stored Accounts
      - Stored Cards

      ![B2B configuration - default payment method settings](./assets/b2b-features-default-payment-methods.png)<!--- zoom --->

1. To specify the default shipping methods for B2B orders, set **Applicable Shipping Methods** to one of the following:

   - `All Shipping Methods`
   - `Specific Shipping Methods`

     For the specific option, select the **Shipping Methods** that you want to make available to your customers by holding down the Ctrl key (PC) or the Command key (Mac) as you click each option.

     The list of shipping methods shows which are currently [enabled or disabled](https://docs.magento.com/user-guide/configuration/sales/delivery-methods.html).

     ![B2B configuration - default shipping methods](./assets/b2b-features-shipping-methods.png)<!--- zoom --->

1. To enable purchase orders for company accounts, expand ![Expansion selector](../assets/icon-display-expand.png) the **Order Approval Configuration** section and set **Enable Purchase Orders** to `Yes`.

   ![Order Approval Configuration](./assets/b2b-features-order-approval.png)<!--- zoom --->

   You must also enable purchases orders for each [company account](account-company-create.md) where you want to activate them.

1. When complete, click **Save Config**.

## Configure order approval

The ability to track order processing and purchase orders gives company administrators control over the actions of the company's buyers. The order approval functionality is available when the purchase orders feature is enabled by a store administrator.

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **General** and choose **B2B Features**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Order Approval Configuration** section.

1. To allow companies to create purchase orders, set **Enable Purchase Orders** to `Yes`.

1. When complete, click **Save Config**.

   The purchase orders feature is enabled at the website level. To enable this type of order for a company, do the same with the appropriate settings in each company profile.

## Configure purchase orders

1. On the _Admin_ sidebar, go to **Customers** > **Companies**.

1. Find the company in the list and click **Edit**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Advanced Settings** section.

1. Set **Enable Purchase Orders** to `Yes`.

1. When complete, click **Save**.

After activation, the **Approval Rules** section is displayed on the storefront [Account Dashboard](https://docs.magento.com/user-guide/customers/account-dashboard.html) for a company administrator.s

>[!NOTE]
>
>Purchase order access on the storefront must be granted by the company administrator based on [company user role permissions](account-company-roles-permissions.md). 

## Configure payment on account

Payment on Account is an offline payment method that allows companies to make purchases up to the credit limit that is specified in their profile. Payment on Account can be enabled globally, or per company, and appears during checkout only if enabled. When _Payment on Account_ is used as a payment method, a message appears at the top of the order that indicates the status of the account. To configure this payment method for a specific company, see [Manage Company Accounts](account-company-manage.md).

>[!NOTE]
>
>Payment on Account is not supported for orders with [multiple shipping addresses](https://docs.magento.com/user-guide/shipping/shipping-multiaddress.html) and does not appear among the payment options for these orders.

To enable Payment on Account for your store:

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, choose **Payment Methods**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Payment on Account** section.

   ![Payment on Account](./assets/payment-methods-payment-on-account.png)<!--- zoom --->

   >[!NOTE]
   >
   >If necessary, first deselect the **Use system value** checkbox to change these settings.

1. To allow payment on account, set **Enabled** to `Yes`.

1. Enter a **Title** that identifies the payment method during checkout, or you can accept the `Payment on Account` default title.

1. If orders typically wait for approval, accept the default **New Order Status** as `Pending` until it is approved.

   If you prefer, you can use the `Processing` or `Suspected Fraud` status for new orders with this payment method.

1. Set **Payment from Applicable Countries** to one of the following:

   - `All Allowed Countries` - Customers from all [countries](https://docs.magento.com/user-guide/stores/country-options.html) specified in your store configuration can use this payment method.
   - `Specific Countries` - After you choose this option, the _Payment from Specific Countries_ list appears. To select multiple countries, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

1. Set **Minimum Order Total** and **Maximum Order Total** to the order amounts required to qualify for this payment method.

   >[!NOTE]
   >
   >An order qualifies if the total falls between, or exactly matches, the minimum or maximum total values.

1. Enter a **Sort Order** number that sets the position of this item in the list of payment methods that is displayed during checkout.

   The value is relative to the other payment methods. (`0` = first, `1` = second, `2` = third, and so on.)

1. When complete, click **Save Config**.
