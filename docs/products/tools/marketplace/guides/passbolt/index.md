---
slug: Deploy Passbolt Through The Linode Marketplace
title: "Deploy Passbolt Through The Linode Marketplace"
description: 'Deploy Passbolt password manager through the Linode Marketplace.'
og_description: 'Deploy Passbolt password manager through the Linode Marketplace.'
keywords: ['passbolt','password manager','security','authentication']
license: '[CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0)'
authors: ["Linode"]
published: 2024-02-05
modified_by:
  name: Linode
---

[Passbolt Password Manager](https://github.com/passbolt/passbolt_api) is an open-source password manager designed for teams and businesses. It allows users to securely store, share and manage passwords. 

## Deploying a Marketplace App 

{{< content "deploy-marketplace-apps-shortguide">}}

{{< content "marketplace-verify-standard-shortguide">}}

{{< note >}}
**Estimated deployment time:** Passbolt should be fully installed within 5-10 minutes after the Compute Instance has finished provisioning.
{{< /note >}}

## Configuration Options

- **Supported distributions:** Ubuntu 22.04 LTS
- **Recommended plan:** We recommend a 4GB Dedicated CPU or Shared Compute instance for Passbolt.

### Passbolt Options

{{< content "marketplace-required-limited-user-fields-shortguide">}}

## Getting Started after Deployment

After Passbolt is deployed, the installation screen will be available at `http://example.com/install/`. Credentials are saved to `/root/.credentials`.

Please visit [Passbolt Installation Documentation](https://help.passbolt.com/hosting/install/ce/ubuntu/ubuntu.html) for information on how to set up and configure Passbolt.

### Database Configuration Options
* Database connection url - Use `localhost` if using the locally configured mysql database. Otherwise, add your database connection string here.
* Username, Password, Database name - These are located at `/root/.credentials`

### Email Configuration
Postfix is installed as part of the Marketplace App, allowing you to send mail. To send a test email through the Email Configuration screen, use the following:
* Sender name - root
* Sender email - root@<yourdomain.com>
* SMTP host - Add your server hostname
* Use TLS? - No
* Port - 25
* Authentication method - None
* Client - client

{{< note >}}
It is strongly recommended that you follow the best practices for configuring a mail server to ensure mail deliverability. Please see the [Running a Mail Server](https://www.linode.com/docs/guides/running-a-mail-server/) guide for more information.
{{< /note >}}

{{< note >}}
**Mail Server Settings:** To make the most out of Passbolt you need a working email setup for email notifications (e.g. - account registration, password recovery and other critical notifications). For more information on setting this up, see the [Configure Email Providers](https://help.passbolt.com/configure/email/setup) page on Passbolt's website.  
{{< /note >}}

{{< content "marketplace-update-note-shortguide">}}
