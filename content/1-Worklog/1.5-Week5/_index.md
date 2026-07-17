---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---


### Week 5 Objectives:

* Explore how to monitor and analyze utilization costs on AWS.
* Master methodologies for right-sizing EC2 instances to match actual utilization demands.
* Learn about Monolith architecture and deployment workflows onto AWS Elastic Beanstalk.
* Get familiar with the structural mindset of decomposing a functional component from a Monolith into a Serverless Microservice.
* Practice binding AWS Lambda calculations with Amazon S3 following an event-driven model.

### Tasks to implement this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Learn about AWS Cost Explorer<br>- Learn about cost by service and account<br>- Learn about Savings Plans and Reserved Instances<br>- **Practice:**<br>&emsp; + View costs and usage by service<br>&emsp; + Filter cost data by time range<br>&emsp; + Create custom EC2 cost reports<br>&emsp; + View data transfer cost overview | 18/05/2026 | 18/05/2026 | <https://000034.awsstudygroup.com> |
| 3 | - Learn about EC2 Right-Sizing<br>- Learn about AWS Compute Optimizer<br>- **Practice:**<br>&emsp; + Create an IAM Role for CloudWatch Agent<br>&emsp; + Assign the IAM Role to an EC2 Instance<br>&emsp; + Install CloudWatch Agent<br>&emsp; + Monitor CPU and memory metrics<br>&emsp; + View EC2 right-sizing recommendations | 19/05/2026 | 19/05/2026 | <https://000032.awsstudygroup.com> |
| 4 | - Learn about TravelBuddy Monolith application architecture<br>- Prepare practice environment<br>- **Practice:**<br>&emsp; + Create a Key Pair<br>&emsp; + Create a CloudFormation Stack<br>&emsp; + Connect to a Windows EC2 Instance<br>&emsp; + Install the database<br>&emsp; + Download TravelBuddy source code<br>&emsp; + Verify the application using Eclipse IDE | 20/05/2026 | 20/05/2026 | <https://000050.awsstudygroup.com/> |
| 5 | - Learn about AWS Elastic Beanstalk<br>- Learn about the Monolith application deployment process<br>- **Practice:**<br>&emsp; + Create an Elastic Beanstalk Environment<br>&emsp; + Deploy the TravelBuddy application<br>&emsp; + Check environment health status<br>&emsp; + Access the application post-deployment<br>&emsp; + Update a minor change<br>&emsp; + Verify application APIs | 21/05/2026 | 21/05/2026 | <https://000050.awsstudygroup.com> |
| 6 | - Learn about Serverless Microservices<br>- Learn about Lambda combined with S3 Events<br>- **Basic Practice:**<br>&emsp; + Create an S3 Bucket<br>&emsp; + Create an AWS Lambda Function<br>&emsp; + Configure S3 PutObject Trigger<br>&emsp; + Upload files to trigger Lambda<br>&emsp; + Verify results in CloudWatch Logs<br>&emsp; + Learn image file processing logic<br>&emsp; + Clean up resources post-practice | 22/05/2026 | 22/05/2026 | <https://000052.awsstudygroup.com> |

### Week 5 Achievements:

* Learned how to use AWS Cost Explorer to track costs and utilization.
* Acquired the ability to view costs by:
  * AWS services
  * Time ranges
  * Accounts
  * Resource types
* Understood the significance of Savings Plans and Reserved Instances in cost optimization.
* Understood the concept of Right-Sizing for Amazon EC2.
* Learned how to use CloudWatch Agent to collect additional system metrics.
* Got familiar with resource optimization recommendations from AWS Compute Optimizer.
* Understood the baseline characteristics and limitations of Monolith architecture.
* Prepared the TravelBuddy environment successfully using CloudFormation.
* Deployed a basic Monolith application successfully onto AWS Elastic Beanstalk.
* Learned how to check environment health status and perform application updates on Elastic Beanstalk.
* Understood the mindset of decomposing a functional component from a Monolith into a Microservice.
* Created an AWS Lambda function successfully triggered by file upload events onto Amazon S3.
* Learned how to verify and audit Lambda execution processes through CloudWatch Logs.