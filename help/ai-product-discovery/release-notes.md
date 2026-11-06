---
title: AI Product Discovery Release Notes
description: Review AI Product Discovery release notes for catalog and PDP enrichment features, fixes, upgrade guidance, supported Commerce versions, and known issues.
feature: Release Notes
---
# AI Product Discovery release notes

These release notes cover updates to catalog enrichment and PDP enrichment, including new features, fixes, upgrade requirements, and known issues. Each version entry identifies the affected extension or workflow.

![New](../assets/new.svg) New features
![Fixed issue](../assets/fix.svg) Fixes and improvements
![Known issue](../assets/bug.svg) Known issues

## Release 2.1.2 {#release-2-1-2}

*October 22, 2026*

[!BADGE Supported]{type=Informative tooltip="Supported"} [!DNL Adobe Commerce] 2.4.9, 2.4.8, and 2.4.7 on PHP 8.3 to 8.5.

Version 2.1.2 makes catalog enrichment a self-contained extension. It now includes everything that was previously provided by the separate [!DNL Adobe Brand Visibility] extension (`magento/llm-optimizer`): applying approved suggestions to the catalog, rolling them back, and protecting your own edits from being overwritten.

### Upgrade from earlier versions {#upgrade-from-earlier-versions}

>[!IMPORTANT]
>
>Version 2.1.2 cannot be installed together with the [!DNL Adobe Brand Visibility] extension. If you have it installed, remove it as part of the upgrade.

1. Remove the [!DNL Adobe Brand Visibility] extension, if it is installed:

    ```bash
    composer remove magento/llm-optimizer
    ```

    If the extension was installed by copying or symlinking `Magento/LlmoCatalog` into `app/code`, delete that directory. Do not only disable the module: a disabled module that is still on disk can cause `setup:upgrade` to drop the table that stores the original values of enriched products.

1. Update catalog enrichment and apply the changes:

    ```bash
    composer require magento/module-catalog-enrichment:^2.1
    bin/magento setup:upgrade
    bin/magento cache:flush
    ```

    Flush the cache after the upgrade. The upgrade moves existing access grants to new permission resources, and those grants do not take effect until the cache is cleared.

### Requirements

![New](../assets/new.svg) **PHP 8.3 and [!DNL Adobe Commerce] 2.4.7 or later**—PHP 8.1 is end of life and PHP 8.2 reaches end of life on December 31, 2026, so neither is supported. [!DNL Adobe Commerce] 2.4.6 and earlier are not supported.

### New features

![New](../assets/new.svg) **[!UICONTROL AI Product Discovery] menu**—The catalog enrichment pages now have their own section in the Admin sidebar. Go to **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**. Previously, the page was under **[!UICONTROL Catalog]**.

![New](../assets/new.svg) [!BADGE Beta]{type=Informative tooltip="Not yet generally available"} **[!UICONTROL Product Details Page Enrichment (Beta)]**—A new page under **[!UICONTROL AI Product Discovery]** to review enrichment suggestions for product detail pages. Product details page enrichment is in beta and is not yet generally available.

![New](../assets/new.svg) **Apply and roll back approved suggestions**—Approved name and description updates are written to the catalog by this extension. Commerce records the original value of each enriched attribute the first time it changes, so a rollback always restores the value you had before enrichment, even after several suggestions were applied to the same attribute.

![New](../assets/new.svg) **Your edits are respected**—When you change an enriched name or description in the Admin product form, with **[!UICONTROL Update Attributes]**, or through an import, your value is kept and the related suggestion is marked *Outdated*. A change made at the default scope only affects store views that inherit the value.

![New](../assets/new.svg) **Read-only catalog access for suggestions**—[!DNL Commerce Catalog Agent] can read product, category, attribute set, and product type data to select products for analysis. The read returns only attributes marked **[!UICONTROL Used in Product Listing]**, plus the attributes that can be enriched. It cannot change catalog data.

### Fixes and improvements

![Fixed issue](../assets/fix.svg) **Retried apply reports success**—If an apply request is retried after it has already completed, the retry now reports the changes as applied instead of reporting no changes. Nothing is written twice.

![Fixed issue](../assets/fix.svg) **Only approved services can change the catalog**—Apply and rollback accept only requests from [!DNL Commerce Catalog Agent]. Previously, any valid Adobe IMS token was accepted. The same check now also applies to SOAP requests.

![Fixed issue](../assets/fix.svg) **Clearer errors**—An Adobe IMS outage now returns `401` instead of `500`, so the request is not retried against the catalog, and an unrecognized Adobe IMS environment is rejected instead of being treated as staging.

![Fixed issue](../assets/fix.svg) **Adobe IMS environment**—Catalog enrichment now signs in to the production Adobe IMS environment by default, including on instances connected to a non-production [!DNL Commerce Services] data space. Previously, those instances were sent to the staging environment.

![Fixed issue](../assets/fix.svg) **Sign-in after the [!DNL Adobe Brand Visibility] domain change**—The catalog enrichment page now loads from `abv.adobe.com`, which fixes a sign-in loop after the previous domain started redirecting.

### Known issues

![Known issue](../assets/bug.svg) **Roles with full [!UICONTROL Catalog] access**—A user role saved before this release with all of **[!UICONTROL Catalog]** granted keeps access to the **[!UICONTROL Catalog Enrichment Service API]** resource. Review such roles in **[!UICONTROL System]** > **[!UICONTROL Permissions]** > **[!UICONTROL User Roles]** and clear that resource where it is not needed.

## Release 1.0.2 {#release-1-0-2}

Initial release of the catalog enrichment Admin page. Requires the [!DNL Adobe Brand Visibility] extension to apply suggestions to the catalog.