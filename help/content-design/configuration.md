---
title: Design Configuration
description: Placeholder
---
# Design Configuration

The Design Configuration makes it easy to edit design-related rules and configuration settings by displaying the settings on a single page.

![Design Configuration page](./assets/configuration.png)<!-- zoom -->

## Change the design configuration

1. On the _Admin_ sidebar, go to **Content** > _Design_ > **Configuration**.

1. Find the store view that you want to configure and click **Edit** in the _Action_ column.

   The page displays the current design settings for the store view.

1. To change the default theme, set **Applied Theme** to the theme that you want to apply to the view.

   If no theme is specified, the system default theme is used. Some third-party extensions modify the system default theme.

1. If the theme is to be used for only a specific device, set the **User Agent Rules**.

   ![User-Agent Rules](./assets/configuration-user-agent-rules.png)<!-- zoom -->

   For each device type where you want to specify a theme:

   - Click **Add New User Agent Rule**.

   - For **Search String**, enter the browser ID for the specific device.

      A search string can be either a normal expression or Perl Compatible Regular Expression (PCRE). To learn more, see [User Agent][1]. The following search string identifies Firefox:

            /^mozilla/i

   - For **Theme Name**, choose the theme to be used for the specified device.

   >[!NOTE]
   >
   >You can add as many rules for the devices you want to designate. The search strings are matched in the order they are entered.

1. Under _Other Settings_, expand each section and follow the instructions in the linked topics to edit the settings as needed.

   - [Pagination](https://docs.magento.com/user-guide/catalog/navigation-pagination.html)
   - [HTML Head](page-setup.md#html-head)
   - [Header](page-setup.md#header)
   - [Footer](page-setup.md#footer)
   - [Search Engine Robots](https://docs.magento.com/user-guide/marketing/search-engine-robots.html)
   - [Product Image Watermarks](https://docs.magento.com/user-guide/catalog/product-image-watermarks.html)
   - [Transactional Emails](https://docs.magento.com/user-guide/marketing/email-template-configuration.html)

   ![Other settings to affect design](./assets/configuration-other-settings.png)<!-- zoom -->

1. When complete, click **Save Configuration**.

[1]: https://en.wikipedia.org/wiki/User_agent
