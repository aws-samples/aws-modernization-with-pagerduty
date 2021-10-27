---
title: "Trigger an Incident"
chapter: true
weight: 55
---

## Trigger an Incident

1. Navigate to the URL in the Sample Application CloudFormation output and verify it is running.

1. Stop the EC2 instance.

    - Enter the phrase "`the bird`" into the box under "Enter The Word" and click Submit ![](/images/shutdown_service.png)

1. Navigate to the URL in the Cloudformation output and verify it is NOT running.

1. A PagerDuty Incident should be created in about 2 minutes.

1. Open the Incident, find the Event Details tab to see what CloudWatch sent

1. When ready to restart the EC2 instance, choose the More Actions...RestartEC2Instance menu item

1. The incident should AUTOMATICALLY be resolved in about 2 1/2 minutes.
