---
title: "Create an Event Rule"
chapter: true
weight: 54
---

## Create an Event Rule

In this section we are going to walkthrough how we to setup Rules, for our Amazon event Bridge connection between our AWS account and our PagerDuty account.

We start in our AWS console, on the Amazon Event Bridge page.
(Services → Amazon Event Bridge).

From the left hand side under ”Event” we click on “Rules”

![](/images/ebrules_1.png)


### Create a new Event Rule
From the drop down under “Select event bus” we choose the Event Bus we created in the last section.

And click ”Create rule”.

![](/images/ebrules_2.png)

### Name the Rule
We start by giving our rule a name and a description.

Call it "RestartEC2".

![](/images/ebrules_3.png)

### Define the event pattern 
Next we define the pattern of event that will trigger this rule.

In our case, we have only one type of event that comes from our PagerDuty account that we want to associate with our rule.

So we select “Custom pattern”

Paste in this JSON to the Event pattern:

	{
		"detail-type": [
			"PagerDuty Webhook"
		],
		"detail": {
			"event": ["incident.custom"]
		}
	}


Click Save.

![](/images/ebrules_4.png)

### Verify the event bus 
The Select event bus section should already be correctly filled in.

Next, scroll down to “Select Targets”.



### Define what to trigger

Here we define the action that we want to trigger from PagerDuty, and the target/targets for that.

We can select we from various action from EC2 API Calls to Lambda Invocations.

In our demo, we are going to trigger a reboot. For that we select "EC2 Rebootinstances API call",
input our target Instance ID, and create a new role for this trigger. 

Then scroll down and click “Create”

![](/images/ebrules_5.png)

### Verify the rule

Back on the rules page we will see our newly created rule.

![](/images/ebrules_6.png)


