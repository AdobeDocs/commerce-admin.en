---
title: Operations
description: Lorem ipsum dolor sit amet
---

# Operations

Lorem ipsum dolor sit amet

## Migration

Customer migrating from a non-HIPAA Commerce offering to a HIPAA ready offering must delete their old dataspaces to prevent co-mingling of sensitive and non-sensitive data.

1. Merchant need to delete their old data spaces and only after that should the new HIPAA-SaaS environment be used([commerce services connector](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas) should be configured only after that)
1. If the merchant has a requirement to carry forward their old data/configurations(for example for LS, PREX), there needs to be a migration strategy in place. This process is owned by the merchant.

## Staging

All HIPAA ready offering comes with an additional secondary staging environment to be used by Commerce support team for troubleshooting purposes.  

Customers should not put any Protected Health Information (PHI) in the second staging environment. This secondary staging environment is only used by  Adobe Commerce customer support for troubleshooting purposes.

## Commerce services

- **Non-HIPAA Ready Commerce services**—Customers must not use Adobe Commerce services, such as Live Search, Product Recommendations, Payment Services, Sales Channels, or Commerce Intelligence because they are not HIPAA ready. Customers should only use [HIPAA ready-services](overview.md).

- **Data Connection**—Only the Back-Office Collector within the [Data Connection](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) extension is HIPAA ready. Customers should not send PHI to non-HIPAA ready data connection services, such as storefront events and Audience Activation. Customers must ensure that storefront data collection is disabled.

- **Catalog Service**—By design, [Catalog Service](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/overview) does not process PHI, so it is out of scope for the HIPAA readiness audit and compliance. Customers are responsible for ensuring that they use this service based on their own evaluation of use cases and in consultation with legal counsel. Customers also should not use Catalog Service through the federated service to avoid the risk of passing PHI to non-HIPAA ready services.

- **SaaS Data Export**—The [SaaS Data Export](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) service should be configured to send data only for HIPAA ready components in Adobe Commerce.
