---
title: "AWS PagerDuty Workshop"
chapter: true
weight: 1
---

## AWS PagerDuty Workshop

### Welcome

PagerDuty enables teams to unlock AWS’s unprecedented scale and agility by helping manage complex transitions from siloed and centralized approaches to multiple, distributed teams and hybrid infrastructure. It helps drive changes across your people, technology, and operational processes to ensure your cloud migration journey is painless, agile, and invisible to your customers.

By ingesting alerts from your monitoring tools, ITSM tools, ChatOps tools, PagerDuty becomes the central nexus of your Incident Management process. This gives you the ability to automate those processes so that you are more resource efficient, reducing time and toil for your responders, reducing cost for your business owners and increasing availability for your customers. All of which contributes to building a reputation of brand trust and product reliability in the marketplace.

This technical workshop will help you to understand how PagerDuty can consume CloudWatch Alarm notifications as alerts in order to mobilize the right teams, leverage EventBridge to take automated action and understand use cases other than Infraastructure and Application monitoring.

### Learning Objectives
- How to configure PagerDuty to receive CloudWatch alarm Notifications as Alerts
- Leverage EventBridge to take action from PagerDuty
- Send Security alarms from SecurityHub 

{{% notice warning %}}
<p style='text-align: left;'>
The examples and sample code provided in this workshop are intended to be consumed as instructional content. These will help you understand how various AWS services can be configured to work with PagerDuty.
</p>
{{% /notice %}}