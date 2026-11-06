---
title: Enrichment Settings
description: Configure delivery, monthly agentic traffic jobs, and eligible AI agents shared by Catalog Enrichment and PDP enrichment in AI Product Discovery.
---
# Enrichment settings

Use the **[!UICONTROL Settings]** tab in the AI Product Discovery workspace to manage delivery, monthly agentic traffic jobs, and eligible AI agents for both Catalog Enrichment and PDP enrichment. The Catalog Enrichment workflow also has Commerce connection fields on this tab. For those fields, see [Configure catalog enrichment](catalog-enrichment.md#configure-catalog-enrichment).

## Delivery

The delivery status shows whether Optimize at Edge is connected. This shared delivery setting applies to enriched data from both workflows.

### Optimize at Edge connection

When the status is **[!UICONTROL Connected]**, enriched data is served only to the AI agents selected in the settings below. Your storefront, theme, and content management system do not change. Updates go live within minutes.

## Monthly agentic traffic jobs

Monthly agentic traffic jobs identify product pages that AI agents visit most often and create a job for those pages. Use the shared controls to enable or disable this recurring job and choose how many product pages to include.

### Configure monthly jobs

Select or clear the checkbox for **[!UICONTROL Monthly agentic traffic jobs]** to enable or disable recurring jobs. When enabled, a job is created on the first day of each month.

Use the page-count dropdown to set how many product pages to include, ranked by agent visits. The available values and current selection may vary.

## AI agents

Choose which AI agents receive enriched product data from Catalog Enrichment and PDP enrichment. Everyone else, including shoppers, receives the normal product page.

### Select eligible agents

Select or clear the checkbox beside each agent to include or exclude it from enrichment delivery:

- **[!UICONTROL GPTBot (OpenAI)]**
- **[!UICONTROL ClaudeBot (Anthropic)]**
- **[!UICONTROL PerplexityBot]**
- **[!UICONTROL Google-Extended]**
- **[!UICONTROL Applebot-Extended]**

The checkboxes reflect the current configuration and may vary. Select or clear an agent checkbox to change which agents receive enriched data.
