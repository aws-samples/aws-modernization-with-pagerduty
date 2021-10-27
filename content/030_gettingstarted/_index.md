---
title: "Getting Started"
chapter: true
weight: 3
---

## Getting Started

### Welcome

In this chapter, we will set up the environments needed for this Workshop. 

In order to demonstrate sending a CloudWatch alarm to PagerDuty, we need to have:

1. A PagerDuty account to receive the alert
2. An AWS-based system that can fail. 

First, we will create a new PagerDuty Developer account. This type of account is designed for those who are interested in working with PagerDuty's integrations and configurations from a developer standpoint.  It is not meant to be used in production to monitor live systems.

Secondly, we will use CloudFormation to create an EC2 instance with an HTTP Web Server that can be taken down at will. 

A well-architected Web Server should sit on a private network and be serviced by a load-balancer. The load-balancer should sit on a public network. The CloudFormation template will require this kind of setup.  If this is difficult or inconvenient for you to set up, we also provide a Virtual Private Cloud (VPC) CloudFormation template to do this for you.

### Learning Objectives
- Set up a PagerDuty Developer Account
- Optionally create a VPC for the simple application
- Create an example application in our AWS environment