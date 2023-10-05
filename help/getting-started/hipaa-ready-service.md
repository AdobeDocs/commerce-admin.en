---
title: HIPAA readiness on Adobe Commerce
description: TBD
feature: Security, Roles/Permissions
---
# HIPAA readiness on Adobe Commerce

## Health Insurance Portability and Accountability Act (HIPAA)

The Administrative Simplification subtitle of the Health Insurance Portability and Accountability Act of 1996 (“HIPAA”) provides for the U.S. Department of Health and Human Services to promulgate standards governing the privacy and security of certain individually identifiable health information.  HIPAA was most significantly amended by the Health Information Technology Act for Economic and Clinical Health Act of 2009 (the “HITECH Act”), which added breach notification requirements and expanded the scope of who is governed by HIPAA.  The HIPAA Privacy, Security, and Breach Notification Rules establish important protections for individually identifiable health information called protected health information or “PHI” when created, received, maintained, or transmitted by a HIPAA covered entity or business associate.  A “Covered Entity” is a health care provider, health plan, or a health care clearinghouse.  A “Business Associate” is an entity or person, other than a member of the workforce of a covered entity, who performs functions or activities on behalf of, or provides certain services to, a Covered Entity that involves creating, receiving, maintaining, or transmitting PHI.
The HIPAA Privacy and Security Rules require that a Covered Entity obtain written assurances from a Business Associate in the form of a Business Associate Agreement, or BAA, requiring the Business Associate to safeguard the privacy and security of the Covered Entity’s PHI.

## Adobe Commerce HIPAA-Ready

Adobe Commerce HIPAA-Ready has additional features and functionalities that allow merchants to comply with their respective HIPAA obligations. You can install the Adobe Commerce Hipaa Ready (magento/hipaa-ee) module to your Adobe Commerce on cloud infrastructure. There are some features that also have to be disabled to be compliant with HIPAA.

## [Action Logs](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en)

Audit Log is one of the HIPAA requirements. In Adobe Commerce, we already have an Action Logs feature to record every change made by an Admin user who works in your store. But to meet HIPAA requirements about Audit Log, we made some changes with the feature to record all Admin user and customer actions performed via both the UI and API calls.

We also made some changes with the Action Logs report grid.
- Two new columns Source & Client Type are added.
- Existing column Username renamed to Client Identifier
- Existing column Full Action Name renamed to Target

### Configure Admin actions for logging
This feature is not available anymore since all actions have to be recorded by default.
