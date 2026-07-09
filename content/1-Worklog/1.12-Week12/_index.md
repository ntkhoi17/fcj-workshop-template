---
title: "Week 12 Worklog"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---


### Week 12 Objectives:

* Finalize deep security configurations and establish comprehensive monitoring infrastructure for the DMS project leveraging IAM Least Privilege layers, S3 Private Buckets, Presigned URLs, GuardDuty, Cognito, CloudWatch, X-Ray, and SNS.
* Evaluate and assess the real-world operational performance of the data protection, user authorization perimeters, role-based group separation, and secure asset upload pipelines.
* Initiate complete system teardowns and provisioned resource purges utilizing the automated CDK Destroy command to maximize cost optimization and avoid unexpected billing variances.
* Synthesize the end-to-end Document Management System capstone implementation, documenting critical architecture takeaways and auditing final usage spend indicators across AWS Billing & Cost Explorer profiles.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Learn about IAM Least Privilege paradigms and secure access boundary enforcement within the DMS ecosystem<br>- Explore Amazon S3 data protection models using isolated Private Buckets and ephemeral Presigned URLs<br>- **Practice:**<br>&emsp; + Audit and validate standalone IAM Execution Role profiles mapped independently to each serverless Lambda function<br>&emsp; + Assert narrow **dynamodb:Query** privileges for the **documents** handler and specific **PutItem**/**s3:PutObject** rules for the **upload-intents** scope<br>&emsp; + Verify exclusive **GetItem**/**s3:GetObject** capabilities assigned to the **download-intents** logic and directory administration permissions for the **admin-users** function<br>&emsp; + Conduct configuration compliance checks for global "Block All Public Access" constraints across all 3 S3 buckets and audit token temporal expiration parameters | 06/07/2026   | 06/07/2026      |  |
| 3   | - Explore real-time behavior models inside GuardDuty Malware Protection alongside Cognito Role-Based Access Control frameworks<br>- **Practice:**<br>&emsp; + Inspect runtime health indicators inside the active Malware Protection Plan and review the verified Protected Buckets tree on GuardDuty<br>&emsp; + Trace binary scanning diagnostic evaluations by parsing target S3 object metadata tags within the restricted QuarantineBucket<br>&emsp; + Assert that downstream post-scan logic inside the **process-upload** handler executes exclusively on assets matching the explicit **CLEAN** identifier tag<br>&emsp; + Execute multi-tenant permission hierarchy testing natively on the Frontend application UI against specific JWT Group Claims representing: EMPLOYEE, DEPARTMENT_ADMIN, and SYSTEM_ADMIN groups | 07/07/2026   | 07/07/2026      |  |
| 4   | - Explore deep system auditing techniques using CloudWatch Logs, log querying via CloudWatch Insights, distributed X-Ray tracing, and SNS alerting configurations<br>- **Practice:**<br>&emsp; + Parse and analyze structured JSON execution telemetry collected natively inside dedicated central CloudWatch Log Groups<br>&emsp; + Execute advanced multi-filter diagnostic queries over logging fields leveraging the programmatic CloudWatch Logs Insights parser engine<br>&emsp; + Validate the continuous, automated ledger recording actions triggering append-only database transaction records whenever users interact with assets<br>&emsp; + Evaluate end-to-end trace mapping distributions via AWS X-Ray service views and verify the subscription confirmation status backing the primary SNS Alerting Topic | 08/07/2026   | 08/07/2026      |  |
| 5   | - Launch the automated infrastructure de-provisioning sequence (Cleanup) to purge active platform components out of the AWS account<br>- **Practice:**<br>&emsp; + Change directories into the infrastructure source root **aws/infrastructure** using localized execution terminals<br>&emsp; + Launch the automated stack teardown routine: **npx cdk destroy -c environment=dev**<br>&emsp; + Monitor real-time resource eviction states tracking the parent CloudFormation Stack **DmsStack-dev** on the command-line command shell interface<br>&emsp; + Log into the AWS Management Console to run cross-checks asserting complete eradication of S3 buckets, DynamoDB layouts, Lambda functions, Cognito clusters, API Gateways, EventBridge rules, and active CloudFront distributions | 09/07/2026   | 09/07/2026      |  |
| 6   | - Compile final capstone analysis for the DMS project and conduct a financial post-audit across corporate billing profiles<br>- **Practice:**<br>&emsp; + Access the AWS Billing dashboard and launch Cost Explorer metrics to verify immediate budget spend stabilization following the system cleanup actions<br>&emsp; + Consolidate a comprehensive summary index mapping the deployed AWS services, implemented functional traits, and security layers built across the runtime architecture<br>&emsp; + Document final architectural blueprints detailing the end-to-end secure event-driven Serverless asset ingestion processing stream<br>&emsp; + Record foundational architectural design lessons, compile structural project evaluations, and complete final reporting handoff deliverables | 10/07/2026   | 10/07/2026      |  |

### Week 12 Achievements:

#### 1. Mastering and Executing Least Privilege Principles via Explicit IAM Configurations
* Conducted structural reviews regarding perimeter safety boundaries: verified that mapping decoupled, isolated IAM Execution Roles independently to individual computing scopes—rather than deploying a wildcard master policy (Wildcard Master Role) across the shared platform—radically minimizes vulnerability vectors and contains potential compute breaches.
* **Granular Least Privilege Compliance Mapping Analysis:** * Asserted that the **documents** directory fetch handler is structurally isolated to running solely non-destructive **dynamodb:Query** lookups.
  * Confirmed that the **upload-intents** compute boundary is strictly enclosed within transactional **dynamodb:PutItem** creation parameters and focused **s3:PutObject** payload stream configurations.
  * Verified that the **download-intents** processing node contains execution capabilities strictly bounded to standard **dynamodb:GetItem** steps and secure **s3:GetObject** asset delivery operations.
  * Validated that administrative directory lookup operations are isolated entirely within the single **admin-users** handler possessing scoped Cognito API management paths.
  * Verified that the core backend engine **process-upload** possesses the narrow cross-functional privileges required to shift sandboxed items across staging lines (reading from the Quarantine bucket, writing to the secure Documents bucket, and modifying DynamoDB states).

#### 2. Rigorous Private Storage Perimeter Validation and Presigned URL Isolation Controls
* Completed thorough compliance audits verifying strict asset configuration isolation properties across the multi-bucket storage design layout (**FrontendBucket**, **QuarantineBucket**, **DocumentsBucket**), ensuring that global **Block All Public Access** policies operate flawlessly to block path-traversal attacks or unauthenticated object address guessing attempts originating from public networks.
* Validated the structural correctness of dynamic cryptographic token delivery channels, ensuring that decoupled storage operations (utilizing Presigned PUT URLs for secure asset ingestion and Presigned GET URLs for data egress delivery) match temporal constraints perfectly, dropping all authorization states once timeout intervals expire.

#### 3. Real-Time Anti-Malware Sandboxing Diagnostics via GuardDuty Engine Integration
* Evaluated active threat management indices inside the primary AWS GuardDuty Management Console, ensuring that targeted automated anti-malware parsing schedules (Malware Protection Plan) continuously monitor the defined storage perimeter boundaries (**Protected Buckets**).
* Verified real-time defensive pipeline behaviors: the moment the client interface transfers raw data objects onto the landing zone, integrated anti-malware engines intercept the incoming data stream, check binary states, and append secure operational metadata evaluation markers directly to S3 object attributes (marking uncompromised logs as **CLEAN** and malicious binaries with a **THREAT_FOUND** tag).
* Certified the absolute correctness of post-scan boundary filters: confirmed that the asynchronous backend processing handler **process-upload** successfully intercepts tag modifications, instantly purges high-risk elements to mitigate perimeter threats, and safely moves verified, uncompromised assets into the production core repository.

#### 4. Fine-Grained Tenant Identity Governance utilizing Cognito Group Claims
* Successfully validated runtime context authorization restrictions driven via JSON Web Token (JWT) identity group structures (Group Claims) injected by Amazon Cognito engines, ensuring precise data separation matching employee hierarchies:
  * Deployed the **EMPLOYEE** tier: establishing secure, narrow parameters limiting users strictly to uploading, indexing, and downloading document assets matching their own identity signature.
  * Deployed the **DEPARTMENT_ADMIN** tier: configuring elevated management rights to orchestrate, allocate, and distribute document sharing links across defined departmental perimeters.
  * Deployed the **SYSTEM_ADMIN** tier: provisioning root platform oversight, granting uninhibited rights to execute user directory provisioning, analyze platform telemetry dashboards, and inspect permanent corporate document layers.

#### 5. Advanced System Observability and Query Analytics via CloudWatch Insights & AWS X-Ray
* Mastered operations auditing and runtime log analysis workflows by consuming structured JSON logs generated natively by custom backend compute code and piped to central Amazon CloudWatch Log Groups.
* **Deep Architectural Diagnostics Practice:** Constructed custom query structures inside the CloudWatch Logs Insights engine to filter system traces across matching timestamps (**timestamp**) and transaction descriptors (**message**), asserting the real-time creation of unalterable append-only database logs tracking modifications (asset creation, object lookups, link sharing, and secure data delivery tasks) to guarantee complete compliance with corporate data auditing standards.
* Evaluated unified execution latency profiles across distributed infrastructure components utilizing active service maps generated through AWS X-Ray tracking.

#### 6. Synchronous Alerting Orchestration and Automated Security Signaling
* Validated end-to-end integration mapping logic linking system monitoring thresholds with continuous messaging channels, pairing automated CloudWatch Alarms directly to the primary Amazon SNS notification bus (**DmsAlertTopic**).
* Audited the corporate administrative messaging channels, verifying that subscription endpoints reflect a verified **Confirmed** status state—ready to trigger instantaneous push-notifications to operational engineering teams the moment compute nodes cross hazard lines (such as high **5XX Error Rates**) or breach projected monthly budget frameworks.

#### 7. Automated Infrastructure De-Provisioning and Lifecycle Audits via CDK Destroy Actions
* Managed localized execution terminals to change contexts into the infrastructure engine layer directory **aws/infrastructure**, triggering full stack teardowns by executing the deployment purge command script: **npx cdk destroy -c environment=dev**.
* Observed global resource deletion lifecycles compile across the terminal shell screen, internalizing the critical cloud operational rule that systematic infrastructure danying tasks (Resource Cleanup) are mandatory post-project termination phases to immediately stop all cloud billing accruals and avoid idle computing waste.

#### 8. Cross-Account Asset Eradication Validation on the AWS Web Console
* Conducted deep structural validation audits natively within the AWS Management Web Console, asserting that the primary orchestration template **DmsStack-dev** was completely purged from the AWS CloudFormation platform without generating execution faults.
* Confirmed that all constituent infrastructure parts were cleanly wiped out, confirming the complete deletion of all 3 S3 storage buckets, the NoSQL table array **dms-dev**, all Lambda compute function nodes, REST API Gateway specifications, EventBridge rule configurations, the global CloudFront distribution CDN edge, SNS signaling topics, and the GuardDuty protection runtime layout.

#### 9. Comprehensive Financial Accounting Analysis via AWS Cost Explorer Profiles
* Leveraged cloud financial management systems within the AWS Billing interface paired with advanced Cost Explorer tracking metrics to execute post-cleanup billing validations.
* Analyzed granular data consumption profiles evaluating accrued costs across S3 storage layers, table allocations within DynamoDB, individual Lambda execution counts, data retention tiers inside CloudWatch Logs, and GuardDuty protection plan uptimes—confirming that all operational assets ceased charging processes immediately upon stack destruction and logging residual payment tokens remaining inside the ongoing billing cycle.

#### 10. Summary of project value realization at the end of DMS term
* Successfully completed the multi-tier Document Management System blueprint, achieving an advanced architecture running entirely on modern AWS Serverless design patterns. The final platform perfectly solves core corporate data handling challenges: integrating secure Cognito identity directories, handling public API boundaries via managed API Gateways, enforcing absolute object storage privacy within S3 Private Buckets, executing automated real-time anti-malware scrubbing via GuardDuty, routing asynchronous state indicators using EventBridge buses, modeling lightning-fast NoSQL schema profiles within a DynamoDB Single-Table layout, and centralizing platform observability via CloudWatch/SNS pipelines.
* **Critical Technical Takeaways:**
  * Mastered the implementation engineering required to model, declare, version, and launch cloud-native corporate infrastructure dynamically through source code assets (IaC) utilizing the robust AWS CDK software framework.
  * Developed professional architectural modeling paradigms to separate distributed platform tiers safely into clean independent boundaries (Static UI presentation, API Routing Edges, Modular Compute Logic, Isolated Secure Storage, and Observability layers).
  * Gained high-level proficiency applying NoSQL single-table design principles to streamline lookup performance across deeply varied domain entities, establishing a robust foundation in cloud software engineering to drive complex, enterprise-scale platform deployments in future engineering roles.
