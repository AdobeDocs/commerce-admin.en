---
title: Encryption key
description: Learn how to auto generate or add your own encryption key, which should be changed regularly to improve security.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
---
# Encryption key

Adobe Commerce and Magento Open Source use an encryption key to protect passwords and other sensitive data. An industry-standard Advanced Encryption Standard (AES-256) algorithm is used to encrypt all data that requires decryption. This includes credit card data and integration (payment and shipping module) passwords. In addition, a strong Secure Hash Algorithm (SHA-256) is used to hash all data that does not require decryption.

During the initial installation, you are prompted to either let Commerce generate an encryption key, or enter one of your own. The encryption key tool allows you to change the key as needed. The encryption key should be changed regularly to improve security, and at any time the original key might be compromised. Whenever the key is changed, all legacy data is re-encoded using the new key.

For technical information, see [Advanced on-premises installation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html){:target="_blank"} software in the _Installation Guide_.

![System encryption key](./assets/encryption-key.png)<!-- zoom -->

## Step 1: Make the file writable

To change the encryption key, make sure that the following file is writable: `[your store]/app/etc/env.php`

## Step 2: Change the encryption key

1. On the _Admin_ sidebar, go to **[!UICONTROL System]** > _[!UICONTROL Other Settings]_ > **[!UICONTROL Manage Encryption Key]**.

1. Do one of the following:

   - To generate a new key, set **[!UICONTROL Auto-generate Key]** to `Yes`.
   - To use a different key, set **[!UICONTROL Auto-generate Key]** to `No`. Then in the **[!UICONTROL New Key]** field, enter or paste the key that you want to use.

1. Click **[!UICONTROL Change Encryption Key]**.

1. Keep a record of the new key in a secure location.

   It is required to decrypt the data, if any problems occur with your files.
