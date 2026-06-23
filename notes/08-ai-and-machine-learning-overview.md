# Part 8 - AI and Machine Learning Overview

[← 07](07-amazon-q.md) | [↑ Index](../README.md) | [09 →](09-model-fit-evaluation-inferencing-and-ml-project-lifecycle.md)

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

[← 07](07-amazon-q.md) | [↑ Index](../README.md) | [09 →](09-model-fit-evaluation-inferencing-and-ml-project-lifecycle.md)
