---
title: Shipping carrier setup
description: Learn about the support for commercial shipping accounts that is available for your store.
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
---
# Shipping carrier setup

If you have a commercial account with a supported carrier, you can offer your customers the convenience of choosing that carrier during checkout. The rates are automatically downloaded, so you do not need to look up the information.

>[!NOTE]
>
>See [Commerce Marketplace](../getting-started/commerce-marketplace.md) for additional shipping services for your Commerce installation.

Before you can offer your customers a selection of shipping carriers, you must complete the following steps:

- Configure the [shipping settings](shipping-settings.md) to establish the point of origin for your store.

- Configure the settings for each carrier service that you want to offer.

    - [**UPS**](ups.md)  - United Parcel Service (UPS) offers domestic and international shipping services by land and air to more than 220 countries.
    - [**USPS**](usps.md) - The United States Postal Service (USPS) is the independent postal service of United States government. USPS offers domestic and international shipping services by land and air.
    - [**FedEx**](fedex.md) - FedEx offers domestic and international shipping services by land and air to more than 220 countries.
    - [**DHL**](dhl.md) - DHL offers integrated international services and tailored, customer-focused solutions for managing and transporting letters, goods, and information.

## Dimensional weight

Dimensional weight, sometimes called volumetric weight, is a common industry practice that bases the transportation price on a combination of weight and package volume. In simple terms, dimensional weight determines the shipping rate based on the amount of space a package occupies in the cargo area of the carrier. Dimensional weight is typically used when a package is relatively light compared to its volume.

All major carriers apply dimensional weight to some shipments. However, the manner in which dimensional weight pricing is applied varies from one carrier to another. If your company has a high volume of shipments, even a slight difference in shipping price can translate to thousands of dollars over the course of a year.

## Configuration

The configuration options vary for each carrier. However, all require the following steps:

1. Open a shipping account with the carrier.

1. Enter your account number or user ID, and the gateway URL to their system into the configuration of your store.

### USPS Web Tools API deprecation

Adobe Commerce versions 2.4.6, 2.4.7, and 2.4.8 use the Legacy Web Tools APIs for out-of-the-box shipping integration with USPS. USPS has introduced USPS APIs, a REST-based platform to replace the Legacy Web Tools APIs.

On January 25, 2026, USPS is retiring the Legacy Web Tools APIs. After this date, all requests to the Web Tools APIs will fail.

To avoid disruption of USPS shipping services, take the following actions before January 25, 2026:

- Apply the [USPS REST API Migration quality patch](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/usps-rest-api-migration-patch.html)(AC-1520) to add support for integrating with the USPS REST APIs.

- Update the Commerce USPS configuration to use the REST APIs:

  - [USPS Shipping Carrier configuration](usps.md)

  - [Shipping label configuration](shipping-label-create.md)

