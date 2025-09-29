---
title: Transfer a Commerce account
description: Learn how to transfer your Commerce account to another owner or email address.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
---
# Transfer a Commerce account

As business responsibilities change, you might need to transfer your Commerce account to a new owner or to another email address. This transfer requires a change to the primary user email associated with the account. 

The following information describes the process for transferring a Commerce (MAGEID) account. It does not include changes for Cloud account (Cloud project or New Relic) ownership. For more information about cloud project access, see [Manage user access](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) in the _Commerce on Cloud Infrastructure Guide_.

>[!IMPORTANT]
>
>If the new account owner has purchased extensions using Shared Access, access to those extensions is lost as soon as the Account Transfer process has been initiated. Before requesting the account transfer, make sure that the new owner retrieves the Order IDs for the purchases from [their Marketplace account](https://commercemarketplace.adobe.com/sales/order/history/) and requests a refund for those extensions from the [Marketplace team](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). It is not possible to transfer extension purchases to a different account.

## Identify your transfer type

The type of Commerce account transfer depends on the Commerce account credentials available to the current owner and the new owner. The following scenarios describe the different transfer types based on these credentials.

| Transfer type | Current owner | New owner |
| ------------- | ------------- | --------- |
| [New Adobe ID and email change](#new-adobe-id-and-email-change) | Has a MAGEID that **_has not been connected_** with an Adobe login account | Does not have a MAGEID and is not connected to an Adobe login account. | 
| [Email change](#email-change) | Has a MAGEID that is **_connected_** with an Adobe login account. | Has an Adobe login account, but **_does not have a MAGEID_** connected with an Adobe login account. |
| [Adobe ID switch](#adobe-id-account-switch) | Has a MAGEID that is **_connected_** with an Adobe login account. | Has a MAGEID and is connected to an Adobe login account. |

{style="table-layout:auto"}

>[!NOTE]
>
>As Adobe Commerce continues to integrate with other Adobe solutions, a Commerce account (MAGEID) now requires an association with an Adobe login. This Adobe ID uses the same email address connected to your Commerce account.

## New Adobe ID and email change

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and make sure that you meet the preconditions for this sequence of steps.

This transfer type requires having an Adobe ID that's linked to the existing Commerce account, and then changing that account to the email address for the new owner.

1. Go to the [Commerce account login](https://account.magento.com/customer/account/login/) page.

1. Click **[!UICONTROL Sign in with Adobe ID]**.

1. Click **[!UICONTROL Create an account]**.

1. Enter the email address of the current owner and a password.

1. Click **[!UICONTROL Continue]**.

   This step creates an Adobe ID and links it to the current Commerce account (MAGEID). With this account link, the _[!UICONTROL Email]_ field is blocked from any changes. The configuration of the associated email address is managed from the Adobe ID account.

1. Navigate to [account.adobe.com](https://account.adobe.com/).

1. Click **[!UICONTROL Change Email]**.

1. Enter the new owner's email address.

1. Click **[!UICONTROL Change]**.

   This step generates a verification email sent to the new email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the new email address.

1. Click **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## Email change

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and make sure that you meet the preconditions for this sequence of steps.

This transfer type results in the current account owner losing access to other Adobe products.

1. Navigate to [account.adobe.com](https://account.adobe.com/) and complete the Adobe login.

1. Under your account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter the new owner's email address.

1. Click **[!UICONTROL Change]**.

   This step generates a verification email sent to the new email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the new email address.

1. Click **[!UICONTROL Verify]**.

## Adobe ID account switch

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and make sure that you meet the preconditions for this sequence of steps.

In the case where the current owner and new owner have existing Adobe IDs, and both accounts should remain, but email addresses need to be switched between them. This requires the use of a _temporary_ email address that is valid, but is not associated with an Adobe ID.

### Change to a temporary account

The current owner completes these steps to associate their Adobe ID with another, temporary email address.

1. Navigate to [account.adobe.com](https://account.adobe.com/) and complete the Adobe login.

1. Under your account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter a valid temporary email address that is not used by an Adobe ID.

   You must have access to the email address so that you can retrieve the email with the confirmation code. 

1. Click **[!UICONTROL Change]**.

   This step generates a verification email sent to the temporary email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the temporary email address.

1. Click **[!UICONTROL Verify]**.

1. Log out of the Adobe account.

### New owner steps

After the current owner completes the transfer to a temporary email address, the new owner must complete these steps to change their account configuration to point to the current owner's original email address.

1. Navigate to [account.adobe.com](https://account.adobe.com/) and complete the Adobe login.

1. Under your account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter the current owner's original email address.

1. Click **[!UICONTROL Change]**.

   This step generates a verification email sent to the current owner's original email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the current owner's original email address.

1. Click **[!UICONTROL Verify]**.

1. Log out of the Adobe account.

### Follow up steps

After the new owner successfully configures their Adobe account with the original email address of the current (now previous) owner, complete these steps to transfer ownership.

1. Navigate to [account.adobe.com](https://account.adobe.com/), and complete the Adobe login using the email address for the [temporary account](#change-to-a-temporary-account).

1. Under the account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter the new owner's email address.

1. Click **[!UICONTROL Change]**.

   This step generates a verification email sent to the new owner's email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the new owner's email address.

1. Click **[!UICONTROL Verify]**.

>[!IMPORTANT]
>
>Submit a Support request to inform the Support team that you have updated the account owner's email address. The team must perform additional steps to complete the update such as updating the email address on your [Commerce Marketplace](https://commercemarketplace.adobe.com/) profile. Include the previous account owner's email address in your request.
