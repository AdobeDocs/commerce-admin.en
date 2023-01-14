---
title: Product data attributes reference
description: Use this reference of product data attributes when you work with product data imports and exports.
exl-id: 9ffa4d1f-cbf8-4a08-bb79-33f21e698a74
---
# Product data attributes reference

The following table lists the attributes from a typical product export, in the default order in which they appear. Each attribute is represented in the CSV file as a column, and product records are represented by rows. Columns that begin with an underscore contain service data such as properties or option values for complex data. You can [export](data-export.md) a product from your catalog, to see how each attribute is represented in the data.

The installation used to export this data has the sample data installed, and has two websites and several store views. Although this list includes all columns that are typically exported, the `sku` is the only required value. To import data, you can include only the columns with changes. The `sku` should be the first column, but the order of the rest of the attributes doesn't matter.

## Simple product CSV file structure

|Attribute|Description|
|--- |--- |
|`sku`|(Required) The Stock-Keeping Unit is a unique, alphanumeric identifier that is used to track inventory. A SKU can be up to 64 characters in length. For example: `sku123`<br/>**_Note:_** A SKU longer than 64 characters causes import to fail.|
|`store_view_code`|Identifies the specific store views where the product is available. If blank, the product is available at the default store view. For example: `storeview1`, `english`, `spanish`|
|`attribute_set_code`|Assigns the product to a specific attribute set or product template, according to product type. Once the product is created, the attribute set cannot be changed. For example: `default`|
|`product_type`|Indicates the type of product. Values:<br/>`simple` — Tangible items that are usually sold as single units or in fixed quantities.<br/>`grouped` — A group of separate products that is sold as a set.<br/>`configurable` — A product with multiple options that the customer must select before making a purchase. Inventory can be managed for each set of variations because they represent a separate product with a distinct SKU. For example, a combination of color and size for a configurable product is associated with a specific SKU in the catalog.<br/>`virtual` — A non-tangible product that does not require shipping and is not kept in inventory. Examples include services, memberships, and subscriptions.<br/>`bundle` — A customizable product set  of simple products that are sold together.|
|`categories`|Indicates each category that is assigned to the product. Separate categories and subcategories with a forward slash. To indicate multiple category paths, separate each path with a pipe &#124; symbol. For example: `Default Category/Gear&#124;Default Category/Gear/Bags`|
|`product_websites`|The website code of each website where the product is available. A single product can be assigned to multiple websites, or limited to one. If specifying multiple websites, separate each with a comma and without a space. For example: `base` or `base,website2`|
|`name`|The product name appears in all product listings, and is the name that customers use to identify the product.|
|`description`|The product description provides detailed information about the product, and might include simple HTML tags.|
|`short_description`|The use of the short product description depends on the theme. It might appear in product listings and is sometimes used in RSS feed listings sent to shopping sites.|
|`weight`|The weight of the individual product. The actual product weight is determined by the carrier at the time of shipment.|
|product_online|Determines if the product is available for sale in the store. Values:<br/>`1` — (Yes) The product is enabled, and available for sale.<br/>`2` — (No) The product is disabled, and is not available for sale.|
|`tax_class_name`|The name of the tax class that is associated with this product.|
|`visibility`|Determines if the product is visible in the catalog, and made available for search. Values:<br/>`Not Visible Individually` — The product is not included in product listings, although it might be available as a variation of another product.<br/>`Catalog` — The product appears in all catalog listings.<br/>`Search` —The product is available for search operations.<br/>`Catalog, Search` — The product is included in catalog listings and is also available for search.|
|`price`|The price that the product is offered for sale in your store.|
|`special_price`|The discounted price of the product during the specified date range.|
|`special_price_from_date`|The beginning date of the time period when the special price is in effect.|
|`special_price_to_date`|The last date of the time period when the special price is in effect.|
|`url_key`|The part of the URL that identifies the product. The default value is based on the product name. For example: `product-name`|
|save_rewrites_history|When provided with value `1` with a new `url_key`, a new 301 URL rewrite is generated so that the old URL is redirected to the new URL.|
|`meta_title`|The meta title appears in the title bar and tab of the browser and search results lists. The meta title should be unique to the product, incorporate high-value keywords, and be fewer than 70 characters in length.|
|`meta_keywords`|Meta keywords are visible only to search engines, and are ignored by some search engines. Choose high-value keywords, separated by a comma. For example: `keyword1`, `keyword2`, `keyword3`|
|`meta_description`|Meta descriptions provide a brief overview of the product for search results listings. Ideally, a meta description should be between 150-160 characters in length, although the field accepts up to 255 characters.|
|`base_image`|The relative path for the main image on the product page. Commerce stores files internally in an alphabetical folder structure. You can see the exact location of each image in the exported data. For example: `/sample_data/m/b/mb01-blue-0.jpg`<br/>To upload a new image or write over an existing image, enter the file name, preceded by a forward slash. For example: `/image.jpg`|
|`base_image_label`|The label that is associated with the base image.|
|`small_image`|The  file name of the small image that is used on catalog pages, preceded by a forward slash. For example: `/image.jpg`|
|`small_image_label`|The label associated with the small image. For example: `Small Image 1`, `Small Image 2`|
|`thumbnail_image`|The file names of any thumbnail image to appear in the gallery on the product page, preceded by a forward slash. For example: `/image.jpg`|
|`thumbnail_image_label`|The label associated with any thumbnail images. For example: `Thumbnail 1`, `Thumbnail 2`|
|`created_at`|Indicates the date when the product was created. The date is automatically generated when the product is created, but can be edited later.|
|`updated_at`|Indicates the date when the product was last updated.|
|`new_from_date`|Specifies the "from" date for new product listings, and determines if the product is featured as a new product.|
|`new_to_date`|Specifies the "to" date for new product listings, and determines if the product is featured as a new product.|
|`display_product_options_in`|If the product has multiple options, determines where they appear on the product page. Values: Product Info Column / Block after Info Column|
|`map_price`|The minimum advertised price of the product. (Appears only if MAP is enabled.)|
|`msrp_price`|The manufacturer's suggested retail price for the product. (Appears only if MAP is enabled.)|
|`map_enabled`|Determines if Minimum Advertised Price is enabled in the configuration. Values:<br/>`1` — (Yes) MAP is enabled.<br/>`0` (or blank) — (No)  MAP is not enabled.|
|`gift_message_available`|Determines if a gift message can be included with the product purchase. Values:<br/>`1` — (Yes) The option to include a gift message is presented to the customer.<br/>`0` (or blank) — (No) The option to include a gift message is not presented to the customer.|
|`custom_design`|Lists the available themes that can be applied to the product page.|
|`custom_design_from`|Specifies the beginning date when the selected theme is applied to the product page.|
|`custom_design_to`|Specifies the end date when the selected theme is applied to the product page.|
|`custom_layout_update`|Additional XML code that is applied as a layout update to the product page.|
|`page_layout`|Determines the page layout of the product page. Values:<br/>`No layout updates` — No change is made to the page layout.<br/>`1 column` — Applies a one-column layout to the product page.<br/>`2 columns with left bar` — Applies a two-column layout with a left sidebar to the product page.<br/>`2 columns with right bar` — Applies a two-column layout with a right sidebar to the product page.<br/>`3 columns` — Applies a three-column layout to the product page.<br/>`empty` — Applies a blank layout to the product page.|
|`product_options_container`|If the product has multiple options, determines where they appear on the product page. Values: Product Info Column / Block after Info Column|
|`msrp_display_actual_price_type`|Determines where the actual price of a product is visible to the customer. Values:<br/>`In Cart` — Displays the actual product price in the shopping cart.<br/>`Before Order Confirmation` — Displays the actual product price at the end of the checkout process, just before the order is confirmed.<br/>`On Gesture` — Displays the actual product price in a popup when the customer clicks the _Click for price_ or _What's this?_ link.|
|`country_of_manufacture`|Identifies the country where the product was manufactured.|
|`additional_attributes`|Additional attributes created for the product. For example: <br/>`has_options=0,required_options=0color=Black,has_options=0,required_options=0,size_general=XS`|
|`qty`|The quantity of the product that is currently in stock.|
|`out_of_stock_qty`|The stock level that determines the product to be out of stock.|
|`use_config_min_qty`|Determines if the default value from the configuration is used, and corresponds to the Use Config Settings checkbox. Values:<br/>`1` — (Yes) The default configuration setting is used for the value of this attribute.<br/>`0` (or blank) — (No) The default configuration can be overridden for the value of this attribute.|
|`is_qty_decimal`|Determines if the qty attribute has a decimal value. Values:<br/>`1` — (Yes) The value of the qty attribute is a decimal value.<br/>`0` (or blank) — (No) The value of the qty attribute is a whole number (integer).|
|`allow_backorders`|Determines if your store allows backorders, and how they are managed.|
|`use_config_backorders`|Determines if the default configuration setting for backorders is used, and corresponds to the state of the Use Config Settings checkbox. Values:<br/>`1` — (Yes) The value of the qty attribute is a decimal value.<br/>`0` (or blank) — (No) The value of the qty attribute is a whole number (integer).|
|`min_cart_qty`|Specifies the minimum quantity of the item that can be purchased in a single order.|
|`use_config_min_sale_qty`|Determines if the default configuration setting for minimum quantity is used, and corresponds to the state of the Use Config Settings checkbox. Values:<br/>`1` — (Yes) The value of the qty attribute is a decimal value.<br/>`0` (or blank) — (No) The value of the qty attribute is a whole number (integer).|
|`max_cart_qty`|Specifies the maximum quantity of the product that can be purchased in a single order.|
|`use_config_max_sale_qty`|Determines if the default configuration setting for maximum quantity is used, and corresponds to the state of the Use Config Settings checkbox. Values:<br/>`1` — (Yes) The value of the qty attribute is a decimal value.<br/>**0** (or blank) — (No) The value of the qty attribute is a whole number (integer).|
|`is_in_stock`|Indicates if the product is in stock.|
|`notify_on_stock_below`|Specifies the stock level that triggers an _out of stock_ notification.|
|`use_config_notify_stock_qty`|Determines if the default configuration setting is used to trigger stock level notification, and corresponds to the state of the Use Config Settings checkbox. Values:<br/>`1` — (Yes) The value of the qty attribute is a decimal value.<br/>`0` (or blank) — (No) The value of the qty attribute is a whole number (integer).|
|`manage_stock`|Determines if inventory control is used to manage the product. Values:<br/>`1` — (Yes) Activates full inventory control to manage stock levels of the product.<br/>`0` (or blank) — (No) The system does not track the number of items that are currently in stock.|
|`use_config_manage_stock`|Determines if the default configuration setting for managing stock is used, and corresponds to the state of the Use Config Settings checkbox. Values:<br/>`1` — (Yes) The value of the qty attribute is a decimal value.<br/>`0` (or blank)—(No) The value of the qty attribute is a whole number (integer).|
|`use_config_qty_increments`|Determines if the default configuration setting for quantity increments is used, and corresponds to the state of the Use Config Settings checkbox. Values:<br/>`1` — (Yes) The value of the qty attribute is a decimal value.<br/>`0` (or blank) — (No) The value of the qty attribute is a whole number (integer).|
|`qty_increments`|Determines if the product is sold in quantity increments. Options: `Yes` / `No`|
|`use_config_enable_qty_inc`|Determines if the default configuration setting to enable quantity increments is used, and corresponds to the state of the Use Config Settings checkbox. Values:<br/>`1` — (Yes) The value of the qty attribute is a decimal value.<br/>`0` (or blank) — (No) The value of the qty attribute is a whole number (integer).|
|`enable_qty_increments`|Determines if quantity increments are enabled for the product.|
|`is_decimal_divided`|Determines if parts of the product can be shipped separately. Options: `Yes` / `No`|
|`website_id`|For installations with multiple websites, identifies a specific website where the product is available. If blank, the product is available in all websites.|
|`related_skus`|Lists the SKU of each product that has been identified as a related product. For example: `24-WG080,24-UG03,24-UG01,24-UG02`|
|`related_position`|Determines the position (sort order) of the SKUs that are listed as Related Products in the related_skus column. For example: `1,2,3,4`|
|`crosssell_skus`|Lists the SKU of each product that has been identified as a cross-sell.|
|`crosssell_position`|Determines the position (sort order) of the SKUs that are listed as Cross-sell Products in the `crosssell_skus` column.|
|`upsell_skus`|Lists the SKU of each product that has been identified as an Up sell.|
|`upsell_position`|Determines the position (sort order) of the SKUs that are listed as up-sell products in the `upsell_skus` column.|
|`additional_images`|The  file names of any additional image to be associated with the product, preceded by a forward slash. For example: `/image.jpg`|
|`additional_image_labels`|The labels associated with any additional images. For example: `Label 1`, `Label 2`|
|`custom_options`|Specifies the properties and values assigned to each custom option. For example: <br/>`name=Color, type=drop_down, required=1, price= price_type=fixed, sku=, option_title=Black|name=Color, type=drop_down, required=1, price=, price_type=fixed, sku=, option_title=White`|

{style="table-layout:auto"}

## Service data for product variations

|Attribute|Description|Applies to|
|--- |--- | --- |
|`_super_products_sku`|The generated SKU for a configurable product variation. For example: WB03-XS-Green|Configurable Products|
|`_super_attribute_code`|The attribute code of a configurable product variation. For example: color|Configurable Products|
|`_super_attribute_option`|The value of a configurable product variation. For example: green|Configurable Products|
|`_super_attribute_price_corr`|A price adjustment that is associated with a configurable product variation.|Configurable Products|
|`_associated_sku`|The SKU of a product that is associated with a grouped product.|Grouped Products <br/>Bundle Products|
|`_associated_default_qty`|Determines the quantity of the associated product that is included.|Configurable Products<br/>Grouped Products<br/>Bundle Products|
|`_associated_position`|Determines the position of the associated product when listed with other associated products.|Configurable Products<br/>Grouped Products<br/>Bundle Products|

{style="table-layout:auto"}

## Complex product data attributes

The term complex data refers to the data that is associated with multiple product options. The following product types use data that originates from separate products to create product variations and multiple options.

- [Configurable](../catalog/product-create-configurable.md)
- [Grouped](../catalog/product-create-grouped.md)
- [Bundle](../catalog/product-create-bundle.md)

If you export a configurable product, you would find the standard attributes that make up a simple product, plus the additional attributes that are needed to manage complex data.

![Configurable product - exported data](./assets/data-exported-configurable-product.png)<!-- zoom -->

### Configurable products

|Attribute|Description|
|--- |--- |
|`configurable_variation_labels`|Labels that identify product variations. For example: `Choose Color:` or `Choose Size:`|
|`configurable_variations`|Describes the values associated with a product variation. For example: `sku=sku-red xs,color=red,size=xs,price=10.99,display=1,image=/pub/media/import/image1.png|sku=sku-red-m,color=red,size=m,price=20.88,display=1,image=/pub/media/import/image2.png`|

{style="table-layout:auto"}

### Grouped products

|Attribute|Description|
|--- |--- |
|`associated_skus`|Identifies the SKUs of the individual products that make up the group.|

{style="table-layout:auto"}

### Bundle products

|Attribute|Description|
|--- |--- |
|`bundle_price_type`|Determines if the price of a bundle item is fixed or dynamic.|
|`bundle_sku_type`|Determines if each item is assigned a variable, dynamic SKU, or if a fixed SKU is used for the bundle. Options: Fixed / Dynamic|
|`bundle_weight_type`|Determines if the weight of a bundle item is variable or fixed.|
|`bundle_values`|Describes teach value associated with a bundle option. For example: `name=Bundle Option One,type=dropdown; required=1, sku=sku-option2,price=10, price_type=fixed`|

{style="table-layout:auto"}

## Advanced pricing attributes

Advanced Price Import/Export allows you to quickly update pricing information for product groups and tier prices. The process to [import](data-import.md) and [export](data-export.md) advanced price data is the same as any other entity type. The sample CSV file contains tier and group prices for each product type that supports advanced pricing. Changing advanced pricing does not affect the rest of the product record.

![Example export data - advanced pricing](./assets/data-advanced-pricing-export-sample.png)<!-- zoom -->

|Attribute|Description|
|--- |--- |
|`sku`|(Required) The Stock-Keeping Unit is a unique, alphanumeric identifier that is used to track inventory. A SKU can be up to 64 characters in length. For example: `sku123`<br/>**_Note:_** A SKU longer than 64 characters causes import to fail.|
|`tier_price_website`|The [website code](../stores-purchase/stores.md#add-websites) identifies each website where tier pricing is available. For example: `-  website1 -  All Websites [USD]`|
|`tier_price_customer`|Identifies the [customers' groups](../customers/customer-groups.md) where tier pricing is available. For example: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer`|
|`tier_price_customer_group`|Identifies the customer groups where tier pricing is available. For example: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer`|
|`tier_price_qty`|The quantity of the product that must be ordered to receive the tier price discount.|
|`tier_price`|The discounted tier price of the product. For [bundle products](../catalog/product-create-bundle.md), tier price is calculated as a percentage.|
|`group_price_website`|The [website code](../stores-purchase/stores.md#add-websites) of each website where group pricing is available. If specifying multiple websites, separate each with a comma and without a space. For example: `-  website1 -  All Websites [USD]`|
|`group_price_customer_group`|Identifies the customers' groups where group pricing is available. For example: `-  NOT LOGGED IN -  General -  Wholesale -  Retailer`|
|`group_price`|The discounted group price of the product. For [bundle products](../catalog/product-create-bundle.md), group price is calculated as a percentage.|

{style="table-layout:auto"}
