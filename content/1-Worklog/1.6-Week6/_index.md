---
title: "Week 6 Worklog"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---


### Week 6 Objectives:

* Explore serverless workflow orchestration with AWS Step Functions utilizing State Machines, Task States, Choice States, Parallel States, and error handling mechanisms.
* Practice building serverless applications using AWS Lambda, Amazon S3, Amazon DynamoDB, Amazon API Gateway, and web Frontends.
* Understand serverless application deployment methodologies using the AWS Serverless Application Model (SAM) and deployment automation via AWS CodePipeline.
* Learn user authentication mechanisms with Amazon Cognito and establish a secure, SSL-enabled static website using Amazon S3, Amazon Route 53, AWS Certificate Manager, and Amazon CloudFront.
* Get familiar with asynchronous order processing systems using Amazon SQS and Amazon SNS, alongside Lambda application monitoring via Amazon CloudWatch, CloudWatch Alarms, and AWS X-Ray.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Learn about Getting Started with AWS Step Functions<br>- **Practice:**<br>&emsp; + Study Service Orchestration and the business logic of the sample workflow<br>&emsp; + Provision an AWS Cloud9 Instance for the practice environment<br>&emsp; + Create sample microservices using AWS Lambda<br>&emsp; + Verify Account Application and Data Checking steps<br>&emsp; + Initialize a State Machine via AWS Step Functions<br>&emsp; + Build a workflow utilizing Task States<br>&emsp; + Update execution permissions within the SAM Template<br>&emsp; + Manage State Input and State Output structures<br>&emsp; + Configure Choice States for workflow branching logic<br>&emsp; + Enhance the workflow with Pause and Resume triggers<br>&emsp; + Implement retry and catch configurations for error handling<br>&emsp; + Configure Parallel States for concurrent multi-task processing | 25/05/2026   | 25/05/2026      | <https://000047.awsstudygroup.com/vi/> |
| 3   | - Learn about Serverless - Lambda Interactions with S3 and DynamoDB<br>- Learn about Serverless - Directing Frontends to Invoke API Gateway Endpoints<br>- **Practice:**<br>&emsp; + Study Serverless architectures combining Lambda, S3, DynamoDB, and API Gateway<br>&emsp; + Create image processing Lambda Functions & configure automated S3 Bucket event triggers<br>&emsp; + Define IAM Policies for Lambda Functions & verify execution on S3 object uploads<br>&emsp; + Design a DynamoDB table with Partition Keys and Sort Keys<br>&emsp; + Create a Lambda Function to write records into DynamoDB & deploy the web Frontend<br>&emsp; + Create Lambda Functions to read/delete data records & configure API Gateway Methods<br>&emsp; + Install and enable CORS configurations & verify API invocations via Postman and Frontend | 26/05/2026   | 26/05/2026      | <https://000078.awsstudygroup.com/vi/> <br><br> <https://000079.awsstudygroup.com/vi/> |
| 4   | - Learn about Serverless - Deploying Applications via AWS SAM<br>- Learn about Serverless - User Authentication with Amazon Cognito<br>- **Practice:**<br>&emsp; + Prepare the local workspace for serverless application deployment using AWS SAM<br>&emsp; + Deploy the web Frontend, provision DynamoDB tables, and stage Lambda data processing clusters<br>&emsp; + Configure API Gateway structures using SAM (Define GET, POST, and DELETE APIs)<br>&emsp; + Initialize an Amazon Cognito User Pool for centralized identity management<br>&emsp; + Integrate Cognito authorizers into API Gateway paths and Lambda Backend functions<br>&emsp; + Test User Registration, Login, and Authentication workflows directly on the Frontend UI | 27/05/2026   | 27/05/2026      | <https://000080.awsstudygroup.com/vi/> <br><br> <https://000081.awsstudygroup.com/vi/> |
| 5   | - Learn about Serverless - Setting up an SSL-Enabled Static Website on Amazon S3<br>- Learn about Serverless - Order Processing Workflows with SQS and SNS<br>- **Practice:**<br>&emsp; + Stage a static website architecture on S3 and configure custom Amazon Route 53 domains<br>&emsp; + Generate SSL/TLS public certificate requests via AWS Certificate Manager (ACM)<br>&emsp; + Configure an Amazon CloudFront Distribution to distribute web assets securely over HTTPS<br>&emsp; + Initialize order processing frameworks: Create SQS Queues, SNS Topics, and the OrdersTable<br>&emsp; + Deploy the serverless Lambda cluster: checkout_order, order_management, handle_order, delete_order<br>&emsp; + Validate Checkout pipelines, message broadcasting via SNS, and DynamoDB data persistence | 28/05/2026   | 28/05/2026      | <https://000082.awsstudygroup.com/vi/> <br><br> <https://000083.awsstudygroup.com/vi/> |
| 6   | - Learn about Serverless - Continuous Delivery CI/CD via AWS CodePipeline<br>- Learn about Serverless - Deeper Lambda Monitoring with CloudWatch and AWS X-Ray<br>- **Practice:**<br>&emsp; + Initialize a Git Repository for the SAM Project & establish SAM CI/CD Pipelines<br>&emsp; + Configure CodeBuild jobs to compile application assets and package CloudFormation Templates<br>&emsp; + Establish and execute automated, independent pipeline runs for Backend & Frontend components<br>&emsp; + Synchronize source code updates to automatically compile and push Frontend static folders to S3<br>&emsp; + Run code diagnostics for Lambda via logs, configure Custom Metrics & create CloudWatch Alarms<br>&emsp; + Integrate AWS X-Ray tracking to intercept API Traces, analyzing latency and system errors | 29/05/2026   | 29/05/2026      | <https://000084.awsstudygroup.com/vi/> <br><br> <https://000085.awsstudygroup.com/vi/> |

### Week 6 Achievements:

#### 1. Workflow Orchestration with AWS Step Functions
* Understood the core role of AWS Step Functions as a centralized Service Orchestration engine, seamlessly binding independent microservices into unified business workflows.
* Mastered state machine design principles, capturing state manipulation paradigms through structured State Input and State Output transformations.
* **Complex Workflow Implementation Practice:** Managed an integrated Cloud9 workspace to build sample logic, successfully configuring operational states: Task States to execute Lambda routines, Choice States to perform logical conditional branching, Parallel States to run concurrent multi-threaded execution blocks, and integrated token-based Callback patterns to handle human-in-the-loop validation gates.
* **Fault Tolerance Engineering:** Implemented native structural error handling using explicit `Retry` definitions for transient failure mitigation and `Catch` statements to capture exceptions and smoothly route execution states.

#### 2. Core Serverless Architecture Engineering (Lambda, S3, DynamoDB, API Gateway)
* Developed deep structural mastery regarding standard Serverless paradigms: aligning financial operational budgets with actual system consumption metrics (Pay-as-you-go), driving boundless horizontal auto-scaling, and completely offloading underlying runtime administration tasks.
* **Inbound Media Ingestion Pipeline Practice:**
  * Configured automated S3 `PutObject` events to asynchronously trigger down-stream image optimization Lambda functions, embedding specialized Lambda Layers to streamline source deployment package sizing.
  * Engineered robust NoSQL database layouts on Amazon DynamoDB utilizing optimized Partition Keys and Sort Keys, managed granular least-privilege IAM Policies, and ran CRUD transactions via the official AWS SDK.
  * Built secure API management boundaries with Amazon API Gateway acting as an ingestion layer to compute functions, handled method configurations, and deployed Cross-Origin Resource Sharing (CORS) overrides allowing external frontends to invoke service endpoints across Postman and production configurations.

#### 3. Advanced Serverless Framework Design with AWS SAM (Serverless Application Model)
* Mastered the AWS SAM structural layout to specify, declare, and version complex serverless infrastructures-as-code using minimal, readable YAML configurations.
* **Infrastructure Prototyping Practice:** Re-architected previous decoupled infrastructure elements directly into organized SAM deployment templates, capturing unified declarations for multi-method API Gateways (GET/POST/DELETE), associated Lambda compute clusters, and backing DynamoDB definitions to generate precise compiled AWS CloudFormation templates.

#### 4. Centralized Identity Federation via Amazon Cognito
* Clearly differentiated architectural roles separating Cognito User Pools (handling directory retention, credentials management, registration loops, and MFA/OTP validation pathways) from Identity Pools (exposing short-lived, authenticated AWS IAM authorization tokens to grant direct resource interface accesses).
* **Identity Integration Practice:** Provisioned a central Cognito User Pool, bound secure Token Authorizers directly across API Gateway routes, and successfully validated operational security pipelines (User Signup, Login verification, and Token exchange tokens) mapped against the Frontend user interface.

#### 5. Secure CDN Global Edge Asset Distribution via CloudFront and Amazon S3
* Grasped modern content delivery patterns protecting web traffic in transit via SSL/TLS encryption, custom domain configurations, and localized edge caching structures.
* **Edge Routing Infrastructure Practice:** Established custom Hosted Zones inside Amazon Route 53 to manage public records, requested managed public SSL/TLS certificates via AWS Certificate Manager (ACM), and engineered an global Amazon CloudFront Distribution layer to deliver static S3 assets with optimal low-latency parameters and maximum edge safety boundaries.

#### 6. Asynchronous Event-Driven Order Processing via Amazon SQS and Amazon SNS
* Mastered asynchronous event-driven design topologies to decouple frontend checkout ingestion paths entirely from downstream transaction processing layers, insulating application states from sudden load spikes.
* **Serverless Order Execution Practice:** Initialized high-throughput Amazon SQS messaging queues paired with fan-out Amazon SNS Topics, engineered a cohesive serverless compute execution pipeline (`checkout_order`, `order_management`, `handle_order`, `delete_order`), and validated end-to-end multi-consumer message processing loops driving decoupled transactional records straight into backing DynamoDB arrays.

#### 7. Automated Serverless Lifecycle Pipelines via AWS CodePipeline
* Understood DevOps practices applied specifically to distributed serverless architectures, eliminating manual execution variances and securing continuous, standardized version releases.
* **Continuous Delivery Automation Practice:** Assembled organized source Git Repositories, created automated CodeBuild compile specifications to package SAM build artifacts, and deployed two isolated, concurrent pipelines inside CodePipeline: a dedicated Backend continuous delivery track (orchestrating automatic CloudFormation Stack updates on logic adjustments) and a distinct Frontend pipeline (compiling presentation layers and synchronizing structural static assets straight to backing S3 static web-hosting endpoints).

#### 8. Deep Serverless System Observability via CloudWatch and AWS X-Ray
* Grasped the critical importance of deep cloud auditing, telemetry tracing, and log metrics mapping (Observability) within distributed, asynchronous serverless execution fields.
* **Production Operations Practice:**
  * Extracted runtime diagnostics via CloudWatch Logs to execute rapid troubleshooting and inspect granular error tracebacks across individual Lambda invocations.
  * Engineered custom business-level metrics tracking application states, mapping them directly onto specific CloudWatch Alarms to automate notification routing if system limits breach configured thresholds.
  * Activated distributed transaction parsing via AWS X-Ray Traces to visualize global Service Maps, accurately measuring temporal latency boundaries and identifying processing bottlenecks spanning edge API Gateways down to compute layers.
