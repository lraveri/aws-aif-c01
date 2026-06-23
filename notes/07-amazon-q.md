# Part 7 - Amazon Q

[← 06](06-prompt-engineering.md) | [↑ Index](../README.md) | [08 →](08-ai-and-machine-learning-overview.md)

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

[← 06](06-prompt-engineering.md) | [↑ Index](../README.md) | [08 →](08-ai-and-machine-learning-overview.md)
