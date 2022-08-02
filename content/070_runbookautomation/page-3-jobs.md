---
title: "Create Automation Jobs"
chapter: true
weight: 3
---

## Create Automation Jobs

In this section, we will describe what a PagerDuty RBA Job is, as well as how to create a job to collect CloudWatch logs using a pre-built plugin.

### What is a Job?

PagerDuty RBA jobs provide a means to encapsulate a process. A job is a configuration representing input options, the steps in the process, filter expressions where those steps will execute, and execution control parameters that specify if steps are run in parallel, or what to do if an error occurs in one of the steps. PagerDuty RBA lets you organize and execute jobs and observe the progress as the job is running. You can also view a list of the currently running jobs or drill down to see the output of individual executing steps.

### Why create a Job?

- You might find certain command executions are done repeatedly, and perhaps, represent what has become a routine procedure.
- Another user in your organization needs a simple self-service interface to run a procedure across a set of resources.
- Routine processes need to be encapsulated and become the basis for other routine procedures.

### Create Job

From within the project page navigation panel, click on "Jobs", followed by "Create a new Job", this will bring up a job creation form.

![](/images/pd_rba_job_setup_1.png)

Under the "Details" tab, set Job Name to `Get NGINX Access Logs via AWS CloudWatch`.

![](/images/pd_rba_job_setup_2.png)

### Create Job Step

Click on the "Workflow" tab and then scroll down to "Add a Step" - select "Workflow Steps" tab and then scroll down and select the "Aws / CloudWatch / Logs" plugin step.

![](/images/pd_rba_job_setup_3.png)

![](/images/pd_rba_job_setup_4.png)

Update the job step with the following parameters listed below and click on "Save" once completed.

#### Credentials

- access keyID: AWS Access Key ID
- Secret Key: The path to the AWS Secret Key uploaded earlier - you may use the select button to navigate for this path.

#### Connection

- Region: Select `us-east-1` under the dropdown to populate

#### Query Settings

- CloudWatch Log Group: Set to `/ec2/nginx/logs`
- Unit of Time: Select `Minutes` under the dropdown to populate
- Past Time Range: Enter `5` for 5 minute lookback

#### CloudWatch Query

- Query String: Copy and paste the following query
  ```
  fields @timestamp, @message
  | sort @timestamp desc
  | limit 100
  ```

#### Step Label

You can provide a friendly label for job steps - i.e. `Get NGINX access.log`

#### Screenshot of Job Step

{{% notice info %}}

<p style='text-align: left;'>
Don't forget to save the job step itself - any modifications to any job steps will require the intermediate save step.
</p>
{{% /notice %}}

![](/images/pd_rba_job_setup_5.png)

### Complete Creation of Job

{{% notice info %}}

<p style='text-align: left;'>
Once you have updated the job step details and clicked on "Save", you will need to save down the job definition itself.  
Click on "Create" within the outer scope at the bottom to create and save the job.
</p>
{{% /notice %}}

![](/images/pd_rba_job_setup_6.png)

Once the job has been created, PagerDuty RBA will redirect you to the job execution page.

![](/images/pd_rba_job_setup_7.png)
