---
title: "Week 8 Worklog"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---


### Week 8 Objectives:

* Explore event-driven architectures on AWS using Amazon SNS and Amazon SQS, encompassing Pub/Sub models, Message Filtering, and Advanced Message Filtering.
* Practice data sharing topologies and high-availability system construction using Amazon EBS Multi-Attach, NVMe Reservations, MySQL HA Clusters, and Windows Failover Clustering.
* Get familiar with network infrastructure auditing via VPC Flow Logs and network traffic analysis utilizing Amazon CloudWatch Logs.
* Learn secure delegation mechanisms for the Billing Console alongside financial governance, restricting resource provisioning through IAM Policies based on Region, EC2 Family, Instance Size, and EBS Volume Type.
* Understand how to securely manage sensitive credentials using AWS Secrets Manager integrated with Amazon RDS and AWS Fargate compute layers.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Learn about Building Event-driven Architectures with Amazon SNS and Amazon SQS<br>- Learn about Network Infrastructure Auditing with VPC Flow Logs<br>- **Practice:**<br>&emsp; + Prepare infrastructure layers for the Event-driven layout and install the Event Generator package<br>&emsp; + Create an SQS Queue named OrdersQueue and subscribe it to the Orders SNS Topic<br>&emsp; + Create an SQS Queue named Orders-EU and configure a Subscription Filter Policy (`location = eu-west`)<br>&emsp; + Create an SQS Queue named Orders-RL and configure an Advanced Filter Policy based on order volumes<br>&emsp; + Initialize the network environment, provision, and activate VPC Flow Logs streaming to Amazon CloudWatch Logs | 08/06/2026   | 08/06/2026      | <https://000077.awsstudygroup.com/> <br><br> <https://000074.awsstudygroup.com> |
| 3   | - Learn about Shared Storage Data Architectures with Amazon EBS Multi-Attach and NVMe Reservations<br>- **Practice:**<br>&emsp; + Provision a Prod VPC, a Test VPC, and launch corresponding target EC2 Instances<br>&emsp; + Create an EBS Volume (`io2`) supporting Multi-Attach and attach it to multiple concurrent host servers<br>&emsp; + Install PostgreSQL, populate sample mock datasets, and perform database backup/restore runs<br>&emsp; + Configure NVMe Reservations to control coordinate access boundaries across concurrent Prod/Test environments<br>&emsp; + Verify compiled registration logs using Reservation Register and Reservation Report actions | 09/06/2026   | 09/06/2026      | <https://100000.awsstudygroup.com/> |
| 4   | - Learn about Database High Availability utilizing EBS Multi-Attach and AWS Systems Manager tools<br>- **Practice:**<br>&emsp; + Set up a dedicated network range VPC for the MySQL HA Cluster and map IAM access delegations for SSM paths<br>&emsp; + Launch target EC2 Instances, create shared EBS storage blocks, and configure Logical Volume Management (LVM)<br>&emsp; + Install MySQL configurations and orchestrate internal traffic routing via an Internal Network Load Balancer (NLB)<br>&emsp; + Deploy WordPress connecting to the backend MySQL tier via the NLB; design custom Systems Manager Runbooks & Response Plans<br>&emsp; + Configure CloudWatch Alarms and execute testing scenarios validating automated automated Fail-over infrastructure paths | 10/06/2026   | 10/06/2026      | <https://100001.awsstudygroup.com/> |
| 5   | - Learn about Fault-Tolerant Windows Server Clustering architectures inside the AWS Cloud environment<br>- **Practice:**<br>&emsp; + Build out targeted VPC/Subnet network topologies and initialize an AWS Managed Microsoft Active Directory directory service<br>&emsp; + Launch a fleet cluster of Windows EC2 Instances and join target compute nodes into the system Domain<br>&emsp; + Provision an EBS Multi-Attach volume to serve as a unified, shared cluster storage partition raw block device<br>&emsp; + Install the native Windows Failover Clustering feature and execute the foundational Cluster Validation Wizard checks<br>&emsp; + Assemble a complete Windows Failover Cluster, structuring network routing mappings and shared storage layers | 11/06/2026   | 11/06/2026      | <https://100002.awsstudygroup.com> |
| 6   | - Learn about Delegation Models governing access to the central AWS Billing Console<br>- Learn about FinOps Budgetary and Resource Provisioning Management utilizing granular IAM configurations<br>- Learn about Secure Identity and Secret Token Management via AWS Secrets Manager<br>- **Practice:**<br>&emsp; + Structure an IAM User Group, enable explicit permissions, and assign access policies controlling Billing Console visibility<br>&emsp; + Author advanced Custom IAM Policies enforcing strict provisioning boundaries mapped against Regions, EC2 Families, Instance Sizes, and EBS Volume Types<br>&emsp; + Setup a Secrets Manager operational environment synchronized with interconnecting VPC, EC2, RDS, and ECS Fargate infrastructures<br>&emsp; + Vault secure production RDS credentials and configure automated Lambda-driven rotation loops (Secret Rotation) | 12/06/2026   | 12/06/2026      | <https://000075.awsstudygroup.com> <br><br> <https://000064.awsstudygroup.com> <br><br> <https://000096.awsstudygroup.com> |

### Week 8 Achievements:

#### 1. Event-Driven Architecture Orchestration (Amazon SNS & Amazon SQS)
* Developed deep architectural comprehension separating decoupled transaction spaces (Decoupled Architecture), maximizing individual execution scaling properties between independent message originators (Publishers) and backend data processors (Consumers).
* **Advanced Message Ingestion Filtering:** Mastered intelligent event routing parameters inside Amazon SNS using Subscription Filter Policies (enforcing selective string attribute matches like `location = eu-west`) and Advanced Filter Policies (implementing mathematical boundaries such as `quantity >= 100`), offloading data triage processing logic entirely away from downstream application layers.

#### 2. Perimeter Network Infrastructure Auditing via VPC Flow Logs
* Grasped continuous capture and auditing mechanics tracking public/private internet protocol metadata streams (Inbound/Outbound traffic summaries) cutting through Elastic Network Interfaces (ENI) across targeted VPC subnets.
* **Network Security Administration Practice:** Activated automated VPC Flow Logs streaming straight into central Amazon CloudWatch Logs repositories, parsing discrete `ACCEPT` and `REJECT` transaction flags to isolate infrastructure perimeter rule leaks or identify misconfigured Security Group / Network ACL settings.

#### 3. High-Availability Block Storage Sharing via Amazon EBS Multi-Attach & NVMe Reservations
* Understood structural capabilities backing high-tier Amazon EBS `io2` block storage volumes designed to mount concurrently across multiple standalone EC2 host instances situated inside an isolated Availability Zone (AZ).
* **Concurrent Data Integrity Governance:** Successfully operated concurrent file lock controls via NVMe Reservation tracking frameworks (utilizing `Reservation Register` and `Reservation Report` command structures) to coordinate parallel read/write boundaries across Production and Testing instances hitting shared PostgreSQL targets, neutralizing data corruption risk vectors.

#### 4. Automated MySQL HA Cluster Engineering with AWS Systems Manager Integration
* Engineered an end-to-end high-availability (HA) relational MySQL database cluster layout running atop shared EBS Multi-Attach block devices managed via Logical Volume Management (LVM) layer abstractions.
* **Automated Disaster Recovery (Auto Fail-over):** Constructed an Internal Network Load Balancer (NLB) layer shielding database paths to service inbound WordPress requests, authored adaptive automated infrastructure runbooks via AWS Systems Manager Automation paired with Incident Manager Response Plans and CloudWatch Alarms, enabling the infrastructure to execute rapid automated node promotion sequences upon principal node failures with zero-downtime performance targets.

#### 5. Enterprise Windows Failover Cluster Infrastructure Staging
* Mastered architectural patterns required to deploy production-grade, fault-tolerant enterprise Windows Server ecosystems directly across cloud-based compute landing zones.
* **Microsoft Directory Infrastructure Synchronization:** Provisioned a central AWS Managed Microsoft Active Directory hub, interconnected target Windows EC2 nodes into the managed identity directory system, and passed rigorous validation criteria inside the native Cluster Validation Wizard to run a cluster backed by shared EBS Multi-Attach `io2` block architectures.

#### 6. Enterprise FinOps Infrastructure and Budgetary Governance via IAM Policies
* Developed complete operational proficiency governing financial oversight controls and resource constraint parameters for multi-tier, distributed business organizational units.
* **Resource Privilege Boundary Delegation:** Executed secure operational handoffs enabling programmatic billing console visibility for dedicated IAM User Groups decoupled from root credentials; designed robust Custom IAM Policies restricting asset provisioning capability by locking user access parameters strictly against allowed Regions, targeted architecture classes (EC2 Family), compute sizing scales (Instance Size), and storage hardware definitions (EBS Volume Type) to drive down capital expenditures.

#### 7. Secure Application Credential Lifecycle Management via AWS Secrets Manager
* Eliminated high-risk structural credential leaks arising from hard-coded username/password configurations embedded directly into source tracking systems or container parameters.
* **Sensitive Token Vaulting Practice:** Configured AWS Secrets Manager environments to retain encrypted Amazon RDS administrative database access records, implemented automated zero-downtime rotation scripts using dedicated AWS Lambda rotation handlers, and linked serverless ECS Fargate task deployments to ingest live, dynamic credential blocks securely over internal VPC Endpoints.