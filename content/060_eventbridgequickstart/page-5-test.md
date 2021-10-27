---
title: "Trigger an Incident"
chapter: true
weight: 65
---

## Trigger a P1 Incident

1. Manually Create an Incident in PagerDuty with Priority of P1 on the Service it was set up on
    - Click the Incidents menu in the top bar.
![](/images/p1_inc0.png)
    - Click the "+ New Incident" button on the right-hand side.
![](/images/p1_inc1.png)
    - In the dialog, select the Service you are using, enter a Title for the Incident and Choose P1 for the Priority
{{% notice warning %}}  
Be sure to choose P1 for the Priority or the EventBridge integration will not fire.
{{% /notice %}}
![](/images/p1_inc2.png)
    - Click the "Create Incident" button on the bottom of the dialog.
![](/images/p1_inc3.png)

1. Check the Incident Timeline and check to see that the right Response play has run
    - You should get a Status Message written on the Status tab
1. Resolve the Incident and check to see that the right Response play has run
    - You should get a Status Message written on the Status tab

## Trigger a P2 Incident

1. Manually Create an Incident in PagerDuty with Priority of P2 on the Service it was set up on
    - Follow the instructions above but select a P2 Priority instead.
1. Check the Incident Timeline and check to see that the right Response play has run
    - You should get a Status Message written on the Status tab

