---
title: "Trigger an Incident"
chapter: true
weight: 6
---

## Trigger an Incident

1. Navigate to the URL in the Sample Application CloudFormation output and verify it is running.

1. Stop the EC2 instance.

    - Enter the phrase "`the bird`" into the box under "Enter The Word" and click Submit ![](/images/shutdown_service.png)

1. Navigate to the URL in the Cloudformation output and verify it is NOT running.

1. A PagerDuty Incident should be created in about 2 minutes.

1. Restart the EC2 instance in the EC2 Console.

1. The incident should AUTOMATICALLY be resolved in about 2 1/2 minutes.

