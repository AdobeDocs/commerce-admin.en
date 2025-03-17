---
title: Operations
description: Guidelines for migrating to a HIPAA-ready offering and using the secondary staging environment for troubleshooting.
exl-id: 058b43de-1cee-4557-b2e3-87ee7422bf9b
---
# Operations

Use these guidelines to learn about migrating to the HIPAA-ready offering for Adobe Commerce and using the `staging_for_support` environment for troubleshooting.

## Migration

Customers migrating from a non-HIPAA Commerce offering to a HIPAA-ready offering must adhere to the following guidelines:

1. **Delete existing dataspaces**: Before migration, all existing dataspaces must be deleted to prevent the co-mingling of sensitive and non-sensitive data in the Adobe Commerce SaaS layer. Create a support ticket to delete your dataspaces.
1. **Configure new environment**: The [Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas) setup in the new HIPAA Commerce instance should be configured only after the dataspaces have been deleted. The new HIPAA SaaS environment should only be used after the old dataspaces are deleted. The setup of the Commerce Services Connector automatically triggers the creation of new SaaS dataspaces.
1. **Migration strategy**: The deletion of the SaaS dataspaces is an irreversible process and deletes all of your catalog data and related configurations. A migration strategy must be in place if you want to carry forward any of your old data or configurations. This strategy is the responsibility of the merchant. A support ticket for deleting the existing dataspaces should be created only after migration data backup (if applicable) is done.

>[!NOTE]
>To delete existing dataspaces, customers must create an Adobe Commerce Support ticket titled "HIPAA Migration: Delete SaaS dataspaces", provide their `MAGEID`, and provide the SaaS Project IDs that need to be deleted.

## Troubleshooting with Adobe Commerce Support

The Adobe Commerce HIPAA-ready offering comes with an additional `staging_for_support` environment to be used by the Adobe Commerce Support team for troubleshooting purposes.  

Customers must ensure that `staging_for_support` environment:

- Does not contain any sensitive data, like, but not limited to, Protected Health Information (PHI).
- Must not be used for any production activities.
- Must not be given different name than `staging_for_support` to avoid confusion.
- Is kept up to date with both code and configuration from the production environment to ensure troubleshooting is performed in an environment as close to production as possible.

## Commerce services

- **Non-HIPAA Ready Commerce services**—Customers must not use Adobe Commerce services, such as Live Search, Product Recommendations, Payment Services, Sales Channels, or Commerce Intelligence because they are not HIPAA ready. Customers should only use [HIPAA-ready services](overview.md).

- **Data Connection**—Only the Back-Office Collector within the [Data Connection](https://experienceleague.adobe.com/en/docs/commerce/data-connection/overview) extension is HIPAA ready. Customers should not send PHI to non-HIPAA ready data connection services, such as storefront events and Audience Activation. Customers must ensure that storefront data collection is disabled.

- **Catalog Service**—By design, [Catalog Service](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/overview) does not process PHI, so it is out of scope for the HIPAA readiness audit and compliance. Customers are responsible for ensuring that they use this service based on their own evaluation of use cases and in consultation with legal counsel. Customers should also not use Catalog Service through the federated service to avoid the risk of passing PHI to non-HIPAA ready services.

- **SaaS Data Export**—The [SaaS Data Export](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview) service should be configured to send data only for HIPAA ready components in Adobe Commerce.
