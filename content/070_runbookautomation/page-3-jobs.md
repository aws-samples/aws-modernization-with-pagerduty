---
title: "Create and Execute Automation Jobs"
chapter: true
weight: 3
---

## Create and Execute Automation Jobs

In this section, we will describe what a PagerDuty RBA Job is, as well as how to create and run a job to collect CloudWatch logs.

### What is a Job?

PagerDuty RBA jobs provide a means to encapsulate a process. A job is a configuration representing input options, the steps in the process, filter expressions where those steps will execute, and execution control parameters that specify if steps are run in parallel, or what to do if an error occurs in one of the steps. PagerDuty RBA lets you organize and execute jobs and observe the progress as the job is running. You can also view a list of the currently running jobs or drill down to see the output of individual executing steps.

### Why create a Job?

- You might find certain command executions are done repeatedly, and perhaps, represent what has become a routine procedure.
- Another user in your organization needs a simple self-service interface to run a procedure across a set of resources.
- Routine processes need to be encapsulated and become the basis for other routine procedures.
