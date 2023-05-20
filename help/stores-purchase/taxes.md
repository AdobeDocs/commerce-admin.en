---
title: Taxes
description: Learn how to configure your store to calculate taxes according to the requirements of your locale.
exl-id: bf807132-416f-497a-82c4-b00dba4d3092
---
# Taxes

Configure your store to calculate taxes according to the requirements of your locale. You can set up [tax classes](tax-class.md) for products and customer groups, and create [tax rules](tax-rules.md) that combine product and customer classes, tax zones, and rates. Commerce also provides configuration settings for fixed product taxes, compound taxes, and display for prices across international borders. If you are required to collect a [value-added tax](vat.md), you can set up your store to automatically calculate the appropriate amount with validation.

>[!NOTE]
>
>Adobe Commerce and Magento Open Source releases 2.4.0 through 2.4.3 included the Vertex vendor-developed extension used to integrate with the Vertex Cloud to provide tax management and address cleansing. Starting with the 2.4.4 release, this extension is no longer bundled with the core release and must be installed and updated from the Commerce Marketplace or directly from the vendor. [Contact Vertex](https://marketplace.magento.com/partner/vertex_inc) for information about the extension and documentation.<br><br>
>
>If you have the bundled extension enabled and configured, you must update your composer.json file as part of the 2.4.4 upgrade process and to manage extension updates going forward. See [Upgrade modules](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) in the _Upgrade Guide_.

## Quick reference

Some tax settings have a choice of options that determines the way the tax is calculated and presented to the customer. For more information, see [International Tax Guidelines](international-tax-guidelines.md).

Use the following tables for reference when configuring tax calculation settings:

### Tax calculation methods

Tax calculation method options include [!UICONTROL Unit Price], [!UICONTROL Row Total], and [!UICONTROL Total]. The following table explains how rounding (to two digits) is handled for different settings.

|Setting|Calculation and Display|
|--- |--- |
|[!UICONTROL Unit Price]|Commerce calculates the tax for each item and displays prices tax-inclusive. To calculate the tax total, it rounds the tax for each item, and then adds them together.|
|[!UICONTROL Row Total]|Commerce calculates the tax for each line. To calculate the tax total, it rounds the tax for each line item and then adds them together.|
|[!UICONTROL Total]|Commerce calculates the tax for each item and adds those tax values to calculate the total unrounded tax amount for the order. It then applies the specified rounding mode to the total tax to determine the total tax for the order.|

{style="table-layout:auto"}

### Catalog prices with or without tax

The possible display fields vary depending on the calculation method and whether the catalog prices include or exclude taxes. Display fields have two-decimal precision in normal computations. Some combinations of price settings display prices that both include and exclude tax. When both appear on the same line item, it can be confusing to customers, and triggers a [warning](taxes.md#warning-messages).

|Setting|Calculation and Display|
|--- |--- |
|[!UICONTROL Excluding Tax]|Using this setting, the base item price is used as it is entered and the tax calculation methods are applied.|
|[!UICONTROL IncludingTax]|Using this setting, the base item price that excludes tax is calculated first. This value is used as the base price, and the tax calculation methods are applied.|

{style="table-layout:auto"}

>[!IMPORTANT]
>
>There are changes from earlier versions for EU merchants or other VAT merchants who display prices including tax and operate in several countries with multiple store views. If you load prices with more than two digits of precision, Commerce automatically rounds all prices to two digits to ensure that a consistent price is presented to buyers.

### Shipping prices with or without tax

|Setting|Display|Calculation|
|--- |--- |--- |
|[!UICONTROL Excluding Tax]|Appears without tax.|Normal calculation. Shipping is added to cart total, typically displayed as a separate item.|
|[!UICONTROL Including Tax]|Can be tax inclusive, or tax can be displayed separately.|Shipping is treated as another item in cart with taxes, using the same calculations.|

{style="table-layout:auto"}

### Tax amounts as line items

To display two different tax amounts as separate line items, such as GST and PST for Canadian stores, you must set different priorities for the related tax rules. However, in previous tax calculations, taxes with different priorities would automatically be compounded. To correctly display separate tax amounts without an incorrect compounding of the tax amounts, you can set different priorities, and also select the _Calculate off subtotal only_ checkbox. This setting produces correctly calculated tax amounts that appear as separate line items.

## Warning messages

Some combinations of tax-related options might be confusing to customers and trigger a warning. These conditions might occur when the tax calculation method is set to `Row` or `Total`, and the customer is presented with prices that both exclude and include tax. It can also occur when there is tax on a per-item basis in the cart. Because the tax calculation is rounded, the amount that appears in the cart might differ from the amount that a customer expects to pay.

If your tax calculation is based on a problematic configuration, the following warnings appear:

![Exclamation point](../assets/icon-warning.png) **Warning**. `Tax discount configuration might result in different discounts than a customer might expect for store(s); Europe Website (French), Europe Website (German). Please see source for more details.`

![Exclamation point](../assets/icon-warning.png) **Warning**. `Tax configuration can result in rounding errors for store(s): Europe Websites (French), Europe Websites (German).`

## Place of supply for digital goods (EU)

European Union (EU) merchants must report their digital goods sold by quarter to each member country. Digital goods are taxed based on the customer's shipping address. The law requires merchants to run a tax report and identify the relevant tax amounts for digital goods, as opposed to physical goods.

Merchants must report all digital goods sold by EU member countries on a quarterly basis to a central tax administration, along with payment due for tax collected during the period.

Merchants who have not yet reached the threshold (50k/100k Euro of annual business) must continue to report physical goods sold to the EU states where they have registered VAT numbers.

Merchants who are audited for taxes paid for digital goods, must provide two pieces of supporting information to establish the customer place of residence.

- The customer's shipping address and a record of a successful payment transaction can be used to establish the customer place of residence. (Payment is accepted only if the shipping address matches payment provider information.)
- The information can also be captured directly from the data store in the Commerce database tables.

_**To collect digital goods tax information:**_

1. Load the tax rates for all EU member countries.

1. Create a digital goods product tax class.

1. Assign all your digital goods to the digital goods product tax class.

1. Create [tax rules](tax-rules.md) for your physical goods, using physical product tax classes, and associate them with the appropriate tax rates.

1. Create tax rules for your digital goods, using the product tax class for digital goods, and associate them with the appropriate tax rates for EU member countries.

1. Run the tax report for the appropriate period, and collect the required digital goods information.

1. Export the tax amounts that are related to the tax rates for the digital goods product tax class.

Additional resources:

- [European Commission Taxation and Customs Union ][1]
- [EU 1015 Place of Supply Changes][2]

[1]: https://taxation-customs.ec.europa.eu/taxation/vat/how_vat_works/vat_on_services/index_en.html
[2]: https://www2.deloitte.com/global/en/services/tax.html
