# Part 2 - AWS and Cloud Computing Basics

[← 01](01-introduction-to-ai.md) | [↑ Index](../README.md) | [03 →](03-aws-overview-and-global-infrastructure.md)

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

[← 01](01-introduction-to-ai.md) | [↑ Index](../README.md) | [03 →](03-aws-overview-and-global-infrastructure.md)
