---
title: "Setup AWS Event Bus"
chapter: true
weight: 53
---

## Setup AWS Event Bus

In the AWS Console, select “Services” -> Amazon EventBridge”.

This will display the main Amazon Event Bridge screen.

On the left hand side, click on “Partner event sources” to finish our event bridge integration.

![](/images/ebaws_1.png)

### Activate the Partner Event Source
Under ”Partner Event Sources” we will see our open request for integration that came from our PagerDuty account.

In order to activate it, we will click on ”Associate with event bus” button.

![](/images/ebaws_2.png)

### Associate with an event bus
In the ”Associate with event bus” page we can verify the name and origin of the request and optionally connect this to other accounts or organizations.

To finish the setup we click “Associate”

![](/images/ebaws_3.png)

### Verify the bus is active
Back in our “Partner event sources” page, we will see that the status of event bus is now ”Active”

We have completed the Amazon Event Bridge setup.
Next, we create rules that we can trigger from our PagerDuty Account.

![](/images/ebaws_4.png)

