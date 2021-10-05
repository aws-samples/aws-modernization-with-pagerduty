---
title: "Module Summary"
chapter: true
weight: 6
---

## Module Summary

In this section we learned: 

- Why we would use the EventBridge service
- How to connect PagerDuty to an EventBridge Data source
- How to build a Rule to restart an EC2 instance

### What did we build?

- We have a running EC2 instance with a Web Server
- CloudWatch has an Alarm that checks the health of the Web Server's endpoint. 
- When the Web Service is not running (after you type "the bird" into the web page) it will cause an Alarm to go into "In Alarm" in CloudWatch
- The CloudWatch Alarm will send a Notification to a SNS Topic. 
- The SNS Topic will push an HTTPS POST to the PagerDuty Service we created.
- PagerDuty will create an Incident in that Service.

#### Up until here, it's the same as before - EventBridge starts here:

- For every lifecycle event (Trigger, Acknowledge, Resolve, Custom, etc.), PagerDuty will push an event to EventBridge 
- The EventBridge Event Bus will receive that event and the Rules on that Bus (in our case only one) will fire.
- The Rule we wrote will filter out all events except for the "Custom" one which comes from a menu item that is clicked.
- The Rule will run the Reboot EC2 API action to restart our EC2 Server and force the Nginx service to run again.
- When the CloudWatch Alarm returns to the "OK" state, it will send another Notification to the SNS Topic which is then pushed to the same PagerDuty Service.
- When the PagerDuty Service receives it, the Incident will be Resolved.