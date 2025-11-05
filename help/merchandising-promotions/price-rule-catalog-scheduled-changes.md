---
title: Scheduled changes for catalog price rules
description: Learn how to apply catalog price rules on schedule as part of a campaign and grouped with other content changes.
exl-id: ec4b915f-0a27-438d-b1b0-f1bcd297af6d
feature: Merchandising, Price Rules, Catalog Management
---
# Scheduled changes for catalog price rules

{{ee-feature}}

The Scheduled Changes box appears at the top of the page when a new price rule is saved or updated. Catalog price rules can be applied on schedule as part of a campaign and grouped with other content changes. You can create a campaign based on scheduled changes to a price rule, or apply the changes to an existing campaign.

![Catalog price rule - scheduled changes](./assets/price-rule-catalog-scheduled.png){width="600" zoomable="yes"}

## How scheduled price rule updates work

- All scheduled updates are applied consecutively. This means that any entity can have only one scheduled update at one point of time.

- Any scheduled update is applied to all store views within its time frame. As a result, an entity cannot have different scheduled updates for different store views at the same time. All entity attribute values within all store views, which are not affected by the current scheduled update, are taken from the default values, and not from the previous scheduled update.

- If there are multiple price rules running in the same campaign, the Priority setting of the price rule determines which rule takes precedence. To learn more, see [Content Staging](../content-design/content-staging.md).

## Ending a price rule sale at a specific time

If an active price rule was created without an end date and you need to end it at a specific time, you cannot simply edit the existing scheduled update to add an end date. Instead, you must create a new scheduled update that changes the rule's status to `Inactive`. Set the start date of this new update to the date and time when you want the sale to end.

## Schedule an update to a catalog price rule

1. On the _Admin_ sidebar, go to **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_ > **Catalog Price Rule**.

1. Open the rule in edit mode.

1. In the **[!UICONTROL Scheduled Changes]** box at the top of the page, click **[!UICONTROL Schedule New Update]**.

1. With the **[!UICONTROL Save as a New Update]** option selected, do the following:

    - For **[!UICONTROL Update Name]**, enter a name for the update to the rule.

    - Enter a brief **[!UICONTROL Description]** of the update, including how or why it is applied.

    - Use the _Calendar_ (![Calendar icon](../assets/icon-calendar.png)) to choose the **[!DNL Start Date]** and **[!UICONTROL End Date]** for the scheduled change to be in effect. To create an open-ended change, leave the end date blank.

    ![Catalog price rules - new scheduled changes](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >The start and end date/time is determined by the default Admin panel date/time and time zone, not by the time zone of a particular website. Consider the time zone of the website to properly determine start and end times. Create separate rules for websites in different time zones that need to start and/or stop at specific local times.

1. Scroll down to the **[!UICONTROL Rule Information]** section and change the rule as needed.

   You can schedule changes for any rule parameter, including the websites (scope)/customer groups for the rule, conditions of the rule, and actions applied by the rule. For more information, see [Creating a Catalog Price Rule](price-rules-catalog-create.md).

   >[!NOTE]
   >
   >Whenever you update any rule information parameters, ensure that the _[!UICONTROL Status]_ is set correctly.  If you want the change to result in an actively applied rule, set the status to `Active`.

1. When complete, click **[!UICONTROL Save]**.

    The scheduled change appears at the top of the page, with the start and end dates of the campaign.

## Edit a scheduled rule change

>[!NOTE]
>
>If a campaign is linked to more than one catalog price rule, the campaign can be edited only from the [Content Staging Dashboard](../content-design/content-staging-dashboard.md).

1. In the **[!UICONTROL Scheduled Changes]** box at the top of the page, click **[!UICONTROL View/Edit]**.

1. Make any changes necessary to the scheduled update.

1. Click **[!UICONTROL Save]**.

## Preview the scheduled rule change

1. In the **[!UICONTROL Scheduled Changes]** box at the top of the page, click **[!UICONTROL Preview]**.

    The Preview opens a new browser tab that loads your storefront with the applied scheduled change. Navigate to a product that is affected by the change.

    ![Preview Scheduled Change](./assets/price-rule-catalog-scheduled-update-preview.png){width="600" zoomable="yes"}

1. In the upper-left corner of the Preview window, click **[!UICONTROL Calendar]**.

    The calendar detail shows other campaigns that are scheduled for the same day. Each record in the list is a separate rule update.

    ![List of Scheduled Updates for a Specific Date](./assets/price-rule-catalog-scheduled-preview-calendar.png){width="600" zoomable="yes"}

1. To preview a different day or time, click the **[!UICONTROL Date & Time]** calendar ![Calendar icon](../assets/icon-calendar.png) and do the following:

    - Choose a different date and/or time.

    - Click **[!UICONTROL Preview]**.

1. To return to the calendar, click **[!UICONTROL Calendar]** in the header of the Preview page.

   From here, you can do the following:

   **Share a Link to the Preview**

   To share a link to the store preview with other Admin users, click **[!UICONTROL Share]**. Copy the link to the clipboard and paste it into the body of an email message.

   >[!NOTE]
   >
   >If your [role has access](../systems/permissions-user-roles.md) to manage Admin user accounts, you can create or update an existing user account with Admin permissions so that you can share the preview link.

   **Change the Scope of the Preview**

   To see scheduled changes for different store views, click **[!UICONTROL Scope]** in the header of the Preview page. Choose the website, store, or store view that you want to preview.

1. If necessary, return to the calendar and click **[!UICONTROL View/Edit]** in the _[!UICONTROL Action]_ column to open another scheduled update.
