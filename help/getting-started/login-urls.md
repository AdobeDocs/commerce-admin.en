---
title: Login credentials and URLs
description: Learn about the Commerce URLs and account credentials used to gain access to your Admin and to your storefront.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
TQID: https://experienceleague.adobe.com/8IGacP581jwpVtFnCFXRrG5vuIwCJaAUnbliitMHuf8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: d41d3a54-9721-475c-abd6-295bebfba9e4
    internal-label: Login credentials and URLs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
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

[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."}

Adobe provides a sample data set that includes a sample store with more than 250 products (about 200 of them are configurable products), categories, promotional price rules, CMS pages, banners, and so on. Sample data uses the _Luma_ theme on the storefront. [Installing this sample data](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) is optional, but can be helpful for testing and developing customizations for your eCommerce business.
