---
title: Schedule a Content Update
description: Review this campaign example used to schedule a temporary price change for a product.
exl-id: 36b7d7f6-4590-4192-a82b-e5f645b05f62
---
# Schedule a Content Update

{{ee-feature}}

The following example shows how to schedule a temporary price change for a product. It includes scheduling and previewing changes, and viewing scheduled updates on the calendar. Although this example includes only a single change, a campaign might include multiple changes to products, price rules, CMS pages, and other entities that are scheduled to take place at the same time.

>[!NOTE]
>
>All scheduled updates are applied consecutively, which means that any entity can have only one scheduled update at one point of time. Any scheduled update is applied to all store views within its time frame. As a result, an entity cannot have different scheduled updates for different store views at the same time. All entity attribute values within all store views, which are not affected by the current scheduled update, are taken from the default values, and not from the previous scheduled update.

## Schedule an update to a product

1. From the _[!UICONTROL Products]_ grid, open a product in edit mode.

1. In the _[!UICONTROL Scheduled Changes]_ box at the top of the page, click **[!UICONTROL Schedule New Update]**.

   ![Schedule new update](./assets/content-staging-product-schedule-new-update.png)<!-- zoom -->

1. With the **[!UICONTROL Save as a New Update]** option selected, Set the basic parameters for the update:

   - For **[!UICONTROL Update Name]**, enter a name for the new content staging campaign.

   - Enter a brief **[!UICONTROL Description]** of the update and how it is to be used.

   - Use the Calendar (![Calendar icon](../assets/icon-calendar.png)) tool to choose the **Start Date** and **End Date** for the campaign.

      To create an open-ended campaign, do not specify an end date (leave blank). For this example, the campaign is scheduled to begin at the stroke of midnight for the new year, January 1, 2021 at 12:00 AM PST.

      
      For a price rule campaign that was created without an end date, an end date cannot later be added. In such a case, it is necessary to create a campaign and set the start date to the date you want the old campaign to end and the new one to start. On the start date, the old campaign ends and the new campaign begins as defined.

      ![Scheduling a product update](./assets/content-staging-campaign-schedule-update.png)<!-- zoom -->

      >[!NOTE]
      >
      >Campaign Start Date and End Date must be defined by using the **_default_** Admin time zone, which is converted from the local time zone of each website. For example, if you have multiple websites in different time zones, but you want to start campaign based on a US time zone, you must schedule separate update for each local time zone, and set **[!UICONTROL Start Date]** and **[!UICONTROL End Date]** in converted from each local website time zone to default Admin time zone.

1. Scroll down to _[!UICONTROL Price]_ and click **[!UICONTROL Advanced Pricing]**.

1. Enter a **[!UICONTROL Special Price]** for the product during the scheduled campaign and click **[!UICONTROL Done]**.

1. When complete, click **[!UICONTROL Save]**.

   The scheduled change appears at the top of the product page, with the start and end dates of the campaign.

   ![Scheduled change](./assets/content-staging-scheduled-changes.png)<!-- zoom -->

## Edit the scheduled change

1. In the _Scheduled Changes_ box at the top of the page, click **[!UICONTROL View/Edit]**.

1. Make any changes necessary to the scheduled update.

1. Click **[!UICONTROL Save]**.

## Preview the scheduled change

In the _Scheduled Changes_ box at the top of the page, click **[!UICONTROL Preview]**.

The preview opens a new browser tab, and shows how the product will appear during the scheduled campaign.

![Preview scheduled changes](./assets/content-staging-product-scheduled-update-preview-rope.png)<!-- zoom -->

For more information about using the preview content tools to change the date and scope of the preview, see [Previewing a Campaign](content-staging-preview.md). You can also share a link to the store preview with your colleagues.
