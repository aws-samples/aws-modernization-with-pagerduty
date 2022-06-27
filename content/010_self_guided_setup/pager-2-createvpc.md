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
   - Scroll to bottom section and click **Create stack**


This template deploys a VPC, with a pair of public and private subnets spread
across two Availability Zones. It deploys an internet gateway, with a default
route on the public subnets. It deploys a pair of NAT gateways (one in each AZ), and default routes for them in the private subnets.

This will take a couple of minutes to deploy.

### Manual Setup

   In case of acccess restrctions, you can download this Cloudformation template to your local machine, and run it directly from the console.

   - Right click this link: [YAML File](https://raw.githubusercontent.com/aws-samples/aws-modernization-with-pagerduty/main/static/cfn_files/vpc.yaml) and select "Save link As" , maked sure to save the file as a .yml/yaml file.
   - Open your AWS Console, From **Services** Select **Cloudformation**
   - Click the **Create Stack** button.
   - Under **Template soruce** Select **Upload a template file** , Click **Choose file** button and select the yaml file yopu have downloaded.
   - Click **Next**.
   - Under **Stack Name** input **Workshop-PD**.
   - Under **EnvironmentName** input **Workshop**.
   - Click **Next** then **Next** again.
   - On the final page click **Create stack** to start deploying the template.

