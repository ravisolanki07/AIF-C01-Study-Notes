# 12. Amazon Q

## Overview

Amazon Q is AWS's Generative AI assistant family.

Built on Amazon Bedrock and designed to help:

* Employees
* Developers
* AWS users
* Business users

---

# Amazon Q Business

## Overview

Generative AI assistant for enterprise knowledge and business workflows.

### Capabilities

* Question & Answer
* Summarization
* Content Generation
* Task Automation
* Workflow Assistance

### Examples

* Summarize documents
* Generate reports
* Answer HR questions
* Send meeting invites
* Search company knowledge

---

## Architecture

Built on Amazon Bedrock.

### Limitation

Cannot directly choose or modify the underlying Foundation Model.

---

## Data Connectors

Amazon Q Business includes fully managed RAG capabilities.

### Supported Sources

* Amazon S3
* Amazon RDS
* Amazon Aurora
* Amazon WorkDocs
* Microsoft 365
* Google Drive
* Gmail
* Slack
* SharePoint

### Exam Tip

Question mentions:

* Enterprise search
* Internal company documents
* Managed connectors

→ Amazon Q Business

---

## Plugins

Allow Amazon Q to interact with external systems.

### Examples

* Jira
* ServiceNow
* Zendesk
* Salesforce

### Features

* Read information
* Perform actions
* Custom plugin support

---

## Identity Integration

Uses IAM Identity Center.

### Benefits

* Single Sign-On (SSO)
* Existing permissions respected
* Role-based access control

### External Identity Providers

* Microsoft Entra ID (Azure AD)
* Google Workspace
* Other SAML providers

### Exam Tip

User should only see documents they already have access to.

---

## Administrative Controls

Similar to Bedrock Guardrails.

### Features

* Content restrictions
* Topic restrictions
* Response customization
* Internal-only responses

### Scope

* Global controls
* Topic-specific controls

---

# Amazon Q Apps

## Overview

Create applications using natural language.

### Benefits

* No coding required
* Rapid prototyping
* Business-friendly

### Example

```text
Create a customer support application
that summarizes tickets and drafts responses.
```

---

# Amazon Q Developer

## Overview

AI coding assistant for developers.

### Formerly Known As

AWS CodeWhisperer

---

## Capabilities

### AWS Assistance

* AWS architecture guidance
* Service selection recommendations
* AWS documentation answers

---

### Code Generation

Supports:

* Python
* JavaScript
* TypeScript
* Java
* C#

### Features

* Real-time code suggestions
* Function generation
* Documentation generation
* Test generation

---

### IDE Integrations

* Visual Studio Code
* Visual Studio
* JetBrains IDEs

### Exam Tip

Question mentions:

* Coding assistant
* AWS development help
* Code completion

→ Amazon Q Developer

---

## CLI Integration

Can assist directly from terminal environments.

### Examples

* AWS CLI commands
* Troubleshooting
* Resource explanations

---

# Amazon Q in AWS Services

## Amazon QuickSight

### Features

* Natural language dashboards
* Visualization generation
* Data summarization

### Example

```text
Show monthly sales trends by region.
```

### Exam Tip

Question mentions:

* BI dashboards
* Natural language analytics

→ QuickSight + Amazon Q

---

## Amazon EC2

Provides AI-powered operational assistance.

---

## AWS Chatbot

Integrates AWS notifications into:

* Slack
* Microsoft Teams

### Capabilities

* Billing alerts
* Monitoring alerts
* Support notifications

---

## AWS Glue

Supports ETL workflows.

Amazon Q can assist with:

* Data transformations
* ETL recommendations
* Workflow development

---

# 13. PartyRock

## Overview

Generative AI playground powered by Amazon Bedrock.

### Purpose

Experiment with AI applications without AWS setup complexity.

---

## Features

* No AWS account required
* Rapid prototyping
* Visual interface
* Prompt experimentation

---

## Use Cases

* Learning GenAI
* Building simple apps
* Testing prompts
* Demonstrations

### Exam Tip

Question mentions:

* Learning environment
* Playground
* No AWS account

→ PartyRock

---

# 14. Amazon SageMaker

## Overview

Fully managed machine learning platform.

Supports the complete ML lifecycle:

1. Data preparation
2. Model training
3. Model tuning
4. Model deployment
5. Monitoring

---

# SageMaker Workflow

```text
Data Collection
      ↓
Data Preparation
      ↓
Feature Engineering
      ↓
Training
      ↓
Tuning
      ↓
Deployment
      ↓
Monitoring
```

---

# Automatic Model Tuning (AMT)

Automatically finds optimal hyperparameters.

### Optimizes

* Learning rate
* Batch size
* Training configuration

### Search Methods

* Grid Search
* Bayesian Optimization

### Benefits

* Faster experimentation
* Better model performance

---

# Model Deployment & Inference

## Real-Time Inference

### Characteristics

* Immediate predictions
* Low latency
* Small payloads (~6 MB)

### Use Cases

* Fraud detection
* Recommendation systems
* Chatbots

### Exam Keywords

* Instant response
* Low latency

---

## Serverless Inference

### Characteristics

* No infrastructure management
* Automatic scaling

### Limitations

* Cold starts

### Use Cases

* Intermittent workloads
* Cost optimization

### Exam Keywords

* Infrequent requests
* No server management

---

## Asynchronous Inference

### Characteristics

* Handles large payloads
* Up to 1 GB

### Workflow

```text
Request → S3
Processing
Result → S3
```

### Use Cases

* Video processing
* Large document analysis

### Exam Keywords

* Large payload
* Long-running jobs

---

## Batch Transform

### Characteristics

* Bulk processing
* Offline predictions

### Payload Size

~100 MB+

### Use Cases

* Daily predictions
* Customer segmentation
* Historical analysis

### Exam Keywords

* Bulk processing
* Batch jobs

---

# SageMaker Studio

## Overview

Unified environment for machine learning.

### Features

* Data preparation
* Model development
* Training
* Deployment
* Monitoring

---

## Benefits

### Collaboration

Multiple team members can work together.

### End-to-End Platform

Single location for ML workflows.

### Integrated Tools

* Data Wrangler
* Clarify
* MLflow
* JumpStart

---

# SageMaker Data Wrangler

## Overview

Low-code data preparation service.

---

## Features

### Data Preparation

Supports:

* Tabular data
* Image data

### Feature Engineering

Create useful features for training.

### SQL Support

Perform transformations using SQL.

### Data Quality Checks

Identify:

* Missing values
* Outliers
* Inconsistencies

### Exam Tip

Question mentions:

* Data preparation
* Feature engineering
* Low-code

→ Data Wrangler

---

# SageMaker Feature Store

## Overview

Central repository for ML features.

### Benefits

* Feature reuse
* Consistency
* Governance

### Integration

Works with:

* Data Wrangler
* SageMaker Training Jobs

### Exam Keywords

* Feature storage
* Feature reuse
* Centralized features

---

# Inference

## Definition

Applying a trained model to new data.

### Example

```text
Training:
Historical customer data

Inference:
New customer prediction
```

---

# SageMaker Exam Decision Guide

| Requirement                  | Service                |
| ---------------------------- | ---------------------- |
| Build ML models from scratch | SageMaker              |
| End-to-end ML environment    | SageMaker Studio       |
| Data preparation             | Data Wrangler          |
| Feature repository           | Feature Store          |
| Hyperparameter tuning        | Automatic Model Tuning |
| Instant predictions          | Real-Time Inference    |
| No servers                   | Serverless Inference   |
| Large payloads               | Asynchronous Inference |
| Bulk predictions             | Batch Transform        |
| Experiment with AI apps      | PartyRock              |
| Enterprise AI assistant      | Amazon Q Business      |
| Coding assistant             | Amazon Q Developer     |

---

# Memory Tricks

```text
Q Business = Company Knowledge
```

```text
Q Developer = Coding Assistant
```

```text
PartyRock = Bedrock Playground
```

```text
Data Wrangler = Prepare Data
```

```text
Feature Store = Store Features
```

```text
Real-Time = Fast
```

```text
Serverless = No Servers
```

```text
Asynchronous = Large Files
```

```text
Batch = Bulk Predictions
```
