---
title: Transfer an Adobe Commerce Account
description: Learn how to transfer an Adobe Commerce account to a new owner or email address, choose the right transfer type, verify email changes, and contact Support.
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
# Transfer an Adobe Commerce account

As business responsibilities change, you might need to transfer your Adobe Commerce account to a new owner or to another email address. This transfer requires a change to the primary user email associated with the account.

The following information describes the process for transferring an Adobe Commerce account (MAGEID). It does not include changes to Adobe Commerce on cloud infrastructure project ownership or [!DNL New Relic] ownership. For more information about cloud project access, see [Manage user access](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access) in the _Commerce on Cloud Infrastructure Guide_.

>[!IMPORTANT]
>
>If the new account owner purchased extensions using Shared Access, access to those extensions is lost as soon as the account transfer starts.
>
>Before requesting the account transfer, make sure that the new owner retrieves the Order IDs for the purchases from [their [!DNL Commerce Marketplace] account](https://commercemarketplace.adobe.com/sales/order/history/) and requests a refund from the [[!DNL Commerce Marketplace] team](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). Extension purchases cannot be transferred to a different account.

## Identify your transfer type

The appropriate Adobe Commerce account transfer process depends on the account status of the current owner and the new owner, and on whether the current owner's email address is still accessible. For example, if the current owner has left the company, you might still need access to emails sent to that address.

The following scenarios describe the available transfer options based on these conditions.

| Transfer type | Current owner | New owner |
| ------------- | ------------- | --------- |
| [New Adobe ID and email change](#new-adobe-id-and-email-change) | Has a MAGEID that has not been connected to an Adobe ID | Does not have a MAGEID and does not have an Adobe ID. |
| [Email change only](#email-change) | Has a MAGEID that is connected to an Adobe ID. | Has an Adobe ID, but does not have a MAGEID connected to the account. |
| [Adobe ID account switch](#adobe-id-account-switch) | Has a MAGEID that is connected to an Adobe ID. | Has a MAGEID and is connected to an Adobe ID. |

{style="table-layout:auto"}

>[!NOTE]
>
>As Adobe Commerce continues to integrate with other Adobe solutions, an Adobe Commerce account (MAGEID) now requires an association with an Adobe ID. The Adobe ID uses the same email address connected to your [Adobe Commerce account](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).

## Verify an Adobe ID email change

Several transfer paths use the same verification workflow on [account.adobe.com](https://account.adobe.com/). After you enter the target email address and click **[!UICONTROL Change]**, complete these steps:

1. Open the verification email sent to the address you entered and locate the confirmation code.

1. Enter the confirmation code.

1. Click **[!UICONTROL Verify]**.

## New Adobe ID and email change

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and confirm that this path matches your situation:
>
>- The current owner is still with the company.
>- The current owner either does not have an Adobe ID, or has an Adobe ID that is not connected to their [Adobe Commerce account (MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- The new owner does not have an Adobe ID and does not have an Adobe Commerce account.

Use this path when the current owner has a MAGEID that is not yet linked to an Adobe ID. The current owner first creates and links an Adobe ID, then changes that Adobe ID email address to the new owner's email address.

1. Go to the [Adobe Commerce account login](https://account.magento.com/customer/account/login/) page.

1. Click **[!UICONTROL Sign in with Adobe ID]**.

1. Click **[!UICONTROL Create an account]**.

1. Enter the current owner's email address and password.

1. Click **[!UICONTROL Continue]**.

   This step creates an Adobe ID and links it to the current Adobe Commerce account (MAGEID). With this account link, the _[!UICONTROL Email]_ field is blocked from any changes. The configuration of the associated email address is managed from the Adobe ID account.

1. Navigate to [account.adobe.com](https://account.adobe.com/).

1. Click **[!UICONTROL Change Email]**.

1. Enter the new owner's email address.

   If the new email address is already linked to another account in the system, it cannot be directly used for the transfer. Instead, follow the [Adobe ID account switch](#adobe-id-account-switch) path and use a [temporary email address](#change-to-a-temporary-account).

1. Complete the [email verification steps](#verify-an-adobe-id-email-change).

After the new owner verifies the email address, continue to [Final steps](#final-steps) so that Adobe Commerce Support can update account records such as the [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) profile.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on){transcript=true}

## Email change only {#email-change}

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and confirm that this path matches your situation:
>
>- The current owner is still with the company.
>- The current owner has an Adobe ID that is connected to their [Adobe Commerce account (MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- The new owner has an Adobe ID that is not connected to an Adobe Commerce account.

Before you begin, note that this transfer type results in the current account owner losing access to other Adobe products tied to that Adobe ID.

1. Navigate to [account.adobe.com](https://account.adobe.com/) and complete the Adobe login.

1. Under your account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter the new owner's email address.

   If the new email address is already linked to another account in the system, it cannot be directly used for the transfer. Instead, follow the [Adobe ID account switch](#adobe-id-account-switch) path and use a [temporary email address](#change-to-a-temporary-account).

1. Complete the [email verification steps](#verify-an-adobe-id-email-change).

After the new owner verifies the email address, continue to [Final steps](#final-steps) so that Adobe Commerce Support can update account records such as the [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) profile.

## Adobe ID account switch

>[!IMPORTANT]
>
>Review the [transfer types](#identify-your-transfer-type) and confirm that this path matches your situation:
>
>- The current owner is no longer with the company, but emails sent to the current owner's company email address are still accessible, or your IT team can forward those emails to an authorized contact.
>- The current owner has an Adobe ID that is connected to their [Adobe Commerce account (MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account).
>- The new owner has an Adobe ID that is connected to their Adobe Commerce account.

This transfer type uses a temporary email address to switch account ownership when both the current owner and new owner have existing Adobe IDs, and you want to retain both Adobe IDs. To complete the ownership transfer, you must use a temporary email address that is not associated with an Adobe ID.

### Change to a temporary account

Complete these steps to associate the current owner's Adobe ID with a temporary email address. You must have access to that email address so that you can retrieve the confirmation code.

>[!NOTE]
>
>If you cannot access the current owner's email, ask your IT team to set up email forwarding for the account email address in your company email system. If email forwarding cannot be configured, ensure the new account owner has an Adobe ID and then [submit a support request](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) with all necessary details to initiate the account transfer.

1. Navigate to [account.adobe.com](https://account.adobe.com/) and complete the Adobe login.

1. Under your account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter a valid temporary email address that is not used by an Adobe ID.

1. Complete the [email verification steps](#verify-an-adobe-id-email-change).

1. Log out of the Adobe account.

### New owner steps

After the current owner completes the transfer to a temporary email address, the new owner must complete these steps to change their Adobe ID email address to the current owner's original email address.

1. Navigate to [account.adobe.com](https://account.adobe.com/) and complete the Adobe login.

1. Under your account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter the current owner's original email address.

1. Complete the [email verification steps](#verify-an-adobe-id-email-change).

1. Log out of the Adobe account.

### Follow up steps

After the new owner successfully configures their Adobe ID with the original email address of the current owner, complete these steps to assign that email address to the new owner.

1. Navigate to [account.adobe.com](https://account.adobe.com/), and complete the Adobe login using the email address for the [temporary account](#change-to-a-temporary-account).

1. Under the account name and avatar, click **[!UICONTROL Change Email]**.

1. In the dialog, enter the new owner's email address.

1. Complete the [email verification steps](#verify-an-adobe-id-email-change).

After the new owner verifies the email address, continue to [Final steps](#final-steps) so that Adobe Commerce Support can update account records such as the [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) profile.

## Final steps

Complete these steps after completing the [New Adobe ID and email change](#new-adobe-id-and-email-change), [Email change only](#email-change), or [Adobe ID account switch](#adobe-id-account-switch) process.

1. As the new owner, [submit a support request](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case).

   Include the following details:

   - The previous account owner's email address
   - The new owner's email address
   - A note that you completed an Adobe Commerce account transfer and updated the Adobe ID email address

1. Wait for Adobe Commerce Support to confirm the update.

   Support also updates related records, such as the email address on your [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) profile.

After support completes the request, the new owner can sign in to the Adobe Commerce account with their Adobe ID. The MAGEID remains the entitlement identifier for the account.
