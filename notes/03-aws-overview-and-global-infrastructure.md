# Part 3 - AWS Overview and Global Infrastructure

[← 02](02-aws-and-cloud-computing-basics.md) | [↑ Index](../README.md) | [04 →](04-generative-ai-and-amazon-bedrock-fundamentals.md)

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

[← 02](02-aws-and-cloud-computing-basics.md) | [↑ Index](../README.md) | [04 →](04-generative-ai-and-amazon-bedrock-fundamentals.md)
