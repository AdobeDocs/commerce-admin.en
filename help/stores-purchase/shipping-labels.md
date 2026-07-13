---
title: Shipping labels
description: Learn about shipping label workflow for regular shipments and products with return merchandise authorization.
exl-id: 5da03cf9-5e92-4bb8-ba53-67c6469665ed
feature: Shipping/Delivery, Orders
TQID: https://experienceleague.adobe.com/Cjf9-372TRGIfWXpWR20OUII5XorPdfO1qgG-b2yPYI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Shipping labels

Commerce includes a high level of integration with major shipping carriers, which gives you access to carrier shipping systems to track orders, create shipping labels, and more. Shipping labels can be created for regular shipments and products with return merchandise authorization. In addition to the information provided by the shipping carrier, the label also includes the Commerce order number, number of the package, and the total quantity of packages for the shipment.

![USPS Priority Shipping Label](./assets/shipping-usps-priority-label.png){width="300"}

- [Configure shipping labels](shipping-label-configure.md)
- [Create shipping labels and packages](shipping-label-create.md)

## Shipping label workflow

Shipping labels can be produced at the time a shipment is created, or later. Shipping labels are stored in PDF format and are downloaded to your computer.

### Step 1: Merchant submits shipping label request

The merchant/store manager completes the information necessary to generate labels, and submits the request.

### Step 2: Request sent to carrier

Commerce contacts the shipping carrier, and creates an order in the carrier's system. A separate order is created for each package that is shipped.

### Step 3: Carrier sends label and tracking number

The carrier sends the shipping label and tracking number for the shipment.

- A single shipment with multiple packages receives multiple shipping labels.

- If you generate the same shipping labels multiple times, the original tracking numbers are preserved.

- For returned products with RMA numbers, the old tracking numbers are replaced with new ones.

### Step 4: Merchant downloads and prints the label

After the shipping label is generated, the new shipment is saved and the label can be printed. If the shipping label cannot be created due to problems with the connection or any other reason, the shipment is not created. Depending on your browser settings, the PDF file can be opened and printed. Each label appears on a separate page in the PDF.
