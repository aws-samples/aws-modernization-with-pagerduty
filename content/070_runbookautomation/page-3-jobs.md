[comment]: <> (---)

[comment]: <> (title: "Create Automation Jobs")

[comment]: <> (chapter: true)

[comment]: <> (weight: 3)

[comment]: <> (---)



[comment]: <> (#### Connection)

[comment]: <> (- Region: Select `us-east-1` under the dropdown to populate)

[comment]: <> (#### Query Settings)

[comment]: <> (- CloudWatch Log Group: Set to `/ec2/nginx/logs`)

[comment]: <> (- Unit of Time: Select `Minutes` under the dropdown to populate)

[comment]: <> (- Past Time Range: Enter `5` for 5 minute lookback)

[comment]: <> (#### CloudWatch Query)

[comment]: <> (- Query String: Copy and paste the following query)

[comment]: <> (  ```)

[comment]: <> (  fields @timestamp, @message)

[comment]: <> (  | sort @timestamp desc)

[comment]: <> (  | limit 100)

[comment]: <> (  ```)

[comment]: <> (#### Step Label)

[comment]: <> (You can provide a friendly label for job steps - i.e. `Get NGINX access.log`)

[comment]: <> (#### Screenshot of Job Step)

[comment]: <> ({{% notice info %}})

[comment]: <> (<p style='text-align: left;'>)

[comment]: <> (Don't forget to save the job step itself - any modifications to any job steps will require the intermediate save step.)

[comment]: <> (</p>)

[comment]: <> ({{% /notice %}})

[comment]: <> (![]&#40;/images/pd_rba_job_setup_5.png&#41;)

[comment]: <> (### Complete Creation of Job)

[comment]: <> ({{% notice info %}})

[comment]: <> (<p style='text-align: left;'>)

[comment]: <> (Once you have updated the job step details and clicked on "Save", you will need to save down the job definition itself.  )

[comment]: <> (Click on "Create" within the outer scope at the bottom to create and save the job.)

[comment]: <> (</p>)

[comment]: <> ({{% /notice %}})

[comment]: <> (![]&#40;/images/pd_rba_job_setup_6.png&#41;)

[comment]: <> (Once the job has been created, PagerDuty RBA will redirect you to the job execution page.)

[comment]: <> (![]&#40;/images/pd_rba_job_setup_7.png&#41;)
