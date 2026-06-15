---
title: Returns attribute
description: Learn about the returns attributes and how to create the attributes needed for processing returns on your store.
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
TQID: https://experienceleague.adobe.com/bKSZbmmyG9CWVIf0GzCgGImzHRIUV8HgD6asutC7lFo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Returns attribute

{{ee-feature}}

The returns attributes are used to store information that is needed during the product return process. The default attributes include the condition of the returned product, the reason for the return, and a field that indicates how the return was resolved. The process to create a returns attribute is similar to creating a [customer attribute](../customers/attribute-properties.md).

![Admin - Returns attributes](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Create a returns attribute

1. On the _Admin_ sidebar, go to **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_ > **[!UICONTROL Returns]**.

1. In the upper-right corner, click **[!UICONTROL Add New Attribute]**.

   ![New Return - attribute properties](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Define the properties

1. To identify the attribute during data entry, set the **[!UICONTROL Default Label]**.

1. For **[!UICONTROL Attribute Code]**, enter a code that identifies the attribute within the system.

1. To determine the type of input control that is used for data entry, set **[!UICONTROL Input Type]** to one of the following:

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. To make the field a required item, set **[!UICONTROL Values Required]** to `Yes`.

1. To assign an initial value to the field, enter a **[!UICONTROL Default Value]**.

1. To validate the data entered into the field for accuracy before the record is saved, set **[!UICONTROL Input Validation]** to one of the following:

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. For the `Text Field` and `Text Area` input types, enter the **[!UICONTROL Minimum Text Length]** and **[!UICONTROL Maximum Text Length]**.

1. To apply a preprocessing filter, set **[!UICONTROL Input/Output Filter]** to one of the following:

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. To make the attribute visible to customers, set **[!UICONTROL Show on Storefront]** to `Yes` in the _[!UICONTROL Storefront Properties]_ section.

1. (Optional) For **[!UICONTROL Sort Order]**, enter a number to determine where this attribute appears relative to the others in the same part of the page. (`0` = first, `1` = second, `2` = third, and so on.)

### Manage the labels/options

1. In the left panel, choose **[!UICONTROL Manage Labels/Options]**.

1. In the **[!UICONTROL Manage Titles (Size, Color, etc.)]** section, enter the label for each store view.

   ![Manage labels](./assets/return-attributes.png){width="600" zoomable="yes"}

1. If the **[!UICONTROL Input Type]** for the attribute is `Dropdown`, manage the options in the **[!UICONTROL Manage Options (Values of Your Attribute)]** section.

   - To add an option, click **[!UICONTROL Add Option]** and enter the label for Admin and each store view.
   - To make an option the selected default, choose **[!UICONTROL Is Default]**.
   - To remove an option, click **[!UICONTROL Delete]**.

1. To save changes, click **[!UICONTROL Save Attribute]**.
