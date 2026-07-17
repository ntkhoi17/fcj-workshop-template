---
title: "Week 8 Worklog"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---


### Week 8 Objectives:

* Learn about event-driven architectures using Amazon SNS and Amazon SQS.
* Get familiar with protecting web applications and APIs using AWS WAF.
* Practice encrypting data on Amazon S3 using AWS KMS.
* Reinforce user authentication mechanisms for Single Page Applications (SPA) using Amazon Cognito.
* Practice monitoring serverless applications using Amazon CloudWatch and AWS X-Ray.

### Tasks to implement this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Learn about Event-driven architectures<br>- Learn about Amazon SNS and Amazon SQS<br>- **Practice:**<br>&emsp; + Create an SNS Topic<br>&emsp; + Create an SQS Queue and Subscription<br>&emsp; + Send and receive messages<br>&emsp; + Configure Filter Policies based on attributes<br>&emsp; + Verify messages routed to individual Queues | 08/06/2026 | 08/06/2026 | <https://000077.awsstudygroup.com> |
| 3 | - Learn about AWS Web Application Firewall<br>- Learn about Web ACLs, Managed Rules, and Custom Rules<br>- **Practice:**<br>&emsp; + Prepare a sample application<br>&emsp; + Create a Web ACL<br>&emsp; + Add AWS Managed Rules<br>&emsp; + Create a basic Custom Rule<br>&emsp; + Send requests to verify the Rule<br>&emsp; + View allowed or blocked requests | 09/06/2026 | 09/06/2026 | <https://000026.awsstudygroup.com> |
| 4 | - Learn about AWS Key Management Service<br>- Learn about Customer Managed Keys and Key Policies<br>- **Basic Practice:**<br>&emsp; + Create a Customer Managed Key<br>&emsp; + Configure Key Administrators and Key Users<br>&emsp; + Create an S3 Bucket<br>&emsp; + Enable S3 encryption using AWS KMS<br>&emsp; + Upload and download encrypted data<br>&emsp; + Verify user access permissions | 10/06/2026 | 10/06/2026 | <https://000033.awsstudygroup.com> |
| 5 | - Learn about Single Page Application architecture<br>- Learn about authentication with Amazon Cognito<br>- **Basic Practice:**<br>&emsp; + Create a Cognito User Pool<br>&emsp; + Create an App Client<br>&emsp; + Create a test user account<br>&emsp; + Integrate sign-up and sign-in interfaces<br>&emsp; + Configure a Cognito Authorizer for API Gateway<br>&emsp; + Call the API using a JWT Token | 11/06/2026 | 11/06/2026 | <https://000055.awsstudygroup.com> |
| 6 | - Learn about monitoring Lambda with Amazon CloudWatch<br>- Learn about Distributed Tracing with AWS X-Ray<br>- **Practice:**<br>&emsp; + View Lambda Logs on CloudWatch<br>&emsp; + Monitor Duration, Errors, and Invocations<br>&emsp; + Create a basic CloudWatch Alarm<br>&emsp; + Enable Active Tracing for Lambda<br>&emsp; + Call the API to generate Trace data<br>&emsp; + View the Service Map and analyze latency<br>&emsp; + Clean up resources post-practice | 12/06/2026 | 12/06/2026 | <https://000085.awsstudygroup.com> |

### Week 8 Achievements:

* Understood the role of Event-driven architecture in reducing coupling between components.
* Differentiated between the functions of Amazon SNS and Amazon SQS.
* Successfully created an SNS Topic, an SQS Queue, and a Subscription.
* Learned how to use Filter Policies to route messages.
* Understood the role of AWS WAF in protecting web applications and APIs.
* Successfully created a Web ACL using Managed Rules and a basic Custom Rule.
* Understood the role of AWS KMS in managing encryption keys.
* Successfully created a Customer Managed Key and used it to encrypt data on Amazon S3.
* Differentiated between key administration permissions and key usage permissions.
* Understood the basic structure of a Single Page Application.
* Successfully created a Cognito User Pool, an App Client, and a test user.
* Successfully integrated a Cognito Authorizer with Amazon API Gateway at a basic level.
* Learned how to use JWT Tokens to call protected APIs.
* Successfully monitored Lambda Logs and basic metrics on Amazon CloudWatch.
* Successfully created a CloudWatch Alarm to detect Lambda errors.
* Utilized AWS X-Ray to view the Service Map, Traces, and request latency.