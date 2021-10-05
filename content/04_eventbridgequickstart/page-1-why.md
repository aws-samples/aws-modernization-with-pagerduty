---
title: "What is it?"
chapter: true
weight: 1
---

## What is this Quickstart?

### What is the PagerDuty EventBridge Quickstart?

This Quick Start deploys Amazon EventBridge integration with PagerDuty response plays on the Amazon Web Services (AWS) Cloud. PagerDuty [response plays](https://support.pagerduty.com/docs/response-automation) are packages of incident actions you can apply during an incident's lifecycle.

In this deployment, a software as a service (SaaS) event bus receives event notifications from PagerDuty and delivers them to Amazon EventBridge. An EventBridge rule evaluates incidents and invokes an AWS Step Functions workflow. The Step Functions workflow calls a Lambda function that runs the appropriate PagerDuty response play based on the incident's priority level.

![](/images/quickstart_diagram.png)

### Event flow

For every Incident that is created on a service that has this EventBridge configuration set, it will send a webhook to EventBridge as an event. That event will have in it information about the State and Priority of the Incident. The Lambda code will check if the Incident being triggered or resolved (i.e. opened or closed).

If it is triggered, it will check the Priority value. When it is a P1, it will execute one response play and if it is P2, the it will execute a different one. 

In a similar way, if a P1 incident has been resolved, it will run the associated response play.

All of this is automatic and no user intervention is required.

{{% notice info %}}

To access this Quickstart directly click [here](https://aws.amazon.com/quickstart/eventbridge/pagerduty-response-play/).

{{% /notice %}}