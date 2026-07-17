---
title: "Week 2 Worklog"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---


### Week 2 Objectives:

* Learn how to manage resources, optimize costs, and control access on AWS.
* Understand the mechanisms of application scaling, load balancing, and system monitoring.
* Get familiar with AWS CLI, Lambda, CloudWatch, Grafana, and operations automation.
* Learn about Hybrid DNS and methodologies for migrating servers and databases to AWS.

### Tasks to implement this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Learn about Amazon Lightsail<br>- Learn about Tags and Resource Groups<br>- **Practice:**<br>&emsp; + Deploy WordPress and Databases on Lightsail<br>&emsp; + Configure Networking<br>&emsp; + Assign Tags and create Resource Groups | 27/04/2026 | 27/04/2026 | <https://000045.awsstudygroup.com> <br><br> <https://000027.awsstudygroup.com> |
| 3 | - Learn about Amazon EC2 Auto Scaling<br>- Learn about controlling EC2 permissions using Resource Tags<br>- **Practice:**<br>&emsp; + Create Launch Templates and Target Groups<br>&emsp; + Create Elastic Load Balancers and Auto Scaling Groups<br>&emsp; + Test various Scaling types<br>&emsp; + Create IAM Policies based on Tag conditions | 28/04/2026 | 28/04/2026 | <https://000006.awsstudygroup.com> <br><br> <https://000028.awsstudygroup.com> |
| 4 | - Learn about Amazon CloudWatch and Grafana<br>- Learn about automating EC2 start/stop using Lambda<br>- **Practice:**<br>&emsp; + Analyze Metrics and Logs<br>&emsp; + Create Alarms and Dashboards<br>&emsp; + Install Grafana on EC2<br>&emsp; + Create Lambda Functions to Start/Stop EC2<br>&emsp; + Send notifications via Slack | 29/04/2026 | 29/04/2026 | <https://000008.awsstudygroup.com> <br><br> <https://000029.awsstudygroup.com> <br><br> <https://000022.awsstudygroup.com> |
| 5 | - Learn about Hybrid DNS with Route 53 Resolver<br>- Learn about using the AWS CLI on EC2 Windows/Ubuntu<br>- **Practice:**<br>&emsp; + Deploy Microsoft Active Directory<br>&emsp; + Create Inbound and Outbound Endpoints<br>&emsp; + Create Resolver Rules<br>&emsp; + Install and utilize the AWS CLI | 30/04/2026 | 30/04/2026 | <https://000010.awsstudygroup.com> <br><br> <https://000011.awsstudygroup.com> |
| 6 | - Learn about AWS VM Import/Export<br>- **Practice:**<br>&emsp; + Prepare virtual machines from On-premise environments<br>&emsp; + Export virtual machines from virtualization environments<br>&emsp; + Upload virtual machine files to Amazon S3<br>&emsp; + Import virtual machines into AWS<br>&emsp; + Create AMIs from imported virtual machines<br>&emsp; + Deploy EC2 Instances from AMIs | 01/05/2026 | 01/05/2026 | <https://000014.awsstudygroup.com> |

### Week 2 Achievements:

* Successfully deployed WordPress and Databases on Amazon Lightsail.
* Learned how to use Tags and Resource Groups to classify, search, and manage resources.
* Understood how Auto Scaling Groups combine with Elastic Load Balancers to scale applications and increase availability.
* Learned how to create IAM Policies that control EC2 access based on Resource Tags.
* Utilized CloudWatch to monitor:
  * Metrics
  * Logs
  * Alarms
  * Dashboards
* Installed Grafana on EC2 and connected data for monitoring from AWS.
* Created Lambda Functions to automatically start/stop EC2 instances and send notifications via Slack.
* Understood how Route 53 Resolver supports DNS resolution between Local environments and Amazon VPCs.
* Installed and configured AWS CLI to check, create, and manage AWS resources.
* Understood the process of migrating virtual machines from On-premise environments to AWS using VM Import/Export.
* Learned how to store virtual machine files on Amazon S3, create AMIs, and deploy EC2 Instances from the imported virtual machines.