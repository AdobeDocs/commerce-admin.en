---
title: Login credentials and URLs
description: Learn about the Commerce URLs and account credentials used to gain access to your Admin and to your storefront.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
---
# Login credentials and URLs

Before you proceed with setup and configuration, make sure that you have the information that is required to access the Admin of your store and your Commerce account.

## Storefront URL

The address for your [storefront](storefront.md) is usually the domain that is assigned to your IP address. Some stores are installed at the root, or topmost directory. Others are installed in a directory below the root. The store might reside within a subdomain that is associated with a primary domain. The URL for your store might look like one of the following:

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

If you do not yet have a domain, your store URL includes a series of four numbers, each separated by a period in _dotted quad_ notation.

## Admin URL

The address for your store [Admin](admin.md) is set up during the installation. The default address is the same as your store, but with `/admin` at the end. Although the examples in this guide use the default directory, it is a best practice to run your Admin from a location that is unique to your store.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] account

Your [Commerce account](commerce-account-create.md) provides access to information about your products and services, account settings, billing history, and support resources. To access your account, go to the main Commerce site and click **[!UICONTROL My Account]** in the upper-right corner.

## Customer account

While you are learning your way around the store, make sure to set up a test [customer account](../customers/account-dashboard.md), so you can experience the store and checkout process from the customer's perspective.

## Sample data

Adobe provides a sample data set that includes a sample store with more than 250 products (about 200 of them are configurable products), categories, promotional price rules, CMS pages, banners, and so on. Sample data uses the _Luma_ theme on the storefront. [Installing this sample data](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) is optional, but can be helpful for testing and developing customizations for your eCommerce business.
