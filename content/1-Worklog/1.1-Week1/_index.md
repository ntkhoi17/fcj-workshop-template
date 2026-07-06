---
title: "Week 1 Worklog"
date: 2026-04-20
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---


### Week 1 Objectives:

* Explore foundational knowledge of AWS Cloud, the 2025 AWS Free Tier policy, and tools supporting cost management during the use of AWS services.
* Understand the mechanisms of identity management, access control, and permission granting for AWS services through AWS IAM and IAM Roles.
* Get familiar with the AWS Cloud9 development environment and core infrastructure services including Amazon VPC, Amazon EC2, Amazon S3, and Amazon RDS.
* Practice deploying basic AWS resources to build a foundation for practical exercises and projects in the following weeks.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Learn about AWS Free Tier 2025<br>- Learn about Cost Management with AWS Budgets<br>- Learn about the process of submitting Support Requests from AWS Support | 20/04/2026   | 20/04/2026      | <https://000001.awsstudygroup.com> <br><br> <https://000007.awsstudygroup.com> <br><br> <https://000009.awsstudygroup.com> |
| 3   | - Learn about Access Control Management with AWS Identity and Access Management (AWS IAM)<br>- Learn how to Grant permissions for applications to access AWS services through IAM Roles<br>- **Practice:**<br>&emsp; + Create IAM Users and IAM Groups<br>&emsp; + Configure IAM Policies<br>&emsp; + Assign IAM Roles to AWS services | 21/04/2026   | 21/04/2026      | <https://000002.awsstudygroup.com> <br><br> <https://000048.awsstudygroup.com> |
| 4   | - Learn how to use a browser-based Cloud IDE with AWS Cloud9<br>- Learn about Static Website Hosting services with Amazon S3<br>- **Practice:**<br>&emsp; + Initialize AWS Cloud9 environment<br>&emsp; + Create an S3 Bucket<br>&emsp; + Upload website source code<br>&emsp; + Configure Static Website Hosting | 22/04/2026   | 22/04/2026      | <https://000049.awsstudygroup.com> <br><br> <https://000057.awsstudygroup.com> |
| 5   | - Learn about Network Infrastructure Deployment with Amazon Virtual Private Cloud (Amazon VPC):<br>&emsp; + CIDR Blocks<br>&emsp; + Public Subnets and Private Subnets<br>&emsp; + Internet Gateways<br>&emsp; + Route Tables<br>- **Practice:**<br>&emsp; + Create a custom VPC<br>&emsp; + Create Subnets<br>&emsp; + Configure network routing | 23/04/2026   | 23/04/2026      | <https://000003.awsstudygroup.com> |
| 6   | - Learn about Amazon Elastic Compute Cloud (Amazon EC2)<br>- Learn about Amazon Relational Database Service (Amazon RDS)<br>- **Practice:**<br>&emsp; + Create an EC2 Instance<br>&emsp; + Connect to EC2 via SSH<br>&emsp; + Create an RDS MySQL Instance<br>&emsp; + Configure Security Groups to connect EC2 and RDS | 24/04/2026   | 24/04/2026      | <https://000004.awsstudygroup.com> <br><br> <https://000005.awsstudygroup.com> |

### Week 1 Achievements:

#### 1. AWS Free Tier 2025 Exploration
* Understood AWS free tier offers including Always Free, 12 Months Free, and Trials.
* Grasped the free tier usage limits of several popular services on AWS.
* Learned how to monitor resource usage to limit unexpected costs.

#### 2. AWS Budgets Exploration
* Understood the mechanisms for managing and tracking costs on AWS.
* Created Budgets to monitor resource usage.
* Set up Email Notifications to receive alerts when costs reach configured thresholds.

#### 3. AWS Support Exploration
* Grasped the support plans provided by AWS.
* Understood the process of creating and managing Support Cases.
* Differentiated support request types such as Account and Billing, Technical Support, and Service Limit Increases.

#### 4. AWS Identity and Access Management (IAM) Exploration
* Understood the roles of IAM Users, IAM Groups, and IAM Policies.
* Grasped the principle of least privilege.
* Understood how to control access to AWS resources.

#### 5. User Management and Permissions Practice
* Created IAM Users.
* Created IAM Groups.
* Assigned Policies to Users and Groups.
* Verified access permissions after configuring authorization.

#### 6. IAM Role Exploration
* Differentiated between IAM Users and IAM Roles.
* Understood Trust Policy and Permission Policy mechanisms.
* Learned how to grant permissions to AWS services without using Access Keys.

#### 7. Permission Granting via IAM Role Practice
* Created IAM Roles.
* Assigned Roles to AWS services.
* Verified resource accessibility through the granted Roles.

#### 8. AWS Cloud9 Exploration
* Initialized a Cloud-based development environment.
* Used the source code editor directly on the browser.
* Got familiar with the integrated Terminal and development support tools.

#### 9. Amazon S3 and Static Website Deployment Exploration
* Understood the Object Storage model on Amazon S3.
* Created S3 Buckets and managed stored objects.
* Configured Static Website Hosting.
* Deployed a static website and accessed it through the Website Endpoint.

#### 10. Amazon VPC Exploration
* Understood the role of VPC in building network infrastructure on AWS.
* Grasped components like CIDR Blocks, Subnets, Route Tables, and Internet Gateways.
* Understood the differences between Public Subnets and Private Subnets.

#### 11. Network Infrastructure Deployment Practice
* Created a custom VPC.
* Created Public Subnets.
* Configured Route Tables and Internet Gateways.
* Verified network connectivity within the AWS environment.

#### 12. Amazon EC2 Exploration
* Understood virtual server concepts on AWS.
* Learned about Amazon Machine Images (AMI), Instance Types, Key Pairs, and Security Groups.
* Grasped the process of initializing and managing EC2 Instances.

#### 13. EC2 Deployment Practice
* Created an EC2 Instance.
* Configured Security Groups.
* Connected to the server via SSH.
* Verified the operational status of the Instance.

#### 14. Amazon Relational Database Service (Amazon RDS) Exploration
* Understood the managed database model on AWS.
* Learned about components like Database Instances, Database Engines, and Endpoints.
* Understood security mechanisms and database access control.

#### 15. Amazon RDS Deployment Practice
* Created an RDS MySQL Instance.
* Configured basic parameters for the database.
* Set up Security Groups to allow connectivity.
* Verified connectivity between the EC2 Instance and the RDS Instance.