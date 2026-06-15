---
title: Use AEM Assets
description: Manage your store media assets with AEM Assets.
feature: CMS, Media
exl-id: 55144019-8ba2-4392-b5dd-216e2ee9daf2
TQID: https://experienceleague.adobe.com/c9tgs7PAobBnFZUKX0Zkpik9-kt5O5RXSTYQ61l2sBc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
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
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Use AEM Assets

<!--In ACAP-844, this topic was linked to from the Commerce Admin products images and videos when the Assets integration is enabled. If the URL to the topic changes, be sure to add a redirect.-->

## Update an asset

After you edit an asset in AEM Assets, send the updates to Commerce by approving and reprocessing the asset. Only approved assets are sent to your Commerce instance. Reprocessing the asset ensures that any final changes or metadata updates are captured before the asset is sent to Adobe Commerce.

For details, see the following AEM Assets documentation.

- [Reprocessing digital assets](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/reprocessing)

- [Approve an asset](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/approve-assets)

## Add assets to categories content

You can add assets into your catalog categories content once you have enabled and configured the AEM Assets integration:

1. On the _Admin_ sidebar, navigate to **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Expand the ![Expansion selector](../assets/icon-display-expand.png) in the **[!UICONTROL Content]** section.

   ![Category content](./assets/aem-assets-manage-categories.png){width="600" zoomable="yes"}

1. To display a **[!UICONTROL Category Image]** at the top of the page, click **[!UICONTROL Select from Assets]** to use an image from your AEM Assets folder.

1. Click **[!UICONTROL Save]** and continue.

   For more information to create a category, see [Complete the category content](../catalog/category-create.md#step-3-complete-the-category-content).
