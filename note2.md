# 5. Generative AI Concepts

## Tokenization
Converts input into tokens that models can process.

### Types

#### Word-Based Tokenization
**Example:**  
`AWS Bedrock is awesome`  
**Tokens:**  
`AWS | Bedrock | is | awesome`

#### Subword Tokenization
Breaks uncommon words into smaller pieces.

**Example:**  
`unbelievable`  
**Tokens:**  
`un | believe | able`

### Why It Matters
- Reduces vocabulary size  
- Handles unknown words  
- Improves efficiency  

---

## Context Window (CW)
Maximum number of tokens a model can process.

### Key Points
- Larger context window = more information retained  
- Better coherence across long conversations  
- Higher cost  

### Exam Tip
If the requirement includes:
- Long documents  
- Large conversations  
- More context retention  

→ Choose a model with a larger **Context Window**

---

## Embeddings
Numerical vector representation of data.

### Can Represent
- Text  
- Images  
- Audio  

### Purpose
Captures:
- Meaning  
- Context  
- Relationships  
- Sentiment  

### Common Uses
- Semantic Search  
- Recommendation Systems  
- RAG Applications  
- Similarity Search  

---

# 6. Amazon Bedrock Guardrails

## Overview
Provides safety controls between users and Foundation Models.

### Benefits
- Filter harmful content  
- Protect sensitive information  
- Reduce hallucinations  
- Enforce organizational policies  

### Features
- Multiple guardrails supported  
- Monitor policy violations  
- Analyze user inputs  

---

## Guardrail Policy Types

### Content Filters
Detect and block harmful content.

**Examples:**
- Hate Speech  
- Insults  
- Sexual Content  
- Violence  
- Misconduct  

**Exam Keywords:**
- Harmful content  
- Toxicity  
- Safety filtering  

---

### Denied Topics
Block specific topics entirely.

**Examples:**
- Medical advice  
- Legal advice  
- Financial advice  

**Exam Keywords:**
- Block topic  
- Restricted subject  

---

### Sensitive Information Filters (PII)
Detect and redact sensitive data.

**Examples:**
- Names  
- Email addresses  
- Phone numbers  
- Credit cards  

**Exam Keywords:**
- PII masking  
- Redaction  
- Sensitive information  

---

### Word Filters
Block exact words or phrases.

**Examples:**
- Profanity  
- Competitor names  
- Internal code names  

---

### Contextual Grounding Checks
Used primarily with RAG applications.

**Purpose:**
- Detect hallucinations  
- Ensure answers are grounded in source documents  

**Exam Keywords:**
- RAG  
- Hallucination detection  
- Grounded responses  

---

### Automated Reasoning
Validates responses using logical rules.

**Purpose:**
- Accuracy  
- Consistency  
- Compliance  

**Exam Keywords:**
- Logical validation  
- Rule-based verification  

---

# 7. Amazon Bedrock Agents

## Overview
Agents automate multi-step workflows using Foundation Models.

### Examples
- Infrastructure provisioning  
- Application deployment  
- Business process automation  

---

## Components

### Agent
Orchestrates tasks.

### Task Coordinator
Responsible for:
- Correct task sequence  
- Passing information between tasks  

### Action Groups
Perform actual work.

**Examples:**
- Lambda Functions  
- APIs  
- Databases  
- External services  

---

## Integrations
Agents can communicate with:
- AWS Services  
- Databases  
- APIs  
- SaaS applications  
- Knowledge Bases  

---

## Agent Workflow

1. Define instructions  
   - Example: Help users reset passwords  

2. Configure Action Groups  
   - Example: Lambda, APIs, Knowledge Bases  

3. Agent determines required actions  

4. Agent executes tasks  

5. Returns final response  

---

# 8. Bedrock Monitoring & Pricing

## CloudWatch Integration

### CloudWatch Logs
Stores:
- Prompts  
- Responses  
- Errors  
- Invocation details  

**Use Cases:**
- Troubleshooting  
- Auditing  
- Monitoring  

---

### CloudWatch Metrics

#### Important Metrics

**ContentFilteredCount**
- Measures Guardrail filtering activity  
- ✅ Exam Tip: Used to verify Guardrails are functioning  

**InvocationLatency**
- Measures response time  
- ✅ Exam Tip: High latency → investigate model performance  

---

### CloudWatch Alarms
Trigger alerts based on thresholds.

**Examples:**
- High latency  
- Excessive failures  
- Increased filtering  

---

### CloudWatch Dashboards
Visualize:
- Trends  
- Performance  
- Error rates  
- Usage metrics  

---

# 9. Bedrock Pricing Models

## On-Demand
Pay only for usage.

**Best For:**
- Small projects  
- Prototypes  
- Unpredictable workloads  

---

## Provisioned Throughput
Reserve dedicated model capacity.

**Best For:**
- Production workloads  
- Consistent traffic  

**Benefits:**
- Predictable performance  
- Guaranteed throughput  

---

## Batch Processing
Used for non-urgent workloads.

**Example:**
- Analyze 10,000 reviews overnight  

**Benefits:**
- Up to 50% cheaper  
- Large-scale processing  

**Exam Keywords:**
- Bulk processing  
- Offline jobs  
- Cost optimization  

---

# 10. Amazon Nova Models

## Overview
AWS Foundation Model family.

---

### Nova Premier
**Best For:**
- Complex reasoning  
- Distillation  
- Advanced AI applications  

---

### Nova Pro
**Best For:**
- Complex reasoning  
- General enterprise workloads  

---

### Nova Lite
**Best For:**
- Lower cost  
- Faster responses  

---

### Nova Micro
**Best For:**
- Text-only tasks  
- Lowest latency  

---

### Nova Canvas
**Purpose:**
- Image generation  

✅ **Exam Tip:** Text → Image  

---

### Nova Reel
**Purpose:**
- Video generation  

✅ **Exam Tip:** Text → Video  

---

### Nova Sonic
**Purpose:**
- Speech and voice applications  

✅ **Exam Tip:** Speech AI  

---

### Nova 2 Multimodal Embeddings
](https://github.com/ravisolanki07/AIF-C01-Study-Notes/blob/main/note2)
