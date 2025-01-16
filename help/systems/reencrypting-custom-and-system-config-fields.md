---
title: ReEncrypting certain system configuration and custom encrypted fields.
description: Learn how to re-encrypt certain encrypted configuration values after encryption key has been rotated.
role: Admin
feature: System, Security
---

# ReEncryption

Magento Open Source and Adobe Commerce 2.4.8 provide functionality to re-encrypt certain encrypted system configuration, payment as well as custom fields. These operations be necessary after the encryption key has been rotated.

# Default ReEncryptors

The default ReEncryption configuration provides two re-encryptors - `Magento\Config\Model\Data\ReEncryptorList\CoreConfigDataReEncryptor` to encrypt system configuration fields and `Magento\Sales\Model\Data\ReEncryptorList\SalesOrderPaymentReEncryptor` to re-encrypt payment fields.
You can use the below command to run both re-encryptors after the encryption key has been rotated.

```bash
   bin/magento encryption:data:re-encrypt core_config_data sales_order_payment
   ```

# ReEncrypting Specific Columns in Tables

The SimpleHandler class `Magento\EncryptionKey\Model\Data\ReEncryptorList\ReEncryptor\SimpleHandler` serves as a base for re-encryptors that simply try to re-encrypt specific columns from a table.
Please follow these steps to re-encrypt specific columns in your tables and add a custom ReEncryptor:

1. Create a virtual type handler for the SimpleHandler - `Magento\EncryptionKey\Model\Data\ReEncryptorList\ReEncryptor\SimpleHandler` and provide the table name, primary key, and columns to encrypt as constructor arguments.
```xml
 <virtualType name="Vendor\MyModule\Model\Data\ReEncryptorList\MyCustomPaymentEncryptor\Handler" type="Magento\EncryptionKey\Model\Data\ReEncryptorList\ReEncryptor\SimpleHandler">
        <arguments>
            <argument name="tableName" xsi:type="string">my_custom_payment_table</argument>
            <argument name="identifierField" xsi:type="string">entity_id</argument>
            <argument name="fieldsToReEncrypt" xsi:type="array">
                <item name="cc_number_enc" xsi:type="string">cc_number_enc</item>
            </argument>
        </arguments>
    </virtualType>
```
2. Create a virtual type for `Magento\EncryptionKey\Model\Data\ReEncryptorList\ReEncryptor` and inject the handler created in step 1 as a constructor argument as shown below:

```xml
 <virtualType name="Vendor\MyModule\Model\Data\ReEncryptorList\MyCustomPaymentReEncryptor" type="Magento\EncryptionKey\Model\Data\ReEncryptorList\ReEncryptor">
    <arguments>
        <argument name="description" xsi:type="string">Re-encrypts 'cc_number_enc' column in the 'my_custom_payment_table' DB table.</argument>
        <argument name="handler" xsi:type="object">Vendor\MyModule\Model\Data\ReEncryptorList\MyCustomPaymentEncryptor\Handler</argument>
    </arguments>
</virtualType>
```
3. Finally, add the ReEncryptor created from step 2 to `Magento\EncryptionKey\Model\Data\ReEncryptorList` as shown below

```xml
<type name="Magento\EncryptionKey\Model\Data\ReEncryptorList">
    <arguments>
        <argument name="reEncryptors" xsi:type="array">
            <item name="my_custom_payment_reencryptor" xsi:type="object">Vendor\MyModule\Model\Data\ReEncryptorList\MyCustomPaymentReEncryptor</item>
        </argument>
    </arguments>
</type>
```

You can run the following command to test that the newly created re-encryptor shows up in the list of available encryptors and there were no errors

 ```bash
   bin/magento encryption:data:list-re-encryptors
   ```
If the above step was successful, you can run the following command to re-encrypt specific columns in your database table using the re-encryptor

```bash
   bin/magento encryption:data:re-encrypt my_custom_payment_reencryptor
   ``
