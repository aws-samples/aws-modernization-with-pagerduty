---
title: "Response Plays"
chapter: true
weight: 2
---

## Response Plays

### PagerDuty Response Plays

A Response Play is a collection of actions that a Responder might take, kind of like a macro. A Response Play can perform one or more of these actions:

- Add a Conference Bridge and Conference URL
- Invite a preset group of on-call responders or named responders to collaborate on this incident
- Subscribe one or more individuals or teams of Business Stakeholders to this incident so that updates will reach them
- Send out a preset update message to the Business Stakeholders

Since a responder might typically need to perform some or all of these at the same time, a Response Play makes this easy.  By naming it appropriately, the responder can easily choose the right people, the right message and the right conference bridge information once and save time when in the moment.  

### For this exercise

Suppose then that we want a certain set of Business Stakeholders to receive a message that a Service they care about is having an issue. We might want to run that Response Play when the incident triggers. However, not for EVERY incident, just the incidents with a Priority "P1". We might have a second Response Play for "P2" incidents.  Lastly, we might have a third one that sounds an "all clear" for "P1" incidents when it is resolved.

To that end, we can create three Response plays for use with our Quickstart. The Parameters for the CloudFormation template will ask for IDs of the three plays.

### Create a Response Play for P1 Incidents

Let's create the first Response Play.  This one will run when a new Incident is created and the Incident is a P1.

For simplicity's sake, it will do two things: Add you to the list of Business Stakeholders and send a message.

{{% notice info %}}
For additional documentation on how to create a Response Play click [here](https://support.pagerduty.com/docs/response-automation#create-a-response-play).
{{% /notice %}}

First, choose the Automation menu, then Response Plays.

![](/images/resp_1.png)

Then click the blue button  "+ New Response Play"

![](/images/resp_2.png)

Name the new Response Play "P1 Play" and then scroll down.

![](/images/resp_3.png)

Check the box next to "Subscribe people who..." and then find yourself in the box underneath.

Then, check the box next to "Publish a status update..." and enter the message "`We have a new P1 Issue. Update in 15 minutes.`"

{{% notice tip %}}

The radio button under "Who can run this play on demand?" should be "No one" since we are going to run this automatically.

{{% /notice %}}

### Create a second Response Play for P2 Incidents

Use the __same steps__ as above for a new Response Play but change the name and the Message to send as:

- Name: "`P2 Play`"
- Message: "`We have a new P2 Issue. Update in 30 minutes.`"

### Create a third Response Play for Resolving Incidents

Use the __same steps__ as above for a new Response Play but change the name and the Message to send as:

- Name: "`Resolve Play`"
- Message: "`We have resolved this issue. Postmortem will be published within 3 days.`"


