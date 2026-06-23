# Part 4 - Generative AI and Amazon Bedrock Fundamentals

[← 03](03-aws-overview-and-global-infrastructure.md) | [↑ Index](../README.md) | [05 →](05-bedrock-evaluation-rag-guardrails-agents-and-nova.md)

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

[← 03](03-aws-overview-and-global-infrastructure.md) | [↑ Index](../README.md) | [05 →](05-bedrock-evaluation-rag-guardrails-agents-and-nova.md)
