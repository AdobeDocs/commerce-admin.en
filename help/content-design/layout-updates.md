---
title: Layout Updates
description: Learn how layout updates make it possible to customize the layout of a page.
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
---
# Layout Updates

Before you begin working with custom layout updates, it is important to understand how the pages of your store are constructed, and the difference between the terms *layout* and *layout update*. Layout refers to the visual and structural composition of the page. Layout update refers to a specific set of XML instructions that can override or customize how the page is constructed.

The XML layout of your [!DNL Commerce] store is a hierarchical structure of containers and blocks. Some elements appear on every page, and others appear only on specific pages. To learn more about layout, containers, and blocks, see [Layout overview][1] in the _Frontend Developer Guide_.

The [Widget](widgets.md) tool is an easy way to add an existing [content block](blocks.md) to the default layout of a page. For more advanced updates, you must save the XML layout update code on the server, and then reference the file as a custom layout update from the Admin. For an overview of the process, see [Use Layout Updates](layout-updates.md#place-a-block-using-layout-updates).

In the following diagram, the names that refer to containers are black and the block types, or block class paths, are blue.

![Standard block layout diagram](./assets/page-layout-default.png)<!-- zoom -->

|Block type|Description|
|--- |--- |
|`page/html`|The name of this block is `root` and it is one of the few root blocks in the layout. You can also create your own block and name it `root`, which is the standard name for blocks of this type. There can be only one block of this type per page.|
|`page/html_head`|The block name is `head` and it is a child of the root block. There can be only one block of this type per page and it must not be removed.|
|`page/html_notices`|The block name is `global_notices` and it is a child of the root block. If this block is removed from the layout, the global notices do not appear on the page. There can be only one block of this type per page.|
|`page/html_header`|The block name is `header` and it is a child of the root block. This block corresponds to the visual header at the top of the page and contains several standard blocks. There can be only one block of this type per page and it must not be removed.|
|`page/html_wrapper`|Although included in the default layout, this block is deprecated and is included only to ensure backward compatibility. Do not use blocks of this type.|
|`page/html_breadcrumbs`|The name of this block is `breadcrumbs` and it is a child of the header block. This block displays breadcrumbs for the current page. There can be only one block of this type per page. |
|`page/html_footer`|The block name is `footer` and it is a child of the root block. The footer block corresponds to the visual footer at the bottom of the page and contains several standard blocks. There can be only one block of this type per page and it must not be removed.|
|`page/template_links`|There are two blocks of this type in the standard layout. The `top.links` block is a child of the header block and corresponds to the top navigation menu. The `footer_links` block is a child of the footer block and corresponds to the bottom navigation menu. <br/><br/>**_Note:_** It is possible to manipulate the template links, as shown in the examples.|
|`page/switch`|There are two blocks of this type in a standard layout. The `store_language` block is a child of the header block and corresponds to the top language switcher. The `store_switcher` block is a child of the footer block and corresponds to the bottom store switcher.|
|core/messages|There are two blocks of this type in a standard layout. The `global_messages` block displays global messages. The `messages` block is used to display all other messages. If you remove these blocks, the customer does not see any messages.|
|`core/text_list`|This type of block is widely used throughout [!DNL Commerce] as a placeholder for rendering children blocks.|
|`core/profiler`|There is only one instance of this type of block per page. It is used for the internal [!DNL Commerce] profiler and should not be used for any other purpose.|

{style="table-layout:auto"}

## Place a Block Using Layout Updates

[Layout updates](layout-updates.md) make it possible to customize the layout of a page. Layout updates offer more flexibility than a [widget](widgets.md), but require access to the server and a basic knowledge of XML.

The following steps show how to use a layout update to place a block on a page. For specific examples and help with syntax, see [Common layout customization tasks][4] in the _Frontend Developer Guide_.

### Step 1: Create the block

1. Create the [block](block-add.md) that you want to place.

1. Take note of the `block_id`, because it is used in the layout update instructions.

### Step 2: Compose the layout update in XML

1. Compose the layout instructions in XML to [Reference a CMS Block][3].

1. Save the [layout instructions][2] on the server in the layout folder where XML files are saved for the theme.

   For example:

   `<theme_dir>/<Namespace>_<Module>/layout`

   The [layout handle][4] is the filename that begins with `cms_page_view_selectable_`, followed by the URL key of the CMS page, the layout update option, and the `xml` file suffix. In the following example, `customer-service` is the URL key of the page, and `ChatTool` is the option that you select to apply the layout update to the page.

   `cms_page_view_selectable_`<`customer-service`>`_`<`ChatTool`>`.xml`

   |Element|Description|
   |--- |--- |
   |CMS Page Identifier|The URL key of the page with any forward slash (`/`) replaced by an underscore (`_`).|
   |Layout Update Name|The option that appears in the _Custom Layout Update_ list.|

   {style="table-layout:auto"}   

### Step 3: Reference the layout update from the page

1. On the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Elements]_ > **[!UICONTROL Pages]**.

1. Find the page where you want to place the block and open it in edit mode.

1. Scroll down and expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL Design]** section.

1. To display all available layout updates that are associated with the page, click **Custom Layout Update** arrow.

   ![Custom Layout Update list](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. Select the layout update that you want to apply to the page.

### Step 4: Save and refresh cache

1. When complete, click **[!UICONTROL Save & Close]**.

1. In the message at the top of the workspace, click **[!UICONTROL Cache Management]** and refresh each invalid cache.

[1]: https://developer.adobe.com/commerce/frontend-core/guide/layouts/
[2]: https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/
[3]: https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/
[4]: https://developer.adobe.com/commerce/frontend-core/guide/layouts/
