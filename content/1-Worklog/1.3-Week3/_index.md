---
title: "Week 3 Worklog"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---


### Week 3 Objectives:

* Learn how to manage and operate servers using AWS Systems Manager.
* Practice securely connecting to EC2 instances via Session Manager.
* Get familiar with Infrastructure as Code using AWS CloudFormation.
* Learn about advanced permission limitation mechanisms in AWS IAM.
* Get familiar with AWS Security Hub and AWS Backup.

### Tasks to implement this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Learn about AWS Systems Manager<br>- Learn about Patch Manager and Run Command<br>- **Practice:**<br>&emsp; + Create a Windows EC2 Instance<br>&emsp; + Create and assign an IAM Role to EC2<br>&emsp; + Verify Managed Nodes<br>&emsp; + Scan patches using Patch Manager<br>&emsp; + Run remote commands using Run Command | 04/05/2026 | 04/05/2026 | <https://000031.awsstudygroup.com> |
| 3 | - Learn about AWS Systems Manager Session Manager<br>- **Practice:**<br>&emsp; + Create a Public Subnet and a Private Subnet<br>&emsp; + Create a Public EC2 and a Private EC2<br>&emsp; + Create an IAM Role for Session Manager<br>&emsp; + Create necessary VPC Endpoints<br>&emsp; + Connect to the EC2 inside the Private Subnet<br>&emsp; + Configure storing Session Logs into Amazon S3 | 05/05/2026 | 05/05/2026 | <https://000058.awsstudygroup.com> |
| 4 | - Learn about Infrastructure as Code with AWS CloudFormation<br>- **Practice:**<br>&emsp; + Create an IAM Role for CloudFormation<br>&emsp; + Write a basic CloudFormation Template<br>&emsp; + Verify Template syntax<br>&emsp; + Create and update a CloudFormation Stack<br>&emsp; + Verify deployed resources | 06/05/2026 | 06/05/2026 | <https://000037.awsstudygroup.com> |
| 5 | - Learn about IAM Permission Boundaries<br>- Learn about IAM Roles and Conditions<br>- **Practice:**<br>&emsp; + Create a policy that limits maximum permissions<br>&emsp; + Apply a Permission Boundary to an IAM User<br>&emsp; + Verify permissions in allowed Regions<br>&emsp; + Create an IAM Role and perform Switch Role<br>&emsp; + Limit Assume Role by IP addresses or time frames | 07/05/2026 | 07/05/2026 | <https://000030.awsstudygroup.com> <br><br> <https://000044.awsstudygroup.com> |
| 6 | - Learn an overview of AWS Security Hub<br>- Learn about AWS Backup<br>- **Practice:**<br>&emsp; + Activate AWS Security Hub<br>&emsp; + View Security Score and security findings<br>&emsp; + Create a Backup Vault and a Backup Plan<br>&emsp; + Assign resources to the Backup Plan<br>&emsp; + Configure notifications using Amazon SNS<br>&emsp; + Monitor Backup Job statuses | 08/05/2026 | 08/05/2026 | <https://000018.awsstudygroup.com> <br><br> <https://000013.awsstudygroup.com> |

### Week 3 Achievements:

* Understood the role of AWS Systems Manager in centralized server management.
* Learned how to use Patch Manager to check patches and Run Command to run remote commands.
* Successfully connected to EC2 instances in both Public Subnets and Private Subnets using Session Manager.
* Understood the roles of IAM Roles and VPC Endpoints when managing Private EC2 instances.
* Learned how to store Session Logs in Amazon S3 to track connection activities.
* Understood the basic components of AWS CloudFormation:
  * Template
  * Stack
  * Resource
  * Parameter
* Successfully wrote and deployed a basic CloudFormation Template.
* Understood how Permission Boundaries limit the maximum permissions of an IAM User.
* Learned how to create an IAM Role and limit Assume Role using Conditions.
* Got familiar with the Security Score and security findings in AWS Security Hub.
* Successfully created a Backup Vault, a Backup Plan, and monitored backup statuses.
* Learned how to use Amazon SNS to receive notifications about backup activities.