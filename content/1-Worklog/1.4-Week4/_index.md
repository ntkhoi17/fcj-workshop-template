---
title: "Week 4 Worklog"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---


### Week 4 Objectives:

* Learn how to connect two VPCs using VPC Peering.
* Get familiar with Docker and the application packaging process using Containers.
* Practice storing Docker Images on Amazon ECR.
* Learn about the basic components of Amazon ECS.
* Learn about long-term cost optimization options for EC2 and RDS.

### Tasks to implement this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Learn about VPC Peering<br>- Learn about Network ACLs and Cross-Peer DNS<br>- **Practice:**<br>&emsp; + Prepare two VPCs and an EC2 Instance<br>&emsp; + Create a VPC Peering connection<br>&emsp; + Update Route Tables<br>&emsp; + Verify the connection between two VPCs<br>&emsp; + Activate Cross-Peer DNS | 11/05/2026 | 11/05/2026 | <https://000019.awsstudygroup.com> |
| 3 | - Learn about Docker and Docker Images<br>- Learn about Docker Containers and Docker Compose<br>- **Practice:**<br>&emsp; + Install necessary tools<br>&emsp; + Run the application in a Local environment<br>&emsp; + Create a Docker Image<br>&emsp; + Launch a Docker Container<br>&emsp; + Verify the application using Docker Compose | 12/05/2026 | 12/05/2026 | <https://000015.awsstudygroup.com> |
| 4 | - Learn about Amazon Elastic Container Registry<br>- Learn how to deploy Docker on EC2<br>- **Practice:**<br>&emsp; + Create an Amazon ECR Repository<br>&emsp; + Configure an IAM Role for EC2<br>&emsp; + Create an EC2 Instance<br>&emsp; + Push a Docker Image to Amazon ECR<br>&emsp; + Pull the Image and run the Container on EC2 | 13/05/2026 | 13/05/2026 | <https://000015.awsstudygroup.com> |
| 5 | - Learn an overview of Amazon ECS<br>- Learn about ECS Clusters, Task Definitions, and ECS Services<br>- **Basic Practice:**<br>&emsp; + Create an ECS Cluster<br>&emsp; + Create a simple Task Definition<br>&emsp; + Create an ECS Service<br>&emsp; + Deploy a Container from Amazon ECR<br>&emsp; + Verify the status of ECS Tasks<br>&emsp; + Clean up resources post-practice | 14/05/2026 | 14/05/2026 | <https://000016.awsstudygroup.com> |
| 6 | - Learn about Savings Plans<br>- Learn about Reserved Instances and Reserved DB Instances<br>- Compare commitment-based utilization models<br>- **Practice:**<br>&emsp; + View Savings Plans Recommendations<br>&emsp; + Analyze commitment terms and payment options<br>&emsp; + Compare Savings Plans with Reserved Instances<br>&emsp; + Summarize and review Week 4 content | 15/05/2026 | 15/05/2026 | <https://000042.awsstudygroup.com> |

### Week 4 Achievements:

* Understood how VPC Peering connects resources between two VPCs using private network addresses.
* Learned how to update Route Tables and verify connectivity between two VPCs.
* Differentiated between Security Groups and Network ACLs.
* Understood the basic concepts of Docker:
  * Docker Image
  * Docker Container
  * Dockerfile
  * Docker Compose
* Packaged and ran an application using Docker in a Local environment.
* Learned how to create Repositories and store Docker Images on Amazon ECR.
* Deployed a basic Docker Container on Amazon EC2.
* Understood the main components of Amazon ECS:
  * ECS Cluster
  * Task Definition
  * ECS Task
  * ECS Service
* Practiced deploying a basic Container on Amazon ECS.
* Understood the differences between Savings Plans, Reserved Instances, and Reserved DB Instances.
* Learned how to view Savings Plans Recommendations for cost optimization options.
