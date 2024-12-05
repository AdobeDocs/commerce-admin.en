---
title: Operations
description: Guidelines for migrating to a HIPAA-ready offering and using the secondary staging environment for troubleshooting.
---

# Operations

Guidelines for migrating to a HIPAA-ready offering and using the "staging_for_support" environment for troubleshooting.

## Migration

Customers migrating from a non-HIPAA Commerce offering to a HIPAA-ready offering must adhere to the following guidelines:

1. **Delete Existing Dataspaces**: Before migration, all existing dataspaces must be deleted to prevent the co-mingling of sensitive and non-sensitive data in the Adobe Commerce SaaS layer. Raise a support ticket to delete your dataspaces - more details in the note below.
2. **Configure New Environment**: The [Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas) setup in the new HIPAA commerce instance should be configured only after the dataspaces have been deleted in step 1. The new HIPAA-SaaS environment should be used only after the old dataspaces are deleted. The setup of the Commerce Services Connector automatically triggers the creation of new SaaS dataspaces.
3. **Migration Strategy**: The deletion of the SaaS dataspaces is an irreversible process. This will delete all your catalog data and related configurations. A migration strategy needs to be in place if you wish to carry forward any of your old data or configurations. This strategy is the responsibility of the merchant. A support ticket for deleting the existing dataspaces should be created only after migration data backup (if applicable) are done.

>[!NOTE]
>To delete the existing dataspaces, customers must create a ticket with Adobe Commerce support titled "HIPAA Migration: Delete SaaS Dataspaces" and provide their MAGEID along with the SaaS Project IDs that need to be deleted.

## Troubleshooting with Adobe Commerce support

All HIPAA ready offering comes with an additional "staging_for_support" environment to be used by Commerce support team for troubleshooting purposes.  

Customers must ensure that "staging_for_support" environment:
- Does not contain any sensitive data, like, but not limited to, Protected Health Information (PHI).
- Must not be used for any production activities.
- Must not be given different name than ""staging_for_support"" to avoid confusion.
- Is kept up to date with both code and configuration from the production environment to ensure troubleshooting is performed in an environment as close to production as possible.

## Commerce services

- **Non-HIPAA Ready Commerce services**—Customers must not use Adobe Commerce services, such as Live Search, Product Recommendations, Payment Services, Sales Channels, or Commerce Intelligence because they are not HIPAA ready. Customers should only use [HIPAA ready-services](overview.md).

- **Data Connection**—Only the Back-Office Collector within the [Data Connection](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) extension is HIPAA ready. Customers should not send PHI to non-HIPAA ready data connection services, such as storefront events and Audience Activation. Customers must ensure that storefront data collection is disabled.

- **Catalog Service**—By design, [Catalog Service](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/overview) does not process PHI, so it is out of scope for the HIPAA readiness audit and compliance. Customers are responsible for ensuring that they use this service based on their own evaluation of use cases and in consultation with legal counsel. Customers also should not use Catalog Service through the federated service to avoid the risk of passing PHI to non-HIPAA ready services.

- **SaaS Data Export**—The [SaaS Data Export](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) service should be configured to send data only for HIPAA ready components in Adobe Commerce.
