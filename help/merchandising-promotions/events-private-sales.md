---
title: Private sales and events
description: Learn about using private sales and other catalog events to increase sales to your existing customer base and to generate buzz and new leads.
exl-id: 0b890463-b1e5-4327-8d8a-372afd53312a
feature: Reporting, Promotions/Events
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/8MvnlOp5muOQbx3b7dSKguc4wf-k47v9AtaHXu7b9pU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
subfeature_v2:
  - id: bd0aa680-a881-4f35-9dcf-843b0574bc5f
    internal-label: Private sales reports
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
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Private sales and events

{{ee-feature}}

Private sales and other catalog events are a great way to use your existing customer base to generate buzz and new leads, or to offload surplus inventory. You can create limited-time sales, limit sales to specific members, or create a stand-alone private sale page. You can also define invitations and event details. Increase brand loyalty and generate a buzz by giving your best customers the VIP treatment. Offer exclusive access to member only sales or private sales to increase brand loyalty. You can also use these sales to liquidate excess merchandise. Customer groups are useful in setting up these types of members only and VIP sales.

![Example storefront - event on home page](./assets/storefront-event-home-page.png){width="700" zoomable="yes"}

## Event management components

- **Categories** - Each event is associated with a [category](../catalog/category-create.md) from your catalog.

- **Events** - Event sales are based on a starting and ending date. You can use a [countdown ticker](#event-ticker) to show the time remaining.

- **Catalog event carousel** - When the [Catalog Event widget](../content-design/widget-event-carousel.md) is enabled in the configuration, it can be placed on store pages as a listing of open and upcoming events, sorted by end date. If two or more events have the same end date, the events are sorted based on the order specified in the configuration.

- **[!UICONTROL Websites]** - Category permissions are based primarily on [customer groups](../customers/customer-groups.md).

- **Category permissions** - [Category permissions](../catalog/category-permissions.md) gives you full control over the specific activities that can take place in a given category.

- **Access restrictions** - Prevents public [access](event-configure.md#restrict-access) to the site by redirecting to a landing page, login page, or registration page.

- **Invitations** - Email messages are sent with a link to create an account in the store. You can restrict the ability to create an account to only those who receive an [invitation](invitations.md).

- **Private sales reports** - The [Private Sales Reports](../getting-started/private-sales-reports.md) provide information about invitations sent, customers invited, and conversions.

## Event ticker

The ticker block displays a countdown ticker for open events, with the start and end date for upcoming events. If an event has closed, the ticker shows the starting and ending dates.

![Example storefront - event carousel](./assets/storefront-event-ticker-carousel.png){width="700" zoomable="yes"}

If the category page ticker is enabled for an event, the ticker block appears at the top of the category listing. If the product page ticker is enabled, the ticker block also appears at the top of the product page of any product that is associated with the category.

The event ticker can be enabled when you [creating events](event-create.md).

![Example storefront - event sidebar](./assets/storefront-event-sidebar.png){width="700" zoomable="yes"}
