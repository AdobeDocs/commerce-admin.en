---
title: Prelaunch Checklist
description: Use this list to check the required configuration settings to make sure that everything is correct before your store goes to production.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
---
# Prelaunch Checklist

After you complete the design, development, and testing of your store, check the following configuration settings to make sure that everything is correct before the store _goes live_. For a comprehensive description of every configuration setting, see the [Configuration Reference](https://docs.magento.com/user-guide/stores/configuration.html).

## General settings

- [Store URLs](https://docs.magento.com/user-guide/stores/store-urls.html) - Verify that the store URLs for the storefront and Admin are correct for a live production environment.
- Security Certificate - Before launching your store, install a 100% Signed and Trusted Security Certificate for the domain specified in the Base URL.
- [Store Email Addresses](https://docs.magento.com/user-guide/stores/store-email-addresses.html) - Complete all the email addresses that are used to send and receive email notifications, such as new orders, invoices, shipments, credit memos, product price alerts, and newsletters. Make sure that each field contains a valid business email address.

## Marketing settings

- [Email Templates](https://docs.magento.com/user-guide/marketing/email-templates.html) - Update the default email templates to reflect your brand. Make sure to update the configuration if you create templates.
- [Sales Communications](https://docs.magento.com/user-guide/marketing/sales-communications.html) - Make sure that your invoices and packing slips include the correct business information and reflect your brand.
- [Google Tools](../merchandising-promotions/google-tools.md) - [!DNL Commerce] provides integration with Google API to allow your business to use Google Analytics and Google AdWords.

## Sales settings

- [Cart Options](https://docs.magento.com/user-guide/sales/cart-configuration.html) - Look at the cart configuration settings, to see if there is anything that you want to change, such as setting the minimum order amount and lifetime of the prices in the cart.
- [Checkout Options](https://docs.magento.com/user-guide/sales/checkout-options.html) - Look at the checkout options, to see if there is anything that you want to change, such as setting up terms and conditions, and configuring guest checkout.
- [Taxes](https://docs.magento.com/user-guide/tax/taxes.html) - Make sure that taxes are properly configured according to your business tax rules and local requirements.
- [Delivery Methods](https://docs.magento.com/user-guide/shipping/delivery.html) - Enable all carriers and delivery methods to be used by the company.
- [PayPal](https://docs.magento.com/user-guide/payment/paypal.html) - If you plan to offer your customers the convenience of paying with PayPal, open a PayPal Merchant Account, and set up a payment method. Run some test transactions in Sandbox Mode before the store goes live.
- [Payment Methods](https://docs.magento.com/user-guide/payment/payments.html) - Enable the payment methods that you plan to use, and make sure that they are properly configured. Check the order status settings, accepted currency, allowed countries, and so on.

## System settings

[Cron (Scheduled Tasks)](https://docs.magento.com/user-guide/system/cron.html) - Cron jobs are used to process email, catalog price rules, newsletters, customer alerts, Google sitemaps, update currency rates, and so on. Make sure that Cron jobs are set to run at the appropriate time interval, in minutes.
