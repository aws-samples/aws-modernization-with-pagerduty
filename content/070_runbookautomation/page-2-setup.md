---
title: "Setup Project"
chapter: true
weight: 2
---

## Setup Project

In this section, we will describe what a PagerDuty Runbook Automation (RBA) project is, as well as create and configure a project for this workshop.

### What is a Project?

A project is a place within PagerDuty RBA to separate management activity. All PagerDuty RBA activities occur within the context of a project. Multiple projects can be maintained on the same PagerDuty RBA instance.

Projects are independent from one another, so you can use them to organize unrelated systems within a single PagerDuty RBA instance. This can be useful for managing different teams, infrastructures, environments or applications.

### Create Project

Log into PagerDuty RBA using the credentials provided to you by your PagerDuty representative.

![](/images/pd_rba_login.png)

Once you have logged in, click on "New Project" to bring up the project creation page.  
Define the project name using the format `AWS-PD-COMPANYNAME-USERNAME` and click on "Create" to create the project for this workshop.

![](/images/pd_rba_project_setup_1.png)

### Add AWS Secret Key to Project Keystore

To interact with AWS via API, PagerDuty RBA can securely store and use AWS secrets through it's [key storage](https://docs.rundeck.com/docs/manual/key-storage/key-storage.html).
From within the project page navigation panel, click on "Project Settings" followed by "Key Storage".

![](/images/pd_rba_project_setup_2.png)

Click on "Add or Upload a Key" to bring up key storage modal.

![](/images/pd_rba_project_setup_3.png)

Ensure that key type is set to "Password" and paste in your AWS Secret Key under the "Enter text" input field, along with a name/alias for reference.

![](/images/pd_rba_project_setup_4.png)

Once entered, click on "Save" to upload and store your secret; this will be visible on page refresh.

![](/images/pd_rba_project_setup_5.png)
