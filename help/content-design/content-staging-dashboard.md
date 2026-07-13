---
title: Content staging dashboard
description: Use the content staging dashboard to access an overview of all active and upcoming campaigns.
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/Hwrb3dYdJlggWN-Z-nUKxVBhsejFMZR-yWIgRzfJifQ
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Content staging dashboard

{{ee-feature}}

The [!UICONTROL Content Staging] Dashboard provides an overview of all active and upcoming campaigns. The format of the dashboard can be changed from a grid to a timeline. You can also use filters to find campaigns, customize the column layout, and save different views of the grid. For more information about the workspace controls, see [Admin workspace](../getting-started/admin-workspace.md).

![Staging dashboard in grid view](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## View the staging dashboard

1. On the _Admin_ sidebar, go to  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_ > **[!UICONTROL Dashboard]**.

1. To change the format of the dashboard, set the **[!UICONTROL View As]** control to `list`, `Grid`, or `Timeline`.

   ![Timeline view](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   When the timeline is displayed, the slider in the lower-right corner can be used to adjust the view from one to four weeks. Each column represents one day.

1. If the timeline is displayed, drag the slider to the `4w` position on the far right to view a longer span of time.

   ![Four-week view](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. To display general information about the campaign, click any item on the page.

   - To open the campaign, click **[!UICONTROL View/Edit]**.

   - To see how the campaign looks to customers in the store on that day, click **[!UICONTROL Preview]**.

   ![Campaign information](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## Staging dashboard column descriptions

|Column|Description|
|--- |--- |
|[!UICONTROL Status]|Campaign's status. `Active` or `Upcoming`.|
|[!UICONTROL Update Name]|The name of the campaign.|
|[!UICONTROL Includes]|Defines how many objects are included in the campaign.|
|[!UICONTROL Start Time]|The date when the campaign starts.|
|[!UICONTROL End Time]|The date when the campaign ends.|
|[!UICONTROL Description]|Additional description of each campaign.|
|[!UICONTROL Action]|The actions that can be applied to an individual record include:<br/>**[!UICONTROL View/Edit]** - Opens the campaign in edit mode.<br/>**[!UICONTROL Preview]** - Displays the campaign in preview mode.|

{style="table-layout:auto"}

## Edit a Campaign

Existing campaign objects can be edited from the staging dashboard, except for price rule campaigns that do not have end dates.

>[!NOTE]
>
>If an active campaign is initially created without an end date, the campaign cannot be edited later to include an end date. In such a case, it is necessary to create a duplicate campaign and enter the end date that is needed.

![Campaign detail](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

The campaign in this example includes two categories and three individual products.

Follow the steps below to edit any of the objects in this campaign.

1. On the _Admin_ sidebar, go to  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_ > **[!UICONTROL Dashboard]**.

1. Find the campaign in the displayed list or timeline and open it to access the details:

   - For a list display, click **[!UICONTROL Select]** and then **[!UICONTROL View/Edit]** in the _[!UICONTROL Action]_ column.
   - For a timeline display, click once to display the summary and then click **[!UICONTROL View/Edit]**.

1. Update any of the settings in the _[!UICONTROL General]_ section as needed.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) any section that contains an item to be edited.

   ![Updating the assigned products for a campaign item](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. Click **[!UICONTROL Save]**.
