---
title: PayPal Settlement report
description: Learn about the PayPal Settlement report as a tool to manage PayPal transactions.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="PaaS only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed PaaS infrastructure) and on-premises projects only."
TQID: https://experienceleague.adobe.com/c7v5oSsVPmD6r6obfGEoxPiGkMI4KMWAmfJAW0-CCJk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
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
# PayPal Settlement report

The PayPal Settlement report provides merchants with the information about each transaction that affects the settlement of funds.

>[!NOTE]
>
>Before generating settlement reports, the store administrator must request PayPal Merchant Technical Services to create an SFTP user account, enable settlement reports generation, and enable SFTP in their PayPal business account.

After configuring and enabling settlement reports in the PayPal merchant account, Adobe Commerce and Magento Open Source will start generating reports during the following 24 hours. The list of available settlement reports can be viewed from the Admin.

**_To view settlement reports:_**

1. On the _Admin_ sidebar, go to **[!UICONTROL Reports]** > _[!UICONTROL Sales]_ > **[!UICONTROL PayPal Settlement]**.

   ![PayPal Settlement Reports](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. For the most recent updates, click **[!UICONTROL Fetch Updates]** in the upper-right corner.

   The system connects to the PayPal SFTP server to fetch the reports. When the process is complete, a message appears with the number of reports fetched. The report includes the following information for each transaction:

   |Report column | Description |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | One of the following reference codes:<br/>- Order IDT<br/>- Transaction ID<br/>- Subscription ID |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** - The text entered by the merchant on the transaction at PayPal.<br/>**[!UICONTROL Transaction Debit or Credit]** - The direction of money movement of gross amount.<br/>**[!UICONTROL Fee Debit or Credit]** - The direction of money movement for fee. |

   {style="table-layout:auto"}
