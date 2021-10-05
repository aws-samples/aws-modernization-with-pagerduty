---
title: "Deploy the Integration"
chapter: true
weight: 4
---

## Deploy the Integration

### Parameters of the CloudFormation Template

In your AWS Console, you will deploy the CloudFormation template provided.

The template has a set of parameters you will need to fill in while creating the CloudFormation Stack.

| Parameter | Description |
| --- | ----------- |
| Event&nbsp;source&nbsp;name | Name of the Amazon EventBridge PagerDuty event source to associate with an event bus. <br/> For example, `aws.partner/pagerduty.com/1234567890/test-event-source`. |
| Create event bus | Select Yes when no Event Bus has been created yet. Select No if there is already an existing bus. |
| PagerDuty API key | A valid REST API key in PagerDuty. |
| PagerDuty&nbsp;user&nbsp;email | Email address of a valid PagerDuty user on whose behalf to run the Response Play |
| P1 response play | Response play that is run on the creation of a P1 incident. See below. |
| P2 response play | Response play that is run on the creation of a P2 incident. See below. |
| Resolved&nbsp;response&nbsp;play | Response play that is run on the resolution of a P1 incident. See below. |

### Perform pre-requisites

To create a REST API key in PagerDuty, Use the instructions [here](https://support.pagerduty.com/docs/generating-api-keys#generating-a-general-access-rest-api-key). 

To find the id of a Response Play (required for this exercise), open the list of Response Plays.

![](/images/rp_setup1.png)

Now, find and edit the Response Play that you want to run when a P1 Incident is created. Select the id in the URL Address and copy it.

![](/images/rp_setup2.png)

Do the same for a P2 Response Play and a Resolved Response Play.

### Build the CloudFormation Stack

To begin building your CloudFormation Stack, click [here](https://fwd.aws/k54Ky?).

The deployment takes about 5 minutes to complete. EventBridge integrations are supported in all AWS Regions except the AWS GovCloud (US) Regions.




