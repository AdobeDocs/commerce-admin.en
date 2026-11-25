---
title: Enrichment Settings
description: Configure delivery, monthly agentic traffic jobs, and eligible AI agents shared by Catalog Enrichment and PDP enrichment in AI Product Discovery.
---
# Enrichment settings

Use the **[!UICONTROL Settings]** tab in the AI Product Discovery workspace to configure your Adobe Commerce instance. When configured, catalog and PDP enrichments are surfaced in the AI Product Discovery workspace.

The fields on this tab identify the [!DNL Adobe Commerce] environment and store view that AI Product Discovery connects to. For IMS sign-in and organization requirements, see the [AI Product Discovery prerequisites](prerequisites.md).

1. In the Admin, go to **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]** or **[!UICONTROL Product Details Page Enrichment]**.
1. In the **[!UICONTROL Scope]** list at the top of the page, select the store view you want to configure, or leave **[!UICONTROL All Store Views]** to manage settings across store views.
1. Open the **[!UICONTROL Settings]** tab.
1. In **[!UICONTROL Commerce Configuration]**, expand the store view panel labeled with its URL.

   Provide your [!DNL Adobe Commerce] environment details to enable the AI Product Discovery service and audit workflows.

   ![Commerce Configuration on the Catalog Enrichment Settings tab](./assets/catalog-enrichment-commerce-config.png){zoomable="yes"}

1. Enter the required connection details for the store view.

    - **[!UICONTROL Store View URL]**: URL corresponding to the store view (for example, `https://brand.example.com/fr/`).
    - **[!UICONTROL Environment ID]**: Unique identifier for the [!DNL Adobe Commerce] environment that the connection accesses.
    - **[!UICONTROL Website Code]**, **[!UICONTROL Store Code]**, and **[!UICONTROL Store View Code]**: Website, store, and store view codes for the Commerce website. These values must match the codes in your Commerce Admin.
    - **[!UICONTROL Host Name]**: Host name of your [!DNL Adobe Commerce] instance.
    - **(Optional - for catalog enrichment only)** Under **[!UICONTROL Catalog field limits]**, select **[!UICONTROL Limit maximum characters for product name]** and specify the character limit for any generated product names. Select **[!UICONTROL Limit maximum characters for product description]** and specify the character limit for any generated product descriptions.

1. Click **[!UICONTROL Save]**.

After you save, wait for any initial sync or validation job to complete before relying on catalog or audit results for that store view. It may take up to 24 hours for product suggestions to appear on the **[!UICONTROL Catalog Enrichment]** page.

To remove a store view configuration, expand that entry and click **[!UICONTROL Delete]**.

## Field descriptions {#commerce-connection-fields}

Required fields are marked with an asterisk (*) on the **[!UICONTROL Commerce Configuration]** form.

| Field | Required | Description |
| --- | --- | --- |
| Store View URL | Yes | URL corresponding to the store view (for example, `https://brand.example.com/fr/`). |
| Environment ID | Yes | Unique identifier for the [!DNL Adobe Commerce] environment that the connection accesses. |
| Website Code | Yes | Website Code of the Commerce website. |
| Store Code | Yes | Store Code of the Commerce website. |
| Store View Code | Yes | Store View of the Commerce website. |
| Host Name | Yes | Host name of your [!DNL Adobe Commerce] instance. |
| Catalog field limits (Catalog enrichment only) | No | Define character limits for any generated product names and descriptions. |
