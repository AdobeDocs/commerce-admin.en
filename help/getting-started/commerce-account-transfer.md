---
title: Transfer a Commerce account
description: Learn how to transfer your Commerce account to another owner or email address.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
TQID: https://experienceleague.adobe.com/CIyzus4f8WcBH-jW9R1nCL-gkl065DLTHbjNn0K6e7E
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
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
# Transfer a Commerce account

As business responsibilities change, you might need to transfer your Commerce account to a new owner or to another email address. This transfer requires a change to the primary user email associated with the account. 

The following information describes the process for transferring a Commerce (MAGEID) account. It does not include changes for Cloud account (Cloud project or New Relic) ownership. For more information about cloud project access, see [Manage user access](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) in the _Commerce on Cloud Infrastructure Guide_.

>[!IMPORTANT]
>
>If the new account owner has purchased extensions using Shared Access, access to those extensions is lost as soon as the Account Transfer process has been initiated. Before requesting the account transfer, make sure that the new owner retrieves the Order IDs for the purchases from [their Marketplace account](https://commercemarketplace.adobe.com/sales/order/history/) and requests a refund for those extensions from the [Marketplace team](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). It is not possible to transfer extension purchases to a different account.

## Identify your transfer type

The appropriate Commerce account transfer process depends on the account status of the current owner and the new owner, and on whether the current owner's email address is still accessible. For example, if the current owner has left the company, you might still need access to emails sent to that address. 

The following scenarios describe the available transfer options based on these conditions.

| Transfer type | Current owner | New owner |
| ------------- | ------------- | --------- |
| [New Adobe ID and email change](#new-adobe-id-and-email-change) | Has a MAGEID that **_has not been connected_** to an Adobe login account | Does not have a MAGEID and **_does not have_** an Adobe login account. |
| [Email change only](#email-change) | Has a MAGEID that is **_connected_** with an Adobe login account. | Has an Adobe login account, but **_does not have a MAGEID_** connected to the account. |
| [Adobe ID account switch](#adobe-id-account-switch) | Has a MAGEID that is **_connected_** to an Adobe login account. | Has a MAGEID and **_is connected_** to an Adobe login account. |

{style="table-layout:auto"}

>[!NOTE]
>
>As Adobe Commerce continues to integrate with other Adobe solutions, a Commerce account (MAGEID) now requires an association with an Adobe login. This Adobe ID uses the same email address connected to your [Commerce account.](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)

## New Adobe ID and email change

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and make sure that you meet the preconditions for this sequence of steps.
>
>Follow these steps when:
>- the Current owner is still with the company
>- the Current owner either does not have an Adobe login account, or has an Adobe login account that is not connected to their [Commerce account (MAGE ID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)
>- the New owner does not have an Adobe login account and does not have a Commerce account

This transfer type requires the Current owner to have an Adobe ID that's linked to an existing Commerce account, and then changing that account to the email address for the New owner.

1. Go to the [Commerce account login](https://account.magento.com/customer/account/login/) page.

1. Click **[!UICONTROL Sign in with Adobe ID]**.

1. Click **[!UICONTROL Create an account]**.

1. Enter the email address of the current owner and their password.

1. Click **[!UICONTROL Continue]**.

   This step creates an Adobe ID and links it to the current Commerce account (MAGEID). With this account link, the _[!UICONTROL Email]_ field is blocked from any changes. The configuration of the associated email address is managed from the Adobe ID account.

1. Navigate to [account.adobe.com](https://account.adobe.com/).

1. Click **[!UICONTROL Change Email]**.

1. Enter the new owner's email address.
  
   If the new email address is already linked to another account in the system, it cannot be directly used for the transfer. Instead, the process requires using a [temporary email address](#change-to-a-temporary-account) to facilitate the change.

1. Click **[!UICONTROL Change]**.

   This step generates a verification email sent to the new email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the new email address.

1. Click **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## Email change

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and make sure that you meet the preconditions for this sequence of steps.
>
>Follow these steps when:
>- the Current owner is still with the company
>- the Current owner has an Adobe login account that has been connected to their [Commerce account (MAGE ID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)
>- The New owner has an existing Adobe login account that has not been connected to their Commerce account

This transfer type results in the current account owner losing access to other Adobe products.

1. Navigate to [account.adobe.com](https://account.adobe.com/) and complete the Adobe login.

1. Under your account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter the new owner's email address.

   If the new email address is already linked to another account in the system, it cannot be directly used for the transfer. Instead, the process requires using a [temporary email address](#change-to-a-temporary-account) to facilitate the change.

1. Click **[!UICONTROL Change]**.

   This step generates a verification email sent to the new email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the new email address.

1. Click **[!UICONTROL Verify]**.

## Adobe ID account switch

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and make sure that you meet the preconditions for this sequence of steps.
>
>Follow these steps when:
>- the Current owner is no longer with the company, but emails sent to the current owner's company email address are still accessible, or your IT team can forward those emails to an authorized contact
>- the current owner has an Adobe login account that is connected to their [Commerce account (MAGE ID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)
>- the new owner has an Adobe login account that is connected to their Commerce account

This transfer type uses a temporary email address to switch account ownership when both the current owner and new owner have existing Adobe IDs, and you want to retain both Adobe IDs. To complete the ownership transfer, you must use a temporary email address that is not associated with an Adobe ID.

### Change to a temporary account

Complete these steps to associate the Current owner's Adobe ID with another, temporary email address. You must have access to the email address so that you can retrieve the email with the confirmation code.

>[!NOTE]
>
>You must have access to the Current owner's email address so that you can retrieve the email with the confirmation code.
>
>If you cannot access the Current owner's email, ask your IT team to set up email forwarding for the account email address in your company email system. If email forwarding cannot be configured, ensure the new Account Owner has an Adobe ID and then [submit a Support request](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) with all necessary details to initiate the account transfer.

1. Navigate to [account.adobe.com](https://account.adobe.com/) and complete the Adobe login.

1. Under your account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter a valid temporary email address that is not used by an Adobe ID.

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

After the new owner successfully configures their Adobe account with the original email address of the current owner, complete these steps to transfer ownership.

1. Navigate to [account.adobe.com](https://account.adobe.com/), and complete the Adobe login using the email address for the [temporary account](#change-to-a-temporary-account).

1. Under the account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter the new owner's email address.

1. Click **[!UICONTROL Change]**.

   This step generates a verification email sent to the new owner's email address. The email contains a confirmation code that is required to complete the email address change.

1. Enter the confirmation code sent to the new owner's email address.

1. Click **[!UICONTROL Verify]**.

## Final steps

After the new owner completes the steps in the first or third use case, the new owner must [submit a support request](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case) to inform the support team about the email address update. The support team then completes additional tasks, such as updating the email address on the [Commerce Marketplace](https://commercemarketplace.adobe.com/) profile. Include the previous account owner’s email address in the request.
