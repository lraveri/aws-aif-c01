# AIF-C01 Study Program

## Objective

Build complete, up-to-date, exam-oriented notes for the **AWS Certified AI Practitioner (AIF-C01)** exam, starting from official AWS sources and paying special attention to recent additions such as **Kiro**, **Strands Agents**, and **Amazon Bedrock AgentCore**.

## Official basis for this program

This program is based on three verified AWS references:

1. the official AIF-C01 exam guide;
2. the in-scope AWS services list;
3. the exam guide revision history.

## Exam facts to lock in first

- Exam: **AWS Certified AI Practitioner (AIF-C01)**
- Duration: **90 minutes**
- Total questions: **65**
- Scored questions: **50**
- Unscored questions: **15**
- Passing score: **700/1000**

## Domains and weights

- Domain 1: **Fundamentals of AI and ML** - 20%
- Domain 2: **Fundamentals of GenAI** - 24%
- Domain 3: **Applications of Foundation Models** - 28%
- Domain 4: **Guidelines for Responsible AI** - 14%
- Domain 5: **Security, Compliance, and Governance for AI Solutions** - 14%

## Official updates to keep in mind

Revision **v1.1 published on April 30, 2026** explicitly added or strengthened:

- **agentic AI**
- **context engineering**
- **token-based pricing**
- **MCP**
- **prompt versioning and Prompt Management**
- **LLM-as-a-judge**
- **hallucination detection and grounding**
- **Amazon Bedrock AgentCore**
- **Kiro**
- **Strands Agents**
- **Amazon Q**

This means the notes must reflect the updated blueprint, not just the earlier version of the certification.

## Study strategy

Recommended approach:

1. lock down the exact exam scope;
2. study concepts before services;
3. map AWS services to use cases;
4. deepen coverage of new or easily confused topics;
5. consolidate with flashcards and exam-style questions.

## Detailed iteration plan

### Iteration 1 - Exam scope and sources

Objective:

- clarify what is definitely in scope;
- lock the notes structure;
- create a map of official sources.

Expected output:

- `01-exam-scope-and-sources.md`

Coverage:

- exam structure;
- domain weights;
- difference between the official exam guide, in-scope services, and product documentation;
- list of newly introduced topics from revision v1.1 dated April 30, 2026.

### Iteration 2 - Domain 1: Fundamentals of AI and ML

Objective:

- consolidate the base terminology that often causes simple exam mistakes.

Expected output:

- `02-domain-1-ai-ml-fundamentals.md`

Coverage:

- AI, ML, deep learning, neural networks;
- NLP, computer vision, forecasting, recommendation systems;
- training vs inferencing;
- batch, real-time, asynchronous, serverless inferencing;
- supervised, unsupervised, reinforcement learning;
- high-level AI/ML pipeline;
- when to use traditional ML vs foundation models.

### Iteration 3 - Domain 2: Fundamentals of GenAI

Objective:

- fix the core GenAI concepts and the main cost/performance levers.

Expected output:

- `03-domain-2-genai-fundamentals.md`

Coverage:

- foundation models and large language models;
- tokens, context window, embeddings;
- token-based pricing;
- prompt engineering;
- context engineering;
- multimodality;
- model selection factors: cost, latency, quality, compliance, complexity.

### Iteration 4 - Domain 3: Applications of Foundation Models

Objective:

- clarify how foundation models are applied to real use cases.

Expected output:

- `04-domain-3-foundation-models.md`

Coverage:

- in-context learning;
- fine-tuning;
- pre-training at a conceptual level;
- Retrieval-Augmented Generation;
- distillation at a foundational level;
- prompt management;
- foundation model evaluation;
- metrics such as BLEU, ROUGE, BERTScore, LLM-as-a-judge;
- business metrics such as task completion, user satisfaction, cost per interaction.

### Iteration 5 - Agentic AI: Kiro, Strands Agents, AgentCore

Objective:

- create a dedicated block for the recent topics most likely to matter because of the updated exam blueprint.

Expected output:

- `05-domain-3-agents-kiro-strands-agentcore.md`

Coverage:

- what agentic AI means;
- the role of agents in multi-step tasks;
- tool use, memory, orchestration, multi-agent patterns;
- MCP at a conceptual level;
- **Kiro**: what it is, when to mention it, and how it relates to agentic development;
- **Strands Agents**: what it is, its role as an open-source agent SDK, and where it fits in the AWS ecosystem;
- **Amazon Bedrock AgentCore**: main components and when they matter;
- practical differences between Bedrock, AgentCore, Strands, and Kiro.

### Iteration 6 - Domain 4: Responsible AI

Objective:

- cover the ethics and transparency guidance required for the exam.

Expected output:

- `06-domain-4-responsible-ai.md`

Coverage:

- bias and fairness;
- explainability and transparency;
- human oversight;
- human-centered design;
- feedback loops;
- tools such as SageMaker Clarify and Model Cards;
- model limitations and risk communication.

### Iteration 7 - Domain 5: Security, Compliance, Governance

Objective:

- lock the security perimeter without drifting into specialist implementation depth.

Expected output:

- `07-domain-5-security-compliance-governance.md`

Coverage:

- IAM, least privilege, encryption, KMS, Secrets Manager;
- logging and audit trail;
- prompt injection;
- data leakage prevention;
- output filtering and validation;
- Amazon Bedrock Guardrails;
- AgentCore Identity and Policy at a conceptual level;
- shared responsibility model;
- basic compliance and governance.

### Iteration 8 - AWS services to remember

Objective:

- build a compact cheat sheet for final review.

Expected output:

- `08-services-cheat-sheet.md`

Coverage:

- in-scope services by category;
- one-line summary per service;
- when to use it;
- what it is commonly confused with.

### Iteration 9 - Flashcards and practice questions

Objective:

- turn the notes into active-recall material.

Expected output:

- `09-practice-questions-and-flashcards.md`

Coverage:

- direct questions;
- service comparisons;
- mini exam scenarios;
- common mistakes.

### Iteration 10 - Final consolidation

Objective:

- normalize wording and close gaps.

Expected output:

- full review across all files;
- final consistency check against the official blueprint.

Coverage:

- remove duplication;
- label "in scope" vs "useful context";
- capture the latest relevant official updates.

## Recommended study order

Practical order:

1. exam scope;
2. Domain 1;
3. Domain 2;
4. general Domain 3;
5. the agentic AI block;
6. Domain 4;
7. Domain 5;
8. services cheat sheet;
9. flashcards and quizzes;
10. final review.

## Notes quality criteria

Each iteration should produce notes that:

- are consistent with the official exam guide;
- reflect the recent blueprint changes;
- separate concepts, services, and use cases clearly;
- help pass the exam instead of just restating product documentation.

## References

- [AWS Certified AI Practitioner exam guide](https://docs.aws.amazon.com/aws-certification/latest/ai-practitioner-01/ai-practitioner-01.html)
- [In-scope AWS services](https://docs.aws.amazon.com/aws-certification/latest/ai-practitioner-01/aif-01-in-scope-services.html)
- [Revisions](https://docs.aws.amazon.com/aws-certification/latest/ai-practitioner-01/aif-01-revisions.html)
- [Amazon Bedrock AgentCore overview](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/what-is-bedrock-agentcore.html)
- [Kiro docs](https://kiro.dev/docs/)
- [Strands Agents docs](https://strandsagents.com/)

## Last reviewed

- Sources verified on **June 22, 2026**
