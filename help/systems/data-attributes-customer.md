---
title: Customer data attributes reference
description: Use this reference of customer data attributes when you work with customer data imports and exports.
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
TQID: https://experienceleague.adobe.com/-s4plXYkrsdNTL-xxMj41AAxtJJ5q1PKiBUcdnaWhlg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
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
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
---
# Customer data attributes reference

The following tables list the attributes from a typical export of the customers main file and customer addresses. The installation that was used to export this data has two websites and several store views, with the sample data installed.

Each attribute, or field, is represented in the CSV file as a column, and customer records are represented by rows. Columns that begin with an underscore are service entities that contain properties or complex data.

## Customers main file

|Attribute|Description|
|--- |--- |
|`email`|The customer's email address.|
|`_website`||
|`_store`||
|`confirmation`|Confirmation flag.|
|`created_at`|The date the customer account was created.|
|`created_in`|The store view where the account was created.|
|`disable_auto_group_change`|Determines if customer groups can be dynamically assigned during VAT ID validation.|
|`dob`|The customer's date of birth. <br><br>**_Important:_** In keeping with current security and privacy best practices, review the storage and processing of customers' full date of birth (month, day, year). When collected with other personal identifiers (such as _full name_), it is a potential legal and security risk. We recommend limiting the storage of customers' full birth dates and instead suggest using customer year of birth as an alternative.|
|`firstname`|The first name of the customer.|
|`gender`|The customer gender.|
|`group_id`|The ID of the customer group where the customer is assigned.|
|`lastname`|The last name of the customer.|
|`middlename`|The middle name or middle initial of the customer.|
|`password_hash`|Password hash|
|`prefix`|Any prefix that is used with the customer name (such as `Mr.`, `Ms.`, `Mrs.`, and `Dr.`).|
|`rp_token`|Reset password token.|
|`rp_token_created_at`|Date when the password was reset.|
|`store_id`|Store ID|
|`suffix`|Any suffix that is used with the customer name (such as `Jr.`, `Sr.`, and `Esquire`).|
|`taxvat`||
|`website_id`|The website ID of the site where the customer account was created.|
|`password`|The customer password.|

{style="table-layout:auto"}

## Customer addresses

|Attribute|Description|
|--- |--- |
|`_website`||
|`_email`||
|`_entity_id`||
|`city`|The city where the customer address is located.|
|`company`|The company name, if applicable for this address.|
|`country_id`|The country id where the customer address is located.|
|`fax`|The fax number of the customer, if applicable.|
|`firstname`|The customer's first name.|
|`lastname`|The customer's last name.|
|`middlename`|The middle name or middle initial of the customer.|
|`postcode`|The ZIP or postal code where the customer address is located.|
|`prefix`|Any prefix that is used with the customer name (such as `Mr.`, `Ms.`, `Mrs.`, and `Dr.`).|
|`region`|The region where the customer address is located.|
|`region_id`|Region ID|
|`street`|The street address of the customer. A second line of the street address is available if specified in the configuration.|
|`suffix`|If used, the suffix that is associated with the customer's name (such as `Jr.`, `Sr.`, or `III`). |
|`telephone`|The customer's telephone number that is associated with address.|
|`vat_id`|VAT ID is an internal identifier for the VAT Number of the customer when used in VAT Validation.|
|`vat_is_valid`||
|`vat_request_date`||
|`vat_request_id`||
|`vat_request_success`||
|`_address_default_billing_`|Identifies the default billing address. A value of `1` indicates that the address is the default billing address of the customer. Values: 1 / 0|
|`_address_default_shipping_`|Identifies the default shipping address. A value of `1` indicates that the address is the default shipping address of the customer. Values: `1` / `0`|

{style="table-layout:auto"}
