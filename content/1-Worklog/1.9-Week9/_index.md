---
title: "Week 9 Worklog"
date: 15-06-2026
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---



### Week 9 Objectives:

* Explore the overview of the Document Management System capstone project built on the AWS Serverless platform.
* Analyze system architecture, document upload workflows, user authentication, malware scanning, and metadata storage.
* Identify core AWS services utilized in the system including Cognito, API Gateway, Lambda, S3, DynamoDB, EventBridge, GuardDuty, CloudFront, CloudWatch, and SNS.
* Prepare the development environment, deployment tools, and source code structure to support system building in the following weeks.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Learn about the overview of the Document Management System project on AWS Serverless<br>- Study internal document management challenges within enterprises<br>- **Practice:**<br>&emsp; + Define DMS system goals<br>&emsp; + Identify internal user groups<br>&emsp; + Analyze core features such as upload, version management, sharing, audit logs, and analytics<br>&emsp; + Review the structure and content of the capstone project workshop | 15/06/2026   | 15/06/2026      |  |
| 3   | - Learn about the overall architecture of the DMS system<br>- Understand the role of AWS Serverless services within the system<br>- **Practice:**<br>&emsp; + Analyze the authentication workflow using Amazon Cognito<br>&emsp; + Analyze API invocation paths via Amazon API Gateway<br>&emsp; + Analyze the role of AWS Lambda in processing business logic<br>&emsp; + Analyze the role of Amazon S3 in hosting the frontend, quarantine files, and official documents<br>&emsp; + Analyze the role of Amazon DynamoDB in retaining metadata, versions, shares, and audit logs | 16/06/2026   | 16/06/2026      |  |
| 4   | - Learn about secure document upload workflows using Presigned URLs<br>- Understand file quarantine and screening mechanisms prior to official storage<br>- **Practice:**<br>&emsp; + Analyze why files are not uploaded directly through API Gateway<br>&emsp; + Analyze the generation workflow of Presigned PUT URLs from the Intent Lambda<br>&emsp; + Analyze the frontend file upload process into the QuarantineBucket<br>&emsp; + Analyze the GuardDuty Malware Protection scanning mechanism<br>&emsp; + Analyze EventBridge triggering the Upload Processor Function<br>&emsp; + Analyze the process of moving clean files to the DocumentsBucket | 17/06/2026   | 17/06/2026      |  |
| 5   | - Learn about critical design decisions in the DMS system<br>- Understand authorization models and data layer designs<br>- **Practice:**<br>&emsp; + Analyze the rationale behind using Presigned URLs<br>&emsp; + Analyze the design decision to upload through a QuarantineBucket before moving to the DocumentsBucket<br>&emsp; + Analyze DynamoDB single-table design principles<br>&emsp; + Analyze primary entities including Document, Version, Share, AuditLog, UploadIntent, and UserProfile<br>&emsp; + Analyze append-only audit log mechanisms<br>&emsp; + Analyze least-privilege IAM principles tailored for each Lambda Function | 18/06/2026   | 18/06/2026      |  |
| 6   | - Prepare the deployment environment for the DMS project<br>- Explore repository structures and required developer tools<br>- **Practice:**<br>&emsp; + Verify AWS account permissions and required access levels<br>&emsp; + Verify AWS CLI configurations and target deployment profiles<br>&emsp; + Verify Node.js, npm, AWS CDK CLI, and Git installations<br>&emsp; + Study AWS CDK CLI installation and CDK Bootstrap execution commands<br>&emsp; + Explore directory structures: **aws/functions**, **aws/infrastructure**, **frontend**, **contracts**, and **docs**<br>&emsp; + Configure the **DMS_ALERT_EMAIL** environment variable for alert routing | 19/06/2026   | 19/06/2026      |  |

### Week 9 Achievements:

#### 1. Document Management System Capstone Overview
* Understood that the DMS is an internal document management system built on top of a modern AWS Serverless infrastructure.
* Grasped system objectives centered on supporting document uploads, storage boundaries, version control (versioning), secure sharing, and end-to-end tracking of execution histories.
* Understood that the system is purpose-built to serve internal corporate user groups rather than public external audiences.
* Identified this capstone as a comprehensive, multi-tier project designed to consolidate and evaluate deep, multi-disciplinary AWS knowledge acquired across previous weeks.

#### 2. Core Functional Requirements Definition
* Securely uploading document assets.
* Managing multiple document iterations via object versioning.
* Dynamically listing document trees filtered by user roles or departmental boundaries.
* Inspecting structural details and executing secure document downloads via short-lived Presigned URLs.
* Managing rapid data share authorizations or immediate access revocation controls.
* Logging centralized, immutable audit trails using an append-only transaction design for critical operational tasks.
* Visualizing tracking summaries covering aggregate storage footprints and operational velocity via analytics systems.

#### 3. AWS Serverless Architecture Design for DMS
* Understood that Amazon Cognito governs the entire identity verification tier and manages group-based authorization levels (Group Memberships).
* Understood that Amazon API Gateway acts as the single ingestion endpoint and traffic routing proxy for the core REST APIs.
* Understood that AWS Lambda serves as the decoupled serverless compute backend executing business runtime processes.
* Understood that Amazon S3 acts as a versatile storage core: hosting static frontend presentation layers, isolating raw objects in a quarantine zone (Quarantine), and retaining approved assets in a production layer (Documents).
* Understood that Amazon DynamoDB houses non-relational data structures: capturing document metadata, version history arrays, share boundaries, immutable audit records, and brief upload intentions.
* Understood that Amazon EventBridge functions as a central event bus routing state updates resulting from upload lifecycles.
* Understood that Amazon GuardDuty performs automated continuous file scanning (Malware Protection) the moment objects land in the entry zone.
* Understood that Amazon CloudFront deploys a global edge CDN distribution layout to serve the static React presentation application with low-latency boundaries.
* Understood that Amazon CloudWatch and Amazon SNS support runtime logging collections, metric aggregation tracking, and downstream urgent notification broadcasts.

#### 4. Authentication and API Execution Ingestion Mappings
* End-users query system layers securely over accelerated Amazon CloudFront global network connections.
* CloudFront retrieves static React web presentation files out of isolated S3 FrontendBuckets and serves them to client browsers.
* End-users log in via localized Amazon Cognito identity directories, receiving secure JSON Web Tokens (JWT) upon successful verification.
* The frontend client attaches JWT access tokens to authorization request headers when calling backend Amazon API Gateway endpoints.
* API Gateway validates incoming JWT signature configurations natively utilizing a built-in Cognito Authorizer block.
* Fully authorized requests pass seamlessly into downstream serverless Lambda functions tasked with running explicit business computations.

#### 5. Document Ingestion Pipelines via Secure Presigned URLs
* The client frontend initiates an intent request over public APIs to register an incoming asset upload (Upload Intent).
* A specialized Intent Lambda function intercepts the request, calling storage APIs to generate an ephemeral, short-lived Presigned PUT URL.
* The raw target asset stream transfers directly from the client browser straight to the secure S3 QuarantineBucket via the newly minted Presigned URL.
* Moving massive data payloads completely bypasses the API Gateway and Lambda compute layers, neutralizing traditional API size constraints (10MB payload limit) and driving down backend execution overhead.
* The QuarantineBucket functions as an isolated buffer zone designed to securely hold untrusted files until verification systems complete their screening cycles.

#### 6. Automated Malware Screening Workflows
* The appearance of fresh raw data objects inside the QuarantineBucket triggers automated scanning routines via GuardDuty Malware Protection.
* GuardDuty evaluates binary signatures, appending visual validation evaluation metrics as object tags straight to S3 asset metadata.
* Uncompromised files passing validation cleanly receive an explicit **CLEAN** validation flag.
* Compromised structures flag explicit security alarms, marking objects with a **THREAT_FOUND** identifier.
* The central EventBridge bus catches metadata tag modification event states, routing operational execution records down to an Upload Processor Function.
* The Upload Processor Function parses security tag parameters to decide appropriate downstream lifecycle actions.

#### 7. Operational Responsibilities of the Upload Processor Function
* Parses security evaluation tags associated with temporary storage objects inside the QuarantineBucket environment.
* Safely transfers uncompromised items (**CLEAN** files) into the central permanent corporate DocumentsBucket warehouse.
* Updates asset validation records and operational states directly within active DynamoDB non-relational tables.
* Records permanent document metadata schemas and maps distinct version identifier arrays tracking newly introduced document entities.
* Appends complete multi-tier execution log traces directly to centralized Amazon CloudWatch Logs systems.
* Guarantees that infected, unverified, or high-risk objects are permanently blocked from penetrating official enterprise document repositories.

#### 8. NoSQL Schema Optimization via DynamoDB Single-Table Design
* Mastered single-table design principles: consolidating distinct multi-tier business entities into a single, shared DynamoDB table to minimize provisioning costs and simplify administrative database overhead.
* Structured indexing boundaries to identify core structural entities, including: Document, Version, Share, AuditLog, UploadIntent, and UserProfile records.
* Leveraged Global Secondary Indexes (GSI) to execute high-performance multi-dimensional queries across varied index lookup properties.
* Employed native Time to Live (TTL) mechanisms to automate the background eviction and deletion of expired UploadIntent traces, keeping database storage lean.

#### 9. Group-Based User Authorization Paradigms
* Established the **EMPLOYEE** user class: representing standard personnel with foundational, baseline system interaction capabilities.
* Established the **DEPARTMENT_ADMIN** user class: representing management teams with explicit document coordination oversight within designated departmental perimeters.
* Established the **SYSTEM_ADMIN** user class: representing global administrators possessing uninhibited structural oversight and system configuration control.
* Group claim structures (Group Claims) map directly into JSON Web Token (JWT) payloads upon Cognito authorization checks.
* Downstream Lambda compute nodes parse identity token parameters at runtime to enforce access rules before approving business executions.

#### 10. Architectural Security Constraints & Governance Blueprints
* Mandated short-lived Presigned URLs for all upload and download pathways to optimize enterprise networking bandwidth and prevent data payload bottlenecks at the compute layer.
* Enforced strict sandboxing isolation rules: isolating all raw file transfers inside a temporary QuarantineBucket for malware analysis prior to permanent asset promotion.
* Safeguarded downloadable data channels by generating dynamic Presigned GET URLs restricted by tight temporal expiration limits.
* Engineered an immutable ledger model for audit histories following append-only designs, making past transactional records completely tamper-proof.
* Operationalized strict least-privilege paradigms (Least Privilege Principle) by mapping custom, narrow IAM Roles independently to each standalone Lambda Function.

#### 11. Core Workspace Staging & Target Infrastructure Provisioning
* Reviewed AWS account resource allocations, mapping prerequisite IAM access permissions required to provision underlying resources: including IAM Roles, Lambda functions, S3 storage buckets, DynamoDB layouts, Cognito directories, CloudFront distributions, EventBridge buses, GuardDuty protection layers, SNS topics, and CloudWatch metrics.
* Validated local AWS CLI execution blocks, confirming alignment with target corporate deployment profiles.
* Standardized localized developer machines: enforcing Node.js stability at version LTS **20.x** or above paired with npm package management at version **10.x** or higher.
* Completed global tool configuration steps: installing the AWS CDK CLI framework (v2.x) alongside Git version management engines to clone and version source trees.

#### 12. Repository Architecture & Directory Mapping Conventions
* Directory **aws/functions**: Houses decoupled business logic scripts and TypeScript runtime files driving serverless Lambda execution sets.
* Directory **aws/infrastructure**: Retains Infrastructure as Code (IaC) architectures declaring explicit AWS CDK Stack baseline deployments.
* Directory **frontend**: Composes the single-page client presentation layout (SPA) engineered on React and bundled via the fast Vite compilation toolchain.
* Directory **contracts**: Contains standardized OpenAPI API specifications and layout schema contracts.
* Directory **docs**: Aggregates structural technical records, data entity diagrams, and Architecture Decision Records (ADR).
* Standardized execution rules: Mandated the execution of TypeScript build tasks to ensure compiled script outputs exist inside target **dist** release folders prior to launching structural CDK deployment actions.
