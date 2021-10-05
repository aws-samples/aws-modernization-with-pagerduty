---
title: "Create a Simple Application"
chapter: true
weight: 4
---

## Create a Simple Application

Follow these instructions to use CloudFormation to create an environment and a web application as a sample that we use to produce Alarms.

{{% notice warning %}}
<p style='text-align: left;'>
The examples and sample code provided in this workshop are intended to be consumed as instructional content. These will help you understand how various AWS services can be configured to work with PagerDuty.
</p>
{{% /notice %}}

[Click here to deploy using CloudFormation template](https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/create/template?stackName=Workshop-PD-APP&templateURL=https://modernization-workshop-bucket.s3-us-west-2.amazonaws.com/cfn/sample-web-app/Demo-noasg.yml)

   - Create stack, click **Next**
   - Specify stack details,
      - Set the KeyName for the EC2 machine
      - Select 2 Public subnets for the Loadbalancer
      - Select the correct VPC id from the drop down
      - Select a single private Subnet where the EC2 machine will reside.
      - Finally click **Next**
   - Configure stack options, click **Next**
   - Scroll to bottom section under **Capabilities** and check both boxes and click **Create stack**

This template deploys a Loadbalancer and one EC2 machine that hosts an Nginx webserver.

This will take a couple of minutes to deploy.

When it is complete, find the Output subtab and it will show a URL for the website.  Open it in a browser to verify everything is up and running.