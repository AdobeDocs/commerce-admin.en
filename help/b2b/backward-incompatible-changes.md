---
title: Adobe Commerce B2B backward-incompatible changes
description: Learn about changes in Adobe Commerce B2B releases that may require you to update your custom code.
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
---
# Adobe Commerce B2B backward-incompatible changes

Review the high-level reference information for all backward-incompatible changes in B2B for Adobe Commerce releases. See the highlights section for incompatible changes that have a major impact and require detailed explanation and special instructions.

## Highlights

### 1.4.2 to 1.5.0

With the addition of mult-company assignment for company users, customer account information can now include multiple company attributes. The `Magento\Company\Api\Data\CompanyCustomerInterface` was updated to set the default `company_id` for a user. The default is set to the first company assigned to the company user account.

If you are upgrading from a previous release, Adobe recommends implementing the following methods in classes that use the `Magento\Company\Api\Data\CompanyCustomerInterface`.

- Magento\Company\Api\Data\CompanyCustomerInterface::getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface::setIsDefault


## Reference

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}
