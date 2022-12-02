---
title: New Account Options
description: New Account Options include basic account options combined with advanced options.
---

# New Account Options

In the Create New Account Options section of the configuration, the basic account options are combined with more advanced options that relate to VAT ID Validation and custom integrations. The following instructions cover only the most frequently used options. To learn about automatic customer group assignments, see [VAT Validation](../stores-purchase/vat.md).

![Create New Account Options](assets/customer-configuration-create-new-account-options.png)<!-- zoom -->

## Set up the basic customer account options

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _Settings_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Customers]** and choose **[!UICONTROL Customer Configuration]**.

1. Expand the **[!UICONTROL Create New Account Options]** section and do the following:

   - Set **[!UICONTROL Default Group]** to the customer group that is assigned to new customers when an account is created.

   - If you have a Value Added Tax number and want it to be visible to customers, set **[!UICONTROL Show VAT Number on Storefront]** to `Yes`.

   - To require a customer's email during Admin order creation for a customer, set **[!UICONTROL Email is required field for Admin order creation]** to `Yes`.

   - Enter the **[!UICONTROL Default Email Domain]** for the store, such as `mystore.com`

   - Set **[!UICONTROL Default Welcome Email]** to the template that is used for the Welcome email sent to new customers.

   - Set **[!UICONTROL Default Welcome Email without Password]** to the template that is used when a customer account is created that does not yet have a password. For example, a customer account created from the Admin does not yet have a password assigned.

   - Set **[!UICONTROL Email Sender]** to the store contact that appears as the sender of the Welcome email.

   - To require that customers confirm their request to open an account with your store, set **[!UICONTROL Require Emails Confirmation]** to `Yes`. Then, set **[!UICONTROL Confirmation Link Email]** to the template that is used for the confirmation email.

   - Set **[!UICONTROL Welcome Email]** to the template that is used for the Welcome message that is sent after the account is confirmed.

  For detailed information about each of the options available in this configuration option set, see the _Create New Account Options_ [configuration reference](https://docs.magento.com/user-guide/configuration/customers/customer-configuration.html).

1. When complete, click **[!UICONTROL Save Config]**.
