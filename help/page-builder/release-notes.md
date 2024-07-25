---
title: Release Notes for [!DNL Page Builder]
description: Review the release notes for information about all [!DNL Page Builder] releases.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
---
# Release notes for [!DNL Page Builder]

These release notes describe releases of [!DNL Page Builder] and include:

![New](../assets/new.svg) New features

![Fixed issue](../assets/fix.svg) Fixes and improvements

![Known issue](../assets/bug.svg) Known issues

>[!IMPORTANT]
>
>Starting with the 2.4.3 release, [!DNL Page Builder] is now available as a bundled extension in Magento Open Source. It is now the default content-editing tool for both Adobe Commerce and Magento Open Source, and can replace the WYSIWG editor with any third-party module.

## 1.7.2 for Commerce 2.4.5

![New](../assets/new.svg) **New wrapper entity - [!DNL Columns] container introduced for column layouts** - Previously, users could add columns only inside another container/wrapper content type, such as a [!DNL Tab] or [!DNL Row]. Now, the [!DNL Column] has its own wrapper and can be added directly on stage. Also, the [!DNL Columns] container has a settings element where users can specify configuration for this wrapper entity.(PB-500)

![New](../assets/new.svg) **New menu options to duplicate, hide, and delete Columns groups** - With these new options, users can duplicate, hide, and delete [!DNL Columns] groups — just like they can with content types.(PB-507)

![New](../assets/new.svg) (Issue 594)**New multiline column support added to Column group** - With this addition, users can manipulate multiple lines of columns inside one [!DNL Columns] group to make help make column layouts much more flexible.(PB-108)

See [Layout - Column](./column.md) for information about using the new [!DNL Columns] group.

## 1.7.1 for Commerce 2.4.4

![Fixed issue](../assets/fix.svg) Page Builder is now compatible with PHP 8.1.(AC-1300)

![Fixed issue](../assets/fix.svg) Merchants can now add alternative text (`alt_text`) to images (Image, Banner, Slide) to enhance content accessibility.(PB-1193)

![Fixed issue](../assets/fix.svg) Admin users with permissions restricted to Content edit only no longer see an error when using Page Builder to add a product widget to a CMS page. Page Builder also displays an accurate product count on the widget settings page. Previously, Page Builder required permissions to the Catalog module when retrieving product count and displayed this error: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. (MC-42779)

![Fixed issue](../assets/fix.svg) Display issues with the Page Builder Format menu are now resolved with the TinyMCE 5 library upgrade. (AC-446)

![Fixed issue](../assets/fix.svg) You can now use the mouse to edit a **Text To Display** value in the Insert Link popup. (AC-982)

![Fixed issue](../assets/fix.svg) Page Builder now displays all options as expected on the Font Size options menu. Previously, not all options were displayed. (AC-1056)

![Fixed issue](../assets/fix.svg) Upgraded the `phpgt/dom` Composer dependency for the `magento/magento2-page-builder` extension to the latest versions. (magento/magento2-page-builder/pull/779)

![Fixed issue](../assets/fix.svg) Page Builder no longer resizes the Insert Link and Insert Image dialogs when displaying the slider in a small column. (AC-973)

![Fixed issue](../assets/fix.svg) The Page Builder Table Properties menu is now displayed as expected. (AC-407)

![Fixed issue](../assets/fix.svg) Slider dots are no longer displayed on the Insert link or image modal when the mouse is not hovering over the slider. (AC-406)
  
![Fixed issue](../assets/fix.svg) The font size used to display the Table menu options has been optimized. (AC-396)

![Fixed issue](../assets/fix.svg) Corrected anomalies with the positioning of the Insert/Edit Image and Insert/Edit Link dialogs. (AC-397)

![Fixed issue](../assets/fix.svg) Page Builder no longer throws an error when you click on **Text Editor** for a banner. (AC-398)

![Fixed issue](../assets/fix.svg) Page Builder no longer converts all dynamic blocks to one language during upgrade. (MC-42265)
  
## 1.6.0 for Adobe Commerce 2.4.2

![New](../assets/new.svg) (Issue 558)**New [!DNL Page Builder] styling** - [!DNL Page Builder] made massive improvements to how it styles content. The changes now make it easy to create simple CSS selectors to override the existing content type styles. These changes make it possible to create [!DNL Page Builder] themes with rich responsiveness for all content types.

![New](../assets/new.svg) (Issue 429)**Row container now optional** - You can now create content in [!DNL Page Builder] without requiring a Row container. In addition to the Row, the following content types can now be dragged and dropped directly on the stage: HTML, Block, Dynamic Block, Columns, and Tabs.

![New](../assets/new.svg) (Issue 636)**New responsive viewport switcher** - You can now preview your [!DNL Page Builder] content at different device widths (breakpoints) using the new Admin viewport switcher buttons above the stage. The viewport switcher simulates how your content is styled when displayed on the storefront using different devices.

![New](../assets/new.svg) (Issue 637)**New breakpoint-specific form fields** - Content type field values can now be set to specific viewport breakpoints. Icon indicators next to the fields show the viewport that the content type field value is applied to.

![New](../assets/new.svg) (Issue 559)**Removed predefined form field entries** - Advanced form settings for margins, paddings, and border-related properties (border, border width, and border radius) are now set as `default`, so that values can be defined by a module's CSS.

![New](../assets/new.svg) (Issue 635, 557, )**Added stage spacing** - Rows and Columns now provide extra spacing allowances around contained content types on the stage, but not on the storefront. The extra stage spacing makes it easier to access the mouseover option menus for both the container and contained content types.

![Fixed issue](../assets/fix.svg) (MC-37348)**Fixed auto-scrolling to reviews** - Auto-scrolling to product reviews on the storefront is now fixed.

![Fixed issue](../assets/fix.svg) (MC-36227)**Fixed cropped content** - Lengthy category and product descriptions are no longer cropped.

![Fixed issue](../assets/fix.svg) (MC-35402)**Fixed full-width, full-bleed Category content** - Category content can now be displayed in a full-width or full-bleed layout.

![Fixed issue](../assets/fix.svg) (MC-37989)**Security enhancements**

## 1.5.1 for Adobe Commerce 2.4.1-p1

![Fixed issue](../assets/fix.svg) (PB-1140, MC-38812)**Error display** - Fixed an issue in which [!DNL Page Builder] displayed an error when adding Catalog subcategories in the Admin.

## 1.5.0 for Adobe Commerce 2.4.1

![New](../assets/new.svg) (Issue 510, 511, 512, 513)**Immersive, full-screen editing** - Editing [!DNL Page Builder] content is now full-screen only for all areas controlled by [!DNL Page Builder]. This change includes CMS pages, Product and Category pages, Blocks, and Dynamic Blocks. Full-screen editing puts the focus on your content and provides a view that better matches the user experience on the storefront.

![New](../assets/new.svg) (Issue 544)**[!DNL Page Builder] content previews** - By default, [!DNL Page Builder] now provides content previews not only for CMS pages, Blocks, and Dynamic Blocks, but for Product and Category pages as well. You can configure this feature to be on or off for Product and Category pages using the new [!DNL Page Builder] Content Preview setting, accessed in the store configuration at Content Management > Advanced Content Tools.

![New](../assets/new.svg) (Issue 543)**Improved access to Product short descriptions** - By default, a Product short description is now displayed before the longer description. This change results in a match to the order that they appear on the storefront, and prevents the need to scroll through the longer description content to get access to the short description.

![New](../assets/new.svg) (Issue 419)**Prevented nested links in Banners and Slides** - Adding links to both the content and the outer elements of Banners and Slides created nested links which did not display or behave correctly on the storefront. To resolve the issue, links can no longer be added to *both* the Message Text area and the Link attribute for Banners and Slides.

![Fixed issue](../assets/fix.svg) (Issue 421) Fixed issue where setting empty border radius on a Tab Item caused errors and broke Tab Item content.

![Fixed issue](../assets/fix.svg) (Issue 422) Fixed issue where adding certain combinations of conditions to the Products Condition filter caused errors that prevented saving the Products form.

![Fixed issue](../assets/fix.svg) (Issue 425)Fixed issue in which the Slider content type did not behave correctly when the Infinite Loop setting was disabled.

![Fixed issue](../assets/fix.svg) (Issue 426)Fixed the Minimum Advertised Price so that it now works in [!DNL Page Builder].

![Fixed issue](../assets/fix.svg) (Issue 436)Fixed the issue in Safari and IE 11 that prevented dragging and dropping an Image to the upload area in Banners and Slides.

![Fixed issue](../assets/fix.svg) (Issue 525)Fixed the issue in which the Slider content type was not responsive in Firefox.

![Fixed issue](../assets/fix.svg) (Issue 567)Fixed the issue where the widget configuration was creating incorrect selectors in the DOM for the different appearances.

![Fixed issue](../assets/fix.svg) (Issue 609)Fixed the issue in which the Header toolbar hid the content type's option menu, which prevented access to the form and other options.

![Fixed issue](../assets/fix.svg) (Issue 612, 613)Fixed issues where Sliders and multiple rows using parallax backgrounds would not render correctly after toggling the full-screen mode several times.

![Fixed issue](../assets/fix.svg) <!--MC-35220)Fixed the issue where trying to copy the content from a Heading content type to a Text content type prevented [!DNL Page Builder] from saving.

![Fixed issue](../assets/fix.svg) (MC-34620)Fixed the Text content type to correctly handle and save non-Latin-1 characters.

![Fixed issue](../assets/fix.svg) (MC-34679)Fixed [!DNL Page Builder] CSS styles that caused Safari 13.1 to incorrectly render the Luma theme's site menu for small view ports and mobile screens.

![Fixed issue](../assets/fix.svg) (MC-34848)Fixed the HTML content type to correctly display embedded widgets like "Order by SKU" on the Storefront.

## 1.4.1 for Adobe Commerce 2.4.0-p1

![New](../assets/new.svg) (PB-590) Upgraded to TinyMCE 4. Removed TinyMCE 3 to improve security.

## 1.4.0 for Adobe Commerce 2.4.0

![New](../assets/new.svg) (PB-494)Added support for PHP 7.4.

![Fixed issue](../assets/fix.svg) (MC-31247)Fixed an issue where the Products content type did not show configurable products when the condition was set to price.

![Fixed issue](../assets/fix.svg) (PB-179)Fixed the Products alignment configuration to position only the product container itself, not the contents of the product container, such as the product name, price, buttons, images, and other elements.

![Fixed issue](../assets/fix.svg) (MC-33556)Performance improvements.

![Fixed issue](../assets/fix.svg) Security enhancements.

## 1.3.3-p1 for Adobe Commerce 2.3.6-p1

![Fixed issue](../assets/fix.svg) Security enhancements.

## 1.3.3 for Adobe Commerce 2.3.6

![Fixed issue](../assets/fix.svg) (MC-32766)Fixed the Text content type to correctly save the variable directives added to html attributes.

![Fixed issue](../assets/fix.svg) (MC-34590)Fixed the Text content type to correctly handle and save non-Latin-1 characters.

![Fixed issue](../assets/fix.svg) (MC-34677)Fixed [!DNL Page Builder] CSS styles that caused Safari 13.1 to incorrectly render the Luma theme's site menu for small view ports and mobile screens.

![Fixed issue](../assets/fix.svg) (MC-34846)Fixed the HTML content type to correctly display embedded widgets like _Order by SKU_ on the storefront.

![Fixed issue](../assets/fix.svg) Fixed an error that sometimes prevented users from saving content-type forms. The error ("[!DNL Page Builder] was rendering for 5 seconds without releasing locks") caused the loader icon to spin indefinitely after trying to save a form.

## 1.3.2 for Adobe Commerce 2.3.5-p2

![New](../assets/new.svg) Security enhancements.

## 1.3.1 for Adobe Commerce 2.3.5-p1

This version of [!DNL Page Builder] is just a version-number update for Adobe Commerce 2.3.5-p1. All features described for version 1.3.0 apply to this version as well.

## 1.3.0 for Adobe Commerce 2.3.5

![New](../assets/new.svg) **Templates** - [!DNL Page Builder] now has templates that can be created from existing content and applied to new content areas. [!DNL Page Builder] templates save both content and layouts of existing pages, blocks, dynamic blocks, product attributes, and category descriptions. For example, you can save an existing [!DNL Page Builder] CMS page as a template and then apply that template (with all its content and layouts) to quickly create CMS Pages for your site. This new feature is documented here: [Templates](templates.md).

![New](../assets/new.svg) **Video Backgrounds for Rows, Banners, and Sliders** - [!DNL Page Builder] Rows, Banners, and Sliders can now use videos for their backgrounds. These new features are documented here: [Rows](row.md), [Banners](banner.md), [Sliders](slider.md).

![New](../assets/new.svg) **Video support additions and enhancements** - [!DNL Page Builder] now supports a wider variety of video formats. In addition to YouTube and Vimeo videos, the Video content type and the video backgrounds now support video URL links to video formats like `.mp4` and other browser-supported formats. The Video content type also adds an auto-play feature. These new features are documented here: [Video content type](video.md).

![New](../assets/new.svg) **Full Height Rows, Banners, and Sliders** - [!DNL Page Builder] Rows, Banners, and Sliders can now set their heights to the full height of the page using a number with any CSS unit (px, %, vh, em) or a calculation between units (100vh - 237px). These new features are documented here: [Rows](row.md), [Banners](banner.md), [Sliders](slider.md).

![New](../assets/new.svg) **Content type upgrade library** - Developers can now create versions of [!DNL Page Builder] content types without introducing backward-incompatible issues with previous versions. Before this release, significant changes to content type configurations would create display and data-loss issues with previously saved [!DNL Page Builder] content types. The new upgrade library eliminates these issues. The library is designed to upgrade previous versions of content types saved to the database so that they match the configuration changes in the new versions. [!DNL Page Builder] runs the upgrade library on native content types as needed for a new release. This change ensures that the built-in [!DNL Page Builder] content types are always upgraded to match any changes made to content types for a newer release.

   >[!IMPORTANT]
   >
   >If you have created additional database entities for storing [!DNL Page Builder] content, you _must_ add those entities to your `etc/di.xml`. If you do not, the [!DNL Page Builder] content stored in your entity is not updated, causing potential data-loss and display issues. For example, if you have created a blog entity that stores [!DNL Page Builder] content, you must add your blog entity to your `etc/di.xml` file as an `UpgradableEntitiesPool` type so that the upgrade library can update the [!DNL Page Builder] content types used in your blog. For more information and instructions on using the upgrade library, see [Upgrade content types](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) in the _Page Builder Developer Guide_.

![New](../assets/new.svg) **Documentation for adding new appearances** - Developer information now published about [adding appearances](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) for existing or custom content types.

![Fixed issue](../assets/fix.svg) **Various fixes**

- (PB-50)Fixed an issue where the TinyMCE menu for slide content appears underneath other content types if the parent container of the slide is duplicated.
- (PB-166)Updated [!DNL Page Builder] to implement a destroy method to prevent memory leaks in some scenarios.
- (PB-170)Improved TinyMCE performance when multiple instances are used on the Admin stage.
- (PB-252)Fixed an issue in which the Dynamic Block content type does not render on the Admin stage if the top row is marked as hidden.
- (PB-273)Refined mouse-hover events on the Admin stage by removing a 200ms delay from various UI controls. This change makes it easier to work with nested content items on the stage.
- (PB-294)Fixed an issue in which the currency symbol was being escaped improperly in the Product List widget within the Block/Dynamic Block on the Admin stage.
- (PB-296)Fixed an issue in which the product total on the [!DNL Page Builder] edit panel did not work for custom MSI stock products.
- (PB-317)Fixed an issue in which saving [!DNL Page Builder] content with background images on Microsoft Edge does not render those images on the storefront.
- (PB-390)Fixed an issue in which nested [!DNL Page Builder] content fails to save if users click the Save button before the page fully renders.
- (PB-418)Fixed exception error thrown in cron jobs due to [!DNL Page Builder] analytics.

## 1.2.2 for Adobe Commerce 2.3.4-p2

![New](../assets/new.svg) Security enhancements.

## 1.2.1 for Adobe Commerce 2.3.4-p1

![New](../assets/new.svg) Security enhancements.

## 1.2.0 for Adobe Commerce 2.3.4

![New](../assets/new.svg)  **[!DNL Page Builder] integration with PWA Studio** - Added [!DNL Page Builder] content rendering to the Venia app in PWA Studio. [!DNL Page Builder] content can now be viewed within the PWA Studio Venia app. See the [!DNL Page Builder] documentation within [PWA Studio][] for all the information on this new feature.

![New](../assets/new.svg) **Added Product carousel** - (PB-77, PB-173, PB-175)The Products content type now provides an option to display your products in a carousel / slider format, including several options to customize the carousel to your needs.

![New](../assets/new.svg) **Added Product SKU sorting** - (PB-69)The Products content type now provides an option to sort your products by SKU in the order you add them to a list within the Admin.

![New](../assets/new.svg) **Added Product Category sorting** - (PB-181). The Products content type now provides an option to sort your products by category _position_, displaying them in same order that they appear within your Commerce Catalog.

![New](../assets/new.svg) **Added Product selection totals** - (PB-107). The Products content type Admin editor now displays the total number of products that match your product selection options.

![Fixed issue](../assets/fix.svg) **Various fixes**

- (PB-237)Security enhancements.
- (PB-41)Fixed searches within UI select components to make only one AJAX request per search term.
- (PB-76, PB-84)Updated Product previews in the Admin to match the storefront, including the star rating, color, and size options of the product when relevant.
- (PB-169)Fixed an issue in which [!DNL Page Builder] could not be saved when JavaScript minification and bundling are enabled in Commerce.
- (PB-241)Fixed the Admin previews of Products, Blocks, and Dynamic Blocks to render correctly on Commerce installations that define different URLs for the Admin and the frontend.
- (PB-238)Fixed the Admin previews of Products, Blocks, and Dynamic Blocks to render correctly on Commerce installations with B2B installed with the _Login Only_ option enabled. Before this fix, the [!DNL Page Builder] preview would cause the page to redirect to the customer account login.
- (PB-239)Fixed a session error that can occur when previewing a large page in the [!DNL Page Builder] Admin.
- (PB-248)Updated [!DNL Page Builder] LESS styles to prevent storefront style duplication.

## 1.1.1 for Adobe Commerce 2.3.3-p1

![New](../assets/new.svg) Security enhancements.

## 1.1.0 for Adobe Commerce 2.3.3

![New](../assets/new.svg) (MC-15250)Added explicit product sorting to the Products content type.

![New](../assets/new.svg) (MC-17823)Added buttons for inserting images, widgets, and variables in the HTML content type.

![Fixed issue](../assets/fix.svg) Improved [!DNL Page Builder] security.

![Fixed issue](../assets/fix.svg) (MC-1805)Updated [!DNL Page Builder] to support PHP version 7.3.

![Fixed issue](../assets/fix.svg) (MC-4137)Updated TinyMCE to version 4.9.5. This update, along with the additional improvements, fixed several TinyMCE inline editor issues:

- Variables, images, and image links are added where the cursor is place.
- Tables and table cells can be center aligned.
- Copy/paste now pastes content at the cursor position.
- Links can be applied to selected text.
- Bullets are properly aligned.
- Changes within the inline editor can be saved without first clicking outside the editor.

![Fixed issue](../assets/fix.svg) (MC-3880)Fixed an issue in which the minimum height and vertical alignment was inconsistent between sections on the edit panel for each content type.

![Fixed issue](../assets/fix.svg) (MC-14994)Fixed an issue in which the toolbar from the Heading content type was positioned incorrectly when first dropped on the stage.

![Fixed issue](../assets/fix.svg) (MC-15742)Fixed hard-coded margins in both Slider and Video content types.

![Fixed issue](../assets/fix.svg) (MC-16241)Fixed an issue in which the required asterisk symbol was displayed twice on form fields.

## 1.0.3 for Adobe Commerce 2.3.2-p2

![New](../assets/new.svg) Security enhancements.

## 1.0.2 for Adobe Commerce 2.3.2-p1

![New](../assets/new.svg) Security enhancements.

## 1.0.1 for Adobe Commerce 2.3.2

![New](../assets/new.svg) Ensures compatibility with Adobe Commerce 2.3.2.

## 1.0.0 for Adobe Commerce 2.3.1

![New](../assets/new.svg) General availability release


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
