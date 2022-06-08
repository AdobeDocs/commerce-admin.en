---
title: The Default Theme
description: Placeholder
---
# The Default Theme

The _Magento Blank_ responsive theme renders the display of your storefront for different devices and incorporates best practices for desktop, table, and mobile devices. Some themes are designed to be used only with specific devices. When Commerce detects a specific browser ID, or user agent, it uses the theme that is configured to be used for the specific browser. The search string can also include Perl-Compatible Regular Expressions (PCRE). To learn more, see [User Agent][1].

![Themes](./assets/themes.png)<!-- zoom -->

## Filter the theme grid

1. On the _Admin_ sidebar, go to **Content** > _Design_ > **Themes**.

1. Click **Filters**.

1. Enter an ID range, theme name (or title), folder path, or parent theme.

1. Click **Apply Filters** to update the list of themes.

## View the current theme settings

1. On the _Admin_ sidebar, go to **Content** > _Design_ >  **Themes**.

1. In the list of installed themes, find the theme that you want to examine and click the row to display the settings.

1. To view a sample page, click the **Theme Preview Image**.

![Preview theme](./assets/theme-settings.png)<!-- zoom -->

## Apply a default theme

1. On the _Admin_ sidebar, go to **Content** > _Design_ >  **Configuration**.

1. Find the store view that you want to configure and click **Edit** in the _Action_ column.

1. Under _Default Theme_, set **Applied Theme** to the one that you want to use for the current view.

   ![Applied Theme](./assets/theme-default-apply.png)<!-- zoom -->

1. When complete, click **Save Configuration**.

## Add a user agent rule

1. On the _Admin_ sidebar, go to **Content** > _Design_ >  **Configuration**.

1. Under _Design Rule_, click **Add New User Agent Rule**.

   ![Design Rule](./assets/theme-design-rule.png)<!-- zoom -->

1. For **Search String**, enter the browser ID for the specific device.

   Search strings are matched in the order they are entered. For example, for Firefox enter:

    `/^mozilla/i`

1. Repeat the process to enter additional devices.

1. When complete, click **Save Configuration**.

[1]: https://en.wikipedia.org/wiki/User_agent
