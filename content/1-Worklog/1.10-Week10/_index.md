---
title: "Week 10 Worklog"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---


### Week 10 Objectives:

* Get familiar with deploying the DMS project infrastructure using the AWS CDK.
* Deploy identity, storage, database, API, and event processing components sequentially.
* Configure security, monitoring, and frontend distribution for the system.
* Verify deployment results and the output parameters of the CDK Stack.

### Tasks to implement this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Prepare the AWS CDK deployment environment<br>- Learn about the structure of the DMS infrastructure source code<br>- **Practice:**<br>&emsp; + Clone the Repository and install dependencies<br>&emsp; + Create a `.env` file from `.env.example`<br>&emsp; + Verify alert environment variables<br>&emsp; + Build the TypeScript Lambda source code<br>&emsp; + Check the `dist` output folder<br>&emsp; + Execute CDK Bootstrap | 22/06/2026 | 22/06/2026 |  |
| 3 | - Deploy Identity, Storage, and Database layers<br>- **Practice:**<br>&emsp; + Create an Amazon Cognito User Pool and App Client<br>&emsp; + Create system user groups<br>&emsp; + Create FrontendBucket, QuarantineBucket, and DocumentsBucket<br>&emsp; + Enable Block Public Access and configure necessary CORS settings<br>&emsp; + Create an Amazon DynamoDB table<br>&emsp; + Configure TTL, PITR, and required indexes | 23/06/2026 | 23/06/2026 |  |
| 4 | - Deploy Compute and API layers<br>- **Practice:**<br>&emsp; + Review the source code of core Lambda Functions<br>&emsp; + Deploy Lambda functions for user and document management<br>&emsp; + Deploy Lambda functions for creating Upload/Download Intents<br>&emsp; + Deploy the Upload Processor Function<br>&emsp; + Create Amazon API Gateway<br>&emsp; + Integrate the Cognito Authorizer with API Routes | 24/06/2026 | 24/06/2026 |  |
| 5 | - Deploy Security, Event, and Monitoring layers<br>- **Practice:**<br>&emsp; + Configure GuardDuty Malware Protection for the QuarantineBucket<br>&emsp; + Create an EventBridge Rule to receive file scan results<br>&emsp; + Connect EventBridge to the Upload Processor Function<br>&emsp; + Create a CloudFront Distribution for the FrontendBucket<br>&emsp; + Configure Origin Access Control (OAC)<br>&emsp; + Create CloudWatch Log Groups and an SNS Topic for alerting | 25/06/2026 | 25/06/2026 |  |
| 6 | - Deploy and verify the entire DMS infrastructure<br>- **Practice:**<br>&emsp; + Run `cdk synth` to check the Template<br>&emsp; + Review changes using `cdk diff`<br>&emsp; + Deploy the CDK Stack to the `dev` environment<br>&emsp; + Monitor CloudFormation Stack status<br>&emsp; + Record UserPoolId, UserPoolClientId, ApiUrl, and CloudFrontUrl<br>&emsp; + Verify resources on the AWS Console<br>&emsp; + Document and troubleshoot basic deployment errors | 26/06/2026 | 26/06/2026 |  |

### Week 10 Achievements:

* Prepared the deployment environment for the project using the AWS CDK.
* Understood the roles of the following commands:
  * `cdk bootstrap`
  * `cdk synth`
  * `cdk diff`
  * `cdk deploy`
* Built the Lambda source code and verified the output directory prior to deployment.
* Successfully deployed the Amazon Cognito User Pool, App Client, and user groups:
  * EMPLOYEE
  * DEPARTMENT_ADMIN
  * SYSTEM_ADMIN
* Created three S3 Buckets dedicated to:
  * Hosting the Frontend interface.
  * Quarantining newly uploaded files.
  * Storing verified secure documents.
* Configured appropriate Block Public Access and CORS settings for the Buckets.
* Created a DynamoDB table utilizing a Single-table Design model.
* Configured TTL, Point-in-Time Recovery (PITR), and indexes to support querying.
* Successfully deployed the core Lambda Functions of the DMS system.
* Created the API Gateway and integrated the Cognito Authorizer.
* Understood the workflow of generating Presigned URLs for document upload and download operations.
* Configured GuardDuty Malware Protection for the QuarantineBucket.
* Created an EventBridge Rule to route scanning results to the Upload Processor Function.
* Understood how the Upload Processor updates document statuses:
  * `READY`
  * `REJECTED`
  * `FAILED`
* Created a CloudFront Distribution connected to the FrontendBucket via Origin Access Control (OAC).
* Configured CloudWatch Logs and an SNS Topic for monitoring and alerting.
* Successfully deployed the CloudFormation Stack for the development environment.
* Recorded critical CDK Outputs required for configuring the Backend and Frontend.
* Verified the operational status of resources on the AWS Console post-deployment.