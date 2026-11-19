# Policies

Policies define filters that are applied to products in a catalog view. They help tailor the product assortment returned to a storefront or channel. This ensures that the right content is delivered to the right destination. For example, physical stores, marketplaces, and advertising channels like Google, Facebook, and Instagram.

Policies use product attributes like brand, model, or part category to tailor catalog data to business requirements. ​

## Access the Policies workspace

How you open the *Policies* workspace depends on the product you use:

- **Adobe Commerce Admin** (Adobe Commerce as a Cloud Service)—Select *Catalog* > **Policies**.
- **Adobe Commerce Optimizer Studio**—Select *Store setup* > **Policies**.

## Filters

Filters define attribute-based conditions that determine which products match a policy. When associated with a catalog view, a policy helps tailor the products returned for that view. Use product attributes, operators, and values to define the matching conditions.

### Parts of a filter

A filter is composed of the following parts:

|Part|Description|Example|
|---|---|---|
|**Attribute**|The product attribute used for filtering.|`part_category`|
|**Operator**|The condition applied to the attribute.|`IN`, `EQUALS`, `CONTAINS`|
|**Value source**|Specifies whether the values are `STATIC` or `TRIGGER`.|`STATIC` [Learn more](#value-source-types)|
|**Value**|The specific values that meet the condition.|`brakes, suspension`|

### Example

A filter on `part_category` using the `IN` operator with values `brakes` and `suspension` matches products whose `part_category` is either value.

### Value source types

There are two types of value sources: **STATIC** and **TRIGGER**.

Policies with a **Value source** of **STATIC** are considered universal policies. Universal policies define the experience of a website as a whole. This means that the catalog view always executes that policy. The policy execution does not depend on storefront user interaction.

Policies with a **Value source** of **TRIGGER** are referred to as exclusive policies. This means that the catalog view executes that policy only when the trigger is specified in the header of the API call. On the storefront, this means information is displayed based on what the shopper selects. For example, in the following image, there are two drop-down menus: **Brand** and **Model**.

![Trigger value source on storefront](/help/assets/ccdm-shared/setup/policy-trigger.png)

**Brand** and **Model** are defined triggers:

- `AC-Policy-Brand`
- `AC-Policy-Model`

If the shopper clicks the Model drop-down, the header of the API call contains `AC-Policy-Model`, which is configured to show only products specific to the `AC-Policy-Model` policy.

### Multi-value HTTP header triggers {#multi-value-http-header-triggers}

A trigger policy using the `HTTP_HEADER` transport type can receive multiple values in a single header. The values must be separated with commas and the filter operator must be `IN`. Each value is treated as an acceptable match. The values are evaluated with `OR` semantics.

For example, a policy filter using `IN` with the following header:

```
AC-Policy-Vehicle: UNIVERSAL,veh-bolt-mammoth-limited-2025
```

matches products whose `vehicle` attribute is either `UNIVERSAL` or `veh-bolt-mammoth-limited-2025`.

Whereas a filter operator of `EQUALS`, `GREATER_THAN_EQUAL`, or `LESS_THAN_EQUAL` is rejected with a validation error.

#### Syntax notes

- The header name matches the trigger name you configure, for example `AC-Policy-Vehicle`.
- Commas separate individual values within the header. When the same `AC-Policy-_Name_` header appears more than once, its values combine into a single comma-separated header value
- The filter operator is `IN`.
- A policy filter with **Value source** set to `TRIGGER`.
- A trigger whose **Transport type** is `HTTP_HEADER`.

## Create policy

In this section, you create a new policy. The policy can be either **STATIC** or **TRIGGER**.

### Create a STATIC policy

1. From the **[!UICONTROL Policies]** workspace, click the **[!UICONTROL Add Policy]** button.

    A new page opens for you to fill in the policy details. ​

1. Enter the name of the policy, for example "Celport Part Categories".

1. Click the **[!UICONTROL Add Filter]** button.

    A dialog opens for you to add filter details.

1. Add the filter details. For example:

    1. **Attribute** - Enter an attribute from your catalog. For example, "part_category". This name must exactly match the name of the attribute in your catalog.
    1. **Operator** - Choose the operator. For example, **IN**. ​
    1. **Value Source** - Select **STATIC**. ​
    1. **Value** - Enter a value from the attribute definition that you previously specified. For example, enter "brakes" to create a filter for brake parts.
    1. To save the value, press **Enter**.

       If the policy is designed to filter by multiple values, enter each value separately.

1. Click the **[!UICONTROL Save]** button in the filter details dialog. ​

1. Click the menu icon (...) next to the filter you created and select **Enable**. From here, you can also **Edit**, **Disable**, or **Delete** the filter.

    The **Status** column shows a green icon and the word "Enabled".

1. Click the **[!UICONTROL Save]** button to save the new policy.​ If the button is not active, ensure that the policy name is added by clicking the pencil icon next to **New Policy**.

1. To verify your new policy, click the back arrow to return to the **[!UICONTROL Policies]** workspace.

### Create a TRIGGER policy

1. From the **[!UICONTROL Policies]** workspace, click the **[!UICONTROL Add Policy]** button.

    A new page opens for you to fill in the policy details. ​

1. Enter the name of the policy, for example "Celport Part Categories".

1. Click the **[!UICONTROL Add Trigger]** button.

    The **Trigger details** dialog appears.

1. Enter a name for the trigger, such as **AC-Policy-Brand**.

1. Select the **Transport type**. **HTTP_HEADER** is currently the only type supported.

1. Click the **[!UICONTROL Save]** button to save the trigger.

1. Click the **[!UICONTROL Add Filter]** button.

    A dialog opens for you to add filter details.

1. Add the filter details. For example:

    1. **Attribute** - Enter an attribute from your catalog. For example, "part_category". This name must exactly match the name of the attribute in your catalog.
    1. **Operator** - Choose the operator. For example, **IN**. ​
    1. **Value Source** - Select **TRIGGER**. ​
    1. **Value** - Enter the trigger name you created previously (**AC-Policy-Brand**).

    At configuration time, the filter references the configured trigger. At runtime, the API request's header supplies the value or values evaluated by that filter.

1. Click the **[!UICONTROL Save]** button in the filter details dialog. ​

1. Click the menu icon (...) next to the filter you created and select **Enable**. From here, you can also **Edit**, **Disable**, or **Delete** the filter.

    The **Status** column shows a green icon and the word "Enabled".

1. Click the **[!UICONTROL Save]** button to save the new policy.​ If the button is not active, ensure that the policy name is added by clicking the pencil icon next to **New Policy**.

1. To verify your new policy, click the back arrow to return to the **[!UICONTROL Policies]** workspace.

Following these steps creates the policy that can then be linked to a catalog view to control product visibility.
