---
title: "Execute Automation Jobs"
chapter: true
weight: 4
---

## Execute Automation Jobs

In this section, we will execute the PagerDuty RBA job we created previously and describe the outputs.

### Running Jobs

If you're not already redirected, navigate back to your project and click on "Get NGINX Access Logs via AWS CloudWatch" job.
![](/images/pd_rba_job_execution_1.png)
![](/images/pd_rba_job_setup_7.png)

Execute the job by clicking on "Run Job Now". This will redirect you to the job execution page and will update periodically until the job has completed.

![](/images/pd_rba_job_execution_2.png)

![](/images/pd_rba_job_execution_3.png)

Under the nodes panel, expand the node and job step by clicking on the ">" icons.  
You will then see the stdout of the NGINX logs from CloudWatch.

![](/images/pd_rba_job_execution_4.png)

You can further verify the output of these logs by navigating to the URL in the Sample Application CloudFormation output and rerunning the job again.
i.e. you can see `access.log` updated when a user has accessed the Sample Application in the browser.

![](/images/pd_rba_job_execution_5.png)
