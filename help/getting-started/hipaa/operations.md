---
title: Operations
description: Lorem ipsum dolor sit amet
---
### Commerce Services
**Non-HIPAA Ready Commerce Services**
Customer must not use any of the Adobe Commerce SaaS services such as Live Search, product recommendation, payments, sales channel, MBI etc as they are not HIPAA ready. Customer should only use HIPAA ready-services outlined in https://experienceleague.adobe.com/en/docs/commerce-admin/start/compliance/hipaa-ready-service

**Data Connection**
Only Back-office Collector within the Data connection extension is HIPAA ready. Customer should not send PHI to non-HIPAA ready data connection services such as Storefront events and Audience activation. Please ensure that storefront data collection is disabled.

**Catalog Service**
[Catalog service](https://business.adobe.com/products/magento/catalog-service.html), by design does not process PHI, hence is out of scope for HIPAA readiness audit & compliance. Customer is responsible to ensure that they use this service based on their own evaluation of use-cases and in consultation with legal counsel.  Customers also should not use Catalog Service via federated service to avoid the risk of passing PHI to non-HIPAA services

**SaaS Data Export**
[SaaS Data Export](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) should be configured to send data only for HIPAA ready components in Adobe Commerce
# Operations

Lorem ipsum dolor sit amet

## Migration

Customer migrating from a non-HIPAA Commerce offering to a HIPAA ready offering must delete their old dataspaces to prevent co-mingling of sensitive and non-sensitive data.

1. Merchant need to delete their old data spaces and only after that should the new HIPAA-SaaS environment be used([commerce services connector](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas) should be configured only after that)
1. If the merchant has a requirement to carry forward their old data/configurations(for example for LS, PREX), there needs to be a migration strategy in place. This process is owned by the merchant.

## Staging

All HIPAA ready offering comes with an additional secondary staging environment to be used by Commerce support team for troubleshooting purposes.  

Customers should not put any Protected Health Information (PHI) in the second staging environment. This secondary staging environment is only used by  Adobe Commerce customer support for troubleshooting purposes.
