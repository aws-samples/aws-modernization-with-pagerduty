---
title: "Module Summary"
chapter: true
weight: 7
---

## Module Summary

In this section, we learned that AWS and PagerDuty work together so that when a problem is detected via a CloudWatch Alarm, it can send it to PagerDuty to mobilize the right team, give them relevant information on the problem and manage the incident to resolution. 

We also learned how to:

- Create a PagerDuty Service with a CloudWatch Integration 
- Create an SNS Topic
- Create a Notification on the SNS Topic that sends an event to PagerDuty
- Create a new CloudWatch Alarm
- Test that the Alarm sends a notifcation to PagerDuty

### What did we build?

- We have a running EC2 instance with a Web Server
- CloudWatch has an Alarm that checks the health of the Web Server's endpoint. 
- When the Web Service is not running (after you type "the bird" into the web page) it will cause an Alarm to go into "In Alarm" in CloudWatch
- The CloudWatch Alarm will send a Notification to a SNS Topic. 
- The SNS Topic will push an HTTPS POST to the PagerDuty Service we created.
- PagerDuty will create an Incident in that Service.
- When we manually Reboot the EC2 instance in the Console, we force the Nginx service to run again.
- When the CloudWatch Alarm returns to the "OK" state, it will send another Notification to the SNS Topic which is then pushed to the same PagerDuty Service.
- When the PagerDuty Service receives it, the Incident will be Resolved.