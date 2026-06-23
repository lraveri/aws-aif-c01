# Part 10 - AWS Managed AI Services

[← 09](09-model-fit-evaluation-inferencing-and-ml-project-lifecycle.md) | [↑ Index](../README.md) | [11 →](11-ec2-ai-hardware-and-amazon-sagemaker.md)

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

[← 09](09-model-fit-evaluation-inferencing-and-ml-project-lifecycle.md) | [↑ Index](../README.md) | [11 →](11-ec2-ai-hardware-and-amazon-sagemaker.md)
