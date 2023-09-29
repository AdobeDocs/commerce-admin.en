---
title: Prelaunch checklist
description: Use this list to check the required configuration settings to make sure that everything is correct before your store goes to production.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
---
# Prelaunch checklist

After you complete the design, development, and testing of your store, check the following configuration settings to make sure that everything is correct before the store _goes live_. For a comprehensive description of every configuration setting, see the [_Configuration Reference_](../configuration-reference/guide-overview.md).

## General settings

- [Store URLs](../stores-purchase/store-urls.md) - Verify that the store URLs for the storefront and Admin are correct for a live production environment.
- Security Certificate - Before launching your store, install a 100% Signed and Trusted Security Certificate for the domain specified in the Base URL.
- [Store Email Addresses](../getting-started/store-details.md#store-email-addresses) - Complete all the email addresses that are used to send and receive email notifications, such as new orders, invoices, shipments, credit memos, product price alerts, and newsletters. Make sure that each field contains a valid business email address.

## Marketing settings

- [Email Templates](../systems/email-templates.md) - Update the default email templates to reflect your brand. Make sure to update the configuration if you create templates.
- [Sales Communications](../stores-purchase/introduction.md#order-management-and-operations) - Make sure that your invoices and packing slips include the correct business information and reflect your brand.
- [Google Tools](../merchandising-promotions/google-tools.md) - [!DNL Commerce] provides integration with Google API to allow your business to use Google Analytics and Google AdWords.

## Sales settings

- [Cart Options](../stores-purchase/cart-configuration.md) - Look at the cart configuration settings, to see if there is anything that you want to change, such as setting the minimum order amount and lifetime of the prices in the cart.
- [Checkout Options](../stores-purchase/checkout-process.md#checkout-options) - Look at the checkout options, to see if there is anything that you want to change, such as setting up terms and conditions, and configuring guest checkout.
- [Taxes](../stores-purchase/taxes.md) - Make sure that taxes are properly configured according to your business tax rules and local requirements.
- [Delivery Methods](../stores-purchase/delivery.md) - Enable all carriers and delivery methods to be used by the company.
- [PayPal](../stores-purchase/paypal.md) - If you plan to offer your customers the convenience of paying with PayPal, open a PayPal Merchant Account, and set up a payment method. Run some test transactions in Sandbox Mode before the store goes live.
- [Payment Methods](../stores-purchase/payments.md) - Enable the payment methods that you plan to use, and make sure that they are properly configured. Check the order status settings, accepted currency, allowed countries, and so on.

## System settings

[Cron (Scheduled Tasks)](../systems/cron.md) - Cron jobs are used to process email, catalog price rules, newsletters, customer alerts, Google sitemaps, update currency rates, and so on. Make sure that Cron jobs are set to run at the appropriate time interval, in minutes.
