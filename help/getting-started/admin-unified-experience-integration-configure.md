---
title: Configure the Commerce Admin Integration with Experience Cloud
description: Learn about the requirements and process to configure a Commerce on cloud infrastructure environment to deploy the Commerce Admin in the Adobe Unified Shell interface to provide Admin users with an improved user experience.
---
# Configure the Commerce Admin Integration with Experience Cloud

To complete the configuration for the Experience Cloud integration, install and configure the Commerce Admin Unified Experience extension, generate the connection information and credentials for the Adobe I/O Events service and configure the events service in the Commerce Admin.

1. Check the Commerce application environment.

1. Enable the Commerce Admin Unified Experience extension

1. Connect to the Adobe I/O Events

1. Test the integration


## Prerequisites

- Adobe Commerce 2.4.5 or later
- Account provisioning and permissions—Administrators must have access to the following resources to configure the integration for Commerce Admin:
  - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html)—Add and manage Adobe user and developer accounts for the organization
  - [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/)—Developer or system administrator access to generate connection credentials and information for the Adobe I/O Events service
  - [Commerce on cloud infrastructure project](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html?lang=en#get-started-with-the-project-web-interface)—Install required modules and configure the Commerce application server using the Adobe Commerce CLI
 - [Commerce Admin](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html)—Update store configuration and manage Commerce user accounts


## Check the Commerce application and environment


- Verify that Adobe IMS integration is enabled

  - if not enable it

- Verify that an Admin user can authenticate successfully using the Adobe IMS integration

- Verify that the Unified Experience extension is available on your instance

  - if not install it


## Enable the Commerce Admin Unified Experience extension

Provide instructions to enable from the Admin and the command line

Make sure that you have at least one Administrator account that has been provisioned on both the Commerce Admin and the Adobe Admin Console.  Administrator accounts must have the same email address in the Commerce Admin and the Admin Console.

Verify that the Experience Cloud integration is enabled.


## Configure Adobe I/O Events

- From the Adobe Developer Console, generate the credentials and connection information for Adobe I/O events from the Adobe Developer Console

- From the Commerce Admin, connect Commerce to the Adobe I/O Events service

- From the Commerce application server, use the Adobe Commerce CLI to create an event provider to send data from the Commerce Admin to the Adobe I/O events service

- Verify that you can log in to Experience Cloud and open the Commerce Admin from the Commerce Projects workspace


## Add Commerce Admin users to the Admin Console

Commerce Admin users must have two accounts with the same name and primary email address:

- An Adobe Commerce Admin account
- An Adobe account

All Commerce Admin users must be a member of the Adobe organization provisioned on the Commerce instance.


## Test the integration

Verify that a Commerce Administrator can sign in to the Commerce Admin through Experience Cloud and access other Experience Cloud applications and services using the common interface.

1. Sign in to the Commerce Admin from Experience Cloud.

   - Copy and paste the default Admin URL for your Adobe Commerce environment into the address bar.

   - Log in to Experience Cloud

1. View available Commerce Projects

1. Open the Commerce Admin.

1. Verify access to Experience Cloud services

1. Verify that you can complete tasks in the Commerce Admin as expected.

