---
title: Tax guidelines by country
description: <Add description here>
---
# Tax guidelines by country

## U.S. tax configuration

These recommended settings can be used for most tax configurations for stores within the United States.

|Tax option|Recommended setting|
|--- |--- |
|Load catalog prices|Excluding tax|
|FPT|No, because FPT is not taxed.|
|Tax based on|Shipping origin|
|Tax Calculation|On total|
|Tax shipping?|No|
|Apply Discount|Before tax|
|Comment|All tax zones are the same priority; ideally, a zone for state and one or more zones for zip code lookup.|

{style="table-layout:auto"}

### Tax classes

| Tax class | Recommended setting |
|--- |--- |
| Tax Class for Shipping | None |

{style="table-layout:auto"}

### Calculation settings

| Calculation | Recommended setting |
|--- |--- |
| Tax Calculation Method Based On | Total |
| Tax Calculation Based On | Shipping Origin |
| Catalog Prices | Excluding Tax |
| Shipping Prices | Excluding Tax |
| Apply Customer Tax | After Discount |
| Apply Discount on Prices | Excluding Tax |

{style="table-layout:auto"}

### Default tax destination calculation

| Setting | Recommended setting |
|--- |--- |
| Default Country | United States |
| Default State | State where business is located. |
| Default Post Code | The postal code that is used in your tax zones. |

{style="table-layout:auto"}

### Price display settings

| Setting | Recommended setting |
|--- |--- |
| Display Product Prices in Catalog | Excluding Tax |
| Display Shipping Prices | Excluding Tax |

{style="table-layout:auto"}

### Shopping cart display settings

| Setting | Recommended setting |
|--- |--- |
| Display Prices | Excluding Tax |
| Display Subtotal | Excluding Tax |
| Display Shipping Amount | Excluding Tax |
| Display Gift Wrapping Prices | Excluding Tax |
| Display Printed Card Prices | Excluding Tax |
| Include Tax in Grand Total | Yes |
| Display Full Tax Summary | Yes |
| Display Zero Tax Subtotal | Yes |

{style="table-layout:auto"}

### Orders, invoices, credit memos, and display settings

| Setting | Recommended setting |
|--- |--- |
| Display Prices | Excluding Tax |
| Display Subtotal | Excluding Tax |
| Display Shipping Amount | Excluding Tax |
| Include Tax in Grand Total | Yes |
| Display Full Tax Summary | Yes |
| Display Zero Tax Subtotal | Yes |

{style="table-layout:auto"}

### Fixed product taxes (FPT)

| Setting | Recommended setting |
|--- |--- |
| Enable FPT | No, except in California. |

{style="table-layout:auto"}

## UK tax configuration

These recommended settings can be used for most tax configurations for stores within the United Kingdom.

### UK B2C tax configuration

|Tax Option|recommended setting|
|--- |--- |
|Load catalog prices|Excluding tax|
|FPT|Yes, including FPT and description|
|Tax based on|Shipping address|
|Tax Calculation|On total|
|Tax shipping?|Yes|
|Apply Discount|Before tax, discount on prices, including tax.|
|Comment|For merchants marking up supplier invoices (including VAT).|

{style="table-layout:auto"}

### U.K. B2B tax configuration

|Tax Option|recommended setting|
|--- |--- |
|Load catalog prices|Excluding tax|
|FPT|Yes, including FPT and description|
|Tax based on|Shipping address|
|Tax Calculation|On item|
|Tax shipping?|Yes|
|Apply Discount|Before tax, discount on prices, including tax.|
|Comment|For B2B merchants to provide simpler VAT supply chain considerations. Tax calculation on row is also valid; however, check with your taxing jurisdiction. Setup assumes that a merchant is in the supply chain and that goods sold are used by other vendors for VAT rebates and so on. This makes it easy to discern tax by item for faster rebate generation. <br/><br/>**_Note:_** Some jurisdictions require different rounding strategies not currently supported by Commerce, and that not all jurisdictions allow item or row level tax.|

{style="table-layout:auto"}

## Canada tax configuration

>[!IMPORTANT]
>
>Merchants located in a GST/PST province (Montreal) should create one tax rule and show a combined tax amount. Be sure to consult a qualified tax authority if you have any questions. For information about the tax requirements of specific provinces, see the following: [Revenu Québec][1], [Government of Saskatchewan][2], and [Manitoba Information for Vendors][3]

|Tax Option|recommended setting|
|--- |--- |
|Load catalog prices|Excluding tax|
|FPT|Yes, including FPT, description, and apply tax to FPT.|
|Tax based on|Shipping origin|
|Tax Calculation|On total|
|Tax shipping?|Yes|
|Apply Discount|Before tax|

{style="table-layout:auto"}

The following example shows how to set up GST tax rates for Canada and PST tax rates for Saskatchewan, with tax rules that calculate and display the two tax rates. Because this is an example configuration, be sure to verify the correct tax rates and rules for your tax jurisdictions. When setting up taxes, set the store scope to apply the configuration to all applicable stores and websites.

- Fixed product tax is included for relevant goods as a product attribute.
- In Quebec, PST is referred to as TVQ. If you need to set up a rate for Quebec, make sure to use TVQ as the identifier.

### Step 1: Complete tax calculation settings

1. On the _Admin_ menu, go to **System** > **Configuration**.

1. In the left panel, expand **Sales** and select **Tax**.

1. Click to expand each section on the page and complete the following settings:

#### Tax Calculation Settings

|Field|Recommended Setting|
|--- |--- |
|Tax Calculation Method Based On|Total|
|Tax Calculation Based On|Shipping Address|
|Catalog Prices|Excluding Tax|
|Shipping Prices|Excluding Tax|
|Apply Customer Tax|After Discount|
|Apply Discount on Prices|Excluding Tax|
|Apply Tax On|Custom Price (if available)|

{style="table-layout:auto"}

#### Tax Classes

|Field|Recommended Setting|
|--- |--- |
|Tax Class for Shipping|Shipping (shipping is taxed)|

{style="table-layout:auto"}

#### Default Tax Destination Calculation

|Field|Recommended Setting|
|--- |--- |
|Default Country|Canada|
|Default State|(as appropriate)|
|Default Postal Code|* (asterisk)|

{style="table-layout:auto"}

#### Shopping Cart Display Settings

|Field|Recommended Setting|
|--- |--- |
|Include Tax in Grand Total|Yes|
|Display Full Tax Summary|Yes|
|Display Zero in Tax Subtotal|Yes|

{style="table-layout:auto"}

#### Fixed Product Taxes

|Field|Recommended Setting|
|--- |--- |
|Enable FPT|Yes|
|All FPT Display Settings|Including FPT and FPT description|
|Apply Discounts to FPT|No|
|Apply Tax to FPT|Yes|
|Include FPT in Subtotal|No|

{style="table-layout:auto"}

### Step 2: Set up Canadian Goods & Services Tax (GST)

To print the GST number on invoices and other sales documents, include it in the name of the applicable tax rates. The GST appears as part of the GST amount on any order summary.

#### Manage Tax Zones & Rates

|Field|Recommended Setting|
|--- |--- |
|Tax Identifier|Canada-GST|
|Country|Canada|
|State|* (asterisk)|
|Zip/Post is Range|No|
|Zip/Post Code|* (asterisk)|
|Rate Percent|5.0000|

{style="table-layout:auto"}

### Step 3: Set up Canadian Provincial Sales Tax (PST)

Set up another tax rate for the applicable province.

#### Tax Rate Information

|Field|Recommended Setting|
|--- |--- |
|Tax Identifier|Canada-SK-PST|
|Country|Canada|
|State|Saskatchewan|
|Zip/Post is Range|No|
|Zip/Post Code|* (asterisk)|
|Rate Percent|5.0000|

{style="table-layout:auto"}

### Step 4: Create a GST tax rule

To avoid compounding the tax and to correctly display the calculated tax as separate line items for GST and PST, you must set different priorities for each rule and select the **Calculate off subtotal only** checkbox. Each tax appears as a separate line item, but the tax amounts are not compounded.

#### Tax Rule Information

|Field|Recommended Setting|
|--- |--- |
|Name|Retail-Canada-GST|
|Customer Tax Class|Retail Customer|
|Product Tax Class|Taxable GoodsShipping|
|Tax Rate|Canada-GST|
|Priority|0|
|Calculate off subtotal only|Select this checkbox.|
|Sort Order|0|

{style="table-layout:auto"}

### Step 5: Create a PST Tax Rule for Saskatchewan

For this tax rule, make sure to set the priority to 0 and select the **Calculate off subtotal only** checkbox. Each tax appears as a separate line item, but the tax amounts are not compounded.

#### Tax Rule Information

|Field|Recommended Setting|
|--- |--- |
|Name|Retail-Canada-PST|
|Customer Tax Class|Retail Customer|
|Product Tax Class|Taxable GoodsShipping|
|Tax Rate|Canada-SK-PT|
|Priority|1|
|Calculate off subtotal only|Select this checkbox.|
|Sort Order|0|

{style="table-layout:auto"}

### Step 6: Save and test the results

1. When complete, click **Save Config**.

1. Return to your storefront and create a sample order to test the results.

## EU tax configuration

The following example depicts a store based in France that sells 100k+ Euros in France and 100k+ Euros in Germany.

- Tax calculations are managed at the website level.
- Currency conversion and tax display options are controlled individually at the store view level (Select the Use Website checkbox to override the default).
- By setting the default tax country, you can dynamically show the correct tax for the jurisdiction.
- Fixed product tax is included for relevant goods as a product attribute.
- It might be necessary to edit the catalog to ensure that it shows up in the correct category/website/store view.

### Step 1: Create three product tax classes

For this example, it is assumed that multiple VAT-Reduced product tax classes are not needed.

1. Create a VAT-Standard product tax class.

1. Create a VAT-Reduced product tax class.

1. Create a VAT-Free product tax class.

### Step 2: Create tax rates for France and Germany

Create the following tax rates:

|Tax rates|Settings|
|--- |--- |
|France-StandardVAT|Country: France <br/>State/Region: * <br/>ZIP/Postal Code: * <br/>Rate: 20%|
|France-ReducedVAT|Country: France <br/>State/Region: * <br/>ZIP/Postal Code: * <br/>Rate: 5%|
|Germany-StandardVAT|Country: Germany <br/>State/Region: * <br/>ZIP/Postal Code: * Rate: 19%|
|Germany-ReducedVAT|Country: Germany <br/>State/Region: * <br/>ZIP/Postal Code: * <br/>Rate: 7%|

{style="table-layout:auto"}

### Step 3: Set up the tax rules

Create the following tax rules:

|Tax rules |Settings|
|--- |--- |
|Retail-France-StandardVAT |Customer Class: Retail Customer <br/>Tax Class: VAT-Standard <br/>Tax Rate: France-StandardVAT <br/>Priority: 0 <br/>Sort Order: 0|
|Retail-France-ReducedVAT|Customer Class: Retail Customer <br/>Tax Class: VAT Reduced <br/>Tax Rate: France-ReducedVAT <br/>Priority: 0 <br/>Sort Order: 0|
|Retail-Germany-StandardVAT|Customer Class: Retail Customer <br/>Tax Class: VAT-Standard <br/>Tax Rate: Germany-StandardVAT <br/>Priority: 0 <br/>Sort Order: 0|
|Retail-Germany-ReducedVAT|Customer Class: Retail Customer <br/>Tax Class: VAT-Reduced <br/>Tax Rate: Germany-ReducedVAT <br/>Priority: 0 <br/>Sort Order: 0|

{style="table-layout:auto"}

### Step 4: Set up a store view for Germany

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **All Stores**.

1. Under the default website, create a store view for **Germany**.
1. Then, do the following:

   - On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

   - In the upper-left corner, set **Default Config** to the French store.

   - On the General page, expand ![Expansion selector](../assets/icon-display-expand.png) the **Countries Options** section, and set the default country to "France."

   - Complete the locale options as needed.

1. In the upper-left corner, choose the German **Store View**.

1. On the _General_ page, expand ![Expansion selector](../assets/icon-display-expand.png) **Countries Options** and set the default country to `Germany`.

1. Complete the locale options as needed.

### Step 5: Configure tax settings for France

Complete the following General tax settings:

|Field|Recommended Setting|
|--- |--- |
|Tax Classes||
|Tax Class for Shipping|Shipping (shipping is taxed)|
|Calculation Settings||
|Tax Calculation Method Based On|Total|
|Tax Calculation Based On|Shipping Address|
|Catalog Prices|Including Tax|
|Shipping Prices|Including Tax|
|Apply Customer Tax|After Discount|
|Apply Discount on Prices|Including Tax|
|Apply Tax On|Custom Price (if available)|
|Default Tax Destination Calculation||
|Default Country|France|
|Default State||
|Default Postal Code|* (asterisk)|
|Shopping Cart Display Settings||
|Include Tax in Grand Total|Yes|
|Fixed Product taxes||
|Enable FPT|Yes|
|All FPT Display Settings|Including FPT and FPT description|
|Apply Discounts to FPT|No|
|Apply Tax to FPT|Yes|
|Include FPT in Subtotal|Yes|

{style="table-layout:auto"}

### Step 6: Configure tax settings for Germany

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the upper-right corner, set **Store View** to the view to the German store. When prompted to confirm, click **OK**.

1. In the left panel, expand **Sales** and choose **Tax**.

1. In the **Default Tax Destination Calculation** section, do the following:

   - Clear the **Use Website** checkbox after each field,

   - Update the following values to match your site's Shipping Settings [point of origin](shipping-settings.md#point-of-origin).

      - Default Country
      - Default State
      - Default Post Code

      This setting ensures that tax is calculated correctly when product prices include tax.

      ![Default Tax Destination Calculation](./assets/destination-calc-french.png)<!-- zoom -->

1. When complete, click **Save Config**.

[1]: https://www.revenuquebec.ca/en/businesses/
[2]: https://www.saskatchewan.ca/finance
[3]: https://www.gov.mb.ca/finance/taxation/bulletins/004.pdf
