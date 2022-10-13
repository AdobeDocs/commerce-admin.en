---
title: Terms and conditions for checkout
description: <Add description here>
---
# Terms and conditions for checkout

When manual _Terms and Conditions_ functionality is enabled, customers are required to agree to the terms and conditions of the sale before the purchase is finalized. The Terms and Conditions of the sale typically includes disclosure information that might be required by law for B2C or B2B sites, and outlines the rights of the buyer and seller. The Terms and Conditions message appears after the payment information, just before the _Place Order_ button.

![Terms and Conditions at checkout](./assets/storefront-checkout-step2-terms-conditions.png)<!-- zoom -->

## Step 1: Enable terms and conditions for checkout

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the left panel, expand **Sales** and choose **Checkout**.

1. Expand ![Expansion selector](../assets/icon-display-expand.png) the **Checkout Options** section.

   ![Checkout Options](./assets/checkout-terms-options.png)<!-- zoom -->

1. Verify that **Enable Onepage Checkout** is set to `Yes`.

1. Set **Enable Terms and Conditions** to `Yes`.

1. Click **Save Config**.

## Step 2: Add your own terms and conditions information

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Terms and Conditions**.

   ![Terms and Conditions grid](./assets/terms-conditions.png)<!-- zoom -->

1. In the upper-right corner, click **Add New Condition**.

   ![New Condition](./assets/terms-conditions-new.png)<!-- zoom -->

1. Enter the **Condition Name** for internal reference.

1. Set **Status** to `Enabled`.

1. Set **Applied** to `Automatically` or `Manually`.

   - `Automatically` - Conditions are automatically accepted upon checkout.
   - `Manually` - Customers are required to manually accept the conditions to place an order.

1. Set **Show Content as** to one of the following:

   - `Text` - Displays the terms and conditions content as unformatted text.
   - `HTML` - Displays the content as HTML which can be formatted.

1. Select each **Store View** where you want these Terms and Conditions to be used.

1. Scroll down and complete the information to be displayed:

   - Enter the **Checkbox Text** to be used as the text for the Terms and Conditions link. For example, `I understand and accept the terms and conditions of the sale`.

   - In the **Content** box, enter the full text of the terms and conditions of the sale.

1. (Optional) Enter the **Content Height (css)** in pixels to determine the height of the text box where the terms and conditions statement appears during checkout.

   For example, to make the text box 1 inch high on a 96-dpi display, enter `96`. A scroll bar appears if the content extends beyond the height of the box.

1. Click **Save Condition**.
