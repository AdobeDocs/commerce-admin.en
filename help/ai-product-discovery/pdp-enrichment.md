---
title: Create a PDP Enrichment Job
description: Learn how to create a PDP enrichment job, select product pages and catalog facts, manage already-enriched products, and review agent coverage and job details.
---
# Create a PDP enrichment job

Create a product detail page (PDP) enrichment job to choose the product pages and catalog facts that AI agents can access. The enrichment restructures information already in your catalog and does not change your storefront.

## Access PDP enrichment

Open **[!UICONTROL AI Product Discovery]** in the Admin, then select **[!UICONTROL Product Details Page Enrichment]**. This workflow is separate from **[!UICONTROL Catalog Enrichment]**.

## Review PDP enrichment activity

The PDP enrichment page opens to the **[!UICONTROL Optimizations]** tab. Use the dashboard to review AI agent traffic, enrichment coverage, job activity, and jobs that need attention. Shared delivery, monthly agentic traffic, and AI agent settings also apply to Catalog Enrichment. See [Enrichment settings](settings.md).

### Review traffic and coverage

The traffic summary shows how often AI agents visited your product pages during the last four weeks and how that compares with the previous four weeks. Agent labels include [!DNL ChatGPT], [!DNL Claude], [!DNL Perplexity], and [!DNL Gemini].

The coverage summary shows the portion of product pages with enrichment and groups pages into live, to review, and not yet enriched categories. Select **[!UICONTROL Review 44 pages]** to review pages marked for review. The number in the button reflects the current count.

### Review agentic traffic jobs

The **[!UICONTROL From agentic traffic]** section groups jobs by month. Each card shows the job name, number of product pages, AI agent visits, and job status. For a job that is ready to review, select **[!UICONTROL Review & deploy]** to continue.

### Find jobs that need attention

The **[!UICONTROL Needs your attention]** section highlights jobs that require action. A card can show the job name, how products were selected, the number of product pages, the job status, and progress. Depending on the status, use **[!UICONTROL Review & deploy]** to continue reviewing a job.

### Search all jobs

Use the **[!UICONTROL All jobs]** table to find and track jobs. Search by job details or filter the table by status, including **[!UICONTROL Generating]**, **[!UICONTROL Ready to review]**, **[!UICONTROL Deployed]**, **[!UICONTROL Queued]**, or **[!UICONTROL Failed]**. The table lists each job's ID, name, origin, product page count, start date, status, and available actions.

## Create a PDP enrichment job

Start by choosing how to set up the job. Then select product pages and catalog facts, review the summary, and save or run the job.

### Choose a starting point

Choose one of the available options to set up your job:

- **[!UICONTROL Blank]** — Select product pages and configure the job yourself.
- **[!UICONTROL Copy a past job]** — Reuse product pages from an existing job.
- **[!UICONTROL Describe with AI]** — Describe what you want to enrich in plain language.

### Copy a past job

When you copy a past job, search the job list and select a job to reuse its product pages. The list shows details such as the job name, product count, selection method, date, and status.

### Name the job

Enter a name that helps you identify the job later, such as a product category or campaign name. When you copy an existing job, the name field may contain a name based on the source job.

### Select product pages

Choose the product pages to include in the job. Only enabled products with a live product page can be enriched.

Use the search field to find products by name, SKU, or URL. Narrow the results with filters for category, price, status, and store view. Select **[!UICONTROL More filters]** to see additional options.

Select the checkboxes next to the products you want to include. The table shows each product, its product page URL, and price. The counts above the table show how many products match the current search and filters and how many you selected.

To exclude products that already have enrichment, select **[!UICONTROL Hide already enriched]**.

### Handle enriched products

If selected products were enriched by a previously deployed job, the page identifies them and shows the related job numbers. Choose how to handle these products before you continue:

- Select **[!UICONTROL Skip them]** to exclude the already-enriched products from this job.
- Select **[!UICONTROL Overwrite them]** to include the products and replace their existing enrichment.

### Choose catalog facts

In **[!UICONTROL What AI agents will see]**, select the catalog fact groups to include in the enrichment. These groups organize information already in your catalog. They do not add new product information.

- **[!UICONTROL Product attributes]** — Core details, such as material, dimensions, and care instructions.
- **[!UICONTROL Variants & options]** — Available sizes, colors, and configurations.
- **[!UICONTROL Feature bullets]** — Short, factual highlights from your catalog.
- **[!UICONTROL Category & relationships]** — Category paths and related products.
- **[!UICONTROL Price & availability]** — Current price, stock, and shipping information. This information updates when your catalog syncs.

### Review the job summary

Review the summary before you save or run the job. It includes the job name, number of product pages, already-enriched products, selected fact groups, and estimated time.

The **[!UICONTROL AI agent traffic covered]** panel shows the share of agent visits associated with the selected pages and the reporting period. It also lists top pages in the job and their visit counts. Use this information to understand how your selection relates to agent traffic.

Expand **[!UICONTROL Preview what agents see]** to review the product information included in the enrichment. Only AI agents see this information; your storefront does not change.

### Save or run the job

When you finish configuring the job, choose an action:

- Select **[!UICONTROL Save as draft]** to save the job configuration for later.
- Select **[!UICONTROL Run enrichment]** to start enriching the selected product pages.
- Select **[!UICONTROL Cancel]** to leave the job setup.
