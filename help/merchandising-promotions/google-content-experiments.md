---
title: "[!DNL Google Content Experiments]"
description: Learn how to use [!DNL Google Content Experiments] to set up an A/B test of Commerce products, categories, or content pages.
---
# [!DNL Google Content Experiments]

The following example shows how to set up an A/B test of products, categories, or content pages using Google Analytics Content Experiments. We recommend that you keep two browser tabs open while working through the instructions, because you need to bounce back and forth between the Commerce Admin and your [!DNL Google Analytics] account.

>[!NOTE]
>
>[!DNL Google Content Experiments] has been deprecated and is scheduled for replacement by [Google Optimize](https://support.google.com/optimize/answer/7084762?hl=en).

## Step 1. Enable content experiments (Commerce)

1. Log in to the Admin of your Commerce installation.

1. Follow the instructions to enable [Google Analytics](google-universal-analytics.md) with Content Experiments in the Commerce configuration.

   ![Sales configuration - Google Analytics](./assets/google-analytics-experiments.png)<!-- zoom -->

## Step 2. Set up the variations (Commerce)

Create multiple variations of the same product, category, or page.

- Each variation must have a unique [URL key](../catalog/catalog-urls.md).
- Each variation must have the same [store view](../getting-started/websites-stores-views.md#scope-settings) selected.

You can create up to ten variations of each entity that you want to test. For products, use [Save & Duplicate](../catalog/product-workspace.md) to save time.

## Step 3. Set up the experiment (Google)

>[!NOTE]
>
>You must have the appropriate permissions to the Google account to create an experiment.

1. Open another browser tab, and log into your [Google Analytics][2] account.

   If necessary, navigate to the **[!UICONTROL Account]** and **[!UICONTROL Property]**.

1. In the sidebar on the left, choose **[!UICONTROL Admin]** and use one of the following methods:

   **Method 1:** Choose an Existing View

   In the header of the _[!UICONTROL View]_ column, click the down arrow, and choose the view that is to provide the data for the experiment.

   **Method 2:** Create a New Reporting View

   - In the header of the _View_ column, click **[!UICONTROL Create View]** and do the following:

      - Identify the experiment location as either `Website` or `Mobile app`.

      - Enter a descriptive **[!UICONTROL Reporting View Name]**.

      - Specify the **[!UICONTROL Reporting Time Zone]**.

   - When complete, click **[!UICONTROL Create View]** and then click the back arrow to return to the previous page.

        ![Google Analytics - content experiments reporting](./assets/google-analytics-content-experiments-new-reporting-view.png)<!-- zoom -->

1. In the left panel under _[!UICONTROL Reports]_, choose **[!UICONTROL Behavior]** > **[!UICONTROL Experiments]**.

1. Click **[!UICONTROL Create experiment]** and do the following:

   - Specify the percentage of traffic to redirect.

   - Specify the **[!UICONTROL Original Page URL]** and the URLs of each **[!UICONTROL page variation]** that you want to test.

   - Complete the other options.

1. When the experiment is set up, click **[!UICONTROL Manually Insert the Code]** and copy the code snippet.

## Step 4. Paste code snippet (Commerce)

1. Return to the Admin of your Commerce installation and open the original version of the product, category, or page in edit mode.

1. Expand the **[!UICONTROL View Optimization]** section for the product, category, or page.

1. Paste the code snippet that you copied from Google Analytics into the **[!UICONTROL Experiment Code]** text box.

   >[!NOTE]
   >
   >Do not paste the code snippet into any of the variations.

   ![Product view optimization](../catalog/assets/product-view-optimization.png)<!-- zoom -->

1. When complete, click **[!UICONTROL Save]**.

## Step 5: Review and start the experiment (Google)

1. Return to your [Google Analytics][2] account.

1. Review the experiment settings.

1. If ready to begin, click **[!UICONTROL Start Experiment]**.

   Otherwise, click **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
