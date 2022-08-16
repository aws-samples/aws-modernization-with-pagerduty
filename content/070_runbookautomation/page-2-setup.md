---
title: "Import Diagnostics Project"
chapter: true
weight: 2
---

## Import Diagnostics Project

In this section, we will describe what a PagerDuty Runbook Automation (RBA) project is, as well as import an existing project with prebuilt automation for diagnostics.

### What is a Project?

A project is a place within PagerDuty RBA to separate management activity. All PagerDuty RBA activities occur within the context of a project. Multiple projects can be maintained on the same PagerDuty RBA instance.

Projects are independent from one another, so you can use them to organize unrelated systems within a single PagerDuty RBA instance. This can be useful for managing different teams, infrastructures, environments or applications.

### Create Project

Log into PagerDuty RBA using the credentials provided to you by your PagerDuty representative.

![](/images/pd_rba_login.png)

Once you have logged in, click on "New Project" to bring up the project creation page.  
Define the project **name** as **`automated-diagnostics`** and the **label** as **`Automated Diagnostics`**.  Click on "Create" to create the project for this workshop.

![](/images/pd_rba_project_setup_1.png)

#### Download and Import the Project Template

You can download the existing Diagnostics Project template by clicking [here](https://github.com/rundeckpro/automated-diagnostics-project/releases/download/1.1/automated-diagnostics-1.1.zip) and unzip the downloaded file.

In the PagerDuty RBA project created in the previous set, click on **Project Settings** and then **Import Archive**:
![](/images/import_project_template.png)

In the **Choose a Rundeck archive** section, click **Choose File** and select the **`automated-diagnostics-xxxxxx-xxxxx.rdproject.jar`** file from the downloaded zip folder.

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
