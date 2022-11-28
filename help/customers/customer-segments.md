---
ee_only: true
title: Customer Segments
group: customers
---

# Customer Segments

Customer segments allow you to dynamically display content and promotions to specific customers, based on properties such as customer address, order history, shopping cart contents, and so on. You can optimize marketing initiatives based on targeted segments with shopping cart price rules. You can also generate reports and export the list of targeted customers. Because customer segment information is constantly refreshed, customers can become associated and disassociated from a segment as they shop in your store.

To better understand the difference between [customer groups]({% link customers/customer-groups.md %}) and customer segments, note where they are used:

||Customer segment|Customer group|
|--- |--- |--- |
|Catalog price rule||✔️|
|Cart price rule|✔️|✔️|
|Tier price||✔️|
|Related product rule|✔️||
|Dynamic block|✔️||
|Reward exchange rates||✔️|
|Category permissions||✔️|
|Invitations||✔️|

## eBooks

- **Customer Segmentation** — Learn how to increase profits and overall customer satisfaction. Get the [eBook][1]{:target="_blank"} now!
- **Segmentation Tactics** — Improve the targeting of your messages and promotions to create meaningful conversations with your customers. Get the [eBook][2]{:target="_blank"} now!

[1]: https://magento.com/resources/identifying-your-most-profitable-customers-introduction-customer-segmentation
[2]: https://magento.com/resources/3-segmentation-tactics-ignite-conversion

## Customer Segment Attributes

Customer segments are defined in a manner similar to shopping cart and catalog price rules. For an attribute to be used in a customer segment condition, the [Use in Customer Segment]({% link stores/attributes-customer.md %}) property must be set to `Yes`. Customer segment conditions can incorporate the following types of attributes:

| Attribute | Description |
|---|---|
| Customer Address Fields | You can define any of the address fields, such as city or country. Any address in a customer's address book can match these conditions for the customer to match. Or, you can specify that only the default billing or shipping addresses can be used to match a customer. Customer address attributes are available only for customers who are logged in to their accounts. |
| Customer Information Fields | Miscellaneous customer information can be defined, including Customer Group, name, email, newsletter subscription status, and Store Credit balance. Customer information is available only for customers who are logged in to their accounts. |
| Cart Fields | Cart properties can be based on either quantity (line items or total quantity) or the value (grand total, tax, gift card, etc.) of the cart contents. |
| Products | You can reference products that are currently in the shopping cart or wish list, or that have previously been viewed or ordered. You can also set a date range for when this occurred. The products are defined using product attributes. |
| Order Fields | Order characteristics for past orders can be defined based on the billing/shipping address in the order, the total or average amount or quantity of the orders, or the total number of orders. You can also set a date range for when this occurred, and the order status of the orders that match these conditions. Available only for customers who are logged in. Conditions that are set for shoppers who are not logged in stop working when they log in. |