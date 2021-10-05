---
title: "CloudWatch Integration"
chapter: true
weight: 2
---

## CloudWatch Integration

### Welcome

In this chapter, we will set up Cloudwatch to alarm when the sample application is unreachable and then send an event to PagerDuty.

PagerDuty can accept events from hundreds of monitoring systems. Even better, it does not expect each event to have the same format, but will accept anything. To make this easier, PagerDuty has built over 500 integrations to better understand those formats. 

In PagerDuty, the way to configure a private ingestion point, we would first create a Service. A Service is a configuration object for a monitored system or subsystem, like Payment Processing, the Checkout Application Server, or the Inventory Database for example. A Service might have more than one kind of integration associated with it. 

Then, the monitoring system would be directed to send events to that integration end point. This is typically done via an HTTPS POST.

For a CloudWatch Alarm, a notification can be pushed to a Simple Notification Service (SNS) Topic. We would configure a subscription to that Topic that POSTs the event to the correct integration in PagerDuty.

### Learning Objectives
- Create a PagerDuty Service with a CloudWatch Integration 
- Create an SNS Topic
- Create a Notification on the SNS Topic that sends an event to PagerDuty
- Create a new CloudWatch Alarm
