# Part 13 - AWS Security Services and Supporting AWS Basics

[← 12](12-responsible-ai-security-compliance-and-governance.md) | [↑ Index](../README.md) | [Index →](../README.md)

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

[← 12](12-responsible-ai-security-compliance-and-governance.md) | [↑ Index](../README.md) | [Index →](../README.md)
