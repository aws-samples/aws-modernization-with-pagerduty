---
title: "Create a Cloudwatch Alarm"
chapter: true
weight: 44
---

## Create a Cloudwatch Alarm

In this section we are going to walk through how to create an AWS CloudWatch Alarm.

We start in our AWS Console. In the main AWS Console Window, use the search bar to look for ”CloudWatch”.

![](/images/cw_alarm1.png)

In the AWS CloudWatch console, click “Alarms” on the left side pane.

Then, click the “Create Alarm” button on the right hand side.

![](/images/cw_alarm2.png)

Under “Specify metric and conditions”, click “Select Metric”. This will open the metrics selection page.

![](/images/cw_alarm3.png)

In our scenario we want to track how many unhealthy hosts we have in our Application Load Balancer (ALB) Target Group.

For that we will select the “UnhealthyHostCount” Metric,
Under “ApplicationELB -> Per AppELB, Per TG Metrics”
Then click “Select Metric” 

{{% notice warning %}}
Make sure to select the correct Load Balancer Name from the list
{{% /notice %}}

![](/images/cw_alarm4.png)

In the Metric configuration window we can set the period of sampling for our metric.
For our scenario, let's change the sampling period to 1 minute.

Then, scroll down to the next part of the configuration

![](/images/cw_alarm5.png)

Under conditions, we need to set what triggers our alarm. In our case we want to the alarm to trigger when we have at least __one__ Unhealthy Host on our LB.

For that we will set our condition to “Greater/Equal”.

And give it a value of “1”

Then we click Next.

![](/images/cw_alarm6.png)

Now we set our notifications, for our scenario, we want to send this alarm to PagerDuty.

So we click the “Add notification” button,

And configure our Alarm notification to send a trigger while its “In alarm” state. And then select our SNS topic for PagerDuty.


![](/images/cw_alarm7.png)

We also want to send the OK trigger to PagerDuty , When the alarm is longer firing.
For that we will create another notification, by clicking the “Add notification” button.

And this time selection “OK” as our alarm trigger,

And select the same SNS Topic. After that we can scroll down and click “Next”

![](/images/cw_alarm8.png)

In the last part of the setup add the “Alarm Name” that will displayed, and the description. Finally we click “Next” and go the overview page.

![](/images/cw_alarm9.png)

In the review page we can verify all the details of our alarm.
And edit them in case we need to.

Finally, we click “Create Alarm” on the bottom.

![](/images/cw_alarm10.png)

Now we have returned back to the main ”CloudWatch” page.

And we see our new alarm.

![](/images/cw_alarm11.png)


{{% notice warning %}}
<p style='text-align: left;'>
The examples and sample code provided in this workshop are intended to be consumed as instructional content. These will help you understand how various AWS services can be configured to work with PagerDuty.
</p>
{{% /notice %}}