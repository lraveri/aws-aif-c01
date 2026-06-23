# Part 5 - Bedrock Evaluation, RAG, Guardrails, Agents, and Nova

[← 04](04-generative-ai-and-amazon-bedrock-fundamentals.md) | [↑ Index](../README.md) | [06 →](06-prompt-engineering.md)

### Fine-tuning use cases
Typical use cases:
- a chatbot with a specific persona, tone, or purpose
- training on more up-to-date information than the base model originally had
- training on exclusive internal data such as historical emails or customer support records
- targeted tasks such as classification or accuracy-focused use cases

### Model evaluation in Bedrock
Bedrock supports both `automatic` and `human` evaluation.

### Automatic evaluation
Purpose:
- quality control for model outputs

Built-in task types mentioned:
- text summarization
- question answering
- text classification
- open-ended text generation

Inputs:
- your own prompt dataset
- or built-in curated prompt datasets

How it works:
- the model generates answers
- results are scored automatically
- scores can use statistical methods such as `BERTScore` and `F1`

### Benchmark datasets
Benchmark datasets are curated datasets designed specifically to evaluate language models.

They help measure:
- accuracy
- speed and efficiency
- scalability
- bias and potential discrimination

Important note:
- you can also create your own business-specific benchmark dataset

### Human evaluation
Human evaluation uses a work team such as:
- company employees
- subject-matter experts (`SMEs`)

You define:
- the evaluation metrics
- the scoring method, for example thumbs up/down or ranking

You can use:
- built-in task types
- or a custom task

### Automated metrics
- `ROUGE`: used mainly for summarization and translation quality
- `BLEU`: used especially for translation quality
- `BERTScore`: measures semantic similarity using embeddings
- `Perplexity`: measures how well the model predicts the next token; lower is better

Useful clarification:
- `ROUGE` and `BLEU` focus more on overlap with reference text
- `BERTScore` is better at capturing semantic similarity even when wording changes

### Automated model evaluation in applications
Evaluation can also be tied to business data such as:
- clickstream data
- cart data
- purchased items
- customer feedback

Idea: model quality should be measured not only with technical metrics, but also with feedback loops from real application behavior.

### Business metrics to evaluate a model
Examples listed:
- user satisfaction
- `ARPU` (Average Revenue Per User)
- cross-domain performance
- conversion rate
- efficiency in computation and resource usage

Key idea: a technically strong model is not enough if it does not improve business outcomes.

### RAG and Knowledge Bases
`RAG` stands for `Retrieval-Augmented Generation`.

Purpose:
- let a foundation model use data outside its original training set
- provide more relevant and up-to-date answers

How it works:
- user asks a question
- the system searches a knowledge base for relevant information
- retrieved text is added to the prompt
- the model generates the final answer using both the prompt and retrieved content

Bedrock handles:
- creating vector embeddings
- storing them in the selected vector database

### When to use RAG
Use RAG when:
- real-time or frequently updated data is needed
- the base model does not contain the required internal knowledge
- you want better factual grounding without changing the model itself

### RAG vector databases
AWS options:
- `Amazon OpenSearch Service`
- `Amazon Aurora PostgreSQL`
- `Amazon Neptune Analytics`
- `Amazon S3 Vectors`

Quick interpretation:
- `OpenSearch`: strong fit for scalable similarity search
- `Aurora PostgreSQL`: useful when you want vectors in a relational database
- `Neptune Analytics`: useful for graph-based RAG / `GraphRAG`
- `S3 Vectors`: cost-effective durable storage with sub-second queries

### RAG data sources
Data sources listed:
- `Amazon S3`
- `Confluence`
- `Microsoft SharePoint`
- `Salesforce`
- web pages

### RAG use cases
- customer service chatbots using product docs, FAQs, and troubleshooting guides
- legal research over laws, regulations, precedents, and expert analysis
- healthcare question answering over diseases, treatments, guidelines, research, and patient-related knowledge

### Tokenization
Tokenization is the conversion of raw text into a sequence of tokens.

The setup includes:
- word-based tokenization
- subword tokenization

Useful clarification: tokens are not always whole words; long or rare words may be split into smaller parts.

### Context window
The context window is the number of tokens an LLM can consider when generating text.

Key points:
- larger context windows allow the model to consider more information
- this can improve coherence
- larger context windows also require more memory and processing power

Practical takeaway: context window is one of the first factors to check when selecting a model.

### Embeddings
Embeddings are vector representations of text, images, or audio.

Main ideas:
- vectors are high-dimensional numerical arrays
- they capture features such as meaning, syntax, or sentiment
- embedding models are useful for search applications

### Semantic similarity in embeddings
Words with similar meanings tend to have similar embeddings.

Example implied by the slide:
- `dog` and `puppy` are closer than `dog` and `house`

Why this matters:
- similarity search in RAG depends on embeddings placing related items close together in vector space

### Guardrails
Bedrock `Guardrails` control the interaction between users and foundation models.

Main functions listed:
- filter harmful or undesirable content
- remove `PII` (Personally Identifiable Information)
- enhance privacy
- reduce hallucinations
- allow multiple guardrails
- monitor and analyze user inputs that violate policies

### Bedrock Agents
Bedrock Agents are used for multi-step task execution.

Capabilities mentioned:
- coordinate tasks in the correct order
- pass information across steps
- use predefined action groups
- integrate with systems, services, databases, and APIs
- use RAG when needed

### Agent setup
The setup slide shows that agents can combine:
- `Lambda` functions
- `Knowledge Bases`
- APIs defined with `OpenAPI`
- databases
- action groups

### Agent execution flow
The diagram shows an agent using:
- the user prompt
- conversation history
- instructions
- actions
- knowledge bases
- intermediate results

Core idea: the agent plans and executes multiple steps before producing the final response.

### Bedrock with CloudWatch
Two key observability areas:

`Model invocation logging`
- send invocation logs to `CloudWatch` and `S3`
- logs can include text, images, and embeddings
- logs can be analyzed with CloudWatch Logs Insights

`CloudWatch metrics`
- Bedrock publishes metrics to CloudWatch
- example metric: `ContentFilteredCount`
- you can build CloudWatch alarms on top of these metrics

### Bedrock pricing
Pricing modes listed:

`On-Demand`
- pay as you go
- text models: charged per input and output token
- embedding models: charged per input token
- image models: charged per generated image
- works with base and custom models

`Batch`
- submit multiple predictions together
- output is written as a single file in `Amazon S3`
- can provide discounts of up to `50%`

`Provisioned Throughput`
- reserve model units for a period such as 1 month or 6 months
- throughput is the maximum number of tokens processed per minute
- works with base, fine-tuned, and custom models

### Cost order of model improvement techniques
Cost order from lowest to highest:
1. prompt engineering
2. RAG
3. instruction-based fine-tuning
4. domain adaptation fine-tuning

Main idea:
- prompt engineering and RAG are cheaper because they do not require retraining the model
- fine-tuning is more expensive because it adds training compute

### Bedrock cost-saving points
- `On-Demand` is good for unpredictable workloads
- `Batch` can reduce cost by up to `50%`
- `Provisioned Throughput` is mainly for reserved capacity, not usually for cost savings
- `Temperature`, `Top K`, and `Top P` do not affect pricing
- smaller models are usually cheaper
- the main cost driver is the number of input and output tokens

### Amazon Nova
Amazon Nova is AWS's family of foundation models available through Bedrock.

Positioning:
- AWS's own model family
- designed to be fast, cost-effective, and enterprise-ready

### Amazon Nova model families
`Understanding`
- `Nova Premier`: most capable multimodal model for complex reasoning and strong teacher model for distillation
- `Nova Pro`: balanced accuracy, speed, and cost for many tasks
- `Nova Lite`: low-cost multimodal model with very fast processing
- `Nova Micro`: text-only, lowest latency, very low cost

`Creative`
- `Nova Canvas`: image generation
- `Nova Reel`: video generation

`Speech`
- `Nova Sonic`: conversational speech understanding and generation in multiple languages

### Amazon Nova 2
`Nova 2` is presented as a newer set of models with enhanced capabilities for complex AI apps.

Highlights listed:
- interactive chatbots
- document and video analysis
- AI agent creation
- up to `1M` tokens of context
- advanced reasoning capabilities

Models mentioned:
- `Nova 2 Lite`
- `Nova 2 Sonic`
- `Nova 2 Multimodal Embeddings`
- `Nova 2 Omni`

Important note: Nova and Nova 2 model details may evolve over time.

[← 04](04-generative-ai-and-amazon-bedrock-fundamentals.md) | [↑ Index](../README.md) | [06 →](06-prompt-engineering.md)
