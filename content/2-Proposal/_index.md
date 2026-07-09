---
title: "Proposal"
date: 2026-07-09
weight: 2
chapter: false
pre: " <b> 2. </b> "
---


### 1. Project Summary
The Document Management System (DMS) project is built to create a secure, highly scalable, and cost-effective internal document management system on top of the AWS Serverless platform.
The system allows users to log in, upload documents, manage versions, share documents based on granular permissions, and track continuous operational histories. DMS utilizes core AWS services including Amazon Cognito, API Gateway, Lambda, S3, DynamoDB, EventBridge, GuardDuty, CloudFront, CloudWatch, and SNS.

### 2. Problem Statement
Traditional methods of storing and sharing internal documents often face severe constraints such as difficulties in version control, lack of fine-grained access control, hardships in auditing operational histories, and potential risks of corporate data exposure.
The proposed solution is to build a document management system leveraging a 100% Serverless architecture, where raw file streams transfer directly to Amazon S3 via secure Presigned URLs, undergo automated malware screening prior to permanent storage, and have all metadata managed within optimized DynamoDB single-table layouts.

### 3. Solution Architecture
The system operates along the primary workflow:
* End-users access the system securely over accelerated **Amazon CloudFront** edge connections.
* The static Frontend application is hosted out of an isolated **Amazon S3 FrontendBucket**.
* Users authenticate via **Amazon Cognito** identity directories and receive secure **JWT tokens**.
* The Frontend client dispatches API requests through **Amazon API Gateway**.
* **API Gateway** validates the **JWT** signatures natively using a built-in **Cognito Authorizer**.
* **Core API Lambdas** process primary business logic such as account profiles, document indexes, and file specifications.
* **Intent Lambdas** calculate ephemeral Presigned URLs to handle data ingestion and data egress (upload/download paths).
* The Frontend streams files directly into the secure **Amazon S3 QuarantineBucket** via the generated upload link.
* **Amazon GuardDuty** performs automated binary screening (Malware Protection) on the ingested asset.
* The central **Amazon EventBridge** bus intercepts state transitions and triggers the **Upload Processor Function**.
* The **Upload Processor** parses security tag indicators, updates item operational states inside **DynamoDB**, and safely transfers clean assets into the permanent **DocumentsBucket**.
* **CloudWatch** aggregates execution logging fields and triggers continuous monitoring alerts via **SNS** if the platform encounters exceptions or anomalies.

### 4. Technical Implementation
* **Frontend:** React SPA, distributed globally via Amazon CloudFront edge networks.
* **Backend:** AWS Lambda compute services utilizing Node.js 22 runtime environments to handle business computations.
* **API:** Amazon API Gateway REST API interlocked with native Cognito Authorizers.
* **Storage:** Amazon S3 multi-bucket layout encompassing FrontendBucket, QuarantineBucket, and DocumentsBucket tiers.
* **Database:** Amazon DynamoDB non-relational tables managing document metadata, version history arrays, sharing link metrics, and immutable audit trails.
* **Security:** Cognito group claims for fine-grained user authorization, absolute S3 Private Bucket isolations, dynamic short-lived Presigned URLs, strict IAM Least Privilege execution boundaries, and GuardDuty Malware Protection sandboxing.
* **Observability:** Centralized CloudWatch Logs auditing, continuous X-Ray tracing diagnostics, and automated SNS Alerts signaling.
* **Infrastructure Provisioning:** AWS CDK framework following modern Infrastructure as Code (IaC) deployment models.

### 5. Deployment Roadmap
* **Week 9:** Prerequisite requirements analysis, comprehensive system architectural mapping, and target workspace environment staging.
* **Week 10:** Multi-tier core DMS project infrastructure provisioning utilizing automated AWS CDK pipelines.
* **Week 11:** Backend parameter configurations, root global Admin identity directory creation, integration API verification, and end-to-end document ingestion upload loops validation.
* **Week 12:** Perimeter security configuration controls checks, deep system observability audits, systematic resource de-provisioning cleanup runs, and comprehensive project retrospective sign-off.

### 6. Budget Estimation
Using a serverless architecture, the system operates on a pay-as-you-use model, with costs only incurred based on actual usage. In the test environment, costs are low thanks to AWS's Free Tier.
* **AWS Lambda:** ~0.00 USD (within the free limit for 1 million requests/month).
* **Amazon S3:** ~0.15 USD for external storage and bandwidth.
* **DynamoDB:** ~0.00 USD (25GB of free storage).
* **API Gateway & Cognito:** Free for small-scale internal user storage.
* **Total estimated budget:** Under $1 USD/month for the test environment and approximately under $10 USD/month for a moderately sized real-world environment.

### 7. Risk Assessment and Contingency
* **Data Exposure Risk:** Neutralized by enforcing absolute S3 Private Bucket configurations, global Block Public Access constraints, dynamic Presigned URLs restricted by tight temporal expiration limits, and role-based user token validation mapping via Amazon Cognito directory groups.
* **Malicious File Ingestion Threat:** Remedied by routing all untrusted inbound data streams directly into an isolated QuarantineBucket sandbox, backed by real-time automated threat checking via GuardDuty Malware Protection plans.
* **Payload Size Networking Bottlenecks:** Resolved by bypassing compute networks during ingestion blocks, streaming binary files directly from client browsers straight to S3 storage boundaries instead of passing multi-megabyte data payloads across API Gateways.
* **Unexpected Cloud Spend Accrual:** Mitigated by setting up automated CloudWatch Alarms monitoring system limits, routing urgent notification messages via SNS topics, and systematically triggering multi-environment resource teardown purges upon project evaluation handoffs.

### 8. Expected Outcomes
The capstone project targets the successful implementation of a highly performant, secure internal enterprise document management system complete with robust multi-tenant authorization partitions, asset version tracking capabilities, immutable append-only compliance ledger recording, and automated perimeter data isolation screening.
Through the execution of this deployment lifecycle, engineering teams thoroughly synthesize cutting-edge AWS Serverless architectural design patterns against real-world enterprise requirements, gaining expert-level proficiency in modeling, constructing, securing, and maintaining cloud-native, modern software systems.