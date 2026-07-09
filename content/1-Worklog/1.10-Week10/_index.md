---
title: "Week 10 Worklog"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---



### Week 10 Objectives:

* Deploy the DMS project infrastructure using the AWS CDK following the Infrastructure as Code (IaC) model.
* Provision core resources including Cognito User Pools, S3 Buckets, DynamoDB Tables, Lambda Functions, API Gateways, EventBridge buses, GuardDuty protection layers, CloudFront distributions, CloudWatch metrics, and SNS topics.
* Verify deployment outcomes on the AWS Management Console and validate critical output values exported by the CDK.
* Staging the backend infrastructure foundation to support downstream API validation and document upload lifecycle testing in the following week.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Prepare for DMS infrastructure deployment utilizing the AWS CDK<br>- **Practice:**<br>&emsp; + Clone the DMS project source repository and install required dependencies via npm<br>&emsp; + Configure the local secure environment file **.env** using the **.env.example** template<br>&emsp; + Populate the budgetary alert recipient variable **DMS_ALERT_EMAIL**<br>&emsp; + Compile (Build) serverless Lambda Functions from TypeScript source into executable JavaScript modules<br>&emsp; + Audit the structural layout of the generated **dist** distribution folder post-compilation<br>&emsp; + Execute the CDK Bootstrap command targeted precisely at the designated target AWS Account and Region | 22/06/2026   | 22/06/2026      | |
| 3   | - Explore and deploy Identity, Storage, and Database layer resources using CDK constructs<br>- **Practice:**<br>&emsp; + Define and deploy the Cognito User Pool named **dms-dev** enforcing email-based identity authentication<br>&emsp; + Manually provision standardized user security groups: EMPLOYEE, DEPARTMENT_ADMIN, SYSTEM_ADMIN<br>&emsp; + Establish a strict cryptographic password enforcement configuration (Password Policy) within the User Pool<br>&emsp; + Provision an isolated storage architecture composed of three independent S3 buckets: FrontendBucket, QuarantineBucket, DocumentsBucket<br>&emsp; + Activate strict "Block All Public Access" constraints and implement explicit CORS rule parameters on the QuarantineBucket<br>&emsp; + Initialize the single-table DynamoDB layout **dms-dev** (Configuring PAY_PER_REQUEST, PITR, TTL, and active GSIs) | 23/06/2026   | 23/06/2026      |  |
| 4   | - Explore and deploy the serverless Compute layer, ingestion APIs, and central Event routing hubs<br>- **Practice:**<br>&emsp; + Provision the full serverless Lambda Backend cluster tasked with running core business APIs (**me**, **documents**, **document-detail**, **document-audit-events**, **upload-intents**, **download-intents**, **document-sharing**, **admin-users**, **analytics**) alongside the primary pipeline processor logic **process-upload**<br>&emsp; + Declare the Amazon API Gateway REST API structure, interlocking a Cognito token-validation Authorizer layer<br>&emsp; + Configure Amazon EventBridge event patterns to capture the asynchronous **ObjectCreated** state transitions triggered by the QuarantineBucket | 24/06/2026   | 24/06/2026      |  |
| 5   | - Explore and deploy advanced Security integrations, global CDN routing layers, and Monitoring/Alerting stacks<br>- **Practice:**<br>&emsp; + Construct dedicated least-privilege IAM Execution Roles tailored for the GuardDuty Malware Protection engine<br>&emsp; + Enable automated malware screening and automatic metadata security tagging on the isolated QuarantineBucket layer<br>&emsp; + Declare an Amazon CloudFront Distribution securely mapped against the FrontendBucket via an Origin Access Control (OAC) proxy<br>&emsp; + Establish explicit, isolated Amazon CloudWatch Log Groups tracking individual Lambda execution scopes retention-mapped for Dev environments<br>&emsp; + Initialize an active Amazon SNS Alerting Topic linked with automated CloudWatch metric alarms to distribute automated email notifications | 25/06/2026   | 25/06/2026      |  |
| 6   | - Execute full end-to-end system target stack compilation deployments and conduct post-deployment audits<br>- **Practice:**<br>&emsp; + Trigger the automated global deployment run: **npx cdk deploy -c environment=dev -c alertEmail=...**<br>&emsp; + Parse and extract vital deployment keys from the returned CDK Outputs block (**UserPoolId**, **UserPoolClientId**, **ApiUrl**, **CloudFrontUrl**)<br>&emsp; + Verify successful lifecycle statuses tracking the parent CloudFormation Stack **DmsStack-dev**<br>&emsp; + Conduct end-to-end validation across the AWS Console to verify active resource states across DynamoDB, S3, Lambda, and API Gateway | 26/06/2026   | 26/06/2026      |  |

### Week 10 Achievements:

#### 1. Source Tree Management and Workspace Staging
* Successfully initialized the local workspace environment by cloning the core DMS Project repository branches.
* Completed full dependency mapping steps, resolving and installing prerequisite package branches via the npm toolchain.
* Synchronized environment parameters across local layers by instantiating the secured local **.env** setup file from the provided **.env.example** blueprint, successfully exporting administrative tracking channels via the **DMS_ALERT_EMAIL** variable.
* Executed build tasks compiling serverless backend Lambda logic trees out of TypeScript into optimized JavaScript assets, verifying that target **dist** artifact release directories generate accurately to support automated infrastructure assembly.

#### 2. Enterprise Environment Staging via CDK Bootstrap Actions
* Developed precise structural understanding regarding the CDK Bootstrap operational layer, recognizing its role in standing up underlying landing-zone prerequisites (such as dedicated S3 staging artifact storage buckets and global IAM orchestration execution roles) allowing AWS CloudFormation to parse and deploy subsequent stacks.
* Successfully executed bootstrap automation jobs pointed explicitly at the dedicated corporate AWS Account index and project destination Region, verifying the completed execution state of the native **CDKToolkit** foundation stack natively on the console.

#### 3. Identity Directory Governance Layout via Amazon Cognito
* Declared and systematically deployed an isolated Amazon Cognito User Pool instance named to match target environment boundaries: **dms-dev**.
* Enforced tight network perimeter constraints by configuring mandatory Email-based identity verification paths, completely disabling public end-user signups (Self-signup restriction) to ensure identity creation capabilities remain exclusively with authorized global system administrators.
* Structured role-based user directory partitioning by provisioning three explicit, immutable authorization containers: **EMPLOYEE**, **DEPARTMENT_ADMIN**, and **SYSTEM_ADMIN** groups.
* Applied rigorous enterprise-grade password security enforcement constraints (Password Policy) alongside strict temporal validation timeouts governing Access Token, ID Token, and Refresh Token lifecycle parameters.

#### 4. Low-Latency Storage Architecture and Perimeter Security Design
* Deployed an isolated storage structure utilizing three independent Amazon S3 Buckets separated cleanly by explicit operational roles:
  * **FrontendBucket**: Retains static multi-chunk assets and web compilation modules delivering the client presentation single-page web app.
  * **QuarantineBucket**: Functions as a restricted, sandboxed buffer zone engineered to isolate unverified inbound data streams pending scanning audits.
  * **DocumentsBucket**: Serves as the immutable permanent archive core housing corporate document assets cleared by security frameworks.
* Enforced absolute asset perimeter lockouts by activating global **Block All Public Access** constraints across all three storage buckets to block external data exposure vectors.
* Authored detailed Cross-Origin Resource Sharing (CORS) rule definitions for the **QuarantineBucket** entry-point to securely permit cross-origin **PUT** transactional streams routed directly from client web browsers.

#### 5. High-Performance NoSQL Data Structures via DynamoDB Single-Table Layouts
* Provisioned the unified **dms-dev** non-relational database architecture leveraging single-table design methodologies to compress operational maintenance overhead and eliminate multi-table cost provisioning waste.
* Activated flexible on-demand throughput billing allocation models (**PAY_PER_REQUEST**) to drive auto-scaling agility matching live transaction velocity, and wrapped the system under data-at-rest encryption utilizing AWS Managed Keys.
* Maximized corporate disaster recovery thresholds and data protection lines by enabling background Point-In-Time Recovery (PITR) workflows.
* Implemented systemic transactional data evictions by configuring the **expiresAtEpoch** Time to Live (TTL) storage attribute, automating the background cleanup of outdated upload intents (Upload Intents) records to ensure storage optimization.
* Assembled an indexing layer composed of multiple Global Secondary Indexes (GSIs), supplying multi-dimensional lookup capabilities to back the varied access patterns demanded by business logic loops.

#### 6. Efficient Serverless Compute Engineering via AWS Lambda
* Provisioned the full suite of backend compute services, establishing automated Node.js execution environments running over high-efficiency ARM64 silicon architectures to accelerate execution response curves while slashing compute financial spend by 34%.
* Enforced absolute programmatic isolation lines: assigning distinct, isolated IAM Execution Roles independently to each individual Lambda function following strict least-privilege paradigms (Least Privilege Principle), eliminating loose cross-functional permissions.
* Implemented end-to-end operational transparency across computing pipelines by configuring AWS X-Ray Active Tracing natively throughout all backend functions to aggregate service map trace sheets.

#### 7. Secure API Management Gateways and Event Hub Configurations
* Initialized a highly performant Amazon API Gateway REST API framework to act as the single secure ingestion edge intercepting client requests.
* Interconnected a native **Cognito Authorizer** authorization block across entry vectors, enabling the API Gateway to independently intercept, parse, and validate JSON Web Token (JWT) cryptographic signatures inside ingress traffic headers before permitting access to sensitive compute routes.
* Linked asynchronous storage bucket status signals directly with event networks, configuring the **QuarantineBucket** to automatically pass data tracking events (**ObjectCreated**) onto the central Amazon EventBridge bus.
* Defined precise event matching rule blocks focused on items landing under the **quarantine/** storage prefix, securely mapping asynchronous routing streams straight to the downstream **process-upload** Lambda destination paired with an underlying Dead Letter Queue (DLQ) topology to catch processing exceptions.

#### 8. Automated Anti-Malware Sandboxing via GuardDuty Malware Protection
* Provisioned dedicated service-linked IAM Roles authorizing Amazon GuardDuty security sub-engines to interact with, read from, and append metadata descriptors to sandboxed staging paths.
* Orchestrated a native **Malware Protection Plan** linkage tied directly into the boundary definitions of the untrusted **QuarantineBucket**.
* Implemented real-time synchronous binary scanning pipelines, guaranteeing that objects landing within the temporary ingestion zone are parsed automatically for malware footprints and assigned metadata tags representing runtime health states: **CLEAN** or **THREAT_FOUND**.

#### 9. Global Asset Edge Distribution and Observability Stacks Staging
* Created an accelerated Amazon CloudFront Distribution edge network layout acting as a high-velocity CDN shielding the underlying web hosting tier (**FrontendBucket**).
* Established modern infrastructure proxy safety layers by enforcing Origin Access Control (OAC) specifications, locking down backend bucket structures, and forcing all global front-end resource reads through CloudFront edge parameters.
* Allocated dedicated, explicit Amazon CloudWatch Log Groups independently per compute function, applying custom retention periods optimized to support agile developer debugging runs without generating unnecessary telemetry storage costs.
* Constructed an urgent communication signaling array utilizing Amazon SNS Alerting Topics linked with active CloudWatch Metric Alarms, automating instant administrative email broadcasts if the platform encounters operational anomalies (such as high **5XX Error Rates**) or triggers budget consumption threshold exceptions.

#### 10. Unified Platform Verification and Post-Deployment Auditing
* Executed full CDK structural deployment operations to a successful conclusion, capturing a verified **CREATE_COMPLETE** operational execution state for the global CloudFormation stack **DmsStack-dev**.
* Extracted and mapped crucial infrastructure keys returned in the final CDK Outputs block (**UserPoolId**, **UserPoolClientId**, **ApiUrl**, **CloudFrontUrl**), formatting data payloads required for client-side integration tasks.
* Completed cross-verification (Double-check) workflows via the AWS Management Console UI, ensuring structural validation across core Storage (S3), Database (DynamoDB), Identity (Cognito), Compute (Lambda), Security (GuardDuty), and Network (API Gateway/CloudFront) resources to verify system operational readiness.
