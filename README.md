Nurture import
====

This is just a simple Ruby script that imports contacts from the "Nurture" stage of Pipedrive into the "Nurture" list in our `dobtco_marketing` Sendgrid account.

### How it works

1. It grabs the emails current on the nurture list
2. It grabs the emails of any participants of a deal that's in Pipedrive's "nurture" stage: [see a screenshot](https://dobt-captured.s3.amazonaws.com/ajb/Smithsonian_Institute_deal_-_Deals_2016-08-23_15-51-30.png)
3. Any emails that exist in the list, but not in the pipeline, are destroyed
4. Any emails that exist in the pipeline, but not in the list, are added

### How it's deployed

This script is deployed to Heroku, and runs daily via Heroku Scheduler.

Currently, there is no CI configured -- if changes are made, it must be re-deployed manually.
