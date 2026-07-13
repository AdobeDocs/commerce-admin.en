---
title: Google reCAPTCHA Enterprise
description: Learn how to configure Google reCAPTCHA Enterprise to protect your Adobe Commerce as a Cloud Service storefront from bots and fraudulent activities.
role: Admin
feature: Configuration, Security
badgeSaas: label="SaaS only" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service projects only (Adobe-managed SaaS infrastructure)."
exl-id: 2c88488c-8ff1-41db-b81b-89ad164e134d
TQID: https://experienceleague.adobe.com/oMZleuJsp2QiDD7IsMDV647LWKm938lNvY4--o6G3c8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
    internal-label: Machine learning
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Google reCAPTCHA Enterprise

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform) provides advanced bot protection for your Adobe Commerce as a Cloud Service storefront by using adaptive risk analysis and machine learning to differentiate between human users and bots. This helps to prevent fraudulent activities, spam, and abuse on your site.

>[!NOTE]
>
>This feature does NOT provide reCAPTCHA support for the Admin.

[reCAPTCHA integration](https://experienceleague.adobe.com/developer/commerce/storefront/dropins/user-auth/recaptcha/) describes how to add support for reCAPTCHA Enterprise into your storefront.

See [Google reCAPTCHA V3 and V2](security-google-recaptcha.md) for information about configuring other versions of Google reCAPTCHA.

## Features

Google reCAPTCHA Enterprise includes the following features:

- **Advanced bot detection**: Uses Google Cloud's machine learning models for superior bot detection
- **Risk score analysis**: Provides detailed risk scores (0.0-1.0) for each interaction
- **Configurable thresholds**: Set minimum acceptable risk scores per tenant
- **Multi-tenant Support**: Per-tenant configuration with isolated Google Cloud projects
- **Encrypted credentials**: Service account credentials stored encrypted in a database
- **Form protection**: Protects all standard Commerce forms, including login, checkout, product reviews, and more.

## Prerequisites

You need the following resources before you can configure Google reCAPTCHA Enterprise for your Adobe Commerce as a Cloud Service storefront:

- An active Google Cloud account with reCAPTCHA Enterprise enabled.
- Access to the Google Cloud Console to create and manage reCAPTCHA Enterprise keys.

On multi-tenant Adobe Commerce as a Cloud Service installations, each tenant must have its own Google Cloud project and reCAPTCHA Enterprise keys.

## Step 1: Set up Google reCAPTCHA Enterprise

Follow these general steps to set up Google reCAPTCHA Enterprise for your storefront. For detailed instructions, see the [Google reCAPTCHA Enterprise documentation](https://docs.cloud.google.com/recaptcha/docs/overview).

1. [Create a Google Cloud project](https://developers.google.com/workspace/guides/create-project) for your reCAPTCHA Enterprise implementation.

1. Enable the [reCAPTCHA Enterprise API](https://docs.cloud.google.com/recaptcha/docs/prepare-environment).

1. Create a score-based reCAPTCHA Enterprise [site key](https://docs.cloud.google.com/recaptcha/docs/choose-key-type).

1. Create a Service Account with the `roles/recaptchaenterprise.admin` IAM role.

1. Download the Service Account JSON key file, which contains the credentials needed to authenticate your Adobe Commerce as a Cloud Service storefront with Google reCAPTCHA Enterprise.

## Step 2: Configure Google reCAPTCHA for the storefront

1. On the Adobe Commerce _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. Expand _[!UICONTROL Security]_ and choose **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Scroll down to the **[!UICONTROL reCAPTCHA Enterprise]** section, and complete the configuration as follows.

   - For **[!UICONTROL Site Key]**, copy and paste your reCAPTCHA Enterprise site key from your Google Cloud Console.

   - For **[!UICONTROL Google Cloud Project ID]**, copy and paste the project ID from your Google Cloud project.
   
   - For **[!UICONTROL Service Account JSON]**, copy the contents of the Service Account JSON key file that you downloaded in [Step 1: Set up Google reCAPTCHA Enterprise](#step-1-set-up-google-recaptcha-enterprise).

   - For **[!UICONTROL Minimum Score Threshold]**, enter the minimum score (0.0-1.0) to identify when a user interaction is flagged as a potential risk. A score of 1.0 is a typical user interaction, and 0.0 is likely a bot.

   - For **[!UICONTROL Badge Position]**, choose the position of the invisible reCAPTCHA badge on each page. Options: `Inline` / `Bottom Right` / `Bottom Left`.

   - For **[!UICONTROL Theme]**, choose either `Light Theme` (default) or `Dark Theme` to determine the style of the Google reCAPTCHA box.

   - For **[!UICONTROL Language Code]**, enter a [two-character code](https://developers.google.com/recaptcha/docs/language) that specifies the language used for Google reCAPTCHA text and messaging.

   - For **[!UICONTROL Validation Failure Message]**, optionally change the message displayed on the storefront when validation is not successful.


1. Expand the **[!UICONTROL Storefront]** section and set each storefront form that you want to protect to **[!UICONTROL reCAPTCHA Enterprise]**.

   {{recaptcha-forms-list}}

   ![Storefront options configuration](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Step 3: Save the configuration

1. When configuration settings are complete, click **[!UICONTROL Save Config]**.

1. In the message at the top of the workspace, click **[!UICONTROL Cache Management]** and refresh each invalid cache.
