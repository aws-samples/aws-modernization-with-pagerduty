---
title: "Create a VPC"
chapter: true
weight: 13
---

{{% notice note %}}
<p style='text-align: left;'>
This is an optional step, if you already have a VPC setup you can skip this step.
</p>
{{% /notice %}}


## Provision VPC

   [Click here to deploy using CloudFormation template](https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/create/template?stackName=Workshop-PD-VPC&templateURL=https://modernization-workshop-bucket.s3-us-west-2.amazonaws.com/cfn/master-stacks/vpc-only.yaml)

   - Create stack, click **Next**
   - Specify stack details, click **Next**
   - Configure stack options, click **Next**
   - Scroll to bottom section under **Capabilities** and check both boxes and click **Create stack**


This template deploys a VPC, with a pair of public and private subnets spread
across two Availability Zones. It deploys an internet gateway, with a default
route on the public subnets. It deploys a pair of NAT gateways (one in each AZ), and default routes for them in the private subnets.

This will take a couple of minutes to deploy.