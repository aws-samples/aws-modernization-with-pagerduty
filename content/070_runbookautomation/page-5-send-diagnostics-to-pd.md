---
title: "Present Diagnostics in PagerDuty"
chapter: true
weight: 5
---

## Present Diagnostics in PagerDuty

In this section, we will execute send the diagnostics that were retrieved from CloudWatch Logs to the PagerDuty Incident.  
For this workshop, you will trigger the diagnostics manually - though in practice the automation would be invoked by integrating with [Automation Actions](https://www.pagerduty.com/platform/automation/actions/)
or [Event Orchestration](https://support.pagerduty.com/docs/event-orchestration).  However, these topics are beyond the scope of this workshop.

#### Generate PagerDuty API Token

In the PagerDuty web app:

1. Navigate to **Integrations ->**  **API Access Keys** and click **Create New API Key**.<br>

2. Enter a **Description** that will help you identify the key later on. If you would like it to be read-only, check the **Read-only** option.<br>
3. Click **Create Key**.<br>
4. A unique **API key** will be generated. Copy it to a safe place, as you will not have access to copy this key again. Once it has been copied, click **Close**.<br>

{{% notice info %}}

<p style='text-align: left;'>
If you lose a key you will need to delete it and create a new one.
</p>
{{% /notice %}}

#### Add PagerDuty API Token to Runbook Automation

From within the project page navigation panel, click on **Project Settings** followed by **Key Storage**:
<img style='border:1px solid #327af6' src="/images/project-key-storage.png" />

Click on **+ Add or Upload a Key**.  For the **Key Type** select **Password**.  Paste the PagerDuty API Token into the **Enter Text** field:

<img style='border:1px solid #327af6' src="/images/pd-api-token.png" />

Click **Save**.

Navigate to the **Jobs** tab, and click on **Enrich Incident with CloudWatch Logs**:

<img style='border:1px solid #327af6' src="/images/select-job-to-enrich-incidents.png" />

In the upper-right, click on **Action** and select **Edit this Job...**

Click on the **Workflow Tab** and click into **Step 2**:
<img style='border:1px solid #327af6' src="/images/rba-job-step-2.png" />

Click **Select** to the right of the **API Key** field, and select the PagerDuty API Token you saved in Key Storage.

<img style='border:1px solid #327af6' src="/images/rba-job-set-api-token.png" />

Click **Save** to save the Job Step.  Click **Save** to save the Job definition.

<br><br>

#### Invoke Automation to Post Diagnostics to PagerDuty Incident

In the **PagerDuty Incidents** interface, hover over **Incidents** in the top navigation menu, and select **All Incidents**.

Click on one of the incidents that was triggered from the previous lessons.

In the **URL** of the incident page, copy the string that follows **/incidents/**:

<img style='border:1px solid #327af6' src="/images/pd-incident-id.png" />
In the example above, the **Incident ID** is **Q0D92FIF7DT9RM.**

Navigate back to the **Runbook Automation** interface.  You should be on the **Enrich Incident with CloudWatch Logs** screen:

<img style='border:1px solid #327af6' src="/images/diagnostics-job-options.png" />

In the **PagerDuty User Email** field, place in the email address you used to set up your PagerDuty account.

Paste in the **Incident ID** captured in the previous step into the **PagerDuty Incident ID** field.

Click on **Run Job Now**.  This will invoke the automation to fetch the CloudWatch logs and add them to the timeline of the PagerDuty incident:

<img style='border:1px solid #327af6' src="/images/nginx-logs-pd-incident.png" />

