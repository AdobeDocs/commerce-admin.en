---
title: Operations
description: Guidelines for migrating to a HIPAA-ready offering and using the secondary staging environment for troubleshooting.
exl-id: 058b43de-1cee-4557-b2e3-87ee7422bf9b
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/w3CGUMXmuXy8006HmWG0K-q3ntjbHFAaC61O6t7S4Ao
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
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
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
---
# Operations

{{ee-feature}}

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
