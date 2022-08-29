---
title: "Configure Diagnostics Project"
chapter: true
weight: 2
---

## Configure Diagnostics Project

In this section, you will add your AWS Credentials to the prebuilt Diagnostics Project.

### Add AWS Secret Key to Project Keystore

To interact with AWS via API, PagerDuty RBA can securely store and use AWS secrets through it's [key storage](https://docs.rundeck.com/docs/manual/key-storage/key-storage.html).
From within the project page navigation panel, click on "Project Settings" followed by "Key Storage".

![](/images/pd_rba_project_setup_2.png)

Click on "Add or Upload a Key" to bring up key storage modal.

![](/images/pd_rba_project_setup_3.png)

Ensure that key type is set to "Password" and paste in your AWS Secret Key under the "Enter text" input field, along with a name/alias for reference.

![](/images/pd_rba_project_setup_4.png)

Once entered, click on "Save" to upload and store your secret; this will be visible on page refresh.

{{% notice info %}}

<p style='text-align: left;'>
Take note of the storage path of your AWS secret key; click on the link icon to copy the path for the next section
</p>
{{% /notice %}}

![](/images/pd_rba_project_setup_5.png)
