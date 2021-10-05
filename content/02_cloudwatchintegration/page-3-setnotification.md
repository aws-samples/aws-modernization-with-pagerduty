---
title: "Set an SNS Subscription"
chapter: true
weight: 4
---

## Set an SNS Subscription

For every event places on the topic, we want to push it to PagerDuty. A Subscription on that topic can be created to HTTP POST it to your Service's CloudWatch integration.

### Create a new SNS Subscription.

On the __same SNS Topic just created__, scroll down to the bottom. The Subscriptions subtab should be selected. 

Click the orange button "Create subscription".

![](/images/subs1.png)

On this page, enter the Protocol as HTTPS.  This will cause AWS to send an HTTPS POST to PagerDuty with the Topic's events.

The Endpoint should be the Integration URL from the "Create a PagerDuty Service" step at the end.

![](/images/subs2.png)

You can safely accept the remaining defaults.

Scroll to the bottom and click the orange "Create subscription" button.

![](/images/subs3.png)

Paste in the URL from PagerDuty.

### Verify your Subscription

Verify that your subscription was created successfully.

After a moment, refresh the Subscription page. Verify that your subscription status is __not__ "Pending confirmation". 
![](/images/subs4_pending.png)

PagerDuty will automatically confirm the Subscription if your URL is correct.

You should see the status as "Confirmed".

![](/images/subs5_confirmed.png)

