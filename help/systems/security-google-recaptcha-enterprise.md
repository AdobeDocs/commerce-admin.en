---
title: Google reCAPTCHA Enterprise
description: Learn how to configure Google reCAPTCHA Enterprise to protect your Adobe Commerce as a Cloud Service storefront from bots and fraudulent activities.
role: Admin
feature: Configuration, Security
badgeSaas: label="SaaS only" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce as a Cloud Service projects only (Adobe-managed SaaS infrastructure)."
---
# Google reCAPTCHA Enterprise

[!BADGE Sandbox]{type=Caution tooltip="The items listed are currently only available in Sandbox environments. Adobe makes new releases available in Sandbox environments first to provide time for you to test upcoming changes before the release is available on Production environments."}

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform) provides advanced bot protection for your Adobe Commerce as a Cloud Service storefront by using adaptive risk analysis and machine learning to differentiate between human users and bots. This helps to prevent fraudulent activities, spam, and abuse on your site.

>[!NOTE]
>
>This feature does NOT provide reCAPTCHA support for the Admin.

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

1. In the left panel under _[!UICONTROL Security]_, choose **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Complete the **[!UICONTROL reCAPTCHA Enterprise]** section as follows.

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
