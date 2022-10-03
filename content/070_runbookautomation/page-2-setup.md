---
title: "Configure Diagnostics Project"
chapter: true
weight: 2
---

## Change your Password

Credentials to login for this class will be sent to you by a PagerDuty representative.  Upon first login please follow these steps in Runbook Automation to change the provided password.

1. Click on the person icon in the upper right and choose **Profile**
1. Click the **Change Password** button and select a password.
    - The password must be 10 characters
    - The password must contain letters, numbers and special characters
    - The password can not contain repeating words.
    - Basically... make it complex.
1. Click **Save**

> It is also recommended to edit your profile and add your First and Last name so the instructor and lab admins can better find your account.

## Configure Diagnostics Project

In this section, you will add your AWS Credentials to the prebuilt Diagnostics Project.

### Add AWS Secret Key to Project Keystore

To interact with AWS via API, PagerDuty RBA can securely store and use AWS secrets through it's [key storage](https://docs.rundeck.com/docs/manual/key-storage/key-storage.html).
From within the project page navigation panel, click on "Project Settings" followed by "Key Storage".

<img style='border:1px solid #327af6' src="/images/project-key-storage.png" />

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

### Place AWS Credentials in Project Configuration

Navigate to **Project Settings -> Edit Configuration** and click on **Edit Configuration File**:

![](/images/edit-project-config.png)

Find the line in the file: **`project.aws.access_key`** and replace the value with your AWS Access Key.

Then find the line in the file **`project.aws.secret_key_path`** and replace the value with the Key Storage path copied from the previous step.

The lines in the file should now look similar to this:
```
    project.aws.access_key=AKIAQMZZURQOO7SFOPOD
    proejct.aws.secret_key_path=keys/project/AWS-PD-ACMECORP-GIRAN/aws-secret-key
```

Click **Save** at the bottom of the page.
