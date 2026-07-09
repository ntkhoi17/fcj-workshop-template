---
title: "Week 11 Worklog"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---



### Week 11 Objectives:

* Configure the initial administrative user within Amazon Cognito and comprehensively test the JWT authentication mechanism.
* Validate the performance and correctness of critical backend endpoints such as **/me**, **/upload-intents**, and **/documents** alongside all document-related APIs.
* Verify the end-to-end document upload workflow spanning the frontend/API, QuarantineBucket, GuardDuty scanning engine, permanent DocumentsBucket, and the DynamoDB database layer.
* Launch the React frontend within a local development environment and validate core user interface components: authentication, asset uploading, sharing controls, identity management, immutable audit logging, and analytics reporting.

### Tasks to implement this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2   | - Provision the initial Admin identity within the Amazon Cognito directory<br>- Explore the structural authorization paths governing the **USER_PASSWORD_AUTH** flow<br>- **Practice:**<br>&emsp; + Create the user identity **admin@yourcompany.com** within the Cognito User Pool using the AWS Management Console<br>&emsp; + Enforce a temporary credential string (Temporary Password) targeting the root administrative user account<br>&emsp; + Map the newly provisioned user directly into the highest-tier **SYSTEM_ADMIN** privilege group<br>&emsp; + Analyze and structure the programmatic user creation syntax driven via the AWS CLI toolchain<br>&emsp; + Execute a test authentication call against Cognito APIs and extract the returned **AccessToken** string | 29/06/2026   | 29/06/2026      |  |
| 3   | - Validate the operational status of the **/me** endpoint and foundational account metadata API layers<br>- **Practice:**<br>&emsp; + Dispatch structured programmatic requests targeting the **/me** REST endpoint, attaching the Bearer Token within request headers<br>&emsp; + Assert the structural validity of returned JSON data schemas encompassing fields: **userId**, **email**, **name**, and **groups**<br>&emsp; + Verify that the Amazon API Gateway correctly intercepts, intercepts, and decrypts the cryptographic JWT signature<br>&emsp; + Trace runtime execution outputs inside the CloudWatch Log Groups backing the specialized **me** serverless function<br>&emsp; + Analyze and log platform failure state responses when executing requests with malformed or expired cryptographic tokens | 30/06/2026   | 30/06/2026      |  |
| 4   | - Execute integration verification scenarios tracing secure document upload loops driven via ephemeral Presigned URLs<br>- **Practice:**<br>&emsp; + Invoke the **/upload-intents** endpoint to extract a transient **uploadIntentId** index paired with a secure Presigned PUT URL<br>&emsp; + Perform a direct binary transfer streaming a test asset file **report.pdf** straight into the isolated S3 QuarantineBucket via the generated URL<br>&emsp; + Observe background asynchronous pipelines as GuardDuty Malware Protection initializes automated scanning against the asset stream<br>&emsp; + Inspect metadata tag structures on S3, asserting that validated clean assets systematically shift into the production DocumentsBucket<br>&emsp; + Audit backing DynamoDB non-relational tables to verify item entry schema creation and trace successful promotions to a **READY** state | 01/07/2026   | 01/07/2026      |  |
| 5   | - Test endpoint arrays governing document index retrieval capabilities and validate core multi-tenant interaction actions<br>- **Practice:**<br>&emsp; + Dispatch programmatic requests targeting the **/documents** route using the extracted **AccessToken** to pull file registry lists<br>&emsp; + Match and cross-verify returned object structures—specifically **documentId**, **filename**, and **versionNumber** metadata—against DynamoDB entries<br>&emsp; + Validate the processing accuracy of the document specification endpoint (Document Details) and continuous event extraction route (Audit Events)<br>&emsp; + Invoke the specialized download intent handler to generate a temporary Presigned GET URL to verify data retrieval boundary safety lines | 02/07/2026   | 02/07/2026      |  |
| 6   | - Boot up the React presentation frontend application inside a local development workspace and audit interactive interface modules<br>- **Practice:**<br>&emsp; + Run dependency mapping operations using npm to install interface components inside the localized presentation root directory<br>&emsp; + Launch the localized Vite local development web server using the standard environment execution scripts: **npm run dev**<br>&emsp; + Populate configuration values by binding the **UserPoolId**, **UserPoolClientId**, and base **ApiUrl** strings extracted from the CDK Outputs block<br>&emsp; + Execute end-to-end integration scenario testing: auditing Admin login routines, asset upload/download loops, sharing control sets, department views, audit trails parsing, and analytics visual dashboard blocks | 03/07/2026   | 03/07/2026      |  |

### Week 11 Achievements:

#### 1. Global Root Administrator Identity Staging
* Developed deep security architectural alignment: validated that enforcing absolute restrictions on unauthenticated registration pathways (Self-signup exclusion) is non-negotiable for enterprise document networks to neutralize outside compromise vectors.
* Successfully provisioned the primary root administrative profile **admin@yourcompany.com** inside the managed Cognito User Pool directory, applied ephemeral staging passwords, and bound the identity profile directly into the highest global authorization tier (**SYSTEM_ADMIN**) to serve as an access vehicle for end-to-end integration scenarios.

#### 2. Token-Based Authentication Flow Modeling with Amazon Cognito
* Mastered runtime mechanics governing the programmatic **USER_PASSWORD_AUTH** flow to negotiate secure access handshakes directly against cloud identity providers.
* Extracted the secure cryptographic **AccessToken** payload returned post-verification, analyzing JSON Web Token (JWT) layout attributes to utilize the string as a standardized authorization Bearer Token embedded inside client API traffic headers to traverse edge Cognito Authorizers shielding API Gateways.

#### 3. Endpoint Integrity Validation Mapping the **/me** Identity Interface
* Dispatched authorized request traces to the endpoint **/me**, verifying that the edge API Gateway successfully blocks anonymous traffic, decrypts authentic token layers, and propagates valid upstream execution user contexts straight down to processing tiers.
* Assessed the structural topology of returned JSON payloads, ensuring clean schema parsing across essential tracking variables, including: **userId**, **email**, and **name**, while ensuring accurate runtime role validation against the **SYSTEM_ADMIN** privilege container.

#### 4. Advanced Telemetry Exploitation and API Diagnostics via CloudWatch Logs
* Pinpointed and isolated dedicated Amazon CloudWatch Log Groups tied explicitly to distinct compute function execution scopes.
* Analyzed realtime runtime diagnostic logs emitted during client frontend data iterations, mastering remediation patterns to troubleshoot standard edge anomalies such as missing authorization context blocks (401 Unauthorized errors), corrupted payloads, or temporal token expiration events (Expired Token exceptions).

#### 5. Verification of the Decoupled Ingestion State via Upload Intents APIs
* Dispatched structured **POST** requests targeting the **/upload-intents** endpoint, passing requisite metadata properties describing inbound files (including **filename**, **contentType**, and data payload **size**).
* Captured execution responses dispatched from the backend Lambda tier, parsing out the transient workflow tracker identifier **uploadIntentId** paired with a highly performant, brief, and temporally constrained storage path (Presigned PUT URL).

#### 6. High-Velocity Secure Asset Ingestion Ingestion Optimizations
* Orchestrated direct binary data streams passing a test document **report.pdf** out of local client storage targets straight up to isolated S3 infrastructure layers via the Presigned PUT URL interface.
* Confirmed that massive multi-megabyte data streams route independently of compute networks, avoiding direct path transversals across API Gateways or processing functions—demonstrating the architectural dominance of the pattern in optimizing core networking bandwidth while bypassing standard REST API entry constraints (e.g., API Gateway's 10MB limit).

#### 7. Synchronous Monitoring of Real-Time Malware Isolation Boundaries
* Confirmed that inbound asset streams entering the untrusted staging buffer environment (**QuarantineBucket**) immediately launch automated deep binary scans via integrated GuardDuty Malware Protection rules.
* Audited object metadata properties on the console to check tagging states, asserting that the automated evaluation sub-engines correctly write security tags: stamping uncompromised records with a clear **CLEAN** validation marker, while isolating compromised entities under an explicit **THREAT_FOUND** risk tag during simulation runs with mock malware payloads.

#### 8. Verification of Asynchronous Post-Scan Processing Automations
* Verified that asynchronous pipeline messaging models perform perfectly: tag updates written by the anti-malware engine instantly prompt the central Amazon EventBridge bus to route execution records down to the core **Upload Processor Function**.
* Audited processor function execution logs, confirming that the handler reads security tags, transfers safe data objects directly into the permanent corporate archive warehouse (**DocumentsBucket**), creates core metadata objects, sets matching iteration trackers (**versionNumber**), and transitions entity records to a **READY** state inside single-table DynamoDB layouts.

#### 9. Authorization Audit on Document Directory Access and Metadata APIs
* Dispatched programmatic queries targeting the **/documents** endpoint using the authenticated **AccessToken** block to evaluate the file listing capability across role partitions.
* Asserted that returned index listings correspond with the real state of active data stores, correctly rendering data properties like **documentId**, **filename**, **versionNumber**, and system epoch **timestamp** values matching underlying DynamoDB records.
* Validated operational reliability across complementary high-tier metadata routes, successfully executing data reads across the granular document parameter block (Document Details API) and continuous file transaction histories (Audit Events API).

#### 10. Data Protection Lifecycle Auditing for Data Egress (Secure Download Flow)
* Invoked backend download requests to prompt the **download-intents** compute function to cross-check authorization levels before computing an ephemeral, time-bounded data delivery link (Presigned GET URL).
* Successfully processed local client file downloads out of the permanent **DocumentsBucket** warehouse via the newly generated URL string, proving the validity of a perimeter defense strategy that isolates primary cloud file storage boundaries completely from external internet exposure or address enumeration attacks.

#### 11. Staging and Interconnecting the Presentation Frontend Environment
* Executed package initialization routines within the frontend presentation layer directory, resolving and loading the full suite of client presentation modules and dependencies via the npm package manager.
* Launched the local Vite-driven development server environment, spinning up the web interface at its default local host interface target (**http://localhost:5173**).
* Completed frontend-to-cloud interconnection mapping tasks, wiring the interface code directly to the live cloud backend by populating the structural parameters block extracted from CDK outputs: **UserPoolId**, **UserPoolClientId**, and the root backend endpoint **ApiUrl**.

#### 12. Full End-to-End System Integration Sign-Off Validation
* Authenticated successfully into the user interface using the root administrative profile, executing rigorous end-to-end integration checks across core business workflows without triggering visual anomalies or exceptions:
  * Navigated document tree indices, executing multi-tier secure asset upload loops and verified secure data egress downloads.
  * Configured secure data sharing links (Sharing Links) and modified item-level access control levels.
  * Operated identity provisioning blocks (User Management modules) under global System Admin rights and traced organizational boundaries (Department Management tracking) under Department Admin scopes.
  * Verified continuous tamper-proof ledger activities using the immutable append-only transaction logger, while monitoring structural compute performance metrics natively on the system analytics dashboard.
