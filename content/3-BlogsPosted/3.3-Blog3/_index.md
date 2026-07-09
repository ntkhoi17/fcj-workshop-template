---
title: "Blog 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# Emailing Daily Delta Cost Reports in a Multi-Account Environment Using AWS Lambda and Cost Explorer

In an AWS multi-account environment, tracking costs is an important issue but not always easy to implement. In particular, the finance team or management often do not have direct access to the AWS Billing Console, making cost information sharing a manual process.
This article introduces an automated solution to send daily delta cost reports using AWS Lambda, AWS Cost Explorer API, Amazon EventBridge, and Amazon Simple Email Service (SES). This is a serverless architecture that increases cost visibility and supports more effective cloud management.

### Key Points to Master:
* **The cost management problem in a multi-account environment**
  * Enterprises usually have multiple AWS accounts such as Production, Non-Production, and Sandbox.
  * Billing information is usually centralized in the management account.
  * Not every finance member or leadership has access to the AWS Billing Console.
  * Summarizing and sending cost reports manually is time-consuming and lacks timeliness.
* **The concept of delta cost**
  * Delta cost is the change in cost between the current day and the previous day.
  * This metric helps quickly detect anomalous fluctuations.
  * When costs increase suddenly, the team can check the cause earlier.
  * This is a simple way to increase cost visibility within the organization.
* **Automating reports with Lambda**
  * Lambda is triggered on a daily schedule.
  * The function calls the AWS Cost Explorer API to get cost data.
  * Data is processed, percentage changes are calculated, and formatted into an HTML report.
  * The report is sent via email to the recipient list.
* **Sending emails with Amazon SES**
  * Amazon SES is used to send cost reports to finance, leadership, or stakeholders.
  * Recipients do not need to log in to the AWS Console to view the cost situation.
  * Automated sending helps reduce manual operations in the management process.
* **Allying with FinOps direction**
  * The solution helps the technical team and finance team track costs together more easily.
  * Increases transparency in cloud resource utilization.
  * Supports early detection of accounts or environments with abnormally increasing costs.

### High-Level Architecture Overview:
The processing flow can be simply understood as follows:
1. Amazon EventBridge triggers Lambda according to a daily cron schedule.
2. AWS Lambda calls the AWS Cost Explorer API to get costs from accounts in the organization.
3. Lambda calculates the cost difference compared to the previous day.
4. Lambda formats the data into an HTML report.
5. Amazon SES sends the report to the recipient list.
6. Recipients can track daily costs without accessing the Billing Console.

### The Role of Deployed AWS Services:
* **Amazon EventBridge:** Triggers Lambda automatically on a daily schedule.
* **AWS Lambda:** Processes the logic of getting cost data, calculating delta, and creating reports.
* **AWS Cost Explorer API:** Provides cost and usage data of AWS accounts.
* **Amazon SES:** Sends cost reports via email.
* **AWS Organizations:** Allows managing multiple AWS accounts in the same organization.
* **IAM Role:** Grants permissions for Lambda to access Cost Explorer and send emails.

### Primary Deployment Checklist:
1. Download the CloudFormation template from the original article.
2. Configure the list of AWS accounts to track.
3. Configure the list of recipient emails.
4. Verify emails in Amazon SES.
5. Deploy the CloudFormation stack.
6. Grant appropriate Billing permissions to the IAM Role.
7. Configure the EventBridge rule with a cron expression.
8. Check the automatically sent cost report email.

### Delivered Business Value:
This solution brings many practical benefits to the enterprise:
* Automates the cost report sending process.
* Helps the finance team and leadership track costs more easily.
* Increases cost visibility in a multi-account environment.
* Early detects abnormal cost fluctuations.
* Reduces manual operations when summarizing reports.
* Can be extended to store reports in S3 or build long-term analysis dashboards.

### Conclusion
The solution of sending daily delta cost reports using AWS Lambda and Cost Explorer is a practical example of using serverless to automate cloud operations.
The point I find interesting is that this architecture is quite neat, using managed services of AWS such as Lambda, EventBridge, Cost Explorer API, and SES. Thanks to that, enterprises can track costs more proactively without granting Billing Console access to too many people.
For me, this is a pattern very worth learning because it combines automation, cost management, and FinOps in an AWS multi-account environment.

### Illustrative Diagram

![cost-report-architecture](../../images/cost-report-architecture.png)

### Original Blog Reference
<https://aws.amazon.com/vi/blogs/architecture/email-delta-cost-usage-report-in-a-multi-account-organization-using-aws-lambda/>