---
title: "Week 2 Worklog"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---


### Week 2 Objectives:

* Explore cost optimization, resource management, and access control solutions on AWS using Amazon Lightsail, Tags, Resource Groups, and IAM Policies based on Resource Tags.
* Understand how to automatically scale applications, load balance, and monitor systems using Amazon EC2 Auto Scaling, Elastic Load Balancing, Amazon CloudWatch, and Grafana.
* Get familiar with operations and automation tools on AWS such as AWS CLI, AWS Lambda, CloudWatch Dashboards, and Slack notification integration.
* Learn about hybrid DNS connectivity models, virtual machine migration, and database migration using Route 53 Resolver, VM Import/Export, AWS DMS, and AWS Schema Conversion Tool.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Learn about Compute Cost Optimization with Amazon Lightsail<br>- Learn about Resource Group Management using Tags and Resource Groups<br>- **Practice:**<br>&emsp; + Deploy Lightsail Database<br>&emsp; + Deploy WordPress Instance on Lightsail<br>&emsp; + Configure Networking for Lightsail Instance<br>&emsp; + Assign Tags to AWS resources<br>&emsp; + Filter resources by Tags<br>&emsp; + Create Resource Groups for grouped resource management | 27/04/2026   | 27/04/2026      | <https://000045.awsstudygroup.com> <br><br> <https://000027.awsstudygroup.com> |
| 3   | - Learn about Application Auto Scaling with Amazon EC2 Auto Scaling<br>- Learn about EC2 Service Access Management by Tags via IAM<br>- **Practice:**<br>&emsp; + Prepare network infrastructure for the application<br>&emsp; + Create Launch Template<br>&emsp; + Create Target Group and Elastic Load Balancer<br>&emsp; + Create Auto Scaling Group<br>&emsp; + Test Manual Scaling, Scheduled Scaling, and Dynamic Scaling<br>&emsp; + Create IAM Policy to control EC2 permissions based on Resource Tags<br>&emsp; + Verify EC2 access policies under Tag conditions | 28/04/2026   | 28/04/2026      | <https://000006.awsstudygroup.com> <br><br> <https://000028.awsstudygroup.com> |
| 4   | - Learn about System Monitoring Dashboards with Amazon CloudWatch<br>- Learn about System Monitoring Dashboards with Amazon CloudWatch and Grafana<br>- Learn about Automated Server Start/Stop and Slack messaging with AWS Lambda<br>- **Practice:**<br>&emsp; + View and analyze CloudWatch Metrics<br>&emsp; + Search and analyze CloudWatch Logs<br>&emsp; + Create CloudWatch Alarm<br>&emsp; + Create CloudWatch Dashboard<br>&emsp; + Install Grafana on EC2 Instance<br>&emsp; + Connect Grafana to monitor AWS resources<br>&emsp; + Create Lambda Function to automatically Start/Stop EC2 Instances<br>&emsp; + Configure Slack Incoming Webhook to receive notifications | 29/04/2026   | 29/04/2026      | <https://000008.awsstudygroup.com> <br><br> <https://000029.awsstudygroup.com> <br><br> <https://000022.awsstudygroup.com> |
| 5   | - Learn about Hybrid DNS System Configuration integrated between Local environment and Amazon VPC with Amazon Route 53 Resolver<br>- Learn about Using AWS CLI on Amazon EC2 Windows/Ubuntu<br>- **Practice:**<br>&emsp; + Create Key Pair<br>&emsp; + Initialize CloudFormation Template<br>&emsp; + Configure Security Group<br>&emsp; + Connect to Remote Desktop Gateway<br>&emsp; + Deploy Microsoft Active Directory<br>&emsp; + Create Route 53 Outbound Endpoint<br>&emsp; + Create Route 53 Resolver Rules<br>&emsp; + Create Route 53 Inbound Endpoint<br>&emsp; + Install and configure AWS CLI<br>&emsp; + Verify AWS resources via CLI | 30/04/2026   | 30/04/2026      | <https://000010.awsstudygroup.com> <br><br> <https://000011.awsstudygroup.com> |
| 6   | - Learn about Virtual Machine Migration with AWS VM Import/Export<br>- Learn about Database Migration with AWS Database Migration Service and AWS Schema Conversion Tool<br>- **Practice:**<br>&emsp; + Prepare virtual machine from On-premise environment<br>&emsp; + Export virtual machine from virtualization environment<br>&emsp; + Upload virtual machine to Amazon S3<br>&emsp; + Import virtual machine into AWS<br>&emsp; + Deploy EC2 Instance from imported AMI<br>&emsp; + Install AWS Schema Conversion Tool<br>&emsp; + Connect to source database<br>&emsp; + Convert database schema<br>&emsp; + Create DMS Replication Instance<br>&emsp; + Create Source Endpoint and Target Endpoint<br>&emsp; + Create DMS Migration Task and verify data after migration | 01/05/2026   | 01/05/2026      | <https://000014.awsstudygroup.com> <br><br> <https://000043.awsstudygroup.com> |

### Week 2 Achievements:

#### 1. Amazon Lightsail Exploration
* Understood Amazon Lightsail as a service supporting rapid deployment of popular applications with a simple configuration model.
* Grasped how to deploy open-source applications on Lightsail such as WordPress, PrestaShop, and Akaunting.
* Understood how Lightsail supports application deployment, database, networking, snapshots, and alerts within a single management environment.
* Learned how to use Lightsail to optimize costs for small systems or applications requiring rapid deployment.
* **Resource Deployment Practice on Amazon Lightsail:**
  * Created Lightsail Database.
  * Created WordPress Instance.
  * Configured Ubuntu for Instance.
  * Configured Networking for application.
  * Configured WordPress on Lightsail.
  * Learned how to create Snapshots for resource backup.
  * Learned how to switch to a larger Instance when application scaling is needed.

#### 2. Tag and Resource Groups Exploration
* Understood Tags as metadata labels assigned to AWS resources.
* Grasped the structure of Tags consisting of Keys and Values.
* Understood how to classify resources by purpose, environment, owner, or deployment team.
* Understood the role of AWS Resource Groups in grouping and managing multiple resources simultaneously.
* **Resource Management Practice using Tags:**
  * Created EC2 Instances with assigned Tags.
  * Added and removed Tags on resources.
  * Filtered resources by Tags on AWS Console.
  * Used AWS CLI to manipulate Tags.
  * Created Resource Groups based on Tags to manage resources in groups.

#### 3. Amazon EC2 Auto Scaling Exploration
* Understood the role of Auto Scaling Groups in automatically increasing or decreasing the number of EC2 Instances according to access demand.
* Grasped the benefits of Auto Scaling Groups in increasing availability, optimizing costs, and reducing manual administration tasks.
* Understood how Auto Scaling Groups combine with Elastic Load Balancing to distribute requests to multiple Instances.
* Explored scaling types such as Manual Scaling, Scheduled Scaling, Dynamic Scaling, and Predictive Scaling.
* **Application Deployment Practice with Auto Scaling Groups:**
  * Prepared network infrastructure for the application.
  * Initialized EC2 Instances and Database Instances with Amazon RDS.
  * Installed data for the Database.
  * Deployed web servers.
  * Created Launch Template.
  * Created Target Group.
  * Created Elastic Load Balancer.
  * Created Auto Scaling Group.
  * Tested load distribution capabilities and resource scaling.

#### 4. EC2 Access Management by Resource Tags via IAM Exploration
* Understood how to use Resource Tags to control access to EC2.
* Grasped how to apply the principle of least privilege in IAM Policies.
* Explored how to create conditional IAM Policies based on Tags.
* Understood how IAM Roles are used to grant controlled permissions to specific user groups.
* **EC2 Access Control Practice using IAM and Tags:**
  * Created IAM User for testing purposes.
  * Created conditional IAM Policy.
  * Created IAM Role.
  * Performed Role switching to verify permissions.
  * Checked EC2 access permissions across different Regions.
  * Verified EC2 Instance creation with and without condition-matching Tags.
  * Verified Resource Tag modifications on EC2 Instances.

#### 5. Amazon CloudWatch Exploration
* Understood CloudWatch as a monitoring and management service for operational data of AWS resources, hybrid applications, and on-premises applications.
* Grasped the roles of Metrics, Logs, Alarms, and Dashboards in the system monitoring process.
* Understood how CloudWatch supports performance analysis, incident response automation, and mean-time-to-resolution reduction.
* Explored data storage capabilities for Metrics, Log analysis, and alert creation based on custom thresholds.
* **System Monitoring Practice with CloudWatch:**
  * Viewed Metrics of AWS resources.
  * Performed Metrics searches.
  * Performed Metric mathematics.
  * Created Dynamic Labels.
  * Worked with CloudWatch Logs.
  * Used CloudWatch Logs Insights.
  * Created Metric Filters.
  * Created CloudWatch Alarm.
  * Created CloudWatch Dashboard to visualize system status.

#### 6. Grafana on AWS Exploration
* Understood Grafana as an open-source tool used for monitoring data visualization.
* Grasped how Grafana supports chart creation, data querying, alerting, and system metrics tracking.
* Understood how Grafana can combine with monitoring data from AWS to build intuitive dashboards.
* Knew the role of Grafana in tracking application and infrastructure activities.
* **Grafana Deployment Practice:**
  * Created VPC and Subnets for the practice environment.
  * Created Security Group.
  * Created EC2 Instance.
  * Created IAM User.
  * Created IAM Role.
  * Assigned IAM Role to EC2 Instance.
  * Installed Grafana on Linux EC2 Instance.
  * Monitored AWS resources via Grafana Dashboards.

#### 7. EC2 Cost Optimization with AWS Lambda Exploration
* Understood how to use Lambda Functions to automatically start and stop EC2 Instances.
* Grasped the use cases for servers that only need to operate during specific time windows.
* Understood how to combine Tags, IAM Roles, Lambda, and Slack to automate operations.
* Knew how to reduce costs by turning off servers when they are not in use.
* **Automated EC2 Start/Stop and Slack Notification Practice:**
  * Created VPC.
  * Created Security Group.
  * Created EC2 Instance.
  * Configured Slack Incoming Webhook.
  * Created Tags for the Instance.
  * Created Role for Lambda.
  * Created Lambda Function to stop EC2 Instances.
  * Created Lambda Function to start EC2 Instances.
  * Verified results and notifications sent to Slack.

#### 8. Route 53 Resolver and Hybrid DNS Model Exploration
* Understood the need for DNS integration between On-premise environments and Amazon VPC.
* Grasped the role of Amazon Route 53 in domain name resolution on AWS.
* Understood the components of Route 53 Resolver including Outbound Endpoints, Inbound Endpoints, and Resolver Rules.
* Knew how Route 53 Resolver supports forwarding DNS queries between Local systems and AWS.
* **Hybrid DNS Configuration Practice:**
  * Created Key Pair.
  * Initialized CloudFormation Template.
  * Configured Security Group.
  * Connected to RDGW.
  * Deployed Microsoft Active Directory.
  * Created Route 53 Outbound Endpoint.
  * Created Route 53 Resolver Rules.
  * Created Route 53 Inbound Endpoint.
  * Tested DNS resolution capabilities between Local environment and Amazon VPC.

#### 9. AWS CLI Exploration
* Understood AWS Command Line Interface as a command-line tool allowing interaction with AWS services.
* Grasped how AWS CLI supports operations similar to the AWS Management Console through a command-line shell.
* Knew the environments where AWS CLI can be used, such as Linux Shell, Windows Command Prompt, PowerShell, and remote connections to EC2.
* Understood how to use AWS CLI to verify and manage AWS resources.
* **AWS CLI Usage Practice:**
  * Installed AWS CLI.
  * Verified resources via CLI.
  * Manipulated Amazon S3 using CLI.
  * Manipulated Amazon SNS using CLI.
  * Manipulated IAM using CLI.
  * Manipulated VPC and Internet Gateway using CLI.
  * Created EC2 Instances using AWS CLI.
  * Explored common errors and troubleshooting methods when using CLI.

#### 10. AWS VM Import/Export Exploration
* Understood VM Import/Export as a service supporting the import of virtual machines from virtualization environments into Amazon EC2 and exporting virtual machines from AWS to external environments.
* Grasped usage scenarios such as migrating applications from On-premise to AWS, backing up virtual machines, and creating disaster recovery repositories.
* Understood the role of Amazon S3 in storing virtual machine files during import or export processes.
* Knew how to deploy EC2 Instances from AMIs created after the import process.
* **Virtual Server Migration Practice:**
  * Prepared virtual machine from virtualization environment.
  * Exported virtual machine from On-premise environment.
  * Uploaded virtual machine to Amazon S3.
  * Imported virtual machine into AWS.
  * Created AMI from imported virtual machine.
  * Deployed EC2 Instance from AMI.
  * Explored the process of exporting EC2 Instances or AMIs to external environments.

#### 11. AWS Database Migration Service and Schema Conversion Tool Exploration
* Understood the database schema conversion process when migrating between different database management systems.
* Grasped the role of AWS Schema Conversion Tool in analyzing and converting schemas, views, stored procedures, and functions.
* Understood the role of AWS DMS in migrating data from source databases to target databases.
* Knew the types of data sources and targets available in DMS, such as Oracle, SQL Server, Amazon RDS, Aurora, Amazon S3, and other data systems.
* **Database Migration Practice:**
  * Logged into AWS and prepared the environment.
  * Created Key Pair.
  * Connected to EC2 Instance and installed AWS Schema Conversion Tool.
  * Connected to source database.
  * Configured source database.
  * Created project in Schema Conversion Tool.
  * Converted database schema.
  * Configured target database.
  * Created DMS Replication Instance.
  * Created Source Endpoint and Target Endpoint.
  * Created DMS Migration Task.
  * Verified data content at target database.
  * Monitored the migration process using CloudWatch Metrics, Task Logs, and Table Statistics.