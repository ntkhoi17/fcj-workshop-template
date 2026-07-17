---
title: "Week 12 Worklog"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---


### Week 12 Objectives:

* Review the core security configurations of the DMS system.
* Verify authorization mechanisms, file protection, and malware scanning result handling pipelines.
* Monitor system logs, metrics, and alerting workflows.
* Clean up AWS resources after completing system testing.
* Summarize the project and audit incurred costs within the AWS account.

### Tasks to implement this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Review IAM Least Privilege practices<br>- Audit security configurations for S3 Buckets<br>- **Practice:**<br>&emsp; + Inspect the IAM Roles of core Lambda Functions<br>&emsp; + Review access permissions for DynamoDB and Amazon S3<br>&emsp; + Verify Block Public Access settings on all Buckets<br>&emsp; + Verify expiration lifecycles of Presigned PUT/GET URLs<br>&emsp; + Document permissions requiring adjustments | 06/07/2026 | 06/07/2026 |  |
| 3 | - Verify GuardDuty Malware Protection behaviors<br>- Verify user authorization rules via Amazon Cognito<br>- **Practice:**<br>&emsp; + Verify the operational status of the Malware Protection Plan<br>&emsp; + Audit scan results and assigned tags on S3 Objects<br>&emsp; + Monitor the execution of the Upload Processor Function<br>&emsp; + Confirm that verified clean files are moved to the DocumentsBucket<br>&emsp; + Test basic access privileges across distinct user groups | 07/07/2026 | 07/07/2026 |  |
| 4 | - Inspect CloudWatch Logs and alerting systems<br>- Get familiar with CloudWatch Logs Insights and AWS X-Ray<br>- **Practice:**<br>&emsp; + Review execution logs for Lambda Functions<br>&emsp; + Filter specific log entries using CloudWatch Logs Insights<br>&emsp; + Audit generated system logs inside DynamoDB layers<br>&emsp; + View basic Traces and Service Maps via AWS X-Ray panels<br>&emsp; + Verify the subscription state of target SNS Email destinations | 08/07/2026 | 08/07/2026 |  |
| 5 | - Tear down the DMS project infrastructure components<br>- **Practice:**<br>&emsp; + Check and back up critical data payloads before deletion<br>&emsp; + Empty target S3 Buckets if required to prevent retention lockouts<br>&emsp; + Execute the decommissioning command: `npx cdk destroy -c environment=dev`<br>&emsp; + Track the deletion lifecycle of the CloudFormation Stack<br>&emsp; + Inspect the AWS Console to pinpoint any residual orphan assets<br>&emsp; + Manually purge assets not stripped by the automated CDK routine | 09/07/2026 | 09/07/2026 |  |
| 6 | - Summarize the project accomplishments and audit final costs<br>- **Practice:**<br>&emsp; + Review the AWS Billing panel and Cost Explorer dashboards<br>&emsp; + Analyze financial expenditures broken down by consumed services<br>&emsp; + Perform double-check sweeps to guarantee no active assets remain<br>&emsp; + Synthesize system architecture layouts and functional maps<br>&emsp; + Document technical hurdles and professional lessons learned<br>&emsp; + Finalize and complete the internship report document deliverables | 10/07/2026 | 10/07/2026 |  |

### Week 12 Achievements:

* Understood the vital role of the Least Privilege principle in scoping boundaries for Lambda Functions.
* Audited the baseline access policies applied across core system Lambda scripts:
  * Reading and writing records within DynamoDB tables.
  * Ingesting file payloads into the QuarantineBucket space.
  * Fetching valid document assets out of the secure DocumentsBucket space.
  * Administering user states within the Amazon Cognito directory.
* Verified that Block Public Access configurations are actively enforced on all S3 Buckets.
* Differentiated the distinct operational designs between:
  * Presigned PUT URLs designed to handle file ingestion uploads.
  * Presigned GET URLs designed to handle secure file retrieval downloads.
* Verified the active status of GuardDuty Malware Protection engines tracking the QuarantineBucket.
* Tracked and verified scan verdict tags appended dynamically onto ingested S3 Objects.
* Confirmed that the Upload Processor logic restricts transport routines, moving only verified clean files into the DocumentsBucket.
* Tested and validated baseline operational permission boundaries across configured group domains:
  * EMPLOYEE
  * DEPARTMENT_ADMIN
  * SYSTEM_ADMIN
* Learned how to navigate and audit application runtime traces via Lambda Logs in Amazon CloudWatch.
* Successfully ran granular analysis filters over log payloads using CloudWatch Logs Insights query logic.
* Inspected append-only audit trail records capturing user interaction behaviors with system documents.
* Got familiar with distributed path maps, utilizing Service Maps and Traces within AWS X-Ray panels.
* Confirmed successful subscription validation loops for incident alerts managed through Amazon SNS paths.
* Executed complete environment decommissioning sweeps, stripping CloudFormation Stacks via AWS CDK interfaces.
* Mastered standard procedures for handling persistent data structures that bypass automated stack deletion logic:
  * Non-empty S3 Buckets containing stored assets.
  * Retained log streams inside specific CloudWatch Log Groups.
  * Stateful resources explicitly bounded by protective Removal Policies.
  * CloudFront Distributions going through extended decommissioning statuses.
* Verified the absolute clean state of the account via the AWS Console following CDK Destroy actions.
* Utilized the AWS Billing console and Cost Explorer dashboards to break down financial expenditure metrics by service lines.
* Consolidated documentation outlining the full architecture, application capabilities, and security defense layers of the DMS project.
* Completed all summary sheets, analytical lessons learned, and required internship report documentation milestones.