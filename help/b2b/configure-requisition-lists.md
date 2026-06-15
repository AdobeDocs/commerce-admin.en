---
title: Configure requisition list maximum
description: Learn about requisition list configuration, which controls the maximum number that can be maintained for each customer account.
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
TQID: https://experienceleague.adobe.com/we9sPvRg20kEV4EpfemuA7WW-rjv7G6evjr5MwzRGyM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
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
# Configure requisition list maximum

When the requisition list feature is enabled, customers can create multiple lists of frequently purchased items and use those lists for order placement. It is available for both logged-in users and guests. You can enable requisition lists when you [configure the B2B features](enable-basic-features.md).

A customer can have multiple lists that focus on products from different vendors, buyers, teams, campaigns, or anything else that streamlines common workflows. [Requisition list functionality](requisition-lists.md) is similar to wish lists, with the following differences:

- A requisition list is not cleared after sending items to the shopping cart. It can be used multiple times.
- The user interface for requisition lists uses a compact view in order to display many items.

By default, customers can maintain up to 999 requisition lists for their account. But you can modify the configuration and specify a lower number to lessen the load on your store.

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left panel, expand **[!UICONTROL Customers]** and choose **[!UICONTROL Requisition Lists]**.

   ![Requisition lists - general setting](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. For **[!UICONTROL Number of Requisition Lists]**, enter the maximum number of requisition lists that can be maintained for each customer account.

   The minimum number is `2`, and the maximum is `999`.

1. When complete, click **[!UICONTROL Save Config]**.
