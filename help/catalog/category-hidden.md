---
title: Hidden categories
description: Learn how to use hidden categories for internal purposes or to link to a category that is not included in the navigation menu.
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
TQID: https://experienceleague.adobe.com/vXJFiYxeTBcRQxdc4XGrPEPKuBAcqr-mnuUlh1WIskM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
    internal-label: Categories
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Hidden categories

There are many ways to use hidden categories. You might want to create additional category levels for your own internal purposes, but show only the higher-level categories to your customers. Or, you might want to link to a category that is not included in the navigation menu.

## Create hidden categories

1. On the _Admin_ sidebar, go to **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. In the category tree, select the category you want to hide and do the following:

   - Set **[!UICONTROL Is Active]** to `Yes`.
   - Set **[!UICONTROL Include in Menu]** to `No`.

1. In the **[!UICONTROL Display Settings]** section, set **[!UICONTROL Anchor]** to `No`.

   ![Hidden category](./assets/hidden-categories.png){width="600" zoomable="yes"}

   The hidden category is active, but does not appear in the top menu, or in layered navigation.

1. Complete the following settings for each hidden subcategory to create subcategories:

   >[!NOTE]
   >
   >Although the category is hidden, you can create subcategories beneath it and make them active.

   - Set **[!UICONTROL Enable Category]** to `Yes`.
   - In the **[!UICONTROL Display Settings]** section, set **[!UICONTROL Anchor]** to `Yes`.

   As active categories, you can now link to them from other places in your store, but they do not appear in the menu.

1. When complete, click **[!UICONTROL Save]**.
