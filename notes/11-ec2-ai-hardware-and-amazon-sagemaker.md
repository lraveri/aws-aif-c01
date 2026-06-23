# Part 11 - EC2, AI Hardware, and Amazon SageMaker

[← 10](10-aws-managed-ai-services.md) | [↑ Index](../README.md) | [12 →](12-responsible-ai-security-compliance-and-governance.md)

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

[← 10](10-aws-managed-ai-services.md) | [↑ Index](../README.md) | [12 →](12-responsible-ai-security-compliance-and-governance.md)
