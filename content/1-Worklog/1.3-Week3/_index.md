---
title: "Week 3 Worklog"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---


### Week 3 Objectives:

* Explore service management, server operations, and task automation on AWS through AWS Systems Manager, Patch Manager, Run Command, and Session Manager.
* Understand how to initialize Infrastructure as Code using AWS CloudFormation, including basic templates, stacks, custom resources, and drift detection.
* Learn about advanced identity management and access control restrictions using AWS IAM Identity Center, IAM Permission Boundaries, and IAM Role Conditions.
* Get familiar with security, encryption, and application protection services such as AWS Security Hub, AWS WAF, AWS KMS, and AWS Backup.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Learn about Service Management and task automation using AWS Systems Manager<br>- Learn about working with AWS Systems Manager - Session Manager<br>- **Practice:**<br>&emsp; + Create VPC and Subnets for the Systems Manager environment<br>&emsp; + Create a Public Windows EC2 Instance<br>&emsp; + Create and assign an IAM Role to the EC2 Instance<br>&emsp; + Verify Managed Nodes in Fleet Manager<br>&emsp; + Use Patch Manager to scan and install patches<br>&emsp; + Use Run Command to execute commands across multiple servers<br>&emsp; + Connect Public EC2 and Private EC2 using Session Manager<br>&emsp; + Configure session log storage in Amazon S3<br>&emsp; + Practice Port Forwarding to access a Private Windows Instance | 04/05/2026   | 04/05/2026      | <https://000031.awsstudygroup.com/vi/> <br><br> <https://000058.awsstudygroup.com/vi/> |
| 3   | - Learn about Infrastructure as Code Initialization with AWS CloudFormation<br>- **Practice:**<br>&emsp; + Create an IAM User and IAM Role for CloudFormation<br>&emsp; + Create a Workspace for template authoring<br>&emsp; + Create a basic CloudFormation Template<br>&emsp; + Validate templates prior to deployment<br>&emsp; + Launch a CloudFormation Stack via the AWS CLI<br>&emsp; + Explore advanced CloudFormation concepts<br>&emsp; + Create a Lambda Function as a custom resource<br>&emsp; + Learn about Mappings, StackSets, and Drift Detection | 05/05/2026   | 05/05/2026      | <https://000037.awsstudygroup.com/vi/> |
| 4   | - Learn about Setting up Single Sign-On for Organizations using AWS IAM Identity Center<br>- Learn about Restricting User Permissions with IAM Permission Boundaries<br>- Learn about Restricting Role Switching using Conditions<br>- **Practice:**<br>&emsp; + Create an AWS Account within AWS Organizations<br>&emsp; + Create Users and Groups in IAM Identity Center<br>&emsp; + Create Permission Sets and assign access permissions by Group<br>&emsp; + Verify access via the AWS Access Portal<br>&emsp; + Configure AWS CLI using IAM Identity Center<br>&emsp; + Create a Permission Set with time-based access conditions<br>&emsp; + Create a policy to limit maximum permissions using Permission Boundaries<br>&emsp; + Create an IAM User restricted by Region<br>&emsp; + Verify EC2 permissions in allowed vs restricted Regions<br>&emsp; + Create an IAM Group, IAM User, and Admin IAM Role<br>&emsp; + Configure Switch Role operations<br>&emsp; + Restrict AssumeRole operations by IP address and time windows | 06/05/2026   | 06/05/2026      | <https://000012.awsstudygroup.com/vi/> <br><br> <https://000030.awsstudygroup.com/vi/> <br><br> <https://000044.awsstudygroup.com/vi/> |
| 5   | - Learn about Evaluating security standards with AWS Security Hub<br>- Learn about Application and API Security with Web Application Firewall (AWS WAF)<br>- **Practice:**<br>&emsp; + Study AWS Foundational Security Best Practices, CIS AWS Foundations Benchmark, and PCI DSS standards<br>&emsp; + Enable AWS Security Hub CSPM<br>&emsp; + Enable AWS Config for compliance assessments<br>&emsp; + View Security Scores across compliance frameworks<br>&emsp; + Review findings and security risks<br>&emsp; + Create an S3 Bucket for AWS WAF labs<br>&emsp; + Deploy a sample application<br>&emsp; + Create a Web ACL with Managed Rules<br>&emsp; + Create Custom Rules and advanced Custom Rules<br>&emsp; + Test newly created Rules<br>&emsp; + Configure request logging | 07/05/2026   | 07/05/2026      | <https://000018.awsstudygroup.com/vi/> <br><br> <https://000026.awsstudygroup.com/vi/> |
| 6   | - Learn about Key Management with AWS Key Management Service (AWS KMS)<br>- Learn about Deploying system backup strategies with AWS Backup<br>- **Practice:**<br>&emsp; + Create Policies and Roles for AWS KMS<br>&emsp; + Create Groups and Users to verify access to encrypted data<br>&emsp; + Create a Customer Managed Key in AWS KMS<br>&emsp; + Configure Key Administrators and Key Usage Permissions<br>&emsp; + Create an S3 Bucket and upload data to S3<br>&emsp; + Encrypt S3 data using AWS KMS<br>&emsp; + Enable AWS CloudTrail to record account activity<br>&emsp; + Use Amazon Athena to query logs stored in S3<br>&emsp; + Test access permissions on encrypted data<br>&emsp; + Generate Presigned URLs for time-limited data sharing<br>&emsp; + Create a system Backup Plan<br>&emsp; + Create a Backup Vault and Backup Rules<br>&emsp; + Assign resources to the Backup Plan using Tags<br>&emsp; + Configure backup status notifications via Amazon SNS<br>&emsp; + Verify backup and data recovery operations | 08/05/2026   | 08/05/2026      | <https://000033.awsstudygroup.com/vi/> <br><br> <https://000013.awsstudygroup.com/vi/> |

### Week 3 Achievements:

#### 1. AWS Systems Manager Exploration
* Understood the role of AWS Systems Manager in centralizing AWS resource management.
* Grasped how Systems Manager supports operational tracking, configuration changes, alerting, compliance, and software inventory status.
* Understood how to group resources to manage them by application, production, or development environments.
* Got familiar with Fleet Manager, Managed Nodes, Patch Manager, and Run Command.

#### 2. Server Management with AWS Systems Manager Practice
* Created a VPC and Subnets for the practice environment.
* Created a Public Windows EC2 Instance.
* Created an IAM Role for the EC2 Instance.
* Assigned the IAM Role so the Instance could interact with Systems Manager.
* Verified that the EC2 Instance appeared in the Managed Nodes list.
* Opened terminal sessions to Windows EC2 Instances via Fleet Manager.

#### 3. Patch Manager Exploration and Practice
* Understood that Patch Manager is used to scan and install software patches on servers.
* Performed "Patch now" actions on Windows EC2 Instances.
* Selected the "Scan and install" patch operation.
* Configured appropriate reboot options during the update process.
* Verified patch results upon completion.

#### 4. Run Command Exploration and Practice
* Understood that Run Command allows executing commands simultaneously across multiple servers.
* Used the `AWS-RunPowerShellScript` systems document.
* Executed user verification commands on Windows EC2 Instances.
* Targeted multiple Instances concurrently.
* Configured command output storage to Amazon S3.
* Checked execution results and any generated error logs.

#### 5. AWS Systems Manager Session Manager Exploration
* Understood that Session Manager enables secure server connections to EC2 instances without directly exposing SSH or RDP ports to the Internet.
* Grasped how to connect to both Public and Private EC2 Instances within a VPC.
* Understood the role of VPC Endpoints in establishing connections to Private EC2 Instances.
* Got familiar with `ssm`, `ssmmessages`, and `ec2messages` endpoints.

#### 6. EC2 Connectivity via Session Manager Practice
* Created a VPC.
* Created Public and Private Subnets.
* Created a Security Group.
* Created a Public Linux EC2 Instance.
* Created a Private Windows EC2 Instance.
* Created an IAM Role for Session Manager.
* Enabled DNS Hostnames for the VPC.
* Created VPC Endpoints to support connectivity to the Private Instance.
* Successfully connected to the Private EC2 Instance via Session Manager.

#### 7. Session Logs Management & Port Forwarding Exploration
* Understood that Session History displays connection metadata but does not log detailed command outputs.
* Grasped how to store session logs in Amazon S3 and the role of S3 Gateway Endpoints in writing session records.
* Understood the principle of Port Forwarding to redirect traffic from a local workstation to an instance inside a Private Subnet.
* **Port Forwarding Practice:** Configured the AWS CLI, installed the Session Manager Plugin, and executed commands using the `AWS-StartPortForwardingSession` document to successfully establish an RDP session from a Private Windows Instance back to localhost.

#### 8. AWS CloudFormation Exploration
* Understood CloudFormation as a service that describes and provisions infrastructure resources using code (Infrastructure as Code - IaC).
* Grasped how to use templates to deploy AWS resources automatically and consistently across multiple Regions or accounts, and grew familiar with Stacks, Templates, and Resources.
* **Infrastructure Provisioning Practice:** Created a Workspace, authored and validated basic CloudFormation Templates, and launched Stacks using the AWS CLI.
* **Advanced Feature Research:** Created a Lambda Function as a Custom Resource, explored Mappings for value lookups, implemented StackSets, and used Drift Detection to identify infrastructure configuration variances.

#### 9. AWS IAM Identity Center (AWS Single Sign-On) Exploration
* Grasped how to manage identities and centralize permissions for enterprise personnel within AWS Organizations based on Group Membership and Permission Sets.
* **Identity Setup Practice:** Created AWS accounts, Users, Groups, and Permission Sets within IAM Identity Center to successfully verify access via the AWS Access Portal.
* **CLI Integration and Time-based Access Control:** Configured the AWS CLI for browser-based authentication using the `aws configure sso` command, and authored Permission Sets using Inline Policies with temporary time-bound restrictions to minimize security risks.

#### 10. IAM Permission Boundaries & Conditions Exploration
* Understood that a Permission Boundary is a mechanism used to limit the maximum permissions an IAM User or Role can possess, preventing privilege escalation risks.
* **Permission Restriction Practice:** Created an IAM Policy restricting EC2 administration exclusively to the `ap-southeast-1` Region, applied an admin policy alongside a Permission Boundary to a test user, and successfully verified access denial when switching to other Regions.
* **Switch Role Restrictions Practice:** Created an operational chain of IAM Groups, IAM Users, and Admin IAM Roles to configure Switch Role functionalities bound strictly by specific IP address ranges and precise timeframes using IAM Conditions.

#### 11. AWS Security Hub Exploration
* Understood how Security Hub provides a comprehensive view of security alerts, compliance postures, and aggregated findings from services like GuardDuty, Inspector, and Macie.
* Familiarized with compliance frameworks including AWS Foundational Security Best Practices, CIS AWS Foundations Benchmark, and PCI DSS.
* **CSPM Configuration Practice:** Enabled Security Hub CSPM on the AWS Management Console, synchronized and activated AWS Config for automated compliance scanning, and analyzed the granular Security Score dashboard of the system.

#### 12. AWS Web Application Firewall (AWS WAF) Exploration
* Understood the role of AWS WAF in blocking malicious web requests targeting web applications and APIs via Web ACLs, Managed Rules, and Custom Rules.
* **Application Protection Practice:** Initialized an S3 Bucket, deployed a sample application, configured a Web ACL incorporating advanced Custom Rules, and established request logging for downstream security analysis.

#### 13. AWS Key Management Service (AWS KMS) Exploration
* Understood the mechanisms for creating, automatically rotating, and managing symmetric/asymmetric Customer Managed Keys to safeguard data-at-rest.
* **Key Management Practice:** Segmented responsibilities clearly between Key Administrators and Key Usage Permissions, initialized an S3 Bucket, and configured full data integrity encryption for S3 Objects using AWS KMS.

#### 14. AWS CloudTrail, Amazon Athena, and Encrypted Data Sharing Application
* Grasped how CloudTrail records API activity histories and learned how to utilize Amazon Athena to execute SQL queries directly against logs stored in Amazon S3.
* **Data Security Testing Practice:** Authenticated and validated KMS key decryption boundaries across distinct User Groups, and generated Presigned URLs to share data securely over defined, time-limited intervals.

#### 15. AWS Backup Exploration
* Understood the role of AWS Backup in centralizing and automating data protection policies (EBS, RDS, DynamoDB, EFS) to meet Recovery Time Objectives (RTO) and Recovery Point Objectives (RPO).
* **Backup Scheduling Practice:** Created a system Backup Plan, configured Backup Rules (daily schedule), initialized a Backup Vault, assigned resources using resource Tags, and linked Amazon SNS to automate execution status updates (`BACKUP_JOB_COMPLETED` / `RESTORE_JOB_COMPLETED`) via the AWS CLI.
* **Recovery Verification Practice:** Conducted end-to-end data restoration drills from backup assets to guarantee system availability and data integrity during disaster recovery scenarios.