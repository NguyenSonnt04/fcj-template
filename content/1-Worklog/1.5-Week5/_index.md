---
title: "Week 5 Worklog"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives

- Transform a Spring Boot monolith into microservices.
- Build synchronous, asynchronous, and serverless workflows on AWS.
- Configure authentication, CI/CD, and observability for a distributed system.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2 | **Monolith and Microservices Analysis**<br>- Analyzed the business modules in the existing Java Spring Boot application.<br>- Identified service boundaries and separated functional components into independent services.<br>- Standardized configuration and data requirements for independent operation. | 05/25/2026 | 05/25/2026 |  |
| 3 | **APIs and Service Communication**<br>- Built REST APIs for communication between microservices.<br>- Tested data flows, error codes, and the independent behavior of each service.<br>- Configured Amazon SQS and SNS for asynchronous communication and tested the event flow. | 05/26/2026 | 05/26/2026 |  |
| 4 | **Serverless Application**<br>- Developed AWS Lambda functions for business and data processing.<br>- Combined API Gateway, S3, and DynamoDB into a serverless workflow.<br>- Tested requests, responses, IAM permissions, and data access. | 05/27/2026 | 05/27/2026 |  |
| 5 | **Authentication and Automated Delivery**<br>- Configured Amazon Cognito for a Single Page Application.<br>- Tested registration, login, token issuance, and session management.<br>- Built a CodePipeline workflow for automated build, test, and deployment. | 05/28/2026 | 05/28/2026 |  |
| 6 | **Workflow and Observability**<br>- Built a business workflow with Step Functions and monitored each state.<br>- Explored AppSync and integrated a GraphQL API.<br>- Configured CloudWatch and X-Ray for logs, request tracing, and performance troubleshooting. | 05/29/2026 | 05/29/2026 |  |

### Week 5 Results

- Practiced decomposing a monolith into independent microservices.
- Implemented REST and SQS/SNS communication and a serverless workflow with Lambda, API Gateway, S3, and DynamoDB.
- Configured Cognito, CodePipeline, Step Functions, AppSync, CloudWatch, and X-Ray.
