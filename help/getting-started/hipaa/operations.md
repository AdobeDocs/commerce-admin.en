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
