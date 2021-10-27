---
title: "EventBridge and PagerDuty"
chapter: true
weight: 5
---

## EventBridge and PagerDuty

### Welcome

In this chapter, we will create an EventBridge integration to allow a responder to take action from PagerDuty during an Incident.

PagerDuty is the gold standard for mobilizing the right people when an incident occurs which needs someone to get eyes on it right away. 

PagerDuty also shows its value in taking the work out of *managing the incident* itself. So much of a responder's time is taken up by performing common actions that are easily automatable. Common actions like finding and notifying other teams to assist, keep business stakeholders apprised of resolution progress, or even taking remediation/diagnostic actions on the systems in question.

PagerDuty can take actions in AWS by means of sending an event to EventBridge. EventBridge can call serverless scripts, restart EC2 instances, check the status of services and more. If we connect that to a PagerDuty instance, the responder no longer has to work directly within AWS, but can access all those actions via a menu. 

Even better, we can configure the event to fire when an incident is created, acknowledged or resolved. This way, no human interaction is required and perhaps that action can remediate the problem before a person has to be notified.

### What we'll be doing

We will configure the EventBridge integration in PagerDuty to establish a trusted connection between the PagerDuty subdomain and an AWS Account. This creates a PagerDuty "Partner Event Source" in AWS.

Next, we will connect that Partner Event Source to an event bus which can then take some action. In our case, we can restart an EC2 instance.

### Learning Objectives
- Understand the EventBridge service
- How to connect PagerDuty to an EventBridge Data source
- How to build a Rule to restart an EC2 instance

{{% notice warning %}}
<p style='text-align: left;'>
The examples and sample code provided in this workshop are intended to be consumed as instructional content. These will help you understand how various AWS services can be configured to work with PagerDuty.
</p>
{{% /notice %}}