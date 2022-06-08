---
title: Create and Manage Widgets
description: Placeholder
---
# Create and Manage Widgets

Widgets are reusable components and you can easily create new widgets, as well as modify existing ones to automatically update content across your store. You can also delete widgets that are no longer in use.

![Widgets](./assets/widgets.png)<!-- zoom -->

## Create a widget

The process of creating a widget is nearly the same for each [widget type](widgets.md#widget-types). You can follow the first part of the instructions, and then complete the last part for the specific type of widget you want.

### Step 1: Choose the type

1. On the _Admin_ sidebar, go to **Content** > _Elements_ > **Widgets**.

1. Click **Add Widget**.

1. In the _Settings_ section:

   - Set **Type** to the widget type that you want to create.

   - Verify that **Design Theme** is set to the current theme.

   ![Widget settings](./assets/widget-settings.png)<!-- zoom -->

1. Click **Continue**.

### Step 2: Specify storefront properties and layout

1. In the _Storefront Properties_ section:

   - For **Widget Title**, enter a descriptive title for the widget.

      This title is visible only from the Admin.

   - For **Assign to Store Views**, select the store views where the widget will be visible.

      You can select a specific store view, or `All Store Views`. To select multiple views, hold down the Ctrl key (PC) or the Command key (Mac) and click each option.

   - (Optional) For **Sort Order**, enter a number to determine the order this item appears with others in the same part of the page. (`0` = first, `1` = second, `3` = third, and so on.)

   ![Storefront properties](./assets/widget-storefront-properties.png)<!-- zoom -->

1. In the _Layout Updates_ section, click **Add Layout Update**.

1. Set **Display On** to the type of page where it is to appear.

1. In the **Container** list, choose the area of the page layout where it is to be placed.

   ![Layout updates](./assets/widget-layout-update-home-page.png)<!-- zoom -->

1. If the widget is a link, set **Template** to one of the following:

   | Block Template | Formats the content so it can be placed as standalone unit on the page. |
   | Inline Template | Formats the content so it can be placed inside other content. For example, a link that goes inside a paragraph of text. |

### Step 3: Complete the widget options

The options for each widget type vary slightly, but the process is essentially the same. The following example displays the product list for a specific category, with pagination controls.

1. In the left panel, choose **Widget Options**.

1. Click **Select Block**.

1. Enter a **Title** to appear above the list, such as `Featured Products`.

1. For pagination controls, set **Display Page Control** to `Yes`  and do the following:

   - Enter the **Number of Products per Page**.

   - Enter the total **Number of Products to Display**.

   - Set **Condition** to the category of products to be featured.

      The process is the same as setting a condition for a [price rule](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html).

   ![Widget options](./assets/widget-options-new-product-list.png)<!-- zoom -->

### Step 4: Save and check the result

1. When complete, click **Save**.

1. When prompted, follow the instructions at the top of the workspace to update the cache, as needed.

1. Return to your storefront to verify that the widget is working correctly.

   To move it to a different location, you can reopen the widget and try a different page or block reference.

## Edit a widget

1. On the _Admin_ sidebar, go to **Content** > _Elements_ > **Widgets**.

1. Locate the widget using filters above the grid and click the widget name.

1. Make needed changes.

   Review the steps for creating a widget for information about the widget options.

1. Click the **Save**.

## Delete a widget

1. On the _Admin_ sidebar, go to **Content** > _Elements_ > **Widgets**.

1. Locate the widget using filters above the grid, select the checkbox of the widgets to be deleted.

1. In the upper-left corner of the list, set **Actions** to `Delete`.

1. When complete, click **Submit**.

1. To confirm the action, click **OK**.
