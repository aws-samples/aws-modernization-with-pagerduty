---
title: "Module Summary"
chapter: true
weight: 6
---

## Module Summary

In this section, we learned:

- What the EventBridge Quickstart for PagerDuty is
- How to create a Stack that consumes the EventBridge events from PagerDuty

### What did we build?

- We created a CloudFormation Stack that built for us:
    - An Event Bus on the Partner Event Source from PagerDuty
    - A Rule on that Event Bus
    - A Lambda object with Python code
    - An IAM Role to allow the Lambda object to run

- When PagerDuty sends a trigger event to EventBridge, the Lambda code will check if it's a P1 or P2 and if so, run the appropriate Response Play. 

- When PagerDuty sends a resolved event to EventBridge, the Lambda code will check if it's a P1 and if so, run the Resolved Response Play.

{{% notice warning %}}
Be sure to Delete the CloudFormation Stack we just built to destroy the objects that were created so that no further costs are incurred!
{{% /notice %}}