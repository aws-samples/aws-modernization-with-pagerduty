---
title: "Automation"
chapter: true
weight: 51
---

## Automation

### Why would we want to use EventBridge?

Amazon EventBridge is a serverless event bus that makes it easier to build event-driven applications at scale using events generated from your applications, integrated Software-as-a-Service (SaaS) applications, and AWS services. 

During the Incident management lifecycle, a responder will want to take actions to remediate problems or gather diagnostic information about the situation and environment. It is undesirable to grant specific rights to all responders for all environments for security reasons (using the principle of least-privilege). Encapsulating actions into scripts or actions and allowing only the appropriate teams to execute those (and only those) commands is a way to satisfy both the needs of the responders and the needs of the Security Team.

Since PagerDuty runs on Amazon, EventBridge is ideally placed to take actions within AWS for both remediation and diagnostics. Events generated by PagerDuty and sent to EventBridge never leave the AWS infrastructure onto the Internet and so is inherently more secure.

These events can be manually generated, say a request for deep diagnostic reports that should be run only when deemed necessary, or automatically generated, like a restart of a simple service to get the application back up even before a responder is notified. 

Let's get started!