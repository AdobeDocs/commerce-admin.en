---
title: Commerce Installation
group: Review basic information for Adobe Commerce and Magento Open Source installation.
---
# Commerce Installation

To download and install the latest 2.4.x release on your server, see the [Installation][1]{:target="_blank"} and [Configuration][2]{:target="_blank"} information in the developer documentation. A Commerce installation can be deployed to run in either production or developer mode.

The _Installation Guide_ provides information about installing Adobe Commerce, including these recommended topics:

- [System requirements][3]{:target="_blank"}
- [Prerequisites][4]{:target="_blank"}
- [Installation roadmap][5]{:target="_blank"}
- [Post Installation][6]{:target="_blank"}

## Commerce Modes

Your Commerce installation can be deployed to run in either production or developer mode. Some tools and configuration settings are designed specifically for developers, and can be accessed only while the store is running in developer mode.

Most topics in this guide apply to a Commerce installation that is running in production mode. However, the following configuration settings and topics can be used only when the installation is running in developer mode (each topic is marked  with _Developer Mode Only_ where applicable).

### Configuration settings

See the [Developer](https://docs.magento.com/user-guide/configuration/advanced/developer.html) section of the [Advanced](https://docs.magento.com/user-guide/configuration/advanced.html) configuration settings page for more information.

## General topics

See the following pages for more information about non-configuration setting types of topics for Developer Mode only:

- [Merging CSS Files](https://docs.magento.com/user-guide/design/merge-css.html)
- [Merging JavaScript Files](https://docs.magento.com/user-guide/design/merge-javascript.html)
- [Changing UI Text](https://docs.magento.com/user-guide/system/translate-inline.html)
- [Using Static File Signatures](https://docs.magento.com/user-guide/system/static-file-signature.html)
- [Frontend Development Workflow](https://docs.magento.com/user-guide/system/frontend-development-workflow.html)
- [Optimizing Resource Files](https://docs.magento.com/user-guide/system/file-optimization.html)
- [Template Path Hint](https://docs.magento.com/user-guide/system/template-path-hints.html)
- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce only) [Developer Client Restrictions](https://docs.magento.com/user-guide/system/developer-client-restrictions.html)

The Commerce mode can be changed only from the command line of the server by a user with appropriate permissions. See [Set the Mode](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-mode.html) in the developer documentation for more information.


[1]: https://devdocs.magento.com/guides/v2.4/install-gde/bk-install-guide.html
[2]: https://devdocs.magento.com/guides/v2.4/config-guide/bk-config-guide.html
[3]: https://devdocs.magento.com/guides/v2.4/install-gde/system-requirements.html
[4]: https://devdocs.magento.com/guides/v2.4/install-gde/prereq/prereq-overview.html
[5]: https://devdocs.magento.com/guides/v2.4/install-gde/install-flow-diagram.html
[6]: https://devdocs.magento.com/guides/v2.4/install-gde/install/verify.html
