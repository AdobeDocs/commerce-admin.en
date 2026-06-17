---
title: Catalog enrichment
description: Use the native catalog enrichment capability in Adobe Commerce to review and apply AI-suggested improvements to product names and descriptions for LLM and AI-assisted discovery.
role: Admin, User, Leader
recommendations: noCatalog
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
---
# Catalog enrichment

>[!IMPORTANT]
>
>Access to catalog enrichment is restricted. Contact your Technical Account Manager for details.

Catalog enrichment is a native [!DNL Adobe Commerce] capability that helps you improve product names and descriptions. Your catalog is represented more accurately when shoppers use LLMs and AI assistants for product research and discovery.

This topic covers catalog enrichment only. Suggestions apply to catalog fields in Commerce, not product detail page (PDP) layout, page structure, or other storefront content. PDP enrichment is not part of this capability.

>[!NOTE]
>
>Catalog enrichment is powered by [!DNL Adobe LLM Optimizer] behind the scenes. You use enrichment as part of your Commerce catalog workflow. You do not manage a separate LLM Optimizer integration to apply approved name and description updates. For broader LLM monitoring and optimization outside Commerce, see the [LLM Optimizer product documentation](https://experienceleague.adobe.com/en/docs/llm-optimizer/using/home).

## What catalog enrichment does {#what-catalog-enrichment-does}

Catalog enrichment helps your team move from broad discovery insights to actionable catalog updates:

- Identify gaps and inconsistencies in product names and descriptions that affect how LLMs interpret your products.
- Review suggested improvements with supporting context, including justifications and before-and-after comparisons.
- Apply approved updates directly to the Commerce catalog so the Admin, storefront, and other channels that read those fields stay aligned.

Because product names and descriptions live in Commerce, improving copy once can benefit every channel that consumes that product data. The benefit depends on how and when your systems refresh.

## Who this is for {#who-this-is-for}

- Digital marketers and merchandisers who want product data to be accurate and consistent in LLM-driven answers.
- Digital marketers and merchandisers who need a controlled way to improve catalog copy at scale.
- Commerce administrators who own catalog integrity, Admin processes, and integrations (API, CSV, PIM) that feed product attributes.

## Prerequisites {#prerequisites}

The following prerequisites apply when you have access to catalog enrichment. Contact your Technical Account Manager for details.

- Your storefront can be crawled by LLM-oriented and agentic bots where crawl coverage is required for catalog-aware suggestions.
- Required Commerce services and catalog connectivity are enabled and healthy. Initial enablement is described in [Enable catalog enrichment](#enable-catalog-enrichment).

## How it works {#how-it-works}

Your [!DNL Adobe Commerce] product catalog is the system of record for product data. Catalog enrichment uses Adobe AI services, including Catalog Agent and [!DNL Adobe LLM Optimizer], to analyze catalog signals, propose clearer product names and descriptions, and write approved changes back to Commerce.

| Direction | Purpose |
| --- | --- |
| Commerce catalog -> analysis | Catalog and URL signals feed enrichment suggestions. |
| Enrichment -> Commerce catalog | After you approve an update, changes to product name and description are saved to the Commerce catalog so the Admin and storefront reflect the optimized values. |

## Enable catalog enrichment {#enable-catalog-enrichment}

Work with your Commerce administrator or implementation partner to ensure the following before you review or apply suggestions:

### Install

1. Install the catalog enrichment extension in your Commerce instance by running the following command:

    ```bash
    install
    ```


1. Install Catalog services by running the following command:

    ```bash
    install
    ```

    **[!UICONTROL Catalog enrichment]** now available in the *Catalog* menu.


### Add a store view {#add-store-view}

**To add a store view for catalog enrichment:**

1. In [!UICONTROL Customer Configuration], select the **[!UICONTROL Commerce]** tab.

   ![Commerce configuration on the Customer Configuration tab](../assets/llmo-commerce-config.png){width="700" zoomable="yes"}

1. Click **[!UICONTROL Add Store View]** to create a new row, or expand an existing store view entry to edit it.
1. Enter the **[!UICONTROL Store View URL]** (required).

   Use the storefront URL for that store view, including any locale or path prefix (for example, `https://brand.example.com/` or `https://brand.example.com/fr/`).

1. Enter the **[!UICONTROL Environment ID]** (required).

   This value is the identifier for the Adobe Commerce environment connected to this store view.

### Complete connection details {#complete-connection-details}

**To complete connection details for a store view:**

1. Enter **[!UICONTROL Website Code]**, **[!UICONTROL Store Code]**, and **[!UICONTROL Store View Code]** (required).

   These values must match the codes in your Commerce Admin for the website, store, and store view you connect.

1. Optional: Enter **[!UICONTROL Host Name]** with the hostname of your Commerce instance (for example, `www.example.com`) if that value is different from the URL.
1. Enter the **[!UICONTROL Adobe Commerce Endpoint]**.

   This value is the base URL of your Adobe Commerce instance used for API access.

1. Enter or paste the **[!UICONTROL API Key]** used to authenticate requests to Commerce APIs.

   Click **[!UICONTROL Copy]** next to the field if you need to copy the key elsewhere securely.

1. Click **[!UICONTROL Save]** to store the configuration.

After you save, wait for any initial sync or validation job to complete before relying on enrichment suggestions for that store view.

To remove a store view configuration, open that entry and click **[!UICONTROL Delete]**.

### Setup CDN log forwarding (how?).

After you complete these steps, it will take some time before URLs are identified as needing updating. When they are ready you can review and apply suggestions to your Commerce catalog.

## Review and apply catalog enrichment {#review-and-apply}

After catalog enrichment is enabled, review suggestions and apply approved updates to product names and descriptions in Commerce.

**To open catalog enrichment suggestions:**

1. In the left rail, click **[!UICONTROL Opportunities]**.
1. Click **[!UICONTROL Commerce Opportunity]** to show optimization types for your [!DNL Adobe Commerce] catalog.
1. Select **[!UICONTROL Product Catalog Enrichment]**.

   ![Commerce opportunities filter and Product Catalog Enrichment](../assets/llmo-opportunities.png){width="700" zoomable="yes"}

1. click catalog enrichment from catalog menu.
1. Land on main catalog enrichment page.

    you'll see a list of urls the feature identified as needing to be updated.

- Catalog data that enrichment must read is exported or synchronized according to your architecture (including any SaaS data exporter or connector in your deployment).
- API access, credentials, and environment URLs (sandbox vs production) match the tenant configured for your project.

Administrators complete one-time project configuration to activate catalog enrichment for each store view. Configuration is managed in the [!DNL Adobe LLM Optimizer] [!UICONTROL Customer Configuration] experience (the service that powers enrichment behind the scenes).

### Configuration field reference {#configuration-fields}

| Field | Description |
| --- | --- |
| [!UICONTROL Store View URL] | Public URL of the store view in scope for catalog enrichment. |
| [!UICONTROL Environment ID] | Commerce environment identifier (from your cloud or deployment documentation, or Admin where applicable). |
| [!UICONTROL Website Code] | Commerce website code for the website that owns the catalog. |
| [!UICONTROL Store Code] | Commerce store code for the store under that website. |
| [!UICONTROL Store View Code] | Commerce store view code for the store view (for example, `default`). |
| [!UICONTROL Host Name] | Hostname of the Commerce storefront or instance when the form asks for it in addition to other URLs. |
| [!UICONTROL Adobe Commerce Endpoint] | Instance URL used to reach Commerce APIs. |
| [!UICONTROL API Key] | Secret key for API authentication; treat it like any production credential. |

### Confirm environment readiness {#confirm-tenant-readiness}

- Verify that connected sandbox projects are not mixed with production Commerce data, unless this is intentional.
- Align user roles in Experience Cloud and Commerce so the people who approve catalog updates have the right permissions on both sides.

### Opportunity metrics {#opportunity-metrics}

Each opportunity view summarizes impact so you can prioritize work:

- **[!UICONTROL Product Pages]** or **[!UICONTROL URLs]**: The products evaluated for catalog enrichment.
- **[!UICONTROL Agentic Traffic]**: Visits and interactions initiated by AI agents that can help you prioritize high-impact opportunities first.

### Suggestion states {#suggestion-states}

Catalog enrichment uses the following workflow views:

- **[!UICONTROL Current Suggestions]**: New or active items to review.
- **[!UICONTROL Fixed Suggestions]**: Items you already applied or resolved.
- **[!UICONTROL Ignored Suggestions]**: Items you intentionally excluded from action.

### Deploy approved suggestions {#review-deploy-catalog}

You can edit a suggestion before you deploy it or move it to **[!UICONTROL Ignored Suggestions]** if it does not match your strategy.

**To deploy approved suggestions:**

1. Open **[!UICONTROL Product Catalog Enrichment]** from **[!UICONTROL Opportunities]**.
1. In the **[!UICONTROL URLs with Suggestions]** table, select **[!UICONTROL Current Suggestions]**.
1. Click the expand control for the URL or SKU row to show the proposed product name and product description updates.
1. Review the suggestion and confirm it matches your merchandising and SEO strategy.
1. Select the row for the URL or SKU to update.
1. Click **[!UICONTROL Deploy optimizations]** and confirm.

Approved name and description changes are saved to your [!DNL Adobe Commerce] catalog like other product updates.

>[!IMPORTANT]
>
>Treat each applied update as a production catalog change. Use your normal change-control, staging, and QA practices. Apply updates only after merchandising and SEO stakeholders agree on the final copy.

After you apply an update, suggestions move to **[!UICONTROL Fixed Suggestions]** with an **Applied** status.

## Verify enrichment in the Admin {#verify-in-admin}

**To verify applied catalog enrichment:**

1. Go to **[!UICONTROL Catalog]** > **[!UICONTROL Products]** in the Commerce Admin.
1. Use filters and the **[!UICONTROL Store View]** selector as needed (for example, **[!UICONTROL Default Store View]**).
1. Search for the SKU.
1. Open the product in edit mode.

   The product form shows the enriched product name.

   ![Product name field after catalog enrichment](../assets/llmo-admin-name.png){width="700" zoomable="yes"}

1. Optional: Select **[!UICONTROL Override LLM Optimizer provided Product Name]** if you want to keep a manually entered name instead.

   Manual overrides affect how suggestions stay in sync with the catalog. For more information, see [Manual override in the Admin](#manual-override-in-the-admin).

1. Expand the **[!UICONTROL Content]** section and locate the description field.

   The enriched description appears when you applied description changes.

   ![Description field after catalog enrichment](../assets/llmo-admin-description.png){width="700" zoomable="yes"}

1. Optional: Select **[!UICONTROL Override LLM Optimizer provided Description]** if you want to keep a manually entered description instead.

## Verify enrichment on the storefront {#verify-storefront}

**To verify enrichment on the storefront:**

1. Search for the SKU on your storefront.
1. Open the product page.
1. Confirm that the product name matches what you approved.
1. Confirm that regions that show the long description match what you approved.
1. Optional: Confirm downstream channels that consume the same catalog attributes, where relevant to your rollout.

## Overrides, ingestion, and stale suggestions {#overrides-ingestion}

After catalog enrichment updates a product's name or description, other ingestion systems may change the same fields. Examples include REST API calls, CSV imports, and PIM feeds.

### Original value re-ingested {#original-value-reingested}

If an external process writes the original name or description (the value that existed before enrichment was applied), Commerce continues to honor the enriched value for that field according to the catalog enrichment rules. The suggestion may not revert automatically based on that ingestion alone.

### New value re-ingested {#new-value-reingested}

If the external process sends a new value that is not a repeat of the pre-enrichment text, Commerce honors the new catalog value. For example, a rename from "Red Shoes" to "Iconic Red Shoes" replaces the enriched value. The related enrichment suggestion is typically marked as *Stale* because the live catalog no longer matches the suggestion context.

### Manual override in the Admin {#manual-override-in-the-admin}

If you manually edit the product name or description in the [!DNL Adobe Commerce] Admin:

- The Admin value wins as the system of record for that manual change.
- The enrichment suggestion is marked *Stale*.
- The suggestion workflow moves back toward the original state for that item so you can re-baseline or accept a new suggestion if analysis runs again.

These rules help you know whether catalog enrichment, ingestion feeds, or Admin edits are authoritative when multiple channels touch the same SKU.

## Limits and considerations {#limits}

- Enrichment applies to product names and descriptions only. It does not change PDP layout, widgets, or other page-level storefront content.
- Large catalogs and high URL counts can affect how quickly analysis completes and how many suggestions appear at once.
- Meaningful suggestions assume that LLM-relevant bots can access the product URLs you care about. Robots rules, authentication, geo-blocking, and heavy personalization can reduce coverage.

## Best practices {#best-practices}

- Document system ownership for product name and description so that PIM or feed jobs do not unintentionally conflict with catalog enrichment.
- Coordinate with SEO and brand teams before bulk applying titles or descriptions.
- Re-sync or re-analyze after major catalog imports so that suggestions reflect the current catalog state.

## Examples

This section will provide examples of what enrichment before/after looks like:
