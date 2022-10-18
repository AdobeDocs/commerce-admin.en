---
title: Store localization
description: Learn how to localize a store or store view.
---
# Store localization

Most of the text that appears to be hard-coded on pages throughout your store can be instantly changed to a different language by changing the locale of the view. Changing the locale does not actually translate the text word-for-word, but simply references a different translation table that provides the interface text that is used throughout the store. The text that can be changed includes navigational titles, labels, buttons, and links such as _My Cart_ and _My Account_. You can also use the [Inline Translation](https://docs.magento.com/user-guide/configuration/advanced/developer.html) tool to touch up text in the interface.

Language packs can be found under [Translations & Localization][1]{:target="_blank"} on Commerce Marketplace. New extensions are continually added to Marketplace, so check back often.

## Step 1: Install a language pack

Follow the standard instructions to install the language pack extension. For detailed information about installing an extension, see [General CLI installation][2] in the *Extensions Guide*.

## Step 2: Create a store view for the language

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **All Stores**.

1. Click **Create Store View**.

1. Set the options for the new store view:

   - **Store** — Choose the store that is the parent of the view.

   - **Name** — Enter a name for the store view. For example: Portuguese.

      In the header of the store, the name appears in the _language chooser_.

   - **Code** — Enter a **Code** in lowercase characters to identify the view. For example: `portuguese`.

   - **Status** — To activate the view, set to `Enabled`.

   - **Sort Order** — (Optional) Enter a number to determine the sequence in which this view is listed with other views.

1. When complete, click **Save Store View**.

## Step 3: Change the locale of the store view

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the upper-left corner, set **Store View** to the specific view where the configuration is to apply.

1. When prompted to confirm scope switching, click **OK**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Locale Options** section.

1. Clear the **Use Website** checkbox after the Locale field and set **Locale** to the language that you want to assign to the view.

   If there are several variations of the language available, make sure to choose the one for the specific region or dialect.

1. When complete, click **Save Config**.

   After you change the language of the locale, the remaining content that you have created, including product names and descriptions, categories, [CMS](../content-design/page-translate.md) pages, and blocks must be translated separately for each store view.

## Localize products

If your store has multiple views in different languages, the same products are available in each store view. You can use the same basic product information, such as SKU, price, and inventory level, regardless of language. Then, translate only the product name, description fields, and meta data as needed for each language.

### Step 1: Translate product fields

1. On the _Admin_ sidebar, go to  **Catalog** > **Products**.

1. In the grid, find the product to be translated and open it in edit mode.

1. In the upper-left corner, set **Store View** to the view for the translation and click **OK** when prompted to confirm.

1. For each field to be edited, do the following:

   - Deselect the **Use Default Value** checkbox to the right of the field.

   - Either paste or type the translated text into the field.

   Make sure to translate all text fields, including [image](../catalog/catalog-images-video.md) labels and Alt text, [Search Engine Optimization](../catalog/product-search-engine-optimization.md) fields and any [Custom Options](../catalog/settings-advanced-custom-options.md) information.

1. When complete, click **Save**.

### Step 2: Translate field labels

1. On the _Admin_ sidebar, go to **Stores** > _Attributes_ > **Product**.

1. In the list, find the attribute to be translated and open in edit mode.

1. In the left panel, choose **Manage Labels**.

1. In the _Manage Titles_ section, enter a translated label for each store view.

   ![Enter Translated Labels](./assets/product-attribute-labels-translate.png)<!-- zoom -->

1. When complete, click **Save Attribute**.

### Step 3: Translate all categories

1. On the _Admin_ sidebar, go to **Catalog** > **Categories**.

1. At the upper-left corner, set **Store View** to the view for the translation and click **OK** when prompted to confirm.

1. In the tree, find the category to be translated and open it in edit mode.

1. For _Basic Information_, translate **Category Name**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the _Content_ section and translate **Description**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Search Engine Optimization Settings** section and translate the following fields:

   - **Meta Title**
   - **Meta Keywords**
   - **Meta Description**

1. Under the _Search Engine Optimization Settings_ section, do the following to translate the **URL Key**:

   - Clear the **Use Default Value** checkbox to the right of the field.

   - Enter the translated text.

   - Make sure that the **Create Permanent Redirect for old URL** checkbox is selected.

   ![Translate the URL key](./assets/category-translate-url-key.png)

1. When complete, click **Save Category**.

1. Repeat the process for all categories used in the store.

### Step 4: Translate product attributes and attributes options

1. On the _Admin_ sidebar, go to **Stores** > _Attributes_ > **Product**.

1. Select the attribute to be translated.

1. Choose **Manage Label** on the left and set the **Managed Titles** options to define the attribute title translations.

   ![Manage Titles](./assets/manage-label-tab.png)<!-- zoom -->

1. Choose **Properties** on the left and enter the translated attribute options in the **Manage Options** section.

   ![Manage Options](./assets/manage-option-tab.png)<!-- zoom -->

1. When complete, click **Save Attribute**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html
