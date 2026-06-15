---
title: Security
description: Learn about the tools available to secure your stores and data, and guidelines for a security action plan if your detect a compromise.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
TQID: https://experienceleague.adobe.com/9aJ-ZVqwaIr2IJTY6e2hp3eoZe2v6sxz6WdqP2FiPTc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
---
# Security

There are multiple ways to secure your store and maintain your data security:

- Set up [two-factor authentication](security-two-factor-authentication.md)
- Implement [CAPTCHA](security-captcha.md) or [reCAPTCHA](security-google-recaptcha.md)
- Set up a [Security Scan](security-scan.md) for each domain in your Adobe Commerce or Magento Open Source installation. 

>[!NOTE]
>
>Stores that have enabled [!DNL Adobe Identity Management Services] (IMS) authentication have native Adobe Commerce and Magento Open Source 2FA disabled. Admin users who are logged into their Commerce instance with their Adobe credentials do not need to reauthenticate for many Admin tasks. Authentication is handled by Adobe IMS when the Admin user logs into their current session. See [[!DNL Adobe Identity Management Service] (IMS) Integration Overview](../getting-started/adobe-ims-integration-overview.md).

Visit the [Security Center](https://helpx.adobe.com/security.html){:target="_blank"} to get the latest news about potential vulnerabilities, register for Adobe Security notifications, and access the Adobe Trust Center.

![Security Center](./assets/product-security-home.png){width="700" zoomable="yes"}

For information about security best practices, see [Secure your Commerce Site and Infrastructure](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) in the _Implementation Playbook_.

## Security action plan

If you suspect that your Adobe Commerce or Magento Open Source site is compromised, follow this action plan without delay.

1. **Diagnose**: Run a scan to establish the security status of your Commerce store. Commerce [Security Scan](security-scan.md) is a free service offered by Adobe that allows you to monitor your Commerce sites for known security risks and malware, and to receive security notifications.

1. **Clean**: Hire a [qualified consultant](https://solutionpartners.adobe.com/s/directory/?partner_type=1) or online service to clean your site of all malicious code. Some Commerce community members recommend [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Check the `/media` folder for leftover executable code. Remove all unknown Admin users and reset all Admin passwords.

1. **Protect**: Keep your Commerce installation up to date with the most current release. If you are using an older version, apply all security patches as they become available. Review and follow [Commerce security best practices](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Subscribe to [Commerce Security Alerts](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Report**: If you think that you have found a specific vulnerability in Commerce, [open an issue with Adobe](https://hackerone.com/adobe?type=team) and include technical details.

1. **Upgrade**: For the additional peace of mind that comes from 24/7 support, plan your upgrade to [Adobe Commerce on our Cloud Architecture](https://business.adobe.com/products/magento/cloud-delivery.html) now.
