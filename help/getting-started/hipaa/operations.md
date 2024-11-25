---
title: Operations
description: Guidelines for migrating to a HIPAA-ready offering and using the secondary staging environment for troubleshooting.
---

# Operations

Guidelines for migrating to a HIPAA-ready offering and using the secondary staging environment for troubleshooting.

## Migration

Customers migrating from a non-HIPAA Commerce offering to a HIPAA-ready offering must adhere to the following guidelines:

1. **Delete Existing Dataspaces**: Before migration, all existing dataspaces must be deleted to prevent the co-mingling of sensitive and non-sensitive data.
2. **Configure New Environment**: The new HIPAA-SaaS environment can only be used after the migration is complete and the old dataspaces are deleted. The [Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas) should be configured only after this step.
3. **Migration Strategy**: If there is a need to carry forward old data/configurations (e.g., for LS, PREX), a migration strategy must be in place. This process is the responsibility of the merchant.

>[!NOTE]
>To delete the existing dataspaces, customers must create a ticket with Adobe Commerce support and provide the necessary environment details.

## Troubleshooting with Adobe Commerce support

All HIPAA ready offering comes with an additional secondary staging environment called "Staging 2" to be used by Commerce support team for troubleshooting purposes.  

Customers must ensure that Staging 2 environment:
- Does not contain any sensitive data, like, but not limited to, Protected Health Information (PHI).
- Must not be used for any production activities.
- Must not be given different name than "Staging 2" to avoid confusion.
- Is kept up to date with both code and configuration from the production environment to ensure troubleshooting is performed in an environment as close to production as possible.
