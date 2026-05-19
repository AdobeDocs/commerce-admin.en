---
title: Google reCAPTCHA V3 and V2
description: Learn how to configure Google reCAPTCHA for Admin access and various storefront actions initiated by registered customers.
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/5gL6LIi-okCkQAu--QI4aLcyHlCiNZChc5KtA7t99pA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Google reCAPTCHA V3 and V2

[Google reCAPTCHA](https://developers.google.com/recaptcha) ensures that a human being, rather than a computer (or "bot"), is interacting with your website. Unlike the standard Adobe Commerce and Magento Open Source [CAPTCHA](security-captcha.md), Google reCAPTCHA provides enhanced security with a selection of different display options and methods. Additional website traffic information is available in the dashboard of your Google reCAPTCHA account.

Google reCAPTCHA is configured separately for the Admin and storefront.

- For the Admin, Google reCAPTCHA can be used on the [Sign In](../getting-started/admin-signin.md) page and when a user requests a password reset. If the standard Commerce [CAPTCHA](security-captcha.md) is also enabled, Google reCAPTCHA can be used at the same time without any problem.

- For the storefront, Google reCAPTCHA can be used to sign in to a [customer account](../customers/customer-sign-in.md), send a message from the [Contact Us](../getting-started/store-details.md#contact-us-form) page, and in numerous other storefront locations.

   ![Google reCAPTCHA - customer login](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA can be implemented in several ways:

- _reCAPTCHA v3 Invisible_ — Uses an algorithm to rate user interactions and determines the likelihood that the user is human based on a score.

- _reCAPTCHA v2 Invisible_ — Performs background verification without user interaction. Users and customers are automatically verified, but might be required to select specific images to complete a challenge.

- _reCAPTCHA v2 ("I am not a robot")_ — Validates requests with the _"I'm not a robot"_ checkbox.

>[!IMPORTANT]
>
>Before Google reCAPTCHA can be configured, ensure that your `PHP.ini` file includes the following setting: `allow_url_fopen = 1`. This may require developer assistance. See [Required PHP Settings](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html){:target="_blank"} in the Installation Guide.

## Step 1: Generate Google reCAPTCHA keys

Google reCAPTCHA requires a pair of API keys to enable. You can get these keys free of charge through the reCAPTCHA site. Before generating the keys, you must know the type of reCAPTCHA that you want to use.

1. Open the Google reCAPTCHA Admin Console and log in to your account.

1. For **[!UICONTROL Label]**, enter a name to identify the keys for internal reference.

   You need one set of keys for each reCAPTCHA type that is used in your Adobe Commerce or Magento Open Source installation. For example: `Commerce Invisible`

1. For **[!UICONTROL reCAPTCHA type]**, choose the method that you want to use.

   - _reCAPTCHA v3 Invisible_
   - _reCAPTCHA v2 Invisible_
   - _reCAPTCHA v2 ("I am not a robot")_

1. For **[!UICONTROL Domain]**, enter your store's domain. For example: mystore.com

   If you have multiple stores with different domains, enter each domain on a separate line.

   - Add your store domain and any subdomains.
   - You can add `localhost`, other local VM domains, and staging domains as needed for testing.

1. Select the cloud project

1. Select the checkbox to **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. (Optional) Select the **[!UICONTROL Send alerts to owners]** checkbox to send notification if Google detects issues or suspicious traffic.

1. Click **[!UICONTROL Submit]** to complete registration and receive keys.

   >[!IMPORTANT]
   >
   >Not all keys are applicable for all types of reCAPTCHA, and misapplying them could lead to unexpected behavior. For example, Google reCAPTCHA keys generated for reCAPTCHA v2 "I'm not a robot" do not work with _reCAPTCHA v2 Invisible_ and could block functionality where reCAPTCHA is enabled.

## Step 2: Configure Google reCAPTCHA for the Admin

[!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."}

1. Sign in to your Admin account.

1. On the Admin sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the upper-right corner, set **[!UICONTROL Store View]** to `Default Config`.

1. In the left panel, expand **[!UICONTROL Security]** and click **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >Clear the **[!UICONTROL Use system value]** checkbox for each field that you want to configure.

1. To use _[!DNL reCAPTCHA v2 ("I am not a robot")]_, expand the **[!UICONTROL reCAPTCHA v2 ("I am not a robot")]** section and do the following:

   - For **[!UICONTROL Google API Website Key]**, enter the website key that was created for this reCAPTCHA type when you registered your Google reCAPTCHA account.

   - For **[!UICONTROL Google API Secret Key]**, enter the secret key that is associated with your Google reCAPTCHA account.

   - For **[!UICONTROL Size]**, choose the size of the Google reCAPTCHA box that you want to appear. Options: `Normal (default)` / `Compact`

   - For **[!UICONTROL Theme]**, choose the theme that you want to use to style the Google reCAPTCHA box. Options: `Light Theme (default)` / `Dark Theme`

   - For **[!UICONTROL Language Code]**, enter the two-character code to specify the [language that is used for Google reCAPTCHA text and messaging](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - "I am not a robot"](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. To use _[!DNL reCAPTCHA v2 Invisible]_, expand the **[!UICONTROL reCAPTCHA v2 Invisible]** section and do the following:

   - For **[!UICONTROL Google API Website Key]**, enter the website key that was created for this reCAPTCHA type when you registered your Google reCAPTCHA account.

   - For **[!UICONTROL Google API Secret Key]**, enter the secret key that is associated with your Google reCAPTCHA account.

   - For **[!UICONTROL Invisible Badge Position]**, choose the badge position to be used on each page. Options: `Inline` / `Bottom Right` / `Bottom Left`

   - For **[!UICONTROL Theme]**, choose the theme to be used to style the Google reCAPTCHA box. Options: `Light Theme (default)` / `Dark Theme`

   - For **[!UICONTROL Language Code]**, enter a two-character code that specifies the [language that is used for Google reCAPTCHA text and messaging](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 Invisible](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. To use _[!DNL reCAPTCHA v3 Invisible]_, expand the **[!UICONTROL reCAPTCHA v3 Invisible]** section and do the following:

   - For **[!UICONTROL Google API Website Key]**, enter the website key that was created for this reCAPTCHA type when you registered your Google reCAPTCHA account.

   - For **[!UICONTROL Google API Secret Key]**, enter the secret key that is associated with your Google reCAPTCHA account.

   - Enter the **[!UICONTROL Minimum Score Threshold]** to identify when a user interaction is flagged as a potential risk; where 1.0 is a typical user interaction, and 0.0 is likely a bot. Default: `0.5`

   - For **[!UICONTROL Invisible Badge Position]**, choose the position to be used on each page. Options: `Inline` / `Bottom Right` / `Bottom Left`

   - For **[!UICONTROL Theme]**, choose the theme to be used to style the Google reCAPTCHA box. Options: `Light Theme (default)` / `Dark Theme`

   - For **[!UICONTROL Language Code]**, enter a two-character code that specifies the [language that is used for Google reCAPTCHA text and messaging](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3 Invisible](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. Expand **[!UICONTROL reCAPTCHA Validation Failure Messages]** and enter the messages that appear in the Admin if validation fails or is unable cannot be completed.

   ![reCAPTCHA Failure messages](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. Expand the **[!UICONTROL Admin Panel]** section and configure the following as needed:

   - Set **[!UICONTROL Enable for Login]** to the reCAPTCHA type that you want to use for the Admin Sign In page.

   - Set **[!UICONTROL Enable for Forgot Password]** to the reCAPTCHA type that you want to use for password reset requests.

   ![reCAPTCHA admin options](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## Step 3: Configure Google reCAPTCHA for the storefront

1. In the left panel under _[!UICONTROL Security]_, choose **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Complete the section for each reCAPTCHA type that you want to use in the storefront.

   See the information in _Step 2: Configure Google reCAPTCHA for the Admin_ for details about the options for each reCAPTCHA type.

1. Expand **[!UICONTROL reCAPTCHA Validation Failure Messages]** and enter the messages that appear in the storefront if validation fails or is unable cannot be completed.

1. Expand the **[!UICONTROL Storefront]** section.

   >[!NOTE]
   >
   >Clear the **[!UICONTROL Use system value]** checkbox for each field that you want to configure.

1. Set each storefront location field to the type of reCAPTCHA that you have configured to use.

   {{recaptcha-forms-list}}

   ![Storefront options configuration](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Step 4: Save the configuration

1. When configuration settings are complete, click **[!UICONTROL Save Config]**.

1. In the message at the top of the workspace, click **[!UICONTROL Cache Management]** and refresh each invalid cache.
