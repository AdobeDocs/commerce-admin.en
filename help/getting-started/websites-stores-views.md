---
title: Site, Store, and View Scope
description: Learn about the hierarchy of websites, stores, and store views that you can use to deliver shopping experiences for your customers. 
---
# Site, Store, and View Scope

Every Adobe Commerce and Magento Open Source installation has a [hierarchy](https://docs.magento.com/user-guide/stores/stores-all-stores.html) of websites, stores, and store views. The term _scope_ determines where in the hierarchy a database entity — such as a product, attribute, or category — content element, or configuration setting applies. Websites, stores, and store views have one-to-many parent/child relationships. A single installation can have multiple websites, and each website can have multiple stores and store views.

>[!NOTE]
>
>To learn more, see [Multiple websites or stores ](https://devdocs.magento.com/guides/v2.4/config-guide/multi-site/ms_over.html) in the Commerce developer documentation.

## Websites

Installations begin with a single [website](https://docs.magento.com/user-guide/stores/stores-all-create-website.html), which is called _Main Website_ by default. You can also set up multiple websites for a single installation, each with its own IP address and domain.

## Stores

A single website can have multiple [stores](https://docs.magento.com/user-guide/stores/stores-all-create-store.html), each with its own main menu. The stores share the product catalog, but can have a different selection of products and design. All stores under the same website share the Admin and checkout.

## Store Views

Each store that is available to customers is presented according to a specific _[view](https://docs.magento.com/user-guide/stores/stores-all-create-view.html)_. Initially, a store has a single default view. Additional store views can be added to support different languages, or for other purposes. Customers can use the language chooser in the header to change the store view.

When working with websites, stores, and store views, keep the following in mind:

- Commerce instances have a cascading model: global → website → store → store view.
- Every website has at least one default store and store view.
- Each store view can have a different base URL.
- The primary function of a website is top-level feature configuration.
- The primary function of a store is root category configuration.
- The primary function of a store view is translation information and currency symbol configuration.

## Scope settings

If your Adobe Commerce or Magento Open Source installation has a hierarchy of websites, stores, or views, you can set the context, or “scope” of a configuration setting to apply to a specific part of the installation. The context of many database entities can also be assigned a specific scope to determine how it is used in the store hierarchy. To learn more, see [Product Scope](https://docs.magento.com/user-guide/catalog/product-scope.html) and [Price Scope](https://docs.magento.com/user-guide/catalog/catalog-price-scope.html).

Some configuration settings such as postal code, have a global scope because the same value is used throughout the system. The [website](https://docs.magento.com/user-guide/stores/stores-all-create-website.html) scope applies to any stores below that level in the hierarchy, including all stores and their views. Any item with the scope of [store view](https://docs.magento.com/user-guide/stores/stores-all-create-view.html) can be set differently for each store view, which is typically used to support multiple languages. To override the default values of configuration settings, see [Changing Scope](https://docs.magento.com/user-guide/configuration/scope-change.html).

Unless the store is running in [Single Store Mode](https://docs.magento.com/user-guide/stores/store-mode-single.html), the scope of each configuration setting appears in small text below the field label. If your installation includes multiple websites, stores, or views, choose the [Store View](https://docs.magento.com/user-guide/stores/stores-all-create-view.html) where the settings apply before making any changes.

![Hierarchy of websites, stores, and store views](./assets/scope-multisite.png)<!-- zoom -->

|Scope|Description|
|--- |--- |
|Global|System-wide settings and resources that are available throughout the installation.|
|Website|Settings and resources that are limited to the current website. Each website has a default store.|
|Store|Settings and resources that are limited to the current store. Each store has a default root category (main menu) and default store view.|
|Store View|Setting and resources that are limited to the current store view.|