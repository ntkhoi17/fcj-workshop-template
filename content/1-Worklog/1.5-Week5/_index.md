---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---


### Week 5 Objectives:

* Explore methodologies for server right-sizing, cost visualization, and advanced cost analysis on AWS.
* Understand the process of decomposing and migrating the Monolith TravelBuddy application into a Microservices architecture using Elastic Beanstalk, CodeStar, CodePipeline, Lambda, and API Gateway.
* Practice refactoring data layers and orchestration workflows using Amazon DynamoDB, AWS Lambda, AWS Step Functions, and serverless workflows.
* Learn messaging and event-driven communication patterns between microservices using Amazon SQS, Amazon SNS, Amazon Kinesis, and MQTT.
* Get familiar with building a Single Page Application (SPA) secured by Amazon Cognito authentication and gain hands-on experience with AWS AI services including Amazon Polly, Amazon Rekognition, and Amazon Lex.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Learn about Server Right-Sizing with Amazon EC2 Resource Optimization<br>- Learn about Cost Visualization on AWS<br>- Learn about Advanced Cost Analysis with AWS Glue and Amazon Athena<br>- **Practice:**<br>&emsp; + Gain familiarity with Amazon CloudWatch<br>&emsp; + Create an IAM Role for the Amazon CloudWatch Agent<br>&emsp; + Attach the CloudWatch IAM Role to an EC2 Instance<br>&emsp; + Install the CloudWatch Agent<br>&emsp; + Update Amazon EC2 Resource Optimization parameters<br>&emsp; + Review right-sizing recommendations using AWS Compute Optimizer<br>&emsp; + Analyze cost and usage broken down by service<br>&emsp; + Analyze cost and usage broken down by account<br>&emsp; + Review coverage metrics for Savings Plans and Reserved Instances<br>&emsp; + Generate custom EC2 utilization reports<br>&emsp; + Perform cost analysis with AWS Cost Explorer<br>&emsp; + Prepare the database target for cost analysis workflows<br>&emsp; + Build out the data catalog using AWS Glue<br>&emsp; + Query granular billing data utilizing Amazon Athena | 18/05/2026   | 18/05/2026      | <https://000032.awsstudygroup.com> <br><br> <https://000034.awsstudygroup.com/> <br><br> <https://000040.awsstudygroup.com> |
| 3   | - Learn about Monolith Application Migration strategies<br>- Learn about Automated Application Deployment workflows<br>- **Practice:**<br>&emsp; + Create Key Pairs<br>&emsp; + Provision a CloudFormation Stack for the TravelBuddy environment<br>&emsp; + Establish a connection to the Windows Instance<br>&emsp; + Install and initialize the Database engine<br>&emsp; + Download the TravelBuddy project source repository<br>&emsp; + Validate application operations locally using Eclipse IDE<br>&emsp; + Deploy the Monolith application onto AWS Elastic Beanstalk<br>&emsp; + Update application components and run API queries via Eclipse IDE<br>&emsp; + Prepare the environment for continuous automated delivery<br>&emsp; + Provision an AWS CodeStar Project framework<br>&emsp; + Connect Eclipse IDE to the AWS CodeCommit repository<br>&emsp; + Replace the sample placeholder application code<br>&emsp; + Execute deployment tracking through CodePipeline<br>&emsp; + Identify and troubleshoot pipeline deployment failures<br>&emsp; + Create an EC2 Windows Instance target<br>&emsp; + Setup a CodeDeploy Application and Deployment Group<br>&emsp; + Create an S3 Bucket to retain deployment package artifacts<br>&emsp; + Deploy a background Windows Service utilizing AWS CodeDeploy | 19/05/2026   | 19/05/2026      | <https://000050.awsstudygroup.com> <br><br> <https://000051.awsstudygroup.com> |
| 4   | - Learn about Building and Creating Microservices<br>- Learn about Data Refactoring and Workflow Orchestration<br>- **Practice:**<br>&emsp; + Set up the development workspace and configure Eclipse IDE<br>&emsp; + Create and test an AWS Lambda Function locally<br>&emsp; + Upload and deploy the compiled function package onto AWS Lambda<br>&emsp; + Configure an S3 event trigger to invoke Lambda on object uploads<br>&emsp; + Update Lambda logic to generate thumbnails for `image/jpeg` uploads<br>&emsp; + Implement logic to purge non-image file formats automatically<br>&emsp; + Generate deployment packages and automate workflows using the AWS CLI<br>&emsp; + Deploy the optimized Lambda ImageManager microservice<br>&emsp; + Automate Serverless Microservices using AWS SAM and CloudFormation templates<br>&emsp; + Establish a new development branch and re-deploy via the CI/CD Pipeline<br>&emsp; + Create an Amazon DynamoDB Table asset<br>&emsp; + Configure Global Secondary Indexes (GSI) for enhanced query indexing<br>&emsp; + Automate localized microservice execution flows<br>&emsp; + Expose endpoints by building an API for the microservice tier<br>&emsp; + Update IAM Policies and push execution builds through the pipeline<br>&emsp; + Design visual states and workflows using AWS Step Functions<br>&emsp; + Develop a Lambda Microservice powering a Calculator Workflow logic<br>&emsp; + Expand and scale the execution steps of the Calculation Workflow | 20/05/2026   | 20/05/2026      | <https://000052.awsstudygroup.com> <br><br> <https://000053.awsstudygroup.com> |
| 5   | - Learn about Microservice Messaging and Eventing systems<br>- Learn about Constructing and Authenticating Single Page Applications (SPA)<br>- **Practice:**<br>&emsp; + Prepare the runtime environment and configure the AWS CLI<br>&emsp; + Host and deploy static Web assets onto Amazon S3 bucket storage<br>&emsp; + Run Point-to-Point message patterns from an SQS Publisher to an SQS Subscriber<br>&emsp; + Implement Fan-out patterns from an SQS Publisher to multiple SQS Subscribers<br>&emsp; + Execute sequential messaging utilizing SQS FIFO Queues<br>&emsp; + Orchestrate messaging from an SNS Publisher to multiple SQS Subscribers<br>&emsp; + Stream data records from a Kinesis Publisher down to an SQS Subscriber tier<br>&emsp; + Build event tracking from an MQTT Publisher to an MQTT Subscriber<br>&emsp; + Develop a custom Kinesis Producer data engine<br>&emsp; + Push stream logs and records into the active Amazon Kinesis stream<br>&emsp; + Validate and verify ingested data structures inside Elasticsearch<br>&emsp; + Leverage Kibana dashboards to analyze and discover log records<br>&emsp; + Create a backing Amazon DynamoDB Table for the SPA tier<br>&emsp; + Construct and deploy a Serverless Microservice using manual routines<br>&emsp; + Build out and expose public REST endpoints using Amazon API Gateway<br>&emsp; + Deploy API configurations utilizing automated CodeStar CI/CD tracks<br>&emsp; + Build out the layout structure for the Single Page Application<br>&emsp; + Construct API client consumption models within the client application<br>&emsp; + Integrate secure identity routing via Amazon Cognito User Pools<br>&emsp; + Configure authorization constraints blocking unsecured backend microservices<br>&emsp; + Run test runs for end-user User Registration and Login workflows<br>&emsp; + Trace transaction execution performance via AWS X-Ray service mapping | 21/05/2026   | 21/05/2026      | <https://000054.awsstudygroup.com> <br><br> <https://000055.awsstudygroup.com> |
| 6   | - Learn about AI Service Implementations natively on AWS platforms<br>- Synthesize end-to-end application transformations from Monolith to Microservices<br>- **Practice:**<br>&emsp; + Prepare the system workspace to utilize Amazon Polly engines<br>&emsp; + Explore Amazon Polly and generate Speech/Speech Marks via AWS CLI & Java SDK<br>&emsp; + Build out backend prerequisites to handle Amazon Rekognition workflows<br>&emsp; + Execute Object Detection and Facial Recognition via Amazon Rekognition APIs<br>&emsp; + Deploy and test a working real-time tracking application<br>&emsp; + Deploy the TravelBuddy stack integrated directly with Amazon Lex solutions<br>&emsp; + Model and enhance an intelligent Amazon Lex Chatbot for TravelBuddy users<br>&emsp; + Write a custom Lambda Handler to manage Lex Bot dialog logic paths<br>&emsp; + Publish the finalized Lex Chatbot and review the composite global architecture | 22/05/2026   | 22/05/2026      | <https://000056.awsstudygroup.com> |

### Week 5 Achievements:

#### 1. Amazon EC2 Resource Optimization Exploration
* Understood right-sizing methodology to align EC2 infrastructure capacity with workload demands, eliminating compute resource waste and reducing operational overhead.
* Mastered the implementation of the CloudWatch Agent to capture deeper operating system level metrics, specifically tracking Memory (RAM) utilization boundaries unavailable in hypervisor-level metrics.
* **Infrastructure Optimization Practice:** Developed IAM Roles for EC2 execution, completed systematic agent provisioning across target servers, and extracted automated, actionable resizing guidance using AWS Compute Optimizer engines.

#### 2. Billing Infrastructure Profiling via AWS Cost Explorer
* Mastered granular visual interfaces inside the AWS Billing ecosystem to categorize, track, and decompose financial expenditures across multi-tier accounts, individual standalone services, or specific business product vectors.
* Grasped structural verification analysis methods to trace ongoing coverage parameters and financial consumption rates under deployed Savings Plans and Reserved Instances (RI).
* Constructed custom tailored EC2 allocation report tracking sets to closely monitor utilization anomalies, forecast expenditure curves, and detail data transfer charging parameters across multi-zone infrastructure deployments.

#### 3. Enterprise FinOps Data Architecture via AWS Glue and Amazon Athena
* Grasped the underlying design topologies backing automated large-scale data lake pipelines ingestion processing Cost and Usage Reports (CUR).
* **Big Data Engineering Practice:** Orchestrated automated schema extraction pipelines utilizing AWS Glue Crawlers to structure unformatted data objects, populated a unified central Data Catalog registry, and executed optimized analytical SQL queries via Amazon Athena to isolate granular cost-allocation tags.

#### 4. Monolith Infrastructure Deconstruction (DevAx TravelBuddy Sequence)
* Understood architectural layers, interdependencies, and scaling limitations holding back legacy Monolith systems (specifically legacy TravelBuddy apps running on tight Java Server Pages / Servlet models backed by centralized data engines).
* **Monolith Lifecycle Migration Practice:** Assembled multi-tier testing tiers leveraging AWS CloudFormation stacks, provisioned isolated relational database subsystems, built source elements via local Eclipse environments, and staged the monolithic container onto fully managed AWS Elastic Beanstalk environments to run integration validations.

#### 5. Continuous Integration Delivery Models via CodeStar & CodeDeploy
* Understood automated software release lifecycle principles targeting monolithic enterprise applications to standardize system changes.
* **Continuous Integration Setup Practice:** Initiated unified AWS CodeStar agile delivery project templates tracking CodeCommit code repositories, linked CodeBuild and continuous CodePipeline structures to map source changes straight to Elastic Beanstalk, and set up automated CodeDeploy routines driving localized host runtime environment upgrades via Amazon S3 code artifacts.

#### 6. Microservice Isolation Patterns via Event-Driven AWS Lambda Functions
* Mastered modular architectural decomposition rules to detach compute-heavy, independent operational workflows away from legacy monolithic frameworks into decoupled, event-driven serverless tiers.
* **Serverless Engineering Practice:** Structured native Java-based Lambda function definitions inside Eclipse IDE, configured reactive Amazon S3 object-creation triggers (`PutObject`), implemented image processing processing flows to automatically generate compressed thumbnails for incoming `image/jpeg` streams, and wrote validation loops purging unsupported media formats instantly.

#### 7. Serverless Infrastructure Automation using AWS SAM (Serverless Application Model)
* Understood open-source framework patterns utilizing AWS SAM to build, declare, and version infrastructure-as-code deployments targeting complex serverless application boundaries.
* **Continuous Serverless Deployment Practice:** Managed deployment package synthesis operations via the AWS CLI, authored precise declaration documents specifying functions, API Gateway event targets, and S3 asset repositories, and mapped branch-level updates through continuous delivery pipelines.

#### 8. Data Layer Refactoring (NoSQL Transformation via Amazon DynamoDB)
* Mastered the architectural data transition paths separating structured SQL schemas into non-relational distributed NoSQL topologies following modern Polyglot Persistence models.
* **NoSQL Database Modeling Practice:** Constructed robust Amazon DynamoDB database tables, engineered performance-optimized lookup indices leveraging Global Secondary Indexes (GSI) to maximize partition querying speeds for high-velocity transaction structures, and integrated decoupled routing boundaries via API Gateway under strict IAM access policies via continuous integration engines.

#### 9. Distributed Microservices Coordination using AWS Step Functions
* Understood state machine orchestration methodologies to design, coordinate, and maintain reliable, decoupled visual states across multi-tier serverless microservice execution pipelines.
* **Workflow Automation Practice:** Designed and executed an automated calculation engine workflow mapping multiple sequential serverless Lambda function logic layers, maximizing system resilience and fault tolerance parameters across distributed app tiers.

#### 10. Asynchronous Inter-Service Communication Layouts (SQS, SNS, Kinesis, MQTT)
* Mastered four distinct underlying cloud-based enterprise asynchronous messaging styles to isolate processing faults and decouple dependent microservices components:
  * **Amazon SQS:** Engineered point-to-point transactional queues ensuring reliable asynchronous message consumption, exploring standard queues and strictly sequenced SQS FIFO queues.
  * **Amazon SNS:** Designed fan-out architectural messaging layouts allowing standalone publishers to broadcast event tracking notifications to multiple consumer queues simultaneously.
  * **Amazon Kinesis:** Orchestrated continuous large-scale real-time telemetry streaming architectures capturing active producer message pipelines.
  * **MQTT:** Configured high-velocity, low-overhead event tracking compliant with modern IoT framework standards.
* **Centralized Log Ingestion Practice:** Constructed data processing paths forwarding ingestion streams straight from Amazon Kinesis into Elasticsearch indices, utilizing Kibana data visualization interfaces to run structural diagnostics.

#### 11. Single Page Application (SPA) Architectural Patterns on Cloud Storage
* Understood architectural decoupling separation paradigms dividing front-end client presentation layers entirely away from modular, distributed backend API microservice processing systems.
* **Frontend Hosting Delivery Practice:** Completed deployment operations for a static Single Page Application (SPA) layout running out of securely configured, low-latency Amazon S3 static web-hosting storage structures.

#### 12. Microservices Gatekeeping and Routing via Amazon API Gateway
* Mastered edge-routing security methodologies using Amazon API Gateway as a single reverse-proxy entry point guarding distributed compute backends and managing structural request translations.
* **API Ingestion Configuration Practice:** Engineered backend REST resource endpoints mapped directly onto backing DynamoDB non-relational tables, managing rapid schema updates under fully automated CodeStar continuous integration loops.

#### 13. Advanced Client Authentication Federation via Amazon Cognito
* Mastered standard enterprise Identity Access Control protocols (AAA: Authentication, Authorization, Accounting) required to guarantee end-to-end data safety in public cloud environments.
* **Identity Security Practice:** Provisioned localized Amazon Cognito User Pools acting as an identity control core, built secure JWT token token-verification logic protecting downstream API Gateway paths, executed rigorous edge test scripts validating new User Signup and Login verification pathways, and mapped end-to-end service dependencies utilizing AWS X-Ray telemetry.

#### 14. Cognitive Text-to-Speech Transformation using Amazon Polly Engines
* Understood structural mechanisms native to Amazon Polly cloud engines designed to process raw textual inputs into high-fidelity, natural-sounding audio streams using deep learning models.
* **Applied AI Engineering Practice:** Generated precise speech files using the AWS CLI and Java software development kits (SDK), capturing aligned Speech Marks attributes to synchronize real-time mouth-shapes and temporal visual properties with downstream media playback devices.

#### 15. Computer Vision & Intelligent Natural Language Processing (Rekognition & Lex)
* Mastered advanced deep-learning computer vision capabilities native to Amazon Rekognition alongside contextual multi-turn conversational interface orchestration via Amazon Lex engines.
* **Applied AI Production Practice:**
  * Implemented object detection, granular face tracking, and biometric facial analysis properties utilizing Amazon Rekognition to handle custom image lookup applications.
  * Deployed a fully integrated Amazon Lex multi-turn conversational chatbot directly into the responsive TravelBuddy client framework, linked specialized serverless validation handlers (Lambda validation hooks) to process localized intent fulfillment records, and published production chat releases across unified service structures.
