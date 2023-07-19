---
title: Customer address templates
description: Learn how you can customize the customer address templates.
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
---
# Customer address templates

{{ee-feature}}

You can modify the template that controls the format of customer billing and shipping addresses that appear on printed invoices, shipments, and refunds, as well as in the addresses book of the customer account. If you want to include additional information, you can create [custom attributes](attribute-properties.md) that are associated with the customer account and [address](address-attributes.md), and incorporate them into the template.

## Example 1: short format

For [!UICONTROL Text One Line] address template:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## Example 2: long format

For [!UICONTROL Text], [!UICONTROL HTML], and [!UICONTROL PDF] address templates:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![Customer address templates](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## Change the order of address fields

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left side panel, expand **[!UICONTROL Customers]** and select **[!UICONTROL Customer Configuration]**.

1. Click to expand the **[!UICONTROL Address Templates]** section.

   The section includes a separate set of formatting instructions for each of the following:

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. Edit each template as needed, using the examples for reference.

1. When complete, click **[!UICONTROL Save Config]**.
