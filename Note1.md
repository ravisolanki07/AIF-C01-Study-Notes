# AWS Certified AI Practitioner (AIF-C01) Notes

---

# Table of Contents

1. Amazon Bedrock
2. Foundation Models (FMs)
3. Fine-Tuning
4. Model Evaluation
5. RAG & Knowledge Bases
6. Generative AI Concepts
7. Bedrock Guardrails
8. Bedrock Agents
9. Bedrock Monitoring & Pricing
10. Amazon Nova Models
11. Prompt Engineering
12. Amazon Q
13. PartyRock
14. SageMaker
15. AI & Machine Learning Fundamentals
16. AWS AI Services
17. Responsible AI & Governance
18. AWS Security & Supporting Services
19. Exam Tips & Cheat Sheet

---

# 1. Amazon Bedrock

## Overview

* Fully managed Generative AI service.
* Provides access to Foundation Models (FMs).
* Allows customization and deployment without managing infrastructure.

## Foundation Models (FMs)

### Amazon Titan

* AWS proprietary Foundation Model family.
* Fully managed API access.
* Supports customization and fine-tuning.

### FM Capabilities

Depending on model selection:

* Content Creation
* Text Generation
* Summarization
* Forecasting
* Data Analysis
* Image Generation

### Model Selection Criteria

For exam questions, evaluate:

| Factor   | Description                 |
| -------- | --------------------------- |
| Cost     | Price per token/inference   |
| Latency  | Response speed              |
| Accuracy | Quality of generated output |

### Bedrock Model Comparison

Compare models side-by-side using the Bedrock playground.

Important metrics:

* Token count
* Response time
* Output quality

---

# 2. Fine-Tuning

## Overview

Creates a customized version of a foundation model using your own data.

### When to Use

* Unique brand voice
* Company-specific terminology
* Domain-specific responses

### Data Storage

* Training data commonly stored in Amazon S3

### Exam Tip

Not all foundation models support fine-tuning.

---

## Supervised Fine-Tuning (SFT)

Uses labeled datasets.

### Format

```json
{
  "input": "Question",
  "output": "Expected Answer"
}
```

### Keywords

* Labeled data
* Task-specific learning

**Exam Tip:** If you see "labeled examples" or "input/output pairs", think **Supervised Fine-Tuning**.

---

## Reinforcement Fine-Tuning (RFT)

Uses human preference feedback.

### Process

1. Generate multiple responses
2. Compare outputs
3. Assign rewards
4. Improve model behavior

### Reward Functions

#### Objective Tasks

* Programmatic scoring
* Often implemented with Lambda (Python)

#### Subjective Tasks

* Another model evaluates quality

### Goal

Create outputs that are:

* Helpful
* Honest
* Harmless

### Keywords

* Human preferences
* Reward model
* Preference feedback
* Human values

---

## Distillation

Creates a smaller model from a larger model.

### Benefits

* Lower latency
* Lower cost
* Faster inference

### Architecture

Teacher Model → Student Model

### Exam Keywords

* Reduce cost
* Low latency
* Teacher-Student model

---

# 3. Model Evaluation

## Automatic Evaluation

Used for quality control.

### Common Tasks

* Summarization
* Question Answering
* Classification

### Dataset Sources

* AWS curated datasets
* Custom datasets

### Evaluation Goals

* Accuracy
* Robustness
* Toxicity detection

---

## ROUGE

Used for summarization quality.

### ROUGE-N

Measures matching n-grams.

### ROUGE-L

Measures longest common subsequence.

### Focus

Recall (coverage).

### Exam Keywords

* Summarization
* Key information retained
* Recall
* ROUGE-L

---

## BLEU

Used primarily for translation.

### Focus

Precision.

### Exam Keywords

* Translation
* Fluency
* Precision
* N-gram overlap

---

## BERTScore

Uses embeddings.

### Focus

Semantic similarity.

### Characteristics

* Meaning-based comparison
* Embedding-based evaluation

---

## Perplexity

Measures how well a model predicts the next token.

### Rule

Lower perplexity = better model performance.

---

## Business Metrics

### User Satisfaction

Measures user happiness.

### ARPU

Average Revenue Per User.

### Conversion Rate

Measures desired actions:

* Purchases
* Signups
* Subscriptions

### Efficiency

Measures resource utilization.

---

## Human Evaluation

Responses reviewed by:

* Subject Matter Experts (SMEs)
* Employees
* Human reviewers

### Metrics

* Thumbs Up / Down
* Ranking
* Pairwise Comparison

---

# 4. RAG (Retrieval-Augmented Generation)

## Overview

Allows foundation models to use external knowledge without fine-tuning.

### Benefits

* Up-to-date information
* Lower cost than retraining
* Reduced hallucinations

### Typical Data Sources

* Amazon S3
* SharePoint
* Salesforce
* Confluence
* Websites

---

## RAG Workflow

1. Ingest documents
2. Chunk content
3. Generate embeddings
4. Store embeddings in Vector DB
5. Retrieve relevant chunks
6. Augment prompt
7. Generate response

---

## Embeddings

Generated using models such as Amazon Titan Embeddings.

Stored as vectors in vector databases.

---

## Supported Vector Databases

| Service           | Type           |
| ----------------- | -------------- |
| OpenSearch        | Managed Search |
| Aurora            | Relational     |
| Neptune Analytics | Graph          |
| S3 Vectors        | Cost-effective |
| Redis             | In-memory      |
| MongoDB           | Document       |
| Pinecone          | Vector-native  |

### Exam Favorite

**Amazon OpenSearch**

* Managed
* Serverless option
* Fast nearest-neighbor search
* Scalable indexing

---

## RAG Use Cases

* Knowledge Base Chatbots
* Legal Research
* Healthcare Q&A

---
