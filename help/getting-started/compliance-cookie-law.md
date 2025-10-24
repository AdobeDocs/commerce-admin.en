---
title: Cookie law compliance
description: To keep pace with legislation in many countries regarding the use of cookies, Adobe Commerce and Magento Open Source offer merchants a choice of methods to obtain customer consent.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
---
# Cookie law compliance

Cookies are small files that are saved to the computer of each visitor to your site, and used as temporary holding places for information. Information that is saved in cookies is used to personalize the shopping experience, link visitors to their shopping carts, measure traffic patterns, and improve the effectiveness of promotions. To keep pace with legislation in many countries regarding the use of cookies, Adobe Commerce and Magento Open Source offer merchants a choice of methods to obtain customer consent. For a list of the default cookies in Adobe Commerce and Magento Open Source, the [Cookie Reference](#default-cookies).

>[!NOTE]
>
>If you modify the default [Google privacy settings](../merchandising-promotions/google-tools.md#google-privacy-settings) to comply with the [General Data Protection Regulation](compliance-gdpr.md), it is not necessary to obtain user consent for the use of Google Analytics cookies.

## Cookie restriction mode

When cookie restriction mode is enabled, visitors to your store are notified that cookies are required for full-featured operations. Depending on your theme, the message might appear above the header, below the footer, or somewhere else on the page. The message links to your privacy policy for more information, and encourages visitors to click the Allow button to grant consent. After consent is granted, the message disappears.

Your [privacy policy](privacy-policy.md)) should include the name of your store and contact information, and explain the purpose of each cookie that is used by your store. To learn more, see [Cookie Reference](#default-cookies).

>[!NOTE]
>
>If you change the URL key of the privacy policy, you must also create a custom URL rewrite to redirect traffic to the new URL key. Otherwise, the link in the Cookie Restriction Mode message returns `404 Page Not Found`.

![Example storefront - cookie restriction notice](./assets/storefront-cookie-restriction-message.png){width="600"}

### Step 1: Enable cookie restriction mode

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**.

1. In the left navigation panel under **[!UICONTROL General]**, choose **[!UICONTROL Web]**.

1. Expand the **[!UICONTROL Default Cookie Settings]** section and do the following:

    ![Web configuration - default cookie settings](./assets/web-default-cookie-settings.png){width="600"}
 
    - Enter the **[!UICONTROL Cookie Lifetime]** in seconds.

    - If you want to make cookies available to other folders, enter the **[!UICONTROL Cookie Path]**. To make the cookies available anywhere in the site, enter a forward slash (`/`). This value can contain only the cookie path, and **_cannot_** contain any other cookie parameters.

    - To make the cookies available to a subdomain, enter the subdomain name in the **[!UICONTROL Cookie Domain]** field (`subdomain.yourdomain.com`). To make cookies available to all subdomains, enter the domain name preceded by a period (`.yourdomain.com`). This value can contain only the cookie domain, and **_cannot_** contain any other cookie parameters.

    - To prevent scripting languages, such as JavaScript, from gaining access to cookies, make sure that **Use HTTP Only** is set to `Yes`.

    - Set **[!UICONTROL Cookie Restriction Mode]** to `Yes`.

        If necessary, clear the checkbox and click **[!UICONTROL OK]** to confirm scope switching.

1. When complete, click **[!UICONTROL Save Config]**.

1. When prompted to update the cache, click the **[!UICONTROL Cache Management]** link in the system message and refresh each invalid cache.

### Step 2: Update your privacy policy

Update your [privacy policy](privacy-policy.md) so that it reflects the information that your company collects and how it is used.

## Default cookies

The default cookies in Adobe Commerce and Magento Open Source are classified as Exempt/Non-Exempt to help merchants meet the requirements of privacy regulations such as the [GDPR](compliance-gdpr.md). Merchants should use this information as a guide, and consult with legal advisors to update their Privacy and Cookie Policies as part of a comprehensive privacy regulation compliance strategy.

The following cookies are used by [!DNL Commerce] "out of the box" for on-premise and cloud installations. These cookies may be required by functionality that is explicitly requested by the customer. To learn more about the lifetime of session cookies, see [Session Lifetime](../customers/customer-online-options.md).

Some of these cookies may provide configuration options, including enable/disable, as needed.

### Requested functionality cookies (exempt)
 
#### `add_to_cart` 

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) Captures the product SKU, name, price, and quantity removed from the cart. Allows Google Analytics to know when a product has been added to a cart. 

#### `guest-view`

Links a guest order to a guest (because there is no account for guest).

#### `login_redirect`

Saves redirect URL to route user if successful login and user registration. Saves the page that a user was on prior to log in (to determine the location they will go back to after they log in).

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) Stores banner content locally to improve performance. Banner content is any content that a merchant would display on their website.

#### `mage-messages`

Tracks error messages and other notifications that are shown to the user, such as the cookie consent message, and various error messages. The message is deleted from the cookie after it is shown to the shopper. There is not an option to disable this cookie. This is how one-time information is communicated to the user, such as error messages.

#### `product_data_storage` (local storage)

Stores configuration for product data used to use "Recently Viewed" and "Compare Products" functions. Stores a user's specific settings (for example, if they have recently viewed a product or compared products).

#### `recently_compared_product` (local storage)

Stores product IDs of recently compared products.

#### `recently_compared_product_previous` (local storage)

Stores product IDs of previously compared products for easy navigation.

#### `recently_viewed_product` (local storage)

Stores product IDs of recently viewed products for easy navigation.

#### `recently_viewed_product_previous` (local storage)

Stores product IDs of recently viewed products for easy navigation.

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) Allows Google Analytics to know when a product has been removed from a cart.

#### `stf`

Records the time messages are sent by the SendFriend ([Email a Friend](../stores-purchase/email-a-friend.md)) module. When a shopper sends a link to a product, this cookie records a time-stamp and maintains a count.

#### `X-Magento-Vary`

Indicates when a new version of a page needs to be served from the cache. Supports website performance.

#### `form_key`

A security mechanism that holds a randomly generated value to prevent Cross Site Request Forgery attacks (CSRF) by helping determine whether a request came from a genuine source or a bad actor. This is an industry-standard practice to prevent CSRF attacks.

#### `mage-cache-sessid`

Useful in determining when to clean local storage in the browser after session expiry. This is used to determine if local storage has to be cleaned. The absence of this cookie triggers local storage cleanup.

#### `mage-cache-storage`

Local storage of visitor-specific content that enables e-commerce functions. Unused by default, but when it is used, it's used to expedite checkout so that basic user information is available when someone leaves and returns.

#### `mage-cache-storage-section-invalidation`

Stores information related to which sections of the page need to be invalidated and removed.

#### `persistent_shopping_cart`

Stores the key ID of a persistent cart to make it possible to restore the cart for an anonymous shopper.

#### `private_content_version`

Appends a random, unique number and time to pages with customer content to prevent them from being cached on the server. It is set in multiple places: in PHP, in JavaScript as a cookie, and in JavaScript to local storage.

#### `section_data_ids`

Stores customer-specific information related to shopper-initiated actions, such as wish list display and checkout information.

#### `store`

Tracks the specific store view/locale selected by the shopper.

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) Local storage for Banner functionality. Banner means general website assets any information displayed to a shopper.

#### `PHPSESSID`

Tracks user sessions on the storefront. This is the shoppers who use the end-products.

#### `admin`

Tracks user sessions on the Admin side.

#### `loggedOutReasonCode`

Set when an Admin user is locked out after a certain number of unsuccessful password attempts.

#### `section_data_clean`

Set when a user switches store view. The presence of this cookie triggers JavaScript to reload certain sections on the page to reflect the correct store view.

#### `lang`

Set indirectly by the Admin Analytics module. Being used only in an administrative area of a store. Not applicable to shoppers.

#### `s_fid`

Set indirectly by the Admin Analytics module. Fallback unique visitor ID time/date stamp. It is used to identify a unique visitor if the standard `s_vi` cookie is unavailable due to third-party cookie restrictions. Being used only in an administrative area of a store. Not applicable to shoppers.

#### `s_cc`

Set indirectly by the Admin Analytics module. It is set and read by the JavaScript code to determine if cookies are enabled. Being used only in an administrative area of a store. Not applicable to shoppers.

#### `apt.sid`

Set by the Gainsight PX library indirectly used by the Admin Analytics module. The purpose of this cookie is to allow persistent session ID tracking under the top-level domain of the product and is used as a reference ID to the active session. Being used only in an administrative area of a store. Not applicable to shoppers.

#### `apt.uid`

Set by the Gainsight PX library indirectly used by the Admin Analytics module. The purpose of this cookie is to allow persistent ID tracking under the top-level domain of the product and is used as a reference ID to the user entity. Being used only in an administrative area of a store. Not applicable to shoppers.

#### `s_sq`

Set indirectly by the Admin Analytics module. Used by the ClickMap feature that collects data on where visitors click and what they click. Stores information from each click. Being used only in an administrative area of a store. Not applicable to shoppers.

#### `pagebuilder_modal_dismissed`

Set by the Page Builder Module. Contains a flag that prevents subsequent prompts asking an admin to confirm a certain action from opening if the admin explicitly dismissed them before. Being used only in an administrative area of a store. Not applicable to shoppers.

#### `pagebuilder_template_apply_confirm`

Set by the Page Builder Module. Contains a flag that prevents subsequent prompts asking an admin to confirm a certain action from opening if the admin explicitly dismissed them before. Being used only in an administrative area of a store. Not applicable to shoppers.

#### `accordion-{VARIABLE}-{VARIABLE}`

Being used as a part of tabs functionality implementation only in an administrative area of a store. Not applicable to shoppers.

## Product Recommendations cookies

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) The following cookies are used by Product Recommendations for Adobe Commerce customers. These cookies are installed with the [DataServices module](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure).

- `mg_dnt`: Allows you to [restrict Adobe Commerce data collection](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/developer/setting-cookie) if you have custom code to manage cookie consent on your site.
- `user_allowed_save_cookie`: Used for [cookie restriction mode](#cookie-restriction-mode).
- `authentication_flag`: Indicates if a shopper has signed in or signed out. This cookie is updated at the same time as the `dataservices_customer_id` cookie.
- `dataservices_customer_id`: Indicates if a shopper has signed in or signed out. This cookie contains the customer's unique ID in the system.
- `dataservices_customer_group`: Indicates a customer's group. This cookie is stored as [sha1](https://en.wikipedia.org/wiki/SHA-1) checksum of the customer's group ID.
- `dataservices_cart_id`: Identifies a shopper's cart actions. This cookie contains the customer's unique cart ID in the system.
- `dataservices_product_context`: Identifies a shopper's product interactions. This cookie contains the customer's unique quote ID in the system.

### Product Recommendations local storage data

The following data is saved to local storage for stores using the Luma theme when Live Search or Product Recommendations is installed:

- `ds-cart`: Stores cart information for Luma-specific functionality
- `ds-cart-order`: Stores order information for cart functionality
- `ds-purchase-history`: Tracks customer purchase history
- `ds-view-history-time-decay`: Stores product view history with time-based decay
- `ds-logged-in`: Indicates customer login status. This data only exists when the customer is logged in and is stored even when cookie restriction mode is enabled. This is the only data that Commerce stores in local storage when cookie restriction mode is enabled, regardless of user consent status.

## Additional cookies

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) The following cookies are set for Adobe Commerce customers. These cookies are installed with the [DataServices module](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure).

- `mg`: Set by Snowplow JavaScript tracker. More information can be found in the [Snowplow documentation](https://docs.snowplow.io/docs/sources/trackers/javascript-trackers/web-tracker/tracker-setup/initialization-options/).
- `com.adobe.alloy.getTld`: Given the current web page's hostname, this is the top-most domain that is not a "public suffix" as outlined in https://publicsuffix.org. Essentially, this is the top-most domain that can accept cookies. This cookie is part of the [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
