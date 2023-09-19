---
title: Security scan
description: Learn how to run an enhanced security scan and monitor each of your Adobe Commerce and Magento Open Source sites.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
---
# Security scan

The enhanced security scan allows you to monitor each of your Adobe Commerce and Magento Open Source sites, including PWA, for known security risks and malware, and to receive patch updates and security notifications.

- Gain insight into the real-time security status of your store.
- Receive suggestions based on best practices to help resolve issues.
- Schedule security scan to run weekly, daily, or on demand.
- Run over 21,000 security tests to help identify potential malware.
- Access historical security reports that track and monitor the progress of your sites.
- Access the scan report that shows successful and failed checks, with any recommended actions.

The Security scan tool is available for free from the dashboard of your [Commerce account](../getting-started/commerce-account-create.md). For technical information, see [Set up the Security Scan Tool](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) in the _Commerce on Cloud Infrastructure Guide_.

![Security scan tool](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## Run a security scan

1. Go to the Commerce home page, and sign in to your [Commerce account](../getting-started/commerce-account-create.md) and do the following:

   - In the left panel, choose **[!UICONTROL Security Scan]**.
   - Click **[!UICONTROL Go to Security Scan]**.
   - Read the **[!UICONTROL Terms and Conditions]**.
   - Click **[!UICONTROL Agree]** to continue.

1. On the _[!UICONTROL Monitored Websites]_ page, click **[!UICONTROL +Add Site]**.

   If you have multiple sites with different domains, you must configure a separate scan for each domain.

   ![Monitored Sites](./assets/monitored-website.png){width="600" zoomable="yes"}

1. To verify your ownership of the site domain by adding a confirmation code, do one of the following:

   **Commerce storefront**:

   - Enter the **[!UICONTROL Site URL]** and **[!UICONTROL Site Name]**.
   - Click **[!UICONTROL Generate Confirmation Code]**.
   - Click **Copy** to copy your confirmation code to the clipboard.

      ![Generate Confirmation Code](./assets/scan-site1.png){width="400" zoomable="yes"}

   - Log in to the Admin of your store as a user with full administrator privileges and do the following:

      - In the _Admin_ sidebar, go to **[!UICONTROL Content]** > _[!UICONTROL Design]_ > **[!UICONTROL Configuration]**.
      - Find your site in the list, and click **[!UICONTROL Edit]**.
      - Expand ![Expansion selector](../assets/icon-display-expand.png) the **[!UICONTROL HTML Head]** section.
      - Scroll down to **[!UICONTROL Scripts and Style Sheets]** and click in the text box at the end of any existing code and paste the confirmation code into the text box.

         ![Scripts and Style Sheets](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - When complete, click **[!UICONTROL Save Configuration]**.

   **PWA storefront**:

   - Enter the **[!UICONTROL Site URL]** and **[!UICONTROL Site Name]**.

   - For **[!UICONTROL Confirmation Code]**, choose the `META Tag` option and then click **[!UICONTROL Generate Code]**.

   - Click **[!UICONTROL Copy]** to copy the generated confirmation code META Tag to the clipboard.

      ![Generate Confirmation Code](./assets/scan-site2.png){width="400" zoomable="yes"}

   - Go to the PWA Studio storefront project directory and do the following:

      - Under the PWA Studio project directory, go to `packages > venia-concept > template.html`.
      - Add the copied confirmation code (the generated META Tag) to the HTML head and save the changes.

         ![Copy Confirmation Code](./assets/code-pwa.png){width="600" zoomable="yes"}

      - Go back to the PWA Studio CLI, and use yarn to install project dependencies and run the project build command.

        ```sh
        yarn install &&
        yarn build
        ```

      - *In your Cloud project*, create a `pwa` folder and copy the content inside your storefront project's `dist` folder.

         ```sh
         mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
         ```

      - Use the Git CLI tool to stage, commit, and push these changes to your Cloud project.

         ```sh
         git add . &&
         git commit -m "Added storefront file bundles" &&
         git push origin
         ```

         After the build process completes, the changes will be deployed to your PWA store front.

1. Return to the _[!UICONTROL Security Scan]_ page in your Commerce account and click **[!UICONTROL Verify Confirmation Code]** to establish your ownership of the domain.

1. After a successful confirmation, configure the **[!UICONTROL Set Automatic Security Scan]** options for one of the following types:

   **Scan Weekly (recommended)**:

   - Choose the **[!UICONTROL Week Day]**, **[!UICONTROL Time]**, and **[!UICONTROL Time Zone]** that the scan is to take place each week.
   - By default, the scan is scheduled to begin each week at midnight Saturday, UTC, and continue through early Sunday.

      ![Scan Weekly](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **Scan Daily**:

   - Choose the **[!UICONTROL Time]**, and **[!UICONTROL Time Zone]** that the scan is to take place each day.
   - By default, the scan is scheduled to begin each day at midnight, UTC.

      ![Scan Daily](./assets/scan-daily.png){width="500" zoomable="yes"}

1. Enter the **[!UICONTROL Email Address]** where you want to receive notifications of completed scans and security updates.

    ![Email Address](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. When complete, click **[!UICONTROL Submit]**.

    After the ownership of the domain is verified, the site appears in the Monitored Websites list of your Commerce account.

1. If you have multiple websites with different domains, repeat this process to set up a security scan for each.
