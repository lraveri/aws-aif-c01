# Study Notes

## Part 1 - Introduction to AI

### What AI is
Artificial Intelligence is a branch of computer science that aims to solve problems commonly associated with human intelligence.

Examples of capabilities:
- image creation
- image recognition
- speech-to-text
- learning

### How it works in practice
Basic flow:
- a data scientist prepares a training dataset
- applies a classification algorithm
- trains an AI model
- the user provides an input
- the model returns a classification or prediction

Example shown: given an input image of a fruit, the model classifies the object as `apple`, `peaches`, or `bananas`.

### Essential AI timeline
- 1950s: birth of AI; Alan Turing proposes the Turing Test; John McCarthy introduces the term "Artificial Intelligence"
- 1970s: expert systems; example: `MYCIN`, a rule-based system for detecting bacteria
- 1990s: growth of machine learning and data mining
- 1997: IBM's `Deep Blue` defeats Garry Kasparov in chess
- 2010s: deep learning revolution; Google's `AlphaGo` defeats Lee Sedol in 2016
- 2020s: AI becomes common in everyday life; ethics and regulation also become more important

### Main use cases
- speech transcription and translation
- speech recognition and generation
- playing against humans in games such as chess, Go, and StarCraft
- driving cars and flying airplanes
- code suggestions for developers
- medical diagnosis
- fraud detection
- business process automation

### Practical example: Intelligent Document Processing
Example shown: from an input document such as a PDF or an invoice image, AI extracts structured data and inserts it into a database.

Techniques involved:
- Computer Vision
- Deep Learning
- Natural Language Processing (NLP)

Data extracted in the example:
- seller
- buyer
- items
- price
- quantity

Key idea: AI turns unstructured content into data that a system can use.

### AI today: relationship between the terms
Implicit hierarchy:
- `Artificial Intelligence` is the broadest category
- `Machine Learning` is a subset of AI
- `Deep Learning` is a subset of Machine Learning
- `Generative AI` is a modern subset of Deep Learning focused on generating new content

Useful clarification: today, when many people say "AI", they often mainly think of Generative AI tools such as ChatGPT or DALL-E, but AI is a much broader concept.

## Part 2 - AWS and Cloud Computing Basics

### How websites work
Basic idea:
- clients and servers communicate over a network
- both clients and servers have IP addresses
- requests are sent from the client to the server, and responses come back from the server to the client

Simple clarification: an IP address is the network address used to identify where data should be sent.

### What a server is made of
A server is composed of:
- compute: CPU
- memory: RAM
- storage: data storage
- database: structured data storage
- network components: routers, switches, DNS servers

### Basic IT terminology
- `Network`: cables, routers, and servers connected to each other
- `Router`: forwards data packets between networks and helps send traffic to the right destination on the internet
- `Switch`: sends packets to the correct server or client inside a network

### Traditional infrastructure
Before cloud computing, infrastructure was often hosted in places such as:
- a data center
- an office
- a home or garage

### Problems with the traditional IT approach
- you pay for the data center space
- you pay for power, cooling, and maintenance
- adding or replacing hardware takes time
- scaling is limited
- you need a 24/7 operations team
- disaster recovery is difficult: power outages, fire, earthquakes, and similar failures

Core idea: cloud computing externalizes much of this infrastructure burden.

### What cloud computing is
Cloud computing is the on-demand delivery of:
- compute power
- database storage
- applications
- other IT resources

Main characteristics:
- resources are delivered through a cloud services platform
- pricing is pay-as-you-go
- you can provision the right type and size of resources
- you can access many resources almost instantly
- the cloud provider owns and maintains the underlying hardware
- you provision and use what you need through a web interface or service APIs

### Everyday cloud examples
- `Gmail`: email as a cloud service
- `Dropbox`: cloud storage service
- `Netflix`: video on demand built on AWS

### Cloud deployment models
#### Private Cloud
- used by a single organization
- not exposed to the public
- offers more control
- useful for sensitive applications and specific business needs

#### Public Cloud
- resources are owned and operated by a third-party cloud provider
- delivered over the internet

#### Hybrid Cloud
- keeps some infrastructure on premises and extends some capabilities to the cloud
- gives control over sensitive assets
- also benefits from public cloud flexibility and cost-effectiveness

### Five characteristics of cloud computing
- `On-demand self-service`: users can provision resources without human interaction from the provider
- `Broad network access`: resources are available over the network and accessible from different client platforms
- `Multi-tenancy and resource pooling`: multiple customers share the same infrastructure securely
- `Rapid elasticity and scalability`: resources can be added or removed quickly based on demand
- `Measured service`: usage is measured, and customers pay for what they use

### Six advantages of cloud computing
- trade capital expense (`CAPEX`) for operational expense (`OPEX`)
- pay on demand instead of owning hardware
- reduce total cost of ownership (`TCO`) and operational costs
- benefit from economies of scale
- stop guessing capacity in advance
- increase speed and agility
- stop spending time and money running data centers
- go global in minutes using the provider's global infrastructure

Note: although presented as "six advantages", the list is broader; the main message is cost reduction, flexibility, speed, and global scale.

### Problems solved by the cloud
- `Flexibility`: change resource types when needed
- `Cost-effectiveness`: pay only for what you use
- `Scalability`: support more load by adding stronger or more resources
- `Elasticity`: scale out and scale in when needed
- `High availability and fault tolerance`: build across multiple data centers
- `Agility`: develop, test, and launch applications faster

Useful clarification:
- `Scalability` is the ability to handle growth
- `Elasticity` is the ability to automatically or quickly adjust capacity up and down

### Types of cloud computing
#### Infrastructure as a Service (IaaS)
- provides building blocks for cloud IT
- includes networking, compute, and storage
- offers the highest flexibility
- is the closest model to traditional on-premises infrastructure

#### Platform as a Service (PaaS)
- removes the need to manage the underlying infrastructure
- lets you focus on deploying and managing applications

#### Software as a Service (SaaS)
- complete product run and managed by the service provider

### Responsibility split across service models
- `On-premises`: you manage everything
- `IaaS`: you still manage more layers, while the provider manages the physical infrastructure
- `PaaS`: the provider manages more of the platform
- `SaaS`: the provider manages almost everything

Main pattern: moving from on-premises to SaaS reduces how much infrastructure you manage directly.

### Examples of each cloud model
- `IaaS`: Amazon EC2, GCP, Azure, Rackspace, DigitalOcean, Linode
- `PaaS`: AWS Elastic Beanstalk, Heroku, Google App Engine, Microsoft Azure platform services
- `SaaS`: Gmail, Dropbox, Zoom, and some fully managed AWS services from the user's point of view

### Cloud pricing basics
AWS pricing follows a pay-as-you-go model with three fundamentals:
- compute: pay for compute time
- storage: pay for data stored in the cloud
- data transfer out: pay for data leaving the cloud

Important detail:
- data transfer into the cloud is generally free

Key takeaway: cloud pricing avoids the large upfront costs of traditional IT and aligns spending more closely with actual usage.

## Part 3 - AWS Overview and Global Infrastructure

### Short AWS history
- 2002: AWS launched internally
- 2003: Amazon recognized its infrastructure as a core strength and saw the opportunity to commercialize it
- 2004: first public launch with `SQS`
- 2006: broader public relaunch with `SQS`, `S3`, and `EC2`
- 2007: launch in Europe

### AWS facts
- in 2023, AWS had `$90 billion` in annual revenue
- in Q1 2024, AWS had `31%` market share
- Microsoft was second with `25%`
- AWS was described as a market leader for the 13th consecutive year
- AWS had over `1,000,000` active users

Note: these are point-in-time figures and can change over time.

### Common AWS use cases
AWS is presented as a platform for building sophisticated, scalable applications across many industries.

Examples listed:
- enterprise IT
- backup and storage
- big data analytics
- website hosting
- mobile and social applications
- gaming

### AWS global infrastructure
Core elements:
- `Regions`
- `Availability Zones`
- `Data Centers`
- `Edge Locations / Points of Presence`

### AWS Regions
- AWS has regions across the world
- examples of region names: `us-east-1`, `eu-west-3`
- a region is a cluster of data centers
- most AWS services are region-scoped

Useful clarification: "region-scoped" means resources are usually created in a specific geographic region and managed there.

### How to choose an AWS Region
Main factors:
- compliance, data governance, and legal requirements
- proximity to customers to reduce latency
- service availability, since not every service or feature exists in every region
- pricing, because prices vary by region

Practical takeaway: for a new application, choose the region that best balances legal constraints, latency, available services, and cost.

### Availability Zones (AZs)
- each region contains multiple Availability Zones
- usually `3`, minimum `3`, maximum `6`
- examples: `ap-southeast-2a`, `ap-southeast-2b`, `ap-southeast-2c`
- each AZ consists of one or more discrete data centers
- AZs have redundant power, networking, and connectivity
- AZs are isolated from each other to reduce the impact of disasters
- AZs are connected with high-bandwidth, ultra-low-latency networking

Key idea: deploying across multiple AZs improves availability and fault tolerance.

### Points of Presence / Edge Locations
- Amazon has `400+` points of presence
- this includes `400+` edge locations and `10+` regional caches
- they span `90+` cities across `40+` countries
- they help deliver content to end users with lower latency

Useful clarification: edge locations are used mainly to move content closer to users, especially through services like CloudFront.

### AWS console and service scope
Examples of global AWS services:
- `IAM`
- `Route 53`
- `CloudFront`
- `WAF`

Examples of region-scoped services listed:
- `Amazon EC2`
- `Elastic Beanstalk`
- `Lambda`
- `Rekognition`

Important distinction:
- `Global services` are managed at a global level
- `Region-scoped services` are deployed and operated within a specific AWS region

### Shared Responsibility Model
Core rule:
- AWS is responsible for the `security of the cloud`
- the customer is responsible for `security in the cloud`

Simple interpretation:
- AWS secures the underlying infrastructure
- customers secure their own data, identities, configurations, and usage of services

### AWS Acceptable Use Policy
AWS forbids:
- illegal, harmful, or offensive use or content
- security violations
- network abuse
- email or other message abuse

### Course budget note
Important cost reminders:
- AWS AI services are not always free
- following hands-on labs may generate charges
- some services may offer free trials, such as Amazon Q
- resources should be turned off when no longer needed

Practical takeaway: monitor usage carefully during labs to avoid unnecessary cost.

## Part 4 - Generative AI and Amazon Bedrock Fundamentals

### What Generative AI is
Generative AI is a subset of Deep Learning used to generate new data similar to the data it was trained on.

Types of content:
- text
- images
- audio
- code
- video

Basic pattern:
- a generative model is trained on data
- a user provides a prompt
- the model generates new content

### Foundation Models
Generative AI relies on `Foundation Models` (`FMs`).

Main points:
- FMs are pretrained on large amounts of mostly unlabeled data
- they can handle a broad range of general tasks
- they can later be adapted for specific needs

Examples of tasks:
- text generation
- text summarization
- information extraction
- image generation
- chatbots
- question answering

Important details:
- training foundation models can cost tens of millions of dollars
- GPT-4o is given as an example of a foundation model behind ChatGPT
- providers mentioned: OpenAI, Meta, Amazon, Google, Anthropic
- some models are open source, others are commercial

### Large Language Models (LLMs)
LLMs are a type of AI designed to generate coherent, human-like text.

Main characteristics:
- trained on very large text corpora
- usually very large models
- often have billions of parameters
- trained on books, articles, websites, and other text sources

Typical tasks:
- translation
- summarization
- question answering
- content creation

### How generative language models produce text
Typical interaction flow:
- the user provides a prompt
- the model uses what it learned during training
- it generates new text token by token

Important property:
- output is `non-deterministic`, so the same prompt can produce different answers

Text generation works like this:
- the model generates multiple candidate next words
- each candidate has a probability
- a selection algorithm chooses one of them
- this process repeats word after word

Useful clarification: in practice, models do not "retrieve a memorized sentence"; they predict the next most likely token repeatedly.

### Generative AI for images
Three common image-related patterns:
- `text to image`: generate an image from a text prompt
- `image to image`: transform an existing image into a different style
- `image to text`: describe or analyze what appears in an image

### Diffusion models
For image generation from text, a common approach is `Diffusion Models`, such as `Stable Diffusion`.

Basic idea:
- during training, images are progressively turned into noise
- during generation, the process is reversed to create an image from noise guided by a prompt

### Amazon Bedrock
Amazon Bedrock is AWS's fully managed service for building Generative AI applications.

Main points:
- no servers to manage
- pay-per-use pricing
- unified APIs
- access to many foundation models
- built-in features such as `RAG` and `LLM Agents`
- includes security, privacy, governance, and responsible AI features
- your data used for customization remains under your control

### Foundation models in Bedrock
Bedrock provides access to a wide range of foundation models.

Important points:
- Bedrock can make a copy of the chosen FM for your use
- that copy can be fine-tuned with your own data
- your data is not used to train the base foundation model for everyone else

### Bedrock architecture
The diagram highlights these building blocks:
- `Foundation Models`
- `Interactive Playground`
- `Knowledge Bases (RAG)`
- `Fine-tuning`
- `Amazon S3`
- `Unified API`
- consuming applications

Core idea:
- you can test models interactively
- connect them to your own data through knowledge bases
- fine-tune them using your data in S3
- expose everything to applications through a consistent API layer

### Choosing a base foundation model
Model choice depends on:
- model type
- performance requirements
- capabilities
- constraints
- compliance requirements
- level of customization needed
- model size
- inference options
- licensing terms
- context window
- latency
- multimodal support

### Amazon Titan
Amazon Titan is presented as AWS's family of high-performing foundation models.

Points mentioned:
- available for text, images, and multimodal use cases
- exposed through fully managed APIs
- can be customized with your own data
- smaller models are generally more cost-effective

### Slide example: Titan vs Llama vs Claude vs Stable Diffusion
The comparison slide includes examples such as:
- `Amazon Titan Text Express`
- `Llama-2 70b-chat`
- `Claude 2.1`
- `Stable Diffusion SDXL 1.0`

The slide compares:
- maximum context window
- features
- example use cases
- pricing

Important note: these example prices and model details can change over time.

### Fine-tuning in Bedrock
Fine-tuning means adapting a copy of a foundation model with your own data.

Main points:
- fine-tuning changes the weights of the base model
- training data must follow a required format
- training data must be stored in `Amazon S3`
- not all models support fine-tuning

### Supervised Fine-Tuning (SFT)
Purpose:
- improve performance on specific tasks or domains

How it works:
- uses labeled input-output pairs
- the model learns from examples of the desired answer

Example pattern from the slide:
- `prompt` -> `completion`

Useful clarification: SFT is best when you already know what a good answer should look like and can provide examples.

### Reinforcement Fine-Tuning (RFT)
Purpose:
- improve a model using feedback-based learning

How it works:
- you provide prompts
- the model generates candidate responses
- a reward function evaluates the responses
- the model learns iteratively to favor higher-scoring outputs

Examples mentioned:
- objective evaluation can use `AWS Lambda` code
- subjective evaluation can use another model acting as a judge based on instructions

### Reinforcement Fine-Tuning example
Example use case:
- a technical customer support chatbot

Sample prompt:
- "My app is running very slowly."

The highest-scoring response in the slide is better because it:
- shows empathy
- asks diagnostic questions
- gathers information before acting
- leads to a more efficient resolution

Key idea: RFT optimizes for behavior quality based on scoring, not just imitation of fixed answers.

### SFT vs RFT
Main difference:
- `SFT` learns from provided correct outputs
- `RFT` learns from scores assigned to generated outputs

Simple rule:
- use `SFT` when you have labeled examples
- use `RFT` when you want to optimize model behavior according to a reward signal

### Distillation
Distillation transfers knowledge from a larger `teacher` model to a smaller `student` model.

Main benefits:
- smaller and faster models
- lower cost
- similar behavior to the larger model

Tradeoff:
- some loss of accuracy may occur

Distillation can be up to `75%` less expensive than the original model.

### Fine-tuning cost and operational notes
Important operational notes:
- retraining or fine-tuning a model requires significant budget
- `SFT` is usually cheaper than `RFT`
- the work requires experienced ML engineers
- you must prepare data, run fine-tuning, and evaluate the model
- running a fine-tuned model is also more expensive

Deployment options mentioned:
- run the custom model `on-demand` with price per token
- buy `provisioned throughput`, billed monthly

## Part 5 - Bedrock Evaluation, RAG, Guardrails, Agents, and Nova

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

## Part 6 - Prompt Engineering

### What prompt engineering is
A plain prompt gives limited guidance and leaves more room for the model's interpretation.

Prompt engineering is the practice of designing and optimizing prompts to improve model outputs for a specific need.

A stronger prompt usually contains:
- `Instructions`: what the model must do
- `Context`: background information that guides the answer
- `Input data`: the actual content to process
- `Output indicator`: the expected format or style of the answer

### Naive prompt vs enhanced prompt
A naive prompt might simply ask:
- `Summarize what AWS is`

An enhanced prompt is more specific about:
- audience
- scope
- tone
- output length
- excluded details

Key idea: the more clearly the task is framed, the more likely the output matches the intent.

### Negative prompting
Negative prompting explicitly tells the model what it should not include or do.

Main benefits:
- avoids unwanted content
- keeps the response focused
- improves clarity
- reduces irrelevant or overly technical output

Typical examples of negative instructions:
- do not include detailed technical configurations
- do not speculate
- do not include unrelated personal experiences

### Reminder on text generation
Text is generated probabilistically:
- the model considers possible next tokens
- each token has a probability
- one token is selected
- the process repeats until the answer is complete

This is why prompt wording matters: different wording changes the probability distribution and therefore the output.

### Prompt performance optimization
Key controls:

`System prompts`
- define how the model should behave and reply

`Temperature` (`0` to `1`)
- low temperature: more conservative, focused, repetitive output
- high temperature: more diverse, creative, and less predictable output

`Top P` (`0` to `1`)
- low `Top P`: consider only the most likely portion of candidate tokens
- high `Top P`: consider a wider range of possible tokens

`Top K`
- low `Top K`: fewer candidate tokens, usually more coherent output
- high `Top K`: more candidate tokens, usually more varied output

`Length`
- controls the maximum output length

`Stop sequences`
- tokens or strings that tell the model when to stop generating

### Prompt latency
Latency is how quickly the model responds.

Main factors affecting latency:
- model size
- model type
- number of input tokens
- number of output tokens

Important detail:
- `Top P`, `Top K`, and `Temperature` do not materially drive latency in the same way token count and model size do

### Zero-shot prompting
Zero-shot prompting means asking the model to perform a task without providing examples.

Characteristics:
- relies on the model's general knowledge
- works better with stronger, more capable models
- useful when the task is straightforward or well understood by the model

### Few-shot prompting
Few-shot prompting means giving the model a small number of examples before asking it to perform the task.

Purpose:
- guide style, structure, or reasoning
- reduce ambiguity
- improve consistency

Note:
- providing a single example is often called `one-shot` or `single-shot`

### Chain-of-thought prompting
Chain-of-thought prompting breaks a task into intermediate reasoning steps.

Benefits:
- improves structure
- can improve coherence
- is useful for tasks that naturally require multiple steps

Typical cue:
- `Think step by step`

It can be combined with:
- zero-shot prompting
- few-shot prompting

### RAG as a prompting technique
RAG can also be viewed as a prompting technique because it augments the original prompt with external information.

Effect:
- the response becomes more informed
- the answer is better grounded in relevant source material

### Prompt templates
Prompt templates standardize prompt creation.

They help:
- process user input into a structured prompt
- orchestrate interactions between the model, action groups, and knowledge bases
- format responses consistently
- reuse patterns across many requests

They can also include:
- few-shot examples

Prompt templates can be used with:
- Bedrock Agents

### Prompt injection
Prompt injection happens when a user attempts to manipulate the model by inserting malicious or conflicting instructions into the input.

Typical goal of an injection:
- override the intended prompt behavior
- force the model onto a harmful or unrelated topic
- bypass restrictions

### Protecting against prompt injection
One protection is to include explicit instructions such as:
- ignore unrelated instructions
- ignore malicious attempts to redirect the topic
- stay strictly within the original task context

Core principle:
- user input should be treated as untrusted content when it can influence the prompt structure

## Part 7 - Amazon Q

### Amazon Q Business
Amazon Q Business is a fully managed Generative AI assistant for employees.

Main characteristics:
- built around company knowledge and internal data
- can answer questions
- can provide summaries
- can generate content
- can automate tasks
- can perform routine actions such as time-off requests or meeting invites
- built on Amazon Bedrock

Important detail:
- the underlying foundation model is managed for you rather than selected manually

### Typical Amazon Q Business use cases
Examples:
- write a job posting
- create a short social media post
- summarize what was discussed in team meetings
- answer internal company questions using enterprise knowledge

### Data access in Amazon Q Business
Amazon Q Business connects to enterprise data through:

`Data connectors`
- a fully managed RAG-style integration layer
- connects to many enterprise data sources

Examples of sources:
- `Amazon S3`
- `RDS`
- `Aurora`
- `WorkDocs`
- `Microsoft 365`
- `Salesforce`
- `Google Drive`
- `Gmail`
- `Slack`
- `SharePoint`

### Plugins in Amazon Q Business
Plugins allow Amazon Q Business to interact with third-party services.

Examples:
- `Jira`
- `ServiceNow`
- `Zendesk`
- `Salesforce`

There is also support for:
- custom plugins that connect to external applications through APIs

### Identity and access control
Amazon Q Business can integrate with `IAM Identity Center`.

Main effects:
- users are authenticated before using the application
- users only receive answers based on documents they are allowed to access
- IAM Identity Center can integrate with external identity providers

Examples of identity providers:
- Google
- Microsoft Active Directory

Key idea: Q Business respects document-level access boundaries.

### Admin controls
Amazon Q Business includes admin controls similar to guardrails.

These controls can:
- customize responses for organizational needs
- block specific words or topics
- restrict answers to internal information only
- apply global controls
- apply topic-level controls for more granular behavior

### Amazon Q Apps
Amazon Q Apps lets users create GenAI-powered apps without coding by using natural language.

Main points:
- uses company internal data
- can leverage plugins such as Jira
- aimed at quickly building internal AI apps

### Amazon Q Developer
Amazon Q Developer is focused on AWS usage and software development.

Main capabilities:
- answer questions about AWS documentation
- help with AWS service selection
- answer questions about resources in your AWS account
- suggest CLI commands to make changes
- help analyze bills and costs
- troubleshoot errors

### Amazon Q Developer for cloud work
It can help with:
- understanding cloud infrastructure
- managing AWS resources
- understanding AWS costs

### Amazon Q Developer for coding
Amazon Q Developer also acts as an AI coding assistant.

Capabilities:
- helps build new applications
- supports languages such as Java, JavaScript, Python, TypeScript, and C#
- provides real-time code suggestions
- performs security scans
- helps implement features
- can generate documentation
- can help bootstrap new projects

### IDE extensions
Amazon Q Developer integrates with IDEs such as:
- Visual Studio Code
- Visual Studio

Typical IDE features:
- answer AWS development questions
- code completion
- code generation
- vulnerability scanning
- debugging support
- optimization suggestions

### Amazon Q for QuickSight
Amazon QuickSight is AWS's BI and dashboarding service.

Amazon Q for QuickSight can:
- understand natural-language questions about data
- generate executive summaries
- answer questions about datasets
- generate or edit visuals for dashboards

### Amazon Q for EC2
Amazon Q for EC2 helps choose appropriate EC2 instance types.

It can:
- suggest instances for a new workload
- take workload requirements in natural language
- provide guidance based on performance needs

### Amazon Q for AWS Chatbot
AWS Chatbot brings AWS interactions into tools such as Slack or Microsoft Teams.

With Amazon Q in AWS Chatbot, users can:
- troubleshoot issues
- receive alarm, security, and billing notifications
- create support requests
- ask questions about AWS services
- get remediation guidance

### Amazon Q for Glue
AWS Glue is an ETL service used to move and transform data.

Amazon Q for Glue can help with:
- answering general Glue questions
- linking to documentation
- generating data integration code
- answering questions about Glue ETL scripts
- troubleshooting Glue job errors
- providing step-by-step guidance to identify root causes

### PartyRock
PartyRock is a GenAI app-building playground powered by Amazon Bedrock.

Main points:
- lets you experiment with GenAI app creation
- works with multiple foundation models
- requires no coding
- does not require an AWS account
- has a UI similar to Amazon Q Apps, but with less setup

Practical takeaway: PartyRock is useful for fast experimentation, while Amazon Q Apps is more aligned with internal enterprise use cases.

## Part 8 - AI and Machine Learning Overview

### Artificial Intelligence
AI is a broad field focused on building intelligent systems capable of tasks that usually require human intelligence.

Core capabilities:
- perception
- reasoning
- learning
- problem solving
- decision-making

Hierarchy:
- `AI` is the broadest category
- `Machine Learning` is a subset of AI
- `Deep Learning` is a subset of ML
- `Generative AI` is a subset of Deep Learning

### Common AI use cases
- computer vision
- facial recognition
- fraud detection
- intelligent document processing

### Main AI components
An AI system can be viewed as four layers:
- `Data layer`: collect large amounts of data
- `ML framework and algorithm layer`: choose methods and frameworks for the use case
- `Model layer`: define, train, and optimize the model
- `Application layer`: expose the model to users through an application

### Machine Learning
Machine Learning is a type of AI where machines learn from data instead of following explicitly programmed rules.

Main ideas:
- data is used to improve performance on a task
- the model learns patterns from training data
- the model then makes predictions on new data

Two common outputs:
- regression
- classification

### AI is not the same as ML
Not all AI is machine learning.

Example:
- expert systems such as `MYCIN` use manually written rules instead of learning from data

Key distinction:
- `AI` includes rule-based systems
- `ML` specifically means systems that learn from data

### Deep Learning
Deep Learning uses neural networks with multiple layers to learn complex patterns in data.

Main characteristics:
- inspired by neurons and synapses
- handles more complex patterns than traditional ML
- often requires large datasets
- often requires GPUs

Typical use cases:
- computer vision
- NLP
- language generation

### Neural networks
Neural networks are made of:
- nodes
- connections between nodes
- layers: input, hidden, output

How they work at a high level:
- the network processes many examples
- it identifies patterns
- it adjusts internal connections to improve predictions

### Deep learning intuition
Different layers can learn different types of features.

Example for handwritten digits:
- early layers may detect simple shapes such as lines or curves
- deeper layers combine those patterns into a final prediction

### Generative AI
Generative AI is a subset of Deep Learning built around foundation models.

Main points:
- foundation models are pretrained on large amounts of mostly unlabeled data
- they support broad tasks
- they can be adapted or fine-tuned for specific use cases

Typical tasks:
- text generation
- summarization
- information extraction
- image generation
- chatbots
- question answering

### Transformer models
Transformers are a core architecture behind many modern LLMs.

Why they matter:
- they process a sentence as a whole instead of strictly word by word
- this makes training faster and more efficient
- they use attention mechanisms to assign importance to different words
- this improves coherence and context handling

Examples:
- `BERT`
- `ChatGPT`

### Diffusion models
Diffusion models are commonly used for image generation.

Basic idea:
- training progressively adds noise
- generation reverses that process to produce an image from noise

### Multimodal models
Multimodal models can handle multiple input and output types.

Examples of modalities:
- text
- images
- audio
- video

Example:
- input can combine text, audio, and images
- output can be text, video, or another modality mix

### Useful exam terms
- `GPT`: Generative Pre-trained Transformer
- `BERT`: Bidirectional Encoder Representations from Transformers
- `RNN`: Recurrent Neural Network, useful for sequential data
- `ResNet`: Residual Network, used in image tasks
- `SVM`: Support Vector Machine, used for classification and regression
- `WaveNet`: model for raw audio generation
- `GAN`: Generative Adversarial Network, used to generate synthetic data
- `XGBoost`: implementation of gradient boosting

### Training data
Good models require good data.

Core rule:
- garbage in, garbage out

Two major distinctions:
- labeled vs unlabeled data
- structured vs unstructured data

### Labeled vs unlabeled data
`Labeled data`
- includes inputs and correct output labels
- used mainly for supervised learning

`Unlabeled data`
- includes inputs without output labels
- used mainly for unsupervised learning

### Structured vs unstructured data
`Structured data`
- organized in rows and columns
- common forms: tabular data and time series

Examples:
- customer tables
- stock prices over time

`Unstructured data`
- does not follow a fixed table structure
- often text-heavy or multimedia

Examples:
- reviews
- articles
- images

### Supervised learning
Supervised learning learns a mapping from inputs to known outputs.

Requirements:
- needs labeled data

Main task families:
- regression
- classification

### Regression
Regression predicts a numeric value.

Characteristics:
- output is continuous

Examples:
- house price prediction
- stock price prediction
- temperature forecasting

### Classification
Classification predicts a category or label.

Characteristics:
- output is discrete

Common types:
- binary classification
- multiclass classification
- multi-label classification

Examples:
- spam detection
- animal classification
- customer retention prediction
- diagnostics

Example algorithm mentioned:
- `k-NN`

### Training, validation, and test sets
Typical dataset split:
- `Training set`: usually `60-80%`, used to train the model
- `Validation set`: usually `10-20%`, used to tune parameters
- `Test set`: usually `10-20%`, used for final evaluation

Key idea:
- do not evaluate the final model only on the same data used for training

### Feature engineering
Feature engineering means transforming raw data into more useful features.

Main techniques:
- `Feature extraction`
- `Feature selection`
- `Feature transformation`

Why it matters:
- it can significantly improve model performance
- it is especially important in supervised learning

### Feature engineering on structured data
Examples:
- create `price per square foot`
- keep the most relevant variables
- normalize values so features are on comparable scales

### Feature engineering on unstructured data
Examples:
- convert text into numerical features using `TF-IDF` or embeddings
- extract image features such as edges or textures, often using CNN-based methods

### Unsupervised learning
Unsupervised learning finds patterns or structure in data without labeled outputs.

Common techniques:
- clustering
- association rule learning
- anomaly detection

Use cases:
- customer segmentation
- targeted marketing
- recommender systems

### Clustering
Clustering groups similar items together.

Example:
- customer segmentation based on purchasing behavior

Technique mentioned:
- `K-means`

Outcome:
- each cluster can be targeted differently

### Association rule learning
Association rule learning finds items that often occur together.

Example:
- market basket analysis

Technique mentioned:
- `Apriori`

Use:
- product placement
- promotions

### Anomaly detection
Anomaly detection finds unusual data points that differ from normal behavior.

Example:
- fraudulent credit card transactions

Technique mentioned:
- `Isolation Forest`

### Semi-supervised learning
Semi-supervised learning combines:
- a small amount of labeled data
- a large amount of unlabeled data

Typical pattern:
- train partially on labeled data
- generate pseudo-labels for unlabeled data
- retrain on the mixed dataset

### Self-supervised learning
Self-supervised learning creates supervision from the data itself, without human labels.

Main idea:
- the model solves pretext tasks
- this helps it learn useful representations
- the learned model is then reused for downstream tasks

Common examples:
- predicting masked text
- predicting missing or future parts of data

Important note:
- this approach is widely used for models such as `BERT` and `GPT`

### Reinforcement learning
Reinforcement learning (`RL`) is a type of ML where an agent learns by interacting with an environment to maximize cumulative reward.

Core concepts:
- `Agent`: the decision-maker
- `Environment`: the world the agent interacts with
- `State`: the current situation
- `Action`: a choice made by the agent
- `Reward`: feedback after the action
- `Policy`: the strategy for choosing actions

### How reinforcement learning works
Basic loop:
- observe the current state
- choose an action
- receive a reward
- move to a new state
- update the policy

Goal:
- maximize long-term total reward

### Reinforcement learning example
Example:
- a robot learning to navigate a maze

Reward design shown:
- small penalty for each step
- larger penalty for hitting a wall
- large reward for reaching the exit

Result:
- the agent gradually learns more efficient behavior

### Reinforcement learning applications
- gaming
- robotics
- finance
- healthcare
- autonomous vehicles

### RLHF
`RLHF` stands for `Reinforcement Learning from Human Feedback`.

Purpose:
- use human preferences to guide model behavior
- align model outputs more closely with human goals

Why it matters:
- a response can be technically correct but still worse than a more helpful or more natural response

### How RLHF works
Typical process:
- collect human-written prompts and responses
- fine-tune a model on that data
- have the model generate candidate responses
- gather human preferences between responses
- train a separate reward model from those preferences
- use that reward model inside reinforcement learning to optimize the original model

Key idea:
- human judgment becomes part of the reward signal

## Part 9 - Model Fit, Evaluation, Inferencing, and ML Project Lifecycle

### Model fit
When model performance is poor, one of the first things to check is model fit.

Three common cases:
- `Overfitting`: performs well on training data but poorly on evaluation or unseen data
- `Underfitting`: performs poorly even on training data
- `Balanced fit`: neither overfitting nor underfitting

### Bias
Bias is the error caused by an overly simplistic or inappropriate modeling choice.

High bias usually means:
- the model does not match the training data well
- the model is too simple
- the model is underfitting

Ways to reduce bias:
- use a more complex model
- increase the number of useful features

### Variance
Variance measures how much model performance changes when trained on a different but similar dataset.

High variance usually means:
- the model is too sensitive to the training data
- the model performs well on training data but poorly on unseen data
- the model is overfitting

Ways to reduce variance:
- keep fewer but more relevant features
- repeat train/test splits and validate more carefully

### Bias-variance relationship
Useful intuition:
- high bias -> underfitting
- high variance -> overfitting
- low bias and low variance -> better balance

### Binary classification evaluation
For classification problems, one of the key tools is the `confusion matrix`.

It tracks:
- `True Positive (TP)`
- `False Positive (FP)`
- `True Negative (TN)`
- `False Negative (FN)`

### Main classification metrics
`Precision`
- `TP / (TP + FP)`
- important when false positives are costly

`Recall`
- `TP / (TP + FN)`
- important when false negatives are costly

`Accuracy`
- `(TP + TN) / (TP + TN + FP + FN)`
- more useful when classes are balanced

`F1 score`
- harmonic mean of precision and recall
- useful when you want a balance between the two, especially with imbalanced datasets

### Multiclass confusion matrices
Confusion matrices can also be used for multi-class classification, not only binary classification.

### AUC-ROC
`AUC-ROC` means `Area Under the Receiver Operating Characteristic curve`.

Main ideas:
- value ranges from `0` to `1`
- a higher value is better
- compares true positive rate against false positive rate across multiple thresholds

Why it matters:
- helps choose the threshold that best fits the business tradeoff

### Regression metrics
For regression tasks, key metrics include:
- `MAE` = Mean Absolute Error
- `MAPE` = Mean Absolute Percentage Error
- `RMSE` = Root Mean Squared Error
- `R²` = R-squared

How to interpret them:
- `MAE`, `MAPE`, and `RMSE` measure prediction error
- `R²` measures how much variance in the target is explained by the model

Quick intuition:
- lower `MAE`, `MAPE`, and `RMSE` are better
- `R²` closer to `1` is better

### Inferencing
Inferencing is when a trained model makes predictions on new data.

### Real-time vs batch inferencing
`Real-time inferencing`
- used when decisions must be made quickly
- latency matters more than perfect accuracy
- example: chatbots

`Batch inferencing`
- used on large datasets processed all at once
- often used for analysis workloads
- speed is less important than accuracy or throughput

### Inferencing at the edge
Edge inferencing runs close to where data is generated.

Typical edge-device characteristics:
- limited compute power
- very low latency
- local or offline capability

Common pattern:
- smaller models on edge devices
- larger models on remote servers

Tradeoff:
- local models are faster and more private
- remote models are usually more powerful

### Phases of an ML project
An ML project typically moves through these phases:
- business problem definition
- ML problem framing
- data collection and preparation
- feature engineering
- model training and parameter tuning
- model evaluation
- testing and deployment
- monitoring and debugging
- iteration and retraining

### Business problem and ML framing
Before building a model:
- define business goals
- define budget and success criteria
- define KPIs
- confirm that ML is actually appropriate

This step usually involves collaboration across:
- stakeholders
- data scientists
- data engineers
- ML architects
- subject-matter experts

### Data processing
Data processing includes:
- data collection
- data integration
- data preprocessing
- data visualization
- converting data into a usable format

### Exploratory Data Analysis
`EDA` helps understand the dataset before training.

Common activities:
- graphing and visualization
- checking correlations between variables
- identifying which features may matter most

### Iterative model development
Model development is iterative.

It often includes:
- additional feature engineering
- retraining
- hyperparameter tuning
- re-evaluation
- monitoring after deployment

### Deployment and monitoring
Once results are good enough, the model is deployed for inference.

Possible deployment styles mentioned:
- real-time
- serverless
- asynchronous
- batch
- on-premises

After deployment, monitoring is needed to:
- detect performance drops early
- debug issues
- understand model behavior in production

### Hyperparameters
Hyperparameters are settings defined before training begins.

Examples:
- learning rate
- batch size
- number of epochs
- regularization

Hyperparameter tuning means searching for the values that improve performance and generalization.

Common search methods:
- grid search
- random search

Managed help:
- `SageMaker Automatic Model Tuning (AMT)`

### Important hyperparameters
`Learning rate`
- controls the size of weight updates
- too high can overshoot the optimum
- too low can make training slow

`Batch size`
- number of training examples used in one update step
- smaller batches can be more stable but slower
- larger batches are faster but can be less stable

`Number of epochs`
- how many full passes the model makes over the training dataset
- too few can cause underfitting
- too many can cause overfitting

`Regularization`
- helps control model complexity
- increasing regularization can reduce overfitting

### How to reduce overfitting
Common approaches:
- increase training data size
- use early stopping
- apply data augmentation
- tune hyperparameters
- use ensembling

Main causes of overfitting:
- training data is too small or not representative
- training runs too long on the same data
- model complexity is too high and starts learning noise

### When ML is not appropriate
Machine learning is not always the right solution.

If a problem is deterministic and can be computed exactly, it is often better to write explicit code.

Example:
- if a deck has 5 red cards, 3 blue cards, and 2 yellow cards, the probability of drawing a blue card is exactly `3/10`

Key principle:
- use ML for pattern learning and uncertainty
- use regular programming when the correct answer can be computed directly and reliably

## Part 11 - EC2, AI Hardware, and Amazon SageMaker

### Amazon EC2
`EC2` stands for `Elastic Compute Cloud`.

It is an `Infrastructure as a Service` offering and a core AWS service for running virtual machines.

Main related building blocks:
- `EC2` for virtual machines
- `EBS` for attached block storage
- `ELB` for load balancing
- `ASG` for auto scaling

### EC2 sizing and configuration
Key instance choices include:
- operating system: Linux, Windows, or macOS
- CPU and compute power
- RAM
- storage type and size
- networking configuration
- public IP usage
- firewall rules through `Security Groups`
- bootstrap configuration through `EC2 User Data`

Storage options mentioned:
- `EBS` and `EFS` for network-attached storage
- `Instance Store` for hardware-attached ephemeral storage

### AWS hardware for AI
AWS provides specialized hardware for AI workloads.

`GPU-based EC2 instances`
- examples: `P3`, `P4`, `P5`, `G3` to `G6`
- used for training or inference workloads that benefit from GPUs

`AWS Trainium`
- AWS chip for deep learning training
- designed for very large models, including `100B+` parameter models
- example: `Trn1` instances
- positioned for lower training cost

`AWS Inferentia`
- AWS chip for inference
- designed for high performance and lower inference cost
- examples: `Inf1` and `Inf2`

Key idea:
- `Trainium` is for training
- `Inferentia` is for inference

### Amazon SageMaker
Amazon SageMaker is a fully managed service for building, training, deploying, and operating ML models.

Core value:
- brings the ML workflow into one managed environment
- avoids stitching together many separate tools and servers manually

### SageMaker as an end-to-end ML service
Main lifecycle covered by SageMaker:
- collect and prepare data
- build and train models
- deploy models
- monitor predictions and model quality

### SageMaker built-in algorithms
Examples mentioned:

`Supervised`
- linear regression
- classification
- `KNN`

`Unsupervised`
- `PCA` for feature reduction
- `K-means` for clustering

Other areas:
- anomaly detection
- NLP and summarization
- image classification and detection

### SageMaker Automatic Model Tuning
`AMT` automates hyperparameter tuning.

It helps by handling:
- objective metric selection
- hyperparameter search ranges
- search strategy
- maximum runtime
- early stopping conditions

Main benefit:
- saves time and reduces waste on poor configurations

### SageMaker deployment and inference
SageMaker can deploy models with:
- one-click style managed deployment
- automatic scaling
- no server management

Main inference modes:

`Real-time inference`
- one prediction at a time
- low latency
- best for interactive apps

`Serverless inference`
- good for sporadic traffic
- can tolerate cold starts
- avoids always-on infrastructure

`Asynchronous inference`
- supports payloads up to `1 GB`
- useful for longer-running jobs
- request and response can flow through `Amazon S3`

`Batch Transform`
- used for dataset-wide prediction jobs
- request and response are handled through `Amazon S3`

### Inference mode comparison
Quick decision guide:
- `Real-time`: low latency, interactive requests
- `Serverless`: low traffic, short jobs, cost-efficient when idle most of the time
- `Asynchronous`: large payloads or longer processing
- `Batch Transform`: bulk offline prediction

### SageMaker Studio
SageMaker Studio is the unified interface for end-to-end ML development.

It supports:
- team collaboration
- training and tuning
- debugging
- deployment
- automated workflows

### SageMaker Data Wrangler
Data Wrangler is used for data preparation and feature engineering.

Main capabilities:
- data import
- preview
- visualization
- transformation
- quick model exploration
- export of data flows
- SQL support
- data quality tools

It works for:
- tabular data
- image data

### ML features
Features are the input variables used by ML models in both training and inference.

Key point:
- high-quality reusable features are valuable across multiple datasets and teams

### SageMaker Feature Store
Feature Store centralizes feature management.

Main functions:
- ingest features from multiple sources
- define transformations into features
- publish from Data Wrangler into Feature Store
- make features discoverable in SageMaker Studio

### SageMaker Clarify
SageMaker Clarify focuses on evaluation, explainability, and bias analysis.

Capabilities mentioned:
- evaluate foundation models
- evaluate human factors such as friendliness or humor
- use AWS-managed reviewers or your own employees
- use built-in or custom datasets
- use built-in metrics and algorithms

### Clarify for model explainability
Clarify helps explain why a model made a prediction.

Typical goals:
- understand model behavior before deployment
- debug incorrect predictions after deployment
- improve trust in the model

Example question it helps answer:
- why was a loan application rejected?

### Clarify for bias detection
Clarify can detect and explain bias in datasets and models using statistical metrics.

Bias types mentioned:
- `Sampling bias`
- `Measurement bias`
- `Observer bias`
- `Confirmation bias`

Example:
- if a model disproportionately flags a certain ethnic group, that can indicate a sampling bias problem

### SageMaker Ground Truth
Ground Truth supports human-in-the-loop workflows.

Main uses:
- RLHF
- model review
- customization and evaluation
- data generation and annotation
- labeling datasets

Possible reviewers:
- Mechanical Turk workers
- your employees
- third-party vendors

### SageMaker ML governance
Governance-related features include:
- `Model Cards`
- `Model Dashboard`
- `Role Manager`

Purpose:
- document models
- centralize visibility
- manage role-based access for personas such as data scientists and MLOps engineers

### SageMaker Model Dashboard
Model Dashboard is a centralized portal to search and inspect models.

It helps track:
- deployed models
- threshold violations
- data quality
- model quality
- bias
- explainability

### SageMaker Model Monitor
Model Monitor tracks production model quality over time.

Main purpose:
- detect drift or quality degradation
- alert when performance deviates
- trigger investigation and retraining

### SageMaker Model Registry
Model Registry is the centralized repository for model versioning and management.

It supports:
- cataloging models
- tracking versions
- storing metadata
- managing approval status
- automating deployment workflows
- sharing models

### SageMaker Pipelines
SageMaker Pipelines is the CI/CD workflow service for machine learning.

Main value:
- automate build, train, test, and deploy steps
- reduce manual errors
- make workflows repeatable

Supported step types mentioned:
- `Processing`
- `Training`
- `Tuning`
- `AutoML`
- `Model`
- `ClarifyCheck`
- `QualityCheck`

### SageMaker JumpStart
JumpStart is an ML hub for:
- pre-trained foundation models
- computer vision models
- NLP models
- prebuilt ML solutions

Examples of model sources:
- Hugging Face
- Databricks
- Meta
- Stability AI

Main capabilities:
- browse models
- experiment before deployment
- customize models with your own dataset
- deploy directly on SageMaker

There is also a solution-template path for common business use cases such as:
- demand forecasting
- credit risk prediction
- fraud detection
- computer vision

### SageMaker Canvas
SageMaker Canvas is the no-code visual interface for ML.

It can:
- build models without coding
- access ready-to-use models from Bedrock or JumpStart
- build custom models using `AutoML` through SageMaker Autopilot
- leverage Data Wrangler for data prep

Ready-to-use model integrations mentioned:
- Rekognition
- Comprehend
- Textract

### MLflow on SageMaker
`MLflow` is an open-source tool for managing the ML lifecycle.

On SageMaker it can be used for:
- tracking runs
- managing experiments
- launching tracking servers with SageMaker integration

### SageMaker summary map
Useful mental map:
- `SageMaker`: end-to-end ML platform
- `AMT`: hyperparameter tuning
- `Deployment & Inference`: serving models
- `Studio`: unified UI
- `Data Wrangler`: data prep
- `Feature Store`: reusable features
- `Clarify`: explainability and bias
- `Ground Truth`: labeling and RLHF
- `Model Cards / Dashboard / Registry / Monitor`: governance and lifecycle control
- `Pipelines`: ML CI/CD
- `JumpStart`: model hub and solution templates
- `Canvas`: no-code ML

### Extra SageMaker features
`Network isolation mode`
- SageMaker job containers run without outbound internet access
- they cannot even access `Amazon S3`

`DeepAR`
- forecasting algorithm for time-series data
- based on recurrent neural networks (`RNNs`)

## Part 10 - AWS Managed AI Services

### Why use AWS managed AI services
AWS managed AI services are pre-trained ML services designed for common use cases.

Main benefits:
- fully managed experience
- strong responsiveness and availability
- redundancy across Availability Zones and regions
- specialized hardware behind the service when needed
- pay-for-usage pricing
- provisioned throughput for predictable workloads

### Main service categories
- text and documents
- speech
- vision
- search
- chatbots
- recommendations
- human review
- healthcare AI

### Amazon Comprehend
Amazon Comprehend is a fully managed, serverless NLP service.

It can:
- detect language
- extract key phrases
- extract entities such as people, places, brands, and events
- analyze sentiment
- use tokenization and parts of speech internally
- organize text collections by topic

Typical use cases:
- analyzing customer interactions
- grouping articles by discovered topics

### Comprehend custom classification
Custom classification lets you define your own document categories.

Example:
- classify customer emails by request type

Supported document types include:
- text
- PDF
- Word documents
- images

Analysis modes:
- real-time synchronous analysis for single documents
- asynchronous batch analysis for multiple documents

### Named Entity Recognition
`NER` extracts common predefined entity types from text.

Examples:
- people
- places
- organizations
- dates

### Comprehend custom entity recognition
Custom entity recognition extracts business-specific entities.

Examples:
- policy numbers
- escalation phrases
- domain-specific terms

It requires:
- custom training data
- documents annotated with the target entities

It supports:
- real-time analysis
- asynchronous analysis

### Amazon Translate
Amazon Translate provides natural language translation.

Typical use:
- localizing websites and applications
- translating large volumes of text efficiently

### Amazon Transcribe
Amazon Transcribe converts speech to text using automatic speech recognition (`ASR`).

Main capabilities:
- speech-to-text transcription
- `PII` redaction
- automatic language identification for multilingual audio

Typical use cases:
- customer service call transcription
- subtitling and closed captioning
- media archive indexing

### Improving transcription accuracy
Two main tools improve accuracy:

`Custom vocabularies`
- add specific words or phrases
- useful for brand names, acronyms, jargon, and technical terms

`Custom language models`
- train on domain-specific text
- useful when context matters across large amounts of specialized speech

Best result:
- use both together when needed

### Toxicity detection in Transcribe
Transcribe also includes toxicity detection for voice interactions.

It uses:
- speech cues such as tone and pitch
- text cues from the transcript

Examples of categories:
- sexual harassment
- hate speech
- threats
- abuse
- profanity
- insults

### Amazon Polly
Amazon Polly converts text into lifelike speech.

Typical use:
- applications that need spoken output

### Polly advanced features
`Lexicons`
- define how specific text should be pronounced

`SSML`
- Speech Synthesis Markup Language
- controls pauses, pronunciation, and speaking style

`Voice engines`
- different synthesis engine types are available, such as standard, neural, generative, and long-form options

`Speech marks`
- mark where words or sentences begin and end in audio
- useful for lip sync or highlighting spoken words

### Amazon Rekognition
Amazon Rekognition analyzes images and videos.

It can detect:
- objects
- people
- text
- scenes
- faces

Common use cases:
- labeling
- content moderation
- text detection
- face detection and analysis
- face search and verification
- celebrity recognition
- pathing and movement analysis

### Rekognition custom labels
Custom Labels lets you train Rekognition for your own visual categories.

Examples:
- detect your company logo
- identify your own products on shelves

Important note:
- only a few hundred labeled images or fewer may be enough to start

### Rekognition content moderation
Content moderation detects inappropriate or offensive images.

Typical use:
- filtering harmful content in social media, advertising, or media pipelines

Key point:
- human review can be reduced to a small fraction of total volume
- it integrates with `Amazon A2I` for human review when needed

### Custom moderation adaptors
Custom moderation adaptors extend moderation with your own labeled image set.

Use them when:
- default moderation is not enough
- your policy requires domain-specific moderation rules

### Amazon Lex
Amazon Lex is used to build voice and text chatbots.

Main features:
- intent recognition
- slot collection for required parameters
- multilingual support
- integration with `AWS Lambda`, `Amazon Connect`, `Comprehend`, and `Kendra`

Typical use cases:
- ordering systems
- booking systems

### Amazon Personalize
Amazon Personalize is a fully managed recommendation service.

Typical uses:
- product recommendations
- re-ranking
- personalized marketing

Main benefits:
- real-time personalization
- integration into websites, apps, SMS, and email systems
- faster implementation without building recommendation models from scratch

### Personalize recipes
Recipes are prebuilt algorithms for specific recommendation tasks.

Examples:
- `USER_PERSONALIZATION`
- `PERSONALIZED_RANKING`
- `POPULAR_ITEMS`
- `RELATED_ITEMS`
- `PERSONALIZED_ACTIONS`
- `USER_SEGMENTATION`

Key idea:
- recipes are tuned for recommendation-style use cases

### Amazon Textract
Amazon Textract extracts text, handwriting, forms, and table data from scanned documents.

It is useful for:
- PDFs
- images
- forms
- tables

Typical industries:
- financial services
- healthcare
- public sector

### Amazon Kendra
Amazon Kendra is a fully managed ML-powered document search service.

Main capabilities:
- natural language search
- answer extraction from documents
- learning from user interaction and feedback
- manual tuning of result importance and freshness

Supported content can include:
- text
- PDF
- HTML
- PowerPoint
- Word documents
- FAQs

### Amazon Mechanical Turk
Amazon Mechanical Turk is a crowdsourcing marketplace for simple human tasks.

Typical use:
- large-scale data labeling
- data collection
- business process tasks

Example:
- distribute image-labeling work across a human workforce

### Amazon Augmented AI (A2I)
Amazon A2I adds human review to ML predictions in production.

Main pattern:
- high-confidence predictions return automatically
- low-confidence predictions are routed for human review
- reviewed results can be stored and reused to improve future training

Human reviewers can be:
- your employees
- AWS contractors
- Mechanical Turk workers

Important point:
- the ML model can be built on AWS or elsewhere

### Amazon Transcribe Medical
Amazon Transcribe Medical converts medical speech to text.

Main points:
- HIPAA compliant / HIPAA eligible use case support
- recognizes medical terminology
- supports real-time and batch transcription

Typical use cases:
- physician dictation
- drug safety and side-effect call transcription

### Amazon Comprehend Medical
Amazon Comprehend Medical extracts useful information from unstructured clinical text.

Examples of input:
- physician notes
- discharge summaries
- test results
- case notes

Capabilities:
- NLP over clinical text
- `PHI` detection through the `DetectPHI` API
- integration with `Amazon S3`
- streaming-style analysis through `Kinesis Data Firehose`
- can work together with `Amazon Transcribe`

### AWS HealthScribe
AWS HealthScribe is a HIPAA-eligible service for generating clinical notes from patient-clinician conversations.

Main capabilities:
- rich transcripts
- speaker role identification
- dialogue classification
- medical term extraction
- clinical note generation

Typical benefits:
- reduced documentation time
- AI-generated visit summaries
- better patient visit recap

## Part 12 - Responsible AI, Security, Compliance, and Governance

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

## Part 13 - AWS Security Services and Supporting AWS Basics

### IAM
`IAM` stands for `Identity and Access Management`.

Key points:
- global AWS service
- the root account exists by default and should not be used for daily work
- users represent people
- groups contain users
- a user can belong to multiple groups

### IAM permissions
Permissions are defined through JSON policies attached to:
- users
- groups
- roles

Core principle:
- apply least privilege
- grant only the permissions that are actually needed

### IAM policy structure
Important policy elements:
- `Version`
- `Id` (optional)
- `Statement`

Inside each statement:
- `Sid` (optional)
- `Effect`: `Allow` or `Deny`
- `Principal`
- `Action`
- `Resource`
- `Condition` (optional)

### IAM roles
IAM roles are used when AWS services need to act on your behalf.

Common examples:
- EC2 instance roles
- Lambda execution roles
- CloudFormation roles

### Amazon S3
Amazon S3 is a core AWS storage service used by many AWS services and applications.

Common use cases:
- backup and storage
- disaster recovery
- archive
- hybrid cloud storage
- application and media hosting
- data lakes and analytics
- software delivery
- static websites

### S3 buckets
S3 stores objects inside `buckets`.

Important points:
- buckets are created in a region
- bucket names must be globally unique

Naming constraints highlighted:
- no uppercase letters
- no underscores
- must not look like an IP address
- must start with a lowercase letter or number

### S3 objects
Objects are files stored in a bucket.

Important concepts:
- each object has a `key`
- the key is the full path-like identifier
- folders are only a UI abstraction; S3 is really key-based

Object details:
- object body contains the data
- maximum object size is `50 TB`
- uploads larger than `5 GB` should use multipart upload
- objects can have metadata
- objects can have tags
- objects can have version IDs if versioning is enabled

### S3 storage classes
Main storage classes:
- `S3 Standard`
- `S3 Intelligent-Tiering`
- `S3 Standard-IA`
- `S3 One Zone-IA`
- `S3 Glacier Instant Retrieval`
- `S3 Glacier Flexible Retrieval`
- `S3 Glacier Deep Archive`

Objects can move between classes manually or through lifecycle rules.

### S3 durability vs availability
`Durability`
- probability that data remains intact over time
- S3 is designed for `11 nines` durability across storage classes

`Availability`
- how often the service is accessible
- varies by storage class

Key distinction:
- durability is about not losing data
- availability is about being able to access it right now

### S3 Standard
Use when data is accessed frequently.

Characteristics:
- low latency
- high throughput
- `99.99%` availability

### Infrequent access classes
`S3 Standard-IA`
- lower cost than Standard
- for less frequent access with fast retrieval
- useful for backups and disaster recovery

`S3 One Zone-IA`
- lower cost
- stored in a single AZ
- data can be lost if that AZ is destroyed
- useful for data that can be recreated

### Glacier classes
Use Glacier classes for archive and backup workloads.

Options:
- `Glacier Instant Retrieval`
- `Glacier Flexible Retrieval`
- `Glacier Deep Archive`

Main tradeoff:
- lower storage cost
- retrieval time and retrieval charges become more important

### S3 Intelligent-Tiering
Intelligent-Tiering automatically moves objects between tiers based on access patterns.

Key points:
- includes a small monitoring fee
- avoids manual class selection
- no retrieval charges inside Intelligent-Tiering

### EC2 recap
The final section briefly repeats EC2 basics already covered earlier:
- virtual machines
- attached storage
- load balancing
- auto scaling
- user data bootstrap scripts

Useful additional reminder:
- `EC2 User Data` runs at first instance start and is commonly used for software install and boot-time setup

### AWS Lambda
AWS Lambda is AWS's serverless function service.

Main advantages compared with EC2:
- no server management
- runs on demand
- automatic scaling
- pay per request and compute time

Main limitations:
- designed for short-lived execution
- constrained by execution limits and configured memory

### Lambda benefits
- event-driven execution
- broad integration with AWS services
- easy monitoring through CloudWatch
- multiple language runtimes
- memory can scale up to `10 GB`

### Lambda language support
Examples:
- Node.js
- Python
- Java
- C# / PowerShell
- Ruby
- custom runtimes
- container images that implement the Lambda Runtime API

### Lambda use cases
Examples shown:
- thumbnail generation after an image is uploaded to S3
- scheduled jobs triggered by EventBridge / CloudWatch Events

### Lambda pricing
Pricing is mainly based on:
- request count
- execution duration in GB-seconds

Key idea:
- Lambda is often inexpensive for event-driven workloads

### Amazon Macie
Amazon Macie is a managed data security and privacy service.

Main use:
- discover sensitive data in S3
- especially `PII`

### AWS Config
AWS Config records resource configurations and tracks changes over time.

Useful for:
- compliance auditing
- answering questions such as whether resources are public or misconfigured
- storing configuration history
- generating alerts on changes

Important detail:
- Config is a per-region service, but can be aggregated across regions and accounts

### Amazon Inspector
Amazon Inspector performs automated security assessments.

It evaluates:
- EC2 instances
- container images in `ECR`
- Lambda functions

Main checks:
- package vulnerabilities
- network reachability for EC2
- software vulnerabilities in deployed functions and images

Important detail:
- findings are scored by risk for prioritization

### AWS CloudTrail
CloudTrail provides governance, compliance, and audit visibility.

It tracks API activity from:
- console
- CLI
- SDK
- AWS services

Main uses:
- audit activity history
- investigate deletions or unexpected changes
- export logs to CloudWatch Logs or S3

Important detail:
- CloudTrail is enabled by default

### AWS Artifact
AWS Artifact is a portal for compliance documentation and AWS agreements.

It is useful for:
- downloading compliance reports such as ISO, PCI, and SOC documents
- reviewing and accepting agreements
- supporting internal audits and compliance work

### AWS Audit Manager
AWS Audit Manager helps assess compliance and continuously collect audit evidence.

Capabilities:
- use prebuilt frameworks such as GDPR, HIPAA, PCI DSS, and SOC 2
- scope assessments to accounts and services
- gather evidence automatically
- generate audit-ready reports

### AWS Trusted Advisor
Trusted Advisor provides high-level recommendations for an AWS account.

Main categories:
- cost optimization
- performance
- security
- fault tolerance
- service limits
- operational excellence

### VPC basics
`VPC` means `Virtual Private Cloud`.

Key ideas:
- private network for AWS resources
- regional resource
- contains subnets

`Subnets`
- are AZ-scoped
- can be public or private

### Internet Gateway and NAT Gateway
`Internet Gateway`
- gives public subnets internet connectivity

`NAT Gateway`
- allows private-subnet resources to reach the internet outbound while remaining private

### VPC endpoints and PrivateLink
VPC endpoints allow private access to AWS services without traversing the public internet.

Key points:
- keep traffic internal to AWS
- often powered by `AWS PrivateLink`
- useful for private access to services like Bedrock or S3

Examples:
- `S3 Gateway Endpoint`
- interface endpoints for private service access

### Security-service summary
Useful mental map:
- `IAM`: identities, roles, permissions
- `S3`: storage foundation
- `Lambda`: serverless compute
- `Macie`: sensitive data discovery
- `Config`: configuration tracking and compliance
- `Inspector`: vulnerability assessment
- `CloudTrail`: API auditing
- `Artifact`: compliance documents
- `Trusted Advisor`: account recommendations
- `VPC Endpoints / PrivateLink`: private access to AWS services

### Bedrock security patterns
Important patterns for Bedrock:
- use `IAM` for identity and resource-level access control
- use `Guardrails` to restrict topics and filter harmful content
- use `CloudTrail` to audit Bedrock API calls
- use `Config` to track configuration changes
- use `PrivateLink` / VPC endpoints to keep Bedrock access private

### Bedrock with encrypted S3 data
If Bedrock must access an encrypted S3 bucket:
- the data can be protected with `SSE-KMS`
- Bedrock needs an `IAM role`
- that role must allow access to:
  - the S3 bucket
  - the `KMS` key with decrypt permission

### SageMaker private deployment pattern
SageMaker workloads can be deployed in a VPC with:
- private subnets
- security groups
- S3 VPC endpoints
- IAM roles
- endpoint policies

This supports private access to training data and hosted endpoints.

### Bedrock private application pattern
An application inside a VPC can access Bedrock privately through:
- a Bedrock VPC endpoint
- security groups
- endpoint policies
- `PrivateLink`

### Auditing Bedrock access
CloudTrail can be used to inspect who called Bedrock APIs and whether access was allowed or denied.

This is useful for:
- auditing
- troubleshooting permissions
- investigating unexpected model access
