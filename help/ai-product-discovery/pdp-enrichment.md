---
title: Product Detail Page Enrichment
description: Use [!DNL Adobe Commerce] Product Detail Page Enrichment to review AI-suggested product copy, create enrichment jobs, and deploy approved updates for LLM and AI discovery.
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgeCloud or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c32adafa-ed01-4b31-997e-2413013911b0
    internal-label: Integrations
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---

# Product detail page enrichment

Product detail page (PDP) enrichment helps AI agents access selected facts from your Adobe Commerce catalog for product pages. Choose the product pages and catalog facts to include in an enrichment job. The workflow restructures information already in your catalog; it does not add product information or change your storefront.

## How it works {#how-it-works}

Your Adobe Commerce catalog contains product information such as attributes, variants, categories, prices, and availability. In a PDP enrichment job, you select the product pages and groups of catalog facts to make available to AI agents. The information is organized for agents without changing the storefront experience.

With PDP enrichment, you can:

- Choose specific enabled products that have live product pages.
- Select which groups of existing catalog facts to include.
- Review a summary of the selected pages and facts before saving or running the job.
- Preview the product information included in the enrichment.

| Direction | Purpose |
| --- | --- |
| Commerce catalog -> enrichment job | Select live product pages and the catalog facts to include. |
| Enrichment job -> AI agents | Make the selected, existing product information available in a structured form. The storefront does not change. |

## Access PDP enrichment

Before you begin, review the deployment-specific [AI Product Discovery prerequisites](guide-overview.md#prerequisites). After installing the shared enrichment extension and required Catalog Services, open **[!UICONTROL AI Product Discovery]** in the Admin and select **[!UICONTROL Product Details Page Enrichment]**.

## Review PDP enrichment activity

The PDP enrichment page opens to the **[!UICONTROL Optimizations]** tab. Use the dashboard to review enrichment coverage, job activity, and jobs that need attention. Use the **[!UICONTROL Settings]** tab to natively link your [Adobe Commerce instance to Adobe Brand Visibility](settings.md).

### Find jobs that need attention

The **[!UICONTROL Needs your attention]** section highlights jobs that require action. A card can show the job name, how products were selected, the number of product pages, job status, and progress. Use the available action on a card to continue with the job.

### Search all jobs

Use the table to search for and track jobs. Search by job details or filter by status, including **[!UICONTROL Generating]**, **[!UICONTROL Ready to review]**, **[!UICONTROL Deployed]**, **[!UICONTROL Queued]**, or **[!UICONTROL Failed]**. The table lists each job's ID, name, origin, product page count, start date, status, and available actions.

## Create an enrichment job

In this section, you learn how to creat a product detail page enrichment.

![Create PDP Enrichment](./assets/create-cat-enrich.png)

1. In **[!UICONTROL Optimizations]**, click **[!UICONTROL Create enrichment]**.
1. Enter an **Enrichment name**, such as "Black Friday 2026".
1. Select the **Category**, such as "Coffee".
1. Select the **Attribute set**, such as "Accessories".
1. Select the **Product type**, such as "Simple product".
1. Select the **Price range**.
1. Click **[!UICONTROL Apply filters]**.

    You can preview the products that match your enrichment criteria and click **Customize** to further scope the products you want to enrich.

1. Click **[!DNL Next]** to confirm the specific products you want to enrich.
1. Click **[!DNL Run enrichment]**.

    The enrichment job runs and displays on the **Optimizations** table. When it finishes running, you can [Review and Deploy](#review-and-deploy-an-enrichment-job) the optimizations. 

### Review an enrichment job {#review-and-deploy-an-enrichment-job}

Open an enrichment job.

![List of PDP Enrichment URLs](./assets/pdp-enrich-urls.png)

The **URLs with suggestions** table lists all products with enrichment opportunities. For each product you can:

- **Expand the row** to view the AI Analysis and the proposed enrichment.
- **Edit** the proposed product name or description before applying, to align with your brand voice and merchandising guidelines.
- **Deploy the Optimization** for the products you want to enrich and publish it directly to your Adobe Commerce catalog.
- **Mark as Fixed** once the enrichment has been reviewed and applied.
- **Ignore** suggestions that are not relevant to your catalog strategy.

Suggestions are organized into three views: **Current Suggestions**, **Fixed Suggestions**, and **Ignored Suggestions**. Once an enrichment is applied, it moves to Fixed Suggestions with a status of **Applied** and a **View in Catalog** action to verify the update in Adobe Commerce. Applied enrichments can be rolled back at any time.

### Deploy the optimization

Once you have reviewed the suggestions and selected the product pages to optimize, click **Deploy optimizations** to publish the enrichment at the CDN edge. A **Deploy to Edge** confirmation dialog shows the selected product URLs, the optimization type and the enrichment being applied. After deployment, a confirmation screen confirms which product pages were successfully optimized.

The optimization is delivered exclusively to AI user agents via the CDN edge layer. Human visitors continue to see your existing storefront experience exactly as before with no changes to your PDP design, page performance, or brand experience.

## Limits and considerations {#limits}

- Only enabled products with a live product page can be selected.
- Enrichment organizes facts already present in the catalog; it does not add new product information.
- The Commerce Admin PDP enrichment workflow does not change the storefront.
- PDP enrichment jobs and Catalog Enrichment jobs have different purposes and workflows.
- The Brand Visibility **Enrich Product Detail Pages** opportunity is a separate workflow that uses Optimize at Edge. Do not use its CDN deployment steps as instructions for a Commerce Admin enrichment job.

## Best practices {#best-practices}

- Use clear job names that identify the product group or campaign.
- Preview the facts included in the job and confirm they are accurate and appropriate for AI agents.
- Check whether products were already enriched before deciding to skip or overwrite them.
- Confirm the selected product pages and fact groups in the job summary before running the job.
- Coordinate catalog synchronization and ownership of product facts with the teams responsible for those records.

## Example: Enrich a product with variants and specifications

A product may have catalog information distributed across attributes, options, and feature highlights. For example, a merchant could select **[!UICONTROL Product attributes]** for material and care instructions, **[!UICONTROL Variants & options]** for available sizes or colors, and **[!UICONTROL Feature bullets]** for factual highlights.

The enrichment job organizes the selected catalog information for AI agents. It does not create facts that are absent from the catalog or alter the product page shown to shoppers.
