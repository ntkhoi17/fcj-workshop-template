---
title: "Week 11 Worklog"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---


### Week 11 Objectives:

* Create an administrative account and verify user authentication mechanisms via Amazon Cognito.
* Test core DMS system APIs using JWT Tokens.
* Verify the document upload workflow utilizing Presigned URLs and file handling pipelines post-scanning.
* Test document listing, details retrieval, and file download APIs.
* Launch the React frontend locally and perform baseline functional testing.

### Tasks to implement this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Create an administrative account in Amazon Cognito<br>- Learn about the user authentication workflow<br>- **Practice:**<br>&emsp; + Create an administrative user within the User Pool<br>&emsp; + Set the password configuration for the user<br>&emsp; + Add the user to the SYSTEM_ADMIN group<br>&emsp; + Log in and retrieve the JWT Token<br>&emsp; + Verify group claims inside the Token | 29/06/2026 | 29/06/2026 |  |
| 3 | - Test the user profile info API endpoint<br>- Learn how API Gateway authorizes JWT Tokens<br>- **Practice:**<br>&emsp; + Invoke the `/me` endpoint using a Bearer Token<br>&emsp; + Verify userId, email, and groups parameters<br>&emsp; + Test edge cases with missing or incorrect Tokens<br>&emsp; + Monitor Lambda execution logs via CloudWatch Logs<br>&emsp; + Document baseline error status codes | 30/06/2026 | 30/06/2026 |  |
| 4 | - Test the creation workflow of Upload Intents<br>- Test file uploading procedures via Presigned URLs<br>- **Practice:**<br>&emsp; + Invoke the `/upload-intents` API endpoint<br>&emsp; + Record the returned uploadIntentId and Presigned PUT URL<br>&emsp; + Upload a sample PDF file into the QuarantineBucket<br>&emsp; + Verify the file presence inside Amazon S3<br>&emsp; + Track the Upload Intent state changes within DynamoDB | 01/07/2026 | 01/07/2026 |  |
| 5 | - Verify file scanning outcomes and post-processing steps<br>- Test document management API endpoints<br>- **Practice:**<br>&emsp; + Monitor GuardDuty Malware Protection execution metrics<br>&emsp; + Check EventBridge routing rules and Upload Processor execution logs<br>&emsp; + Verify verified clean files inside the DocumentsBucket<br>&emsp; + Confirm the updated `READY` state within DynamoDB tracking layers<br>&emsp; + Invoke the `/documents` list and detail API endpoints<br>&emsp; + Generate a Presigned GET URL and fetch test files | 02/07/2026 | 02/07/2026 |  |
| 6 | - Spin up the React Frontend application inside a local workspace<br>- Perform basic interface and UI validation tests<br>- **Practice:**<br>&emsp; + Install system dependencies utilizing npm packages<br>&emsp; + Configure local UserPoolId, UserPoolClientId, and ApiUrl parameters<br>&emsp; + Launch the web engine using `npm run dev`<br>&emsp; + Test administrative login features and workflows<br>&emsp; + Verify listing components, document uploads, and download workflows<br>&emsp; + Record UI presentation anomalies and API connectivity errors | 03/07/2026 | 03/07/2026 |  |

### Week 11 Achievements:

* Successfully provisioned an administrative account inside the Amazon Cognito instance.
* Mapped the administrative user identity straight into the SYSTEM_ADMIN group tier.
* Authenticated successfully and extracted JWT Token components to drive backend API validation checks.
* Understood how Amazon API Gateway leverages the Cognito Authorizer hook to authenticate incoming requests.
* Successfully called the `/me` validation endpoint and verified:
  * userId
  * email
  * groups
* Pinpointed baseline token validation failure patterns:
  * Missing Tokens
  * Malformed/Invalid Tokens
  * Expired Tokens
* Mastered using CloudWatch Logs to investigate and audit programmatic Lambda executions.
* Successfully invoked the initialization endpoint to register a new Upload Intent.
* Received the correct unique uploadIntentId tracking hash along with an active Presigned PUT URL.
* Uploaded test payloads natively into the isolated QuarantineBucket layer.
* Tracked continuous multi-state file conditions within Amazon S3 boundaries and DynamoDB records.
* Understood the asynchronous processing pipeline triggered upon GuardDuty file verification routines.
* Verified correct event transport across EventBridge rules down into Upload Processor logs.
* Confirmed that verified clean assets are relocated into the primary secure DocumentsBucket destination.
* Confirmed database row state transitions to `READY` status alongside valid version metadata fields.
* Successfully invoked the core system endpoints to list and pull structural document detail metrics.
* Generated secure Presigned GET URLs and downloaded original source assets directly out of the DocumentsBucket.
* Configured environment constants and launched the React Frontend web framework locally.
* Validated core functional interface flows across:
  * Authentication login routines
  * Document data grid listings
  * Target file uploading handlers
  * File downloading routines
* Documented initial UI presentation glitches and API integration bugs to focus optimization work for subsequent phases.