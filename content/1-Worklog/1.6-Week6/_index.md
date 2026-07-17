---
title: "Week 6 Worklog"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---


### Week 6 Objectives:

* Learn how to orchestrate serverless workflows using AWS Step Functions.
* Practice using AWS Lambda to interact with Amazon S3 and Amazon DynamoDB.
* Build serverless APIs using Amazon API Gateway.
* Get familiar with application deployment using AWS SAM.
* Learn about user authentication mechanisms with Amazon Cognito.

### Tasks to implement this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Learn about AWS Step Functions and State Machines<br>- Learn about Task States and Choice States<br>- **Basic Practice:**<br>&emsp; + Prepare sample Lambda Functions<br>&emsp; + Create a State Machine<br>&emsp; + Configure a Task State to call Lambda<br>&emsp; + Create a Choice State for branching<br>&emsp; + Verify Input and Output of the workflow<br>&emsp; + Learn about Retry and Catch | 25/05/2026 | 25/05/2026 | <https://000047.awsstudygroup.com> |
| 3 | - Learn about Lambda interacting with Amazon S3<br>- Learn about event-driven image processing architectures<br>- **Practice:**<br>&emsp; + Create an S3 Bucket to store images<br>&emsp; + Create an IAM Role for Lambda<br>&emsp; + Create a Lambda Function to process images<br>&emsp; + Configure an S3 PutObject Trigger<br>&emsp; + Upload images to trigger Lambda<br>&emsp; + Verify results in CloudWatch Logs | 26/05/2026 | 26/05/2026 | <https://000078.awsstudygroup.com> |
| 4 | - Learn about Lambda interacting with DynamoDB<br>- Learn about Amazon API Gateway and CORS<br>- **Practice:**<br>&emsp; + Create a DynamoDB table<br>&emsp; + Create Lambda functions to write and read data<br>&emsp; + Create API Gateway Resources and Methods<br>&emsp; + Integrate API Gateway with Lambda<br>&emsp; + Enable CORS<br>&emsp; + Verify the API using Postman | 27/05/2026 | 27/05/2026 | <https://000078.awsstudygroup.com> <br><br> <https://000079.awsstudygroup.com> |
| 5 | - Learn about the AWS Serverless Application Model (SAM)<br>- Learn about the structure of a SAM Template<br>- **Practice:**<br>&emsp; + Install and configure AWS SAM CLI<br>&emsp; + Initialize a SAM Project<br>&emsp; + Declare Lambda and DynamoDB in the Template<br>&emsp; + Run SAM Build and Validate<br>&emsp; + Deploy the application using SAM Deploy<br>&emsp; + Verify the created resources | 28/05/2026 | 28/05/2026 | <https://000080.awsstudygroup.com> |
| 6 | - Learn about authentication with Amazon Cognito<br>- Differentiate between User Pools and Identity Pools<br>- **Practice:**<br>&emsp; + Create an Amazon Cognito User Pool<br>&emsp; + Create an App Client<br>&emsp; + Create a test user<br>&emsp; + Integrate a Cognito Authorizer with API Gateway<br>&emsp; + Verify registration and login<br>&emsp; + Call the API using an Access Token<br>&emsp; + Clean up resources post-practice | 29/05/2026 | 29/05/2026 | <https://000081.awsstudygroup.com> |

### Week 6 Achievements:

* Understood the role of AWS Step Functions in orchestrating serverless services.
* Successfully created a basic State Machine utilizing:
  * Task State
  * Choice State
  * State Input and Output
* Understood the roles of Retry and Catch in workflow error handling.
* Successfully created a Lambda Function triggered by file upload events onto Amazon S3.
* Learned how to use CloudWatch Logs to verify Lambda execution processes.
* Successfully created a DynamoDB table and Lambda Functions to read and write data.
* Understood the basic components of Amazon API Gateway:
  * Resource
  * Method
  * Integration
  * CORS
* Successfully verified serverless APIs using Postman.
* Understood the role of AWS SAM in deploying serverless infrastructure as code.
* Learned how to use the following commands:
  * `sam build`
  * `sam validate`
  * `sam deploy`
* Successfully created an Amazon Cognito User Pool and App Client.
* Understood the differences between User Pools and Identity Pools.
* Successfully integrated a Cognito Authorizer with API Gateway at a basic level.
* Verified registration, login, and API call workflows using tokens.
