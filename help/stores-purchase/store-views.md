---
title: Store views
description: Learn how to add and edit a store view.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
---
# Store views

Store views are typically used to make the store available in different locales. Shoppers can use the language chooser in the header of the store to change the store view.

![Scope - multiple store views](./assets/scope-multiview.svg)<!-- {:width="550px"} -->

## Add a store view

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Settings]_ > **[!UICONTROL All Stores]**.

   ![All Stores](./assets/stores-all.png)<!-- zoom -->

1. Click **[!UICONTROL Create Store View]**.

   ![Create store view](./assets/create-store-view.png)<!-- zoom -->

1. Set **[!UICONTROL Store]** to the parent store of this view.

1. Enter a **[!UICONTROL Name]** for this store view.

   The name appears in the language chooser in the store header. For example: `Spanish`.

1. Enter a **[!UICONTROL Code]** in lowercase characters to identify the view. For example: `spanish`.

1. To activate the view, set **[!UICONTROL Status]** to `Enabled`.

1. (Optional) Enter a **[!UICONTROL Sort Order]** number to determine the sequence in which this view is listed with other views.

1. Click **[!UICONTROL Save Store View]**.

## Edit a store view

Because the view name appears in the language chooser, you might eventually want to change the name of the default view to something more descriptive. The _Name_ field is simply a label and can be easily changed.

If your Adobe Commerce or Magento Open Source installation has a multisite or multi-store setup, do not change the store Code field without verifying that the value is not referenced in the `index.php` file. If you do not have access to the server to examine the file, ask a developer for help.

| Field | Original value | Updated value |
| ----- | -------------- | ------------- |
| [!UICONTROL Name]  | `Default Store View` | `English` |
| [!UICONTROL Code]  | `default` | `english` |

{style="table-layout:auto"}

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** >  _[!UICONTROL Settings]_ > **[!UICONTROL All Stores]**.

1. In the _[!UICONTROL Store View]_ column of the grid, click the name of the view that you want to edit.

   When editing the default view, the _[!UICONTROL Store]_ and _[!UICONTROL Status]_ fields are not available.

   ![Store view - edit default view](./assets/edit-store-view-info.png)<!-- zoom -->

1. Update the following fields as needed:

    - **[!UICONTROL Store]** (non-default views only)
    - **[!UICONTROL Name]**
    - **[!UICONTROL Code]** (only if not used in `index.php`)
    - **[!UICONTROL Status]** (non-default views only)
    - **[!UICONTROL Sort Order]**

1. Click **[!UICONTROL Save Store View]**.

   ![Stores](./assets/all-grid.png)<!-- zoom -->
