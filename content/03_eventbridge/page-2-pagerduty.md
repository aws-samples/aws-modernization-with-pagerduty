---
title: "Configure the Integration"
chapter: true
weight: 2
---

## Configure the Integration

In order to configure the PagerDuty EventBridge integration, you will need to know your AWS Account identifier. 

{{% notice info %}}

Instructions on how to find your Account Identifier are [here](https://docs.aws.amazon.com/general/latest/gr/acct-identifiers.html#FindingYourAccountIdentifiers).
{{% /notice %}}

### Create the Extension 
In PagerDuty, go to the Integrations menu and click Extensions.

Then click on the blue button "+ New Extension"

![Add integration](/images/eb_addext0.png)

A new blank row will appear. Click on the first cell entitled "Select an extension". Begin typing "Amazon EventBridge". Then choose it.

![Choose EventBridge integration](/images/eb_addext1.png)

On the popup, click the blue button "Open Amazon EventBridge Page".

![Add EventBridge integration](/images/eb_addext2.png)

You may need to click the "Add Service" button at the top.

A new, blank form will appear for the new integration. Enter the data as below.

* __Name__ - This is the name that will appear on the Incident Details page under the More Actions menu.
* __AWS Account ID__ - This is your account id that will establish a connection to your AWS account. Instructions on how to find it are [here](https://docs.aws.amazon.com/general/latest/gr/acct-identifiers.html#FindingYourAccountIdentifiers)
* __AWS Region__ - A region must be selected for this event 
* __Services__ - One or more PagerDuty services must be selected. An Incident that is created on any of the services selected here will allow this action to be sent to EventBridge.
* __Event Source Name__ - In the EventBridge Console, this name will be used to create the Partner Event Source.

![Fill in EventBridge integration fields](/images/eb_addext3a.png)

Click the button "Create" to complete the configuration.

The next step will be to set up AWS to do something with the event that is passed to EventBridge.

