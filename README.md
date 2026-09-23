# AWS-ZERO-TO-HERO- DAY 1
# ☁️ Day 1 -- Introduction to Cloud & AWS Basics

> **AWS Learning Journey --- Day 1**
>
> Today I learned the fundamentals of Cloud Computing and AWS, including
> cloud deployment models, public/private/hybrid cloud, service models,
> AWS global infrastructure, and basic pricing models.

------------------------------------------------------------------------

## 🎯 Day 1 Learning Goals

-   Understand why development and DevOps teams use cloud computing.
-   Understand **On-Premises, Cloud, and Hybrid Cloud**.
-   Understand **Public Cloud vs Private Cloud**.
-   Understand how a **Public Cloud** works.
-   Learn about **data centers, networking, and cloud infrastructure**.
-   Understand **On-Demand** and **Pay-As-You-Go** pricing.
-   Understand **IaaS, PaaS, and SaaS**.
-   Understand AWS **Regions, Availability Zones, and Local Zones**.
-   Get a basic introduction to AWS pricing models and AWS history.

------------------------------------------------------------------------

# 1. ☁️ Why Do Developers & DevOps Engineers Need Cloud?

Cloud computing allows teams to use computing resources without
purchasing and maintaining all the physical infrastructure themselves.

### Traditional approach

A company may need to:

``` text
Buy Servers
    ↓
Build Data Center
    ↓
Install Networking
    ↓
Install Operating Systems
    ↓
Configure Applications
    ↓
Maintain Hardware
```

### Cloud approach

With cloud computing:

``` text
Choose Cloud Service
        ↓
Configure Resources
        ↓
Deploy Application
        ↓
Scale When Needed
        ↓
Pay For What You Use
```

### Key benefits

-   ⚡ **Speed** --- resources can be provisioned quickly.
-   📈 **Scalability** --- increase or decrease resources according to
    demand.
-   💰 **Cost Efficiency** --- avoid buying large amounts of hardware
    upfront.
-   🌍 **Global Reach** --- deploy applications in different geographic
    locations.
-   🔒 **Security** --- use cloud security capabilities and controls.
-   🔄 **Reliability** --- build applications across multiple
    infrastructure locations.
-   🚀 **Innovation** --- use managed services instead of building
    everything from scratch.

------------------------------------------------------------------------

# 2. 🏢 On-Premises vs ☁️ Cloud vs 🔄 Hybrid Cloud

## On-Premises

Infrastructure is owned and managed by the organization.

``` text
Company
  ↓
Own Data Center
  ↓
Own Servers
  ↓
Own Network
  ↓
Own Maintenance
```

### Example

A bank may operate some workloads in infrastructure it owns and controls
directly.

### Advantages

-   Maximum direct control over infrastructure.
-   Can be useful when specific compliance, legacy, or control
    requirements exist.

### Challenges

-   High initial hardware cost.
-   Hardware maintenance.
-   Capacity planning.
-   Scaling can take time.

------------------------------------------------------------------------

## Public Cloud

Infrastructure is operated by a cloud provider such as AWS.

``` text
User
  ↓
Internet
  ↓
AWS
  ↓
Compute / Storage / Database / Networking
```

You use cloud resources without owning the underlying physical data
center.

### Examples

-   Amazon Web Services (AWS)
-   Microsoft Azure
-   Google Cloud

------------------------------------------------------------------------

## Hybrid Cloud

A combination of on-premises infrastructure and cloud infrastructure.

``` text
On-Premises
     ↕
Secure Connection
     ↕
Public Cloud
```

### Example

A company may keep an existing database on-premises while running
application servers in AWS.

------------------------------------------------------------------------

# 3. 🌐 Public Cloud vs Private Cloud

## Public Cloud

Cloud infrastructure is provided by a cloud provider and shared among
multiple customers, with logical isolation between customers.

Examples:

-   AWS
-   Azure
-   Google Cloud

## Private Cloud

Cloud infrastructure is dedicated to a single organization.

It may be operated by the organization itself or by a service provider.

### Simple difference

  -----------------------------------------------------------------------
  Public Cloud                        Private Cloud
  ----------------------------------- -----------------------------------
  Provider-operated infrastructure    Dedicated to one organization

  Multiple customers use the          One organization has dedicated
  provider's infrastructure           infrastructure

  Highly scalable                     Greater control over dedicated
                                      environment

  Example: AWS                        Example: organization-dedicated
                                      private cloud
  -----------------------------------------------------------------------

> **Remember:** Public does not mean "everyone can see your data." Cloud
> customers have isolation and access controls.

------------------------------------------------------------------------

# 4. 🔌 How Does Public Cloud Work?

A simplified public-cloud request looks like this:

``` text
User / Developer
       ↓
    Internet
       ↓
  AWS Network
       ↓
AWS Infrastructure
       ↓
┌─────────┬──────────┬──────────┐
│ Compute │ Storage  │ Database │
└─────────┴──────────┴──────────┘
```

For example:

1.  A developer creates an EC2 instance.
2.  AWS allocates compute capacity.
3.  The developer configures the operating system and application.
4.  Users connect to the application through the network.
5.  AWS provides the underlying physical infrastructure.
6.  The customer pays according to the selected pricing model and
    resource usage.

------------------------------------------------------------------------

# 5. 🏭 Data Centers & Networking

Cloud services ultimately run on **physical infrastructure**.

A simplified view:

``` text
AWS Region
   │
   ├── Availability Zone A
   │       └── Data Centers
   │
   ├── Availability Zone B
   │       └── Data Centers
   │
   └── Availability Zone C
           └── Data Centers
```

### Data Center

A physical facility containing infrastructure such as:

-   Servers
-   Storage
-   Networking equipment
-   Power systems
-   Cooling systems
-   Security systems

### Networking

Networking allows users, applications, and cloud services to
communicate.

Common concepts you will learn later:

-   IP addresses
-   DNS
-   Routing
-   Subnets
-   Firewalls
-   Load Balancers
-   VPN
-   VPC
-   Internet connectivity

------------------------------------------------------------------------

# 6. 💳 On-Demand & Pay-As-You-Go

## On-Demand

**On-Demand** means you can provision resources when you need them
without making a long-term commitment.

Example:

``` text
Need EC2
   ↓
Launch EC2
   ↓
Use it
   ↓
Stop/terminate when no longer needed
```

## Pay-As-You-Go

You generally pay for the cloud resources you consume according to the
service's pricing rules.

Simple idea:

> **Use → Pay**

This is one reason cloud computing is useful for learning and
experimentation: you can create resources when needed and remove them
afterward.

⚠️ **Important:** Pay-as-you-go does not mean everything is
automatically free. Some AWS resources continue generating charges while
they are running or stored.

------------------------------------------------------------------------

# 7. 💰 AWS Pricing Models

AWS offers different purchasing/pricing approaches depending on the
service.

### 1. On-Demand

-   No long-term commitment.
-   Pay according to usage.
-   Useful when workloads are unpredictable or short-lived.

### 2. Reserved / Commitment-Based Pricing

-   Commit to using certain resources for a defined period.
-   Can provide lower effective pricing compared with On-Demand when the
    workload is steady.
-   Exact options depend on the AWS service.

### 3. Spot

-   Uses spare AWS compute capacity.
-   Can be significantly cheaper than On-Demand.
-   AWS can interrupt Spot workloads when capacity is needed.
-   Best for workloads designed to tolerate interruptions.

### 4. Free Tier / Free Offers

AWS provides free usage offers for selected services and usage levels.
Always check the current AWS pricing/free-tier terms before launching
resources.

------------------------------------------------------------------------

# 8. 🧱 IaaS, PaaS & SaaS

Cloud services are commonly explained using three service models.

## IaaS --- Infrastructure as a Service

You get infrastructure such as:

-   Virtual machines
-   Storage
-   Networking

### AWS example

**Amazon EC2**

You are responsible for much of the operating system and application
configuration.

``` text
AWS
 ↓
Physical Infrastructure
 ↓
Virtual Machine / EC2
 ↓
Your OS
 ↓
Your Application
```

------------------------------------------------------------------------

## PaaS --- Platform as a Service

The provider manages more of the underlying infrastructure so developers
can focus more on the application.

Typical platform capabilities can include:

-   Runtime environment
-   Managed deployment
-   Scaling
-   Infrastructure management

AWS has several managed/platform-oriented services; the exact
classification can vary depending on the service and how it is used.

------------------------------------------------------------------------

## SaaS --- Software as a Service

A complete software application is provided over the internet.

The provider manages the application and underlying infrastructure.

Examples outside AWS include:

-   Gmail
-   Microsoft 365
-   Salesforce

AWS also offers SaaS-style applications and business software services.

### Easy memory trick

``` text
IaaS → Infrastructure
PaaS → Platform
SaaS → Software
```

------------------------------------------------------------------------

# 9. 🌍 AWS Global Infrastructure

AWS infrastructure is organized geographically.

The three important concepts for Day 1 are:

``` text
Region
  ↓
Availability Zones
  ↓
Data Centers
```

And **Local Zones** extend selected AWS capabilities closer to certain
users and workloads.

------------------------------------------------------------------------

## 🌎 AWS Region

A **Region** is a geographic area where AWS has infrastructure.

Examples of Region identifiers include:

-   `us-east-1`
-   `eu-west-1`
-   `ap-south-1`

A Region contains multiple Availability Zones.

### Why do Regions matter?

You may choose a Region based on factors such as:

-   User location
-   Latency
-   Compliance requirements
-   Service availability
-   Cost
-   Disaster-recovery strategy

------------------------------------------------------------------------

## 🏢 Availability Zone (AZ)

An **Availability Zone** is an isolated location within an AWS Region.

A Region has multiple AZs designed to provide separate infrastructure
locations.

Simple structure:

``` text
AWS Region
│
├── AZ A
│    └── Data Center infrastructure
│
├── AZ B
│    └── Data Center infrastructure
│
└── AZ C
     └── Data Center infrastructure
```

### Why use multiple AZs?

If an application is designed across multiple AZs, it can improve:

-   Availability
-   Fault tolerance
-   Resilience

------------------------------------------------------------------------

## 📍 Local Zones

A **Local Zone** is an AWS infrastructure deployment that places
selected AWS resources closer to users in a particular metropolitan
area.

The goal is mainly to reduce latency for workloads that need to be
physically closer to end users.

### Easy memory trick

``` text
Region     = Large geographic area
AZ         = Isolated location inside a Region
Local Zone = AWS infrastructure closer to specific users
```

------------------------------------------------------------------------

# 10. 🧠 Day 1 Architecture Picture

``` text
                         AWS CLOUD
                            │
                     ┌──────┴──────┐
                     │   REGION    │
                     │  ap-south-1 │
                     └──────┬──────┘
                            │
             ┌──────────────┼──────────────┐
             │              │              │
          AZ - A         AZ - B         AZ - C
             │              │              │
          Data Center    Data Center    Data Center
             │
          Compute
          Storage
          Database
             │
             └──────────────┐
                            │
                       AWS Network
                            │
                         Internet
                            │
                           Users
```

------------------------------------------------------------------------

# 11. 📝 Day 1 Quick Revision

### Cloud

> Using computing resources over a network instead of owning all the
> physical infrastructure yourself.

### On-Premises

> Organization owns/manages its infrastructure.

### Public Cloud

> Cloud infrastructure provided by a cloud provider such as AWS.

### Private Cloud

> Cloud environment dedicated to one organization.

### Hybrid Cloud

> Combination of on-premises and cloud infrastructure.

### IaaS

> Infrastructure such as compute, storage, and networking.

### PaaS

> Managed platform capabilities that let developers focus more on
> applications.

### SaaS

> Complete software delivered as a service.

### On-Demand

> Provision resources when needed without a long-term commitment.

### Pay-As-You-Go

> Pay according to the applicable usage/pricing model.

### Region

> Geographic AWS infrastructure area.

### Availability Zone

> Isolated infrastructure location within a Region.

### Local Zone

> AWS infrastructure placed closer to users in selected metropolitan
> areas.

------------------------------------------------------------------------

# 🎯 Day 1 Takeaway

The main idea I learned today is:

> **Cloud computing lets developers and DevOps teams consume
> infrastructure and services on demand instead of managing all physical
> infrastructure themselves.**

AWS provides global infrastructure where applications can use:

``` text
Compute
   +
Storage
   +
Database
   +
Networking
   +
Managed Services
```

The important concepts I learned on Day 1 are:

**Cloud → On-Premises → Hybrid → Public/Private Cloud → IaaS/PaaS/SaaS →
Data Centers → Networking → Pricing → Regions → Availability Zones →
Local Zones**

------------------------------------------------------------------------

## 📚 Learning Source

This Day 1 study is based on the **AWS Zero to Hero / 7 Days of AWS
Challenge by TrainWithShubham**, combined with my own notes and
understanding.

### Day 1 Topics

-   AWS Pricing Models
-   On-Premises vs Cloud vs Hybrid
-   Public vs Private Cloud
-   IaaS, PaaS, SaaS
-   AWS History & Milestones
-   AWS Global Infrastructure
-   Regions
-   Availability Zones
-   Local Zones
-   Cloud Networking
-   On-Demand & Pay-As-You-Go

------------------------------------------------------------------------

## 🚀 Next Step

**Day 1 complete ✅**

Next, I will continue the AWS learning journey and gradually move from
**AWS fundamentals → core AWS services → hands-on labs → Cloud/DevOps
projects**.

------------------------------------------------------------------------

#7DaysOfAWS #AWSwithTWS #AWS #CloudComputing #DevOps #CloudEngineer
