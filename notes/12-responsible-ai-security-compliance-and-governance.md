# Part 12 - Responsible AI, Security, Compliance, and Governance

[← 11](11-ec2-ai-hardware-and-amazon-sagemaker.md) | [↑ Index](../README.md) | [13 →](13-aws-security-services-and-supporting-aws-basics.md)

### Responsible AI
Responsible AI means building AI systems that are trustworthy, transparent, and designed to reduce harmful outcomes.

Main goal:
- maximize value while reducing risk

### Governance and compliance
`Governance` is about ensuring AI creates value while risks are managed through clear policies, oversight, and accountability.

`Compliance` is about following legal, regulatory, and internal requirements.

### Core dimensions of responsible AI
- `Fairness`: reduce discrimination and support inclusion
- `Explainability`: make decisions understandable
- `Privacy and security`: protect people and sensitive data
- `Robustness`: maintain reliable behavior under different conditions
- `Governance`: define controls, accountability, and oversight
- `Transparency`: communicate clearly about system behavior and limits

### AWS services that support responsible AI
Examples:
- `Amazon Bedrock` model evaluation, both human and automatic
- `Bedrock Guardrails` to filter content and redact `PII`
- `SageMaker Clarify` for bias detection and explainability

### AWS AI Service Cards
AWS AI Service Cards are documentation artifacts that help you understand an AI service.

They are useful for:
- intended use cases
- limitations
- design considerations
- responsible AI aspects

### Interpretability
Interpretability is the degree to which a human can understand why a model made a decision.

Tradeoff:
- simpler models are usually easier to interpret
- more complex models may perform better but can be harder to explain

### Highly interpretable models
Decision trees are an example of a highly interpretable model.

They can be used for:
- classification
- regression

Why they are interpretable:
- decisions are made through explicit branch conditions

### Partial Dependence Plots
`PDPs` show how a single feature influences the predicted outcome while holding other features constant.

They are useful for:
- model interpretation
- understanding feature influence

### Human-Centered Design for explainable AI
Human-Centered Design (`HCD`) means designing AI systems around human needs and decision-making.

Main idea:
- AI should support people, not just automate outputs

### Generative AI capabilities
Main strengths highlighted:
- adaptability
- responsiveness
- simplicity
- creativity and exploration
- data efficiency

### Toxicity
Toxicity means generating offensive, harmful, disturbing, or inappropriate content.

Challenge:
- the definition of toxicity can vary depending on context and policy

### Hallucinations
Hallucinations are outputs that sound plausible but are incorrect.

Why they happen:
- LLMs generate text through next-token probability, not guaranteed factual retrieval

Risk:
- users may trust confident-sounding wrong answers

### Plagiarism and cheating
Generative AI can be misused for:
- academic cheating
- fake writing samples
- low-effort content reuse without proper attribution

### Prompt misuses
Three important misuse categories:

`Poisoning`
- malicious or biased data is inserted into training data
- this can push the model toward harmful behavior

`Exposure`
- sensitive or confidential information is revealed to a model during training or inference
- the model may later expose that information

`Jailbreaking`
- users try to bypass a model's safety restrictions through crafted prompts

### Regulated workloads
Some industries require stricter compliance controls.

Examples:
- financial services
- healthcare
- aerospace

Implication:
- AI systems in these domains may need additional reporting, controls, validation, and auditability

### AI standard compliance challenges
Common challenges:
- complexity and opacity
- system dynamism and adaptability
- changing regulations and standards
- difficulty auditing how decisions are made

### AWS compliance
AWS supports many security and compliance programs.

Examples mentioned:
- `NIST`
- `EU AI Act`

Key idea:
- AWS provides a compliance foundation, but customers still have their own responsibilities

### Model cards
Model Cards are standardized documents describing a model.

They can include:
- intended use
- limitations
- risks
- training details
- source citations
- data origin details

### Why governance and compliance matter
Governance is important to:
- manage AI initiatives at scale
- optimize how AI is used
- reduce organizational risk
- build trust internally and externally

### Governance framework
One practical governance approach is to create an AI governance board or committee.

This group should include representatives from multiple functions, for example:
- technical teams
- legal
- compliance
- security
- business stakeholders

### AWS governance tools
Examples mentioned:
- `AWS Config`
- `AWS Trusted Advisor`
- `AWS CloudTrail`
- `AWS Artifact`
- `AWS Audit Manager`
- `Amazon Inspector`

### Governance strategies
Governance should define:
- policies
- guidelines
- responsible AI principles
- model training rules
- output validation rules
- monitoring and review processes

### Transparency standards
Transparency requires publishing useful information about:
- models
- training data
- key decisions
- known limitations

### Data governance strategies
Data governance should cover:
- responsible AI rules
- fairness and bias controls
- transparency
- accountability
- monitoring of AI and GenAI data flows

### Data management concepts
Important data management areas:
- data lifecycle: collection, processing, storage, consumption, archival
- data logging: track inputs, outputs, performance, and events

### Data lineage
Data lineage means tracking where data comes from and how it moves through systems.

Important elements:
- source citation
- dataset and database origin
- licenses and usage terms
- transformations along the pipeline

### Security and privacy for AI systems
Main security concerns include:
- fake content generation
- manipulated data
- automated attacks
- prompt injection

### Prompt injection defenses
Common defenses:
- prompt filtering
- sanitization
- guardrails
- access controls

### Monitoring AI systems
Monitoring should track both technical and operational quality.

Examples of metrics:
- accuracy
- precision
- recall
- latency
- drift indicators
- safety or policy-violation rates

### Shared responsibility in AI systems
The AWS shared responsibility model still applies:
- AWS secures the cloud infrastructure
- customers secure data, configurations, identities, model usage, and application behavior

### Secure data engineering best practices
Important data-quality dimensions:
- completeness
- accuracy
- consistency
- timeliness
- relevance

Important protection controls:
- data access control
- role-based access control
- governance policies

### Generative AI security scoping matrix
This is a framework to identify and manage GenAI security risks by mapping:
- the application context
- the threat surface
- the control boundaries

### MLOps
`MLOps` extends DevOps principles to machine learning systems.

Its purpose is to ensure models are:
- deployed reliably
- monitored continuously
- retrained systematically
- managed as repeatable production systems

Typical pipeline areas:
- data pipeline
- model build and testing pipeline
- deployment pipeline
- monitoring pipeline

[← 11](11-ec2-ai-hardware-and-amazon-sagemaker.md) | [↑ Index](../README.md) | [13 →](13-aws-security-services-and-supporting-aws-basics.md)
