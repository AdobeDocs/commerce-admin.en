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

## Troubleshooting with Adobe Commerce support

All HIPAA ready offering comes with an additional secondary staging environment called "Staging 2" to be used by Commerce support team for troubleshooting purposes.  

Customers must ensure that Staging 2 environment:
 - Does not contain any sensitive data, like, but not limited to, Protected Health Information (PHI).
 - Must not be used for any production activities.
 - Must not be given different name than "Staging 2" to avoid confusion.
 - Is kept up to date with both code and configuration from the production environment to ensure troubleshooting is performed in an environment as close to production as possible.
