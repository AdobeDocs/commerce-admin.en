---
title: Transfer a Commerce account
description: Learn how to transfer your Commerce account to another owner or email address.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
---
# Transfer a Commerce account

As business responsibilities change, you might need to transfer the ownership of your existing Commerce account to a new owner or to another email address. This transfer requires a change to the primary user email associated with the account. 

The following information describes the process for transferring a Commerce (MAGEID) account. It does not include changes for Cloud account (Cloud project or New Relic) ownership. For more information about cloud project access, see [Manage user access](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) in the _Commerce on Cloud Infrastructure Guide_.

## Identify your transfer type

How you complete this transfer depends on which of the following scenarios describes your situation as the current owner of the account and the new owner (email address) to whom you want to transfer the account:

| Transfer type | Current owner | New owner |
| ------------- | ------------- | --------- |
| [New Adobe ID and email change](#new-adobe-id-and-email-change) | Has a MAGEID that is **_not connected_** with an Adobe login account. | Does not have a MAGEID and is not connected to an Adobe login account. | 
| [Email change](#email-change) | Has a MAGEID that is **_connected_** with an Adobe login account. | Does not have a MAGEID and is not connected to an Adobe login account. |
| [Adobe ID switch](#adobe-id-account-switch) | Has a MAGEID that is **_connected_** with an Adobe login account. | Has a MAGEID and is connected to an Adobe login account with no other Adobe products/services associated. |

{style="table-layout:auto"}

>[!NOTE]
>
>As Adobe Commerce continues to integrate with other Adobe solutions, a Commerce account (MAGEID) now requires an association with an Adobe login. This Adobe ID uses the same email address connected to your Commerce account.

## New Adobe ID and email change

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and make sure that you meet the preconditions for this sequence of steps.

This transfer type requires that you first create an associated Adobe ID and then change that account to the email address for the new owner.

1. Go to your [Commerce account](https://account.magento.com/customer/account/login/).

1. Click **[!UICONTROL Sign in with Adobe ID]**.

1. Click **[!UICONTROL Create an account]**.

1. Enter the email address of the current owner and a password.

1. Click **[!UICONTROL Continue]**.

   This creates an Adobe ID and links it to the current Commerce account (MAGEID). With this account link, the _[!UICONTROL Email]_ field is blocked from any changes. The associated email address is managed by the Adobe ID account.

1. Navigate to [account.adobe.com](https://account.adobe.com/).

1. Click **[!UICONTROL Change Email]**.

1. Enter the new owner's email address.

1. Click **[!UICONTROL Change]**.

   This generates a verification email sent to the new email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the new email address.

1. Click **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## Email change

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and make sure that you meet the preconditions for this sequence of steps.

1. Navigate to [account.adobe.com](https://account.adobe.com/) and complete the Adobe login.

1. Under your account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter the new owner's email address.

1. Click **[!UICONTROL Change]**.

   This generates a verification email sent to the new email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the new email address.

1. Click **[!UICONTROL Verify]**.

## Adobe ID account switch

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and make sure that you meet the preconditions for this sequence of steps.

In the case where the current owner and new owner have existing Adobe IDs, both accounts should remain, but email addresses need to be switched between them. This requires the use of a _temporary_ email address that is valid, but is not associated with and Adobe ID.

### Change to a temporary account

The current owner completes these steps to associate their Adobe ID with another, temporary email address.

1. Navigate to [account.adobe.com](https://account.adobe.com/) and complete the Adobe login.

1. Under your account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter a valid temporary email address that is not used by an Adobe ID.

   You must have access to the email address so that you can retrieve the email with the confirmation code. 

1. Click **[!UICONTROL Change]**.

   This generates a verification email sent to the temporary email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the temporary email address.

1. Click **[!UICONTROL Verify]**.

1. Log out of the Adobe account.

### New owner steps

After the current owner completes the transfer to a temporary email address, complete these steps to change your account over to the current owner.

1. Navigate to [account.adobe.com](https://account.adobe.com/) and complete the Adobe login.

1. Under your account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter the current owner's original email address.

1. Click **[!UICONTROL Change]**.

   This generates a verification email sent to that email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the current owner.

1. Click **[!UICONTROL Verify]**.

1. Log out of the Adobe account.

### Follow up steps

After the new owner successfully transfers their Adobe account to the current (now previous) owner, complete these steps to transfer ownership.

1. Navigate to [account.adobe.com](https://account.adobe.com/) (first account used in the series of steps) and complete the Adobe login.

   This login requires the use of the temporary email address.

1. Under the account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter the new owner's email address.

1. Click **[!UICONTROL Change]**.

   This generates a verification email sent to that email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the new owner.

1. Click **[!UICONTROL Verify]**.

>[!IMPORTANT]
>
>Submit a Support request to inform the Support team that you have updated the account owner's email address. The team must perform additional steps to complete the update such as updating the email address on your [Commerce Marketplace](https://commercemarketplace.adobe.com/) profile. Include the previous account owner's email address in your request.
