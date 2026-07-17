---
title: "Week 9 Worklog"
date: 15-06-2026
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---


### Week 9 Objectives:

* Learn an overview of the Document Management System project built on AWS Serverless.
* Analyze the architecture, functionalities, and core processing workflows of the system.
* Understand mechanisms for user authentication, document uploads, malware scanning, and data storage.
* Prepare the development environment and source code structure for the project.

### Tasks to implement this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Learn an overview of the Document Management System project<br>- Analyze internal document management challenges<br>- **Practice:**<br>&emsp; + Define system objectives<br>&emsp; + Identify user groups<br>&emsp; + List core functionalities<br>&emsp; + Define the project deployment scope | 15/06/2026 | 15/06/2026 |  |
| 3 | - Learn the overall architecture of the DMS system<br>- Understand the roles of various AWS services<br>- **Practice:**<br>&emsp; + Analyze the authentication workflow using Amazon Cognito<br>&emsp; + Analyze the API invocation flow through API Gateway<br>&emsp; + Identify the roles of Lambda, S3, and DynamoDB<br>&emsp; + Design the comprehensive system architecture diagram | 16/06/2026 | 16/06/2026 |  |
| 4 | - Learn about document upload workflows using Presigned URLs<br>- Learn about file quarantine and scanning processes<br>- **Practice:**<br>&emsp; + Analyze the creation flow of Presigned PUT URLs<br>&emsp; + Analyze the upload process into the QuarantineBucket<br>&emsp; + Learn about GuardDuty Malware Protection<br>&emsp; + Analyze EventBridge triggering the Upload Processor<br>&emsp; + Analyze the transfer process of clean files to the DocumentsBucket | 17/06/2026 | 17/06/2026 |  |
| 5 | - Learn about authorization models and data modeling design<br>- Learn about the system's security and architecture choices<br>- **Practice:**<br>&emsp; + Define user groups: EMPLOYEE, DEPARTMENT_ADMIN, and SYSTEM_ADMIN<br>&emsp; + Analyze DynamoDB Single-table Design patterns<br>&emsp; + Identify core system entities<br>&emsp; + Analyze append-only audit logging mechanisms<br>&emsp; + Define the least privilege IAM permissions for each Lambda | 18/05/2026 | 18/05/2026 |  |
| 6 | - Prepare the project development environment<br>- Learn about the Repository structure layouts<br>- **Practice:**<br>&emsp; + Verify AWS CLI and configured AWS Profiles<br>&emsp; + Verify Node.js, npm, Git, and the AWS CDK CLI<br>&emsp; + Learn about the CDK Bootstrap command execution<br>&emsp; + Create the project directory structure<br>&emsp; + Configure alert environment variables<br>&emsp; + Validate environment readiness prior to infrastructure deployment | 19/06/2026 | 19/06/2026 |  |

### Week 9 Achievements:

* Understood the primary objective of the DMS system: managing internal documents utilizing an AWS Serverless framework.
* Identified core system functionalities:
  * Document upload and download processes.
  * Version control management.
  * Permission sharing and access revocation.
  * Audit log recording.
  * Document status monitoring.
* Grasped the underlying roles of key services:
  * Amazon Cognito
  * Amazon API Gateway
  * AWS Lambda
  * Amazon S3
  * Amazon DynamoDB
  * Amazon EventBridge
  * Amazon GuardDuty
  * Amazon CloudFront
  * Amazon CloudWatch
  * Amazon SNS
* Analyzed authentication and API invocation flows utilizing JWT Tokens.
* Understood the architectural rationale for utilizing Presigned URLs for file uploads and downloads.
* Analyzed the isolation and processing pipeline:
  * Uploading files into the QuarantineBucket.
  * Executing malware scanning routines via GuardDuty.
  * Capturing notification events through EventBridge.
  * Handling processing outcomes using the Upload Processor.
  * Transferring verified clean files securely to the DocumentsBucket.
* Understood DynamoDB Single-table Design concepts and the functional roles of Global Secondary Indexes.
* Identified core database entities:
  * Document
  * Version
  * Share
  * AuditLog
  * UploadIntent
  * UserProfile
* Understood authorization boundary setups matching distinct user groups within Amazon Cognito.
* Mastered Least Privilege principles when structuring permission grants for Lambda Functions.
* Completed the comprehensive architectural layout diagram for the full DMS system.
* Configured and verified local installations of AWS CLI, Node.js, npm, Git, and the AWS CDK CLI.
* Map structural workspace directories across: `aws/functions`, `aws/infrastructure`, `frontend`, `contracts`, and `docs`.
* Completed baseline environment validation steps before initializing infrastructure provisioning routines.