# Exam Outline 

Cloud Concepts
    
    Define the AWS Cloud and its value proposition 
    Identify aspects of AWS Cloud economies 
    List the different cloud architecture design principles

Security 
    
    Define the AWS Shared Responsibility model 
    Define AWS CLoud security and compliance concepts
    Identify AWS access management capabilities 
    Identify resource for security support 

Technology 
    
    Define methods of deploying and operating in the AWS Cloud 
    Define the AWS global infrastructure 
    Identify the core AWS services
    Identify resources for technology support

Billing and Pricing 
    
    Compare and contrast the various pricing models for AWS
    Recognise the various structures in relation to AWS billing and pricing
    Identify resources available for billing 
    
Questions are multiple choice
1 out of 4 or 
2 out of 5 or 
3 out of 6

# Cloud Computing 

Someone owns the servers, you rent them - you are responsible for your configuring the cloud services and code 

Benefits 
    
    1. Trade capital expense for variable expense 
        no Upfront-cost Instead of paying for data centers and server 
        Pay On-Demand Pay only when you consume computing resource 
    
    2. Benefit from massive economies of scale 
        Usage from hundreds of thousands of customers aggregated in the cloud 
        You are sharing the cost with other customers to get unbeatable saving
    
    3. Stop guessing capacity 
        Eliminate guesswork about about infrastructure capacity needs. Instead of paying for idle or underutilized servers, you can scale up or down to meet the current need
    
    4. Increase speed and agility 
        Launch resources within a few clicks in minutes instead of waiting days or weeks of your IT to implement the solution on-premise
    
    5. Stop spending money on running and maintaining data centers 
        Focus on your own customers, rather than on the heavy lifting of racking, stacking and powering servers
    
    6. Go global in minutes 
        Deploy your app in multiple regions around the world with a few clicks. 
        Provide lower latency and better experience for your customers at minial cost


Types of Cloud Computing 

    SaaS - Software as a Service - For Customers 
        A completed product that is run and managed by the service provide
    
    PaaS - Platform as a Service - For Developers
        Removes the need for your organisation to manage the underlying infrastructure. Focus on the deployment and management of your applications
    
    IaaS - Infrastructure as a Service - For Admins
        The basic building blocks for cloud IT. Provides access to networking features, computers and data storage space
    

Cloud Computing Deployment Models 

    Cloud - Fully utilizing cloud computing
        Startups
        SaaS offerings 
        New projects and companies

    Hybrid - Using both Cloud and on-premise
        Banks
        FinTech, Investment Management
        Large Professional Service providers
        Legacy on-premise
        
    On-Premise - Deploying resources on-premise, using virtualization and resource management tools, is sometimes called "private cloud"
        Public Sector
        Sensitive Data
        Large Enterprise with heavy regulation 


# AWS Global Infrastructure

69 Availability zones withing 22 Geographical regions around the world - More Edge location than AZ's
    
    Regions - Physical locations in the world with multiple Availability Zones
        A geographically distinct location which has multiple datacenters
        Every Region is physically isolated from and independent of every other region in terms of location, power, water 
        Each Region has two AZ's - Largest is US-EAST - new services become available first here - not all services are available in all regions - US-EAST-1 is where you see all your billing information 
    
    Availability Zones one or more discrete data centers
        An AZ is a datacenter owned and operated by AWS in which AWS services run - Each region has at least 2 AZs
        AZs are represented by a Region Code, followed by a letter identifier - US-EAST-1a
        Multi-AZ Distributing your instances accross multiple AZs allows failover configuration for handling requests when one goes down 
        <10ms latency between AZs
    
    Edge Locations - datacenter owned by a trusted partner of AWS 
        An Edge Location is a datacenter owned by a trusted partner of AWS which has a direct connection to the AWS network
        These locations serve requests for CloudFront and Route53. Requests going to either of these services will be routed to the nearest edge location automaticlly 
        SC Transfer Acceleration traffic and API Gateway endpoint traffic also use AWS Edge Network
        This allows for low latency no matter where the end user is geographically located 

GovCloud(US)

AWS GovCloud Regions allows customers to host sensitive Controlled Unclassified Information and other types of regulated workloads
Gov cloud Regions are only operated by employees who are US.citizens, on US soil
They are only accessible to US entities and root account holders who pass a screening process
Customers can architect secure cloud solutions that comply with 
    FedRAMP High Baseline
    DOJ Criminal Justice Information System Security Policy
    US International Traffic in Arms Regulation
    Export Administration Regulation
    DOD Cloud Computing Security Requirements 


# Billing Preferences 

Go to account - my billing dashboard - go to left-hand side and click on billing preferences - turn on all of them 

To create a budget alarm -> Go to search bar and type budget and click on AWS budget - click on create budget  - click cost budget - set name, period, date, amount - click next - configure the alert - add email 

To set an usage alarm -> Search and click on Cloudwatch - go to the lefthand side and click billing - click create alarm - click metrics and select billing - then add the conditions you want click next - Set the alarm trigger, and create new SNS topic and fill in the details, click next - then add a name and description for the alarm and finish 



# Change IAM Users Sign-in Link 

Go to IAM in search bar - to change the link click customize and chance to suit your preference 

# Create individual IAM users 

Look on the left hand side and open Users - click add user - add user name and access type - set a password for user or require them to set one when they log in - click next then create a group - call it admin - give it administrator access then click nxt - add tags to it if you want -review and create user 

# Auto Scaling 

When Demand is high, it spins up more VMs, when demand is low it powers down the excess VMs

# Elastic load balancer 

Allow you to put a load balancer in front of your instances - traffic flows through the load balancer - will evenly distribute the traffic to multiple instances - if once instance is down, traffic will go to the other instance

Two types - Application load balancer - Network Load Balancer 

# Simple Storage Service S3

S3 is global, not limited to Region - buckets you create are region specific - bucket is a place to contain your files 

# Cloud Front 

Used as a CND(Content Delivery Network) - used to facilitate the shortest route to the user - takes your static content and copies it to multiple edge locations around the world - when someones want to access your content, it will go to the nearest edge location 

# RDS - Relational Database Service 

# Lambda 

Don't have to worry about the servers, you just need to write code - only runs for a small amount of time 50ms 
lambda can be trigger from a variety of different services - you can add a trigger so that the lambda can run 


# Pricing Models 

Four Models:
    
On-Demand - Least Commitment
    
    low cost and flexible
    only pay per hour
    short-term, spiky, unpredictable workloads
    cannot be interrupted
    For first time apps 
    
    When you launch an EC2 instance ot os by default using On-Demand Pricing
    On-demand has no upfront payment and no long term commitment 
    You are charged by the hour or by the minute - varies based on EC2 Instance Types
    On-Demand is for applications where the workload is for short-term, spiky or unpredictable 
    When you have a new app for development or you want to run experiment 
    
        
Reserved Instances - RI- up to 75% off - Best Long-term 
    
    Steady state or predictable usage
    commit to EC2 over a 1 or 3 year term 
    Can resell unused reserved instances

    Designed for applications that have a steady-state, predictable usage, or require reserved capacity
    Reduced Pricing is based on Term x Class Offering x Payment Option 

    Standard - Up to 75% reduced pricing compared to on-demand - Cannot change RI Attributes
    
    Convertible - Up to 54% reduced pricing compared to on-demand - Allows you to change RI Attributes if grater or equal in value
    
    Scheduled - You reserved instances for specific time periods - once a week for a few hours - Saving will vary 
    
    Terms - You commit to a 1 Year or 3 Year contract - the longer the term the greater the savings
    
    Payment Options - AllUpfront, Partial Upfront and No Upfront - The greater upfront the greater the savings 

    RIs can be shared between multiple accounts within an org
    Unused RI can be sold in the Reserved Instance Marketplace 


Spot - up to 90% off - Biggest Savings
    
    Request spare computing capacity 
    flexible start and end times
    Can handle interruptions - server randomly stopping and starting
    For non-critical background jobs

    AWS has unused compute capacity that they want to maximize the utility of their idle servers 
    Spot instances provide a discount of 90% compared to On-Demand Pricing
    Spot Instances can be terminated if the computing capacity is needed by on-demand customers
    
    Designed for applications that have flexible start and end times or applications that are only feasible at very low compute costs
    
    AWS Batch is an easy and convenient way to use Spot Pricing
        Termination Conditions - Instances can be terminated by AWS at anytime
        If your instance is terminated by AWS, you don't get charged for a partial hour of usage
        If you terminate an instance you will still be charged for any hour that it ran 


Dedicated - Most Expensive
    
    Dedicated servers
    Can be on-demand or reserved - up to 70% off
    When you need a guarantee of isolate hardware - enterprise requirements 

    Designed to meet regulatory requirements. When you have strict server-bound licensing that won't support multi-tenancy or cloud deployments#
    
    Multi-Tenant
        When multiple customers are running workloads on the same hardware. Virtual Isolation is what separate customers
    Single Tenant
        When a single customer has dedicated hardware. Physical Isolation is what separates customers 
    
    Offered in both On-demand - 70% off on-demand pricing - and Reserved 
    Enterprises and Large Organizations may have security concerns or obligations about against sharing thae same hardware with other AWS Customers


# Billing and Pricing 

Certain services are free themselves, but the resource they setup will cost you 
    Auto-Scaling - CloudFormation - Elastic beanstalk - Opsworks - Amplify - AppSync - CodeStar

# AWS Support Plans 

Basic 

    - Email Support only 
    - For Billing and Account 
    - 7 Trusted Advisor Checks 
    - $0 a month 

Developer 

    - Tech Support via Email - 24hrs until reply 
    - no third party support 
    - General Guidance <24hrs 
    - system impaired <12hrs 
    - 7 Trusted Advisor checks 
    - $20 a month 

Business 

    - Tech Support via Chat, Phone 24/7 
    - General Guidance <24hrs 
    - System impaired <12hrs 
    - Production System Impaired <4hrs 
    - Production System Down <1hrs 
    - no limit on Trusted Advisor checks 
    - $100 a month

Enterprise 

    - Tech Support via Chat, Phone 24/7 
    - General Guidance <24hrs 
    - System impaired <12hrs 
    - Production System Impaired <4hrs 
    - Production System Down <1hrs 
    - Business Critical System Down <15 mins 
    - Personal Concierge 
    - TAM  
    - no limit on Trusted Advisor checks 
    - $15000 a month

# Create a support case 

# AWS Market place

AWS Marketplace is a curated digital catalogue with thousands of software filing from independent software vendors
Easily find, buy, test and deploy software that already runs on AWS
The product can be free or can have an associated charge. The charge becomes part of your AWS bill, and once you pay, AWS Marketplace pays the provider
The sale channel for ISVs and Consulting Partners allows you to sell your solutions to other AWS customer 

Products that are sold
    
    AMIs
    AWS CloudFormation templates
    SaaS offerings
    Web ACL
    AWS WAF rules 

# AWS Trusted Advisor 

Advises you on security, saving money , performance, service limits and fault tolerance - Automated checklist of best practices on AWS 

Advisor check on 
    
    Cost optimization 
        Idle Load Balancers
        Unassociated Elastic IP Addresses
        
    Performance
        High Utilization of EC2 Instances 
    
    Security 
        MFA on Root Account
        IAM Access Key rotation 

    Fault Tolerance
        RDS Backups
    
    Service Limits
        VPC

# Consolidated Billing 

One Bill for all your accounts
Consolidate your billing and payment methods across multiple AWS accounts into one bill
For billing AWS treats all the accounts in an organization as if the were one account
You can designate one master account that pays the charges of all the other member accounts
Consolidated billing is offered at no additional cost
Use Cost Explorer to visualize usage for consolidated billing 

# Volume Discounts 

AWS has Volume Discounts for many services 
The more you use, the more you save 
Consolidating Billing lets you take advantage of Volume Discounts

# AWS Cost Explorer 

AWS Cost Explorer lets you visualize, understand and manage your AWS costs and usage over time.
If you are have AWS accounts within an AWS Organization costs will be consolidated in the master account
Default reports help you gain insight into your cost drivers and usage trends
Use forecasting to get an idea of future costs 
Can view the data at a monthly or daily level of granularity 
Use filter and grouping functionalities to dig even deeper into your data

# AWS Budgets

Plan your service usage, service costs and Instance reservations - setup alerts if you exceed or are approaching your defined budget
Create cost, usage or revelations budgets 
Can be tracked at the monthly, quarterly, or yearly levels, with customizable start and end dates
Alerts support EC2, RDS, Redshift, and ElastiCache reservation
Budget based on a fixed cost or plan your upfront based on your chosen level 
Can be easily managed from the Budget Dashboard or via the Budgets API
Get notified by providing an email or Chatbot and threshold how close to the current or forecasted budget

# TCO Calculator 

The total Cost of Ownership allows you to estimate how much you would save when moving to AWS from on-premise
Provides you a detailed set of reports that can be used in executive presentations 
The tool is built on underlying calculation models that generate fair assessment of value that you can achieve given the data provided
This TCO helps by reducing the need to invest in large capital expenditures
The tool is for approximation only 

# AWS Landing Zone

Helps Enterprises quickly set-up a secure, AWS multi-account
Provides you with a baseline environment to get started with a multi-account architecture

AWS Account Vending Machine 
Automatically provisions and configure new accounts via landing zones - Service Catalog Template
Uses Single Sign-on for managing and accessing accounts
The environment is customizable to allow customers to implement their own account baselines through a Landing Zone configuration and update pipeline

# Resource groups and Tagging

Tags are words or phrases that act as metadata for organizing your AWS resources 
Resource Groups are a collection of resources that share one or more tags

Helps you organize and consolidate information based on your project and the resources that you use
Resource Groups can display details about a group of resources based on 
    
    Metrics
    Alarms 
    Configuration Settings

At any time you can modify the settings of your resource groups to change what resources appear 

# AWS Quick Start 

Prebuilt templates by AWS and AWS Partners to help you deploy popular stacks on AWS 
Reduce hundreds of manual procedures into just a few steps 

A Quick Start is composed of 3 parts 
    
    A reference architecture for the deployment 
    AWS CloudFormation templates that automate and configure the deployment 
    A deployment guide explaining the architecture and implementation in detail 

Most QuickStart reference deployments enable you to spin up a fully functional architecture in less than an hour 

# Cost and Usage Report 

Generate a detailed spreadsheet, enabling you to better analyze and understand your AWS costs

Places the reports into S3 Bucket -> Use Athena to turn the report into a queryable database -> Use Quick Sight to visualize your billing data as graphs 

# Organizations and Accounts

Organizations -> allow you to centrally manage billing, control access, compliance, security, and share resources across your AWS accounts

Root Account User -> Is a single-sign in identity that has complete access to all AWS services and resources in an account -> Each account has a Root Account User

Organization Units -> are a group of AWS accounts within an organization which can also contain other organizational units -> creating a hierarchy

Service Control Policies -> give central control over the allowed permissions for all accounts in your organization, helping to ensure your account stay within your organizations guidelines 



# Networking 

Region - The geographical location of your network 

AZ - the datacenter of your AWS resources

VPC - a logically isolated section of the AWS CLoud where you can launch AWS resources

Internet Gateway - Enable access to the internet 

Route Table - determines where network traffic from your subnets are directed 

NACLs - Acts as a firewall at the subnet level 

Security groups - Act as a firewall at the instance level 

Subnets - a logical partition og an IP network into multiple, smaller network segments 


# Database Services

DynamoDB - NoSQL - key/value database -> Cassandra

DocumentDB - NoSQL -Document database that is MongoDB compatible -> MongoDB

RDS - Relational Database Service that supports multiple engines -> MySQL, Postgres, Maria DB, Oracle, Microsoft SQL Server, Aurora 
    Aurora - MySQL (5x faster) and PSQL (3x faster) database -> fully managed
    Aurora Serverless -only runs when you need it, like AWS Lambda

Neptune - Managed Graph Database

Redshift - Columner database, petabyte warehouse 

ElastiCache - Redis or Memcached database 

#Provisioning 

Provisioning - the allocation/creation of resources and services to a customer 

Elastic Beanstalk - service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go and Docker

OpsWorks - configuration management service that provides managed instances of Chef and Puppet 

CloudFormation - infrastructure as code, JSON or YAML

AWS QuickStart - premade packages that can launch and configure your AWS compute, network , storage and other services required to deploy a workload on AWS 

AWS MarketPlace - a digital catalogue of thousands of software listings from independent software vendors you can use to find, buy, test and deploy software 


# Computing Services 

EC2 - Elastic Compute Cloud - highly configurable server

ECS - Elastic Container Service - Docker as a Service - Highly scalable - high-performance container orchestration service that supports Docker containers - have to pay for EC2 instances

Fargate - Microservice where you don't think about the infrastructure - pay per task 

EKS - Kubernetes as a Service - easy to deploy, manage and scale containerized applications using Kubernetes 

Lambda - serverless functions - run code without provisioning or managing servers - You pay only for the compute time you consume

Elastic Beanstalk - Orchestrates various AWS services - EC2, S3, Simple Notification Service, CloudWatch, Autoscaling, ELBs

AWS Batch - Plans, schedules and executes your batch computing workloads across the full range of AWS compute services and features like EC2 and Spot Instances 

# Storage Services 

S3 - Simple Storage Service - Object storage 

S3 Glacier - low cost storage - archiving and long-term backup 

Storage Gateway - hybrid cloud storage with local caching - File Gateway - Volume Gateway - Tape Gateway 

EBS - Elastic Block Storage - Hard drive in the cloud you attach to EC2 instances 

EFS - Elastic File Storage - file storage mountable to multiple EC2 instances at the same time 

Snowball - Physically migrate lots of data via a computer suitcase - 50, 80 TBs of space 

Snowball Edge - 100TB version 

Snow mobile - shipping container, pulled by a semi-trailer truck - 100PB 

# Business Centric Services 

Amazon Connect - Call Center - Cloud-based call center service you can setup in just a few clicks - based on the same proven system used by the Amazon customer service teams

WorkSpaces - Virtual Remote Desktop - Secure managed service for provisioning either Windows or Linux desktops in just a few minutes which quickly scales up to thousands of desktops

WorkDocs - A content creation and collaboration service - easily create, edit and share content saved centrally in AWS - AWS version of Sharepoint

Chime - AWS Platform for online meetings, video conferencing and business calling which elastically scales to meet your capacity needs 

WorkMail - Managed business email, contacts and calender service with support for existing desktop and mobile email client applications (IMAP)

Pinpoint - Marketing campaign management system you can use for sending targeted email, SMS, push notifications, and voice messages

SES - Simple Email Service - Cloud-based email sending service designed for marketers and application developers to send marketing, notification, and emails

Quicksight - A business Intelligence (BI) service - Connect multiple datasources and quickly visualise data in the form of graphs with little to no programming knowledge 

# Enterprise Integration 

GOING HYBRID

Direct Connect dedicated Gigabit network connection from your premise to AWS - Imagine having a direct fibre optic cable running straight to AWS 

VPN - establish a secure connection to your AWS network 
    
    Site to site VPN - Connecting your on-premise to your AWS network 
    Client VPN - Connecting a Client to your AWS network 
    
Storage Gateway - A hybrid storage service that enables your on-premises applications to use AWS cloud storage - You can use this for backup and archiving, disaster recovery, cloud data processing, storage tiering and migration

Active Directory - The AWS Directory Service for Microsoft Active Directory also known as AWS Managed Mircosoft AD - enables your directory-aware workloads and AWS resources to use managed Active Directory in the AWS Cloud 

# Logging Services 

CloudTrail - logs all API calls - between AWS services 
    
    Who created the bucket - Detect developer misconfigurations
    Who spun up that expensive EC2 instance - Detect malicious actors
    Who launched this SageMaker Notebook - Automate responses 
    
CloudWatch - is a collection of multiple services

CloudWatch logs - Performance data about AWS Service - Application Logs (Nginx) - Lambda Logs 

CloudWatch Metrics - Represents a time-ordered set of data points - A variable to monitor 

CloudWatch Events - Trigger an event based on condition - every hour take snapshot of server 

CloudWatch Alarms - triggers notifications based on metrics

CloudWatch Dashboard - create visualization based on metrics 

# Shared Responsibility Model 

Customers are responsible for security in the Cloud 

AWS is responsible for security of the cloud 

# AWS Compliance Programs 

A set of internal policies and procedures of a company to comply with laws, rules and regulations or to uphold business reputation 

# AWS Artifact 

No cost, self-service portal for on-demand access to AWS compliance reports 
On-demand access to AWS security and compliance reports and select online agreements 
These checks are based on global compliance frameworks 

# Amazon Inspector 

Hardening - The act of eliminating as many security risks as possible 

AWS Inspector runs a security benchmark against specific EC2 Instances - You can run a variety of security benchmarks

Can perform both Network and Host Assessments
    
    Install the AWS agent on your EC2 Instances
    Run an assessment for your assessment target 
    Review your findings and remediate security issues 


# AWS WAF

AWS Web Application Firewall protect your web applications from common web exploits 

Write your own rules to Allow or Deny traffic based on the contents of an HTTP requests

Use a ruleset from a trusted AWS Security Partner in the AWS WAF Rules Marketplace 

WAF can be attached to either CloudFronts or an Application Load Balancer 

Protect web applications from attacks covered in the OWASP Top 10 - most dangerous attacks:

    Injection - Broken Authentication - Sensitive data exposure - XML External Entities - Broken Access control
    Security misconfigurations - Cross site scripting - Insecure deserialization - Using components with known vulnerabilities - insufficient logging and monitoring 

# AWS Shield 

AWS Shield is managed DDos protection service that safeguards applications running on AWS 

DDoS 
    
    - A malicious attempt to disrupt normal traffic by flooding a website a larger amount of fake traffic 

All AWS customers benefit from the automatic protections of AWS Shield Standard, at no additional charge 

When you route your traffic through Route53 or CloudFront you are using AWS Shield Standard 

Protects you against Layer 3, 4 and 7 attacks 
    
    - 7 application - 4 Transport - 3 Network 

Shield Standard - Free 
    
    For protection against most common DDoS attacks, and access to tools and best practices to build a DDoS resilient architecture 
    Automatically available on all AWS services 

Shield Advanced - $3000 a year 

    For additional protection against larger and more sophisticated attacks, visibility into attacks and 24x7 access to DDoS experts for complex cases 

Available on 

Route 53 - CloudFront - Elastic Load Balancing - AWS Global Accelerator - Elastic IP 

# Penetration Testing 

PenTesting - An authorized simulated cyberattack on a computer system, performed to evaluate the security of the system 

Permitted Services

    EC2 -NAT Gateways - ELB - RDS - CloudFront - Aurora - API Gateways - AWS Lambda and Lambda@Edge - Lightsail resources - Elastic Beanstalk environments 

Prohibited Activities 
    
    DNS zone walking via Route 53 Hosted Zones - DDoS attacks - Port flooding - Protocol flooding - Request flooding

For other simulated events, you will need to submit a request to AWS - Reply could take up to 7 days  

# Amazon Guard Duty 

IDS/IPS - Intrusion Detection System, Intrusion Protection System - A device/software application that monitors a network or systems for malicious activity or policy violations

Guard Duty is a threat detection service that continuously monitors for malicious, suspicious activity and unauthorized behaviour. It uses Machine Learning to analyze the following AWS logs 
    
    CloudTrail Logs 
    VPC Flow Logs
    DNS Logs 
    
It will alert you of Findings which you can automate a incident response via CloudWatch Events or with 3rd Party Services 

# Key Management Systems 

A managed service that makes it easy for you to create and control the encryption keys used to encrypt your data 
    
    KMS is a multi-tenant HSM (Hardware Security Module)
    Many AWS services are integrated to use KMS to encrypt your data with a simple checkbox
    KMS uses Envelope Encryption 
    
Envelope Encryption 
    
    When you encrypt your data, your data is protected but you have to protect your encryption key. When you encrpty your data key with a master key as an additional layer of security 
    
    KMS -> Master Key -> Envelope -> Data Key -> Database 

# Amazon Macie 


mMcie is a fully managed service that continuously monitors S3 data access activity for anomalies, and generates detailed alerts when it detects risk of unauthorized access or inadvertent data leaks


Macie works by using machine learning to analyse your cloud trail logs 

Macie will identify your most at risk users which could lead to a compromise 

Macie has a variety of alerts
    
    Anonymize Access
    location anomaly
    Config Compliance
    Open Permissions
    Credential Loss
    Privilege Escalation
    Data Compliance
    Ransomware
    File Hosting 
    Service disruption
    Identity Enumeration
    Suspicious Access
    Information Loss 

# Security Groups vs NACLs

Security Groups 
    
    Acts as a firewell at the instance level 
    Implicitly denies all traffic - You allow rules 
    Allow an EC2 Instance access on port 22 for SSH
    
NACLs - Network Access Control List 
    
    Acts as a firewall at the subnet level 
    You create Allow and Deny rules
    Block a specific IP address known for abuse 

# AWS VPN 

Lets you establish a secure and private tunnel from your network or device to the AWS global network 

AWS Site to Site VPN
    
    Securely connect on-premise network or branch office site to VPC 

AWS Client VPN
    
    Securely connect users to AWS or on-premises netowrks 
    
    
# Elastic Transcoder vs Media Convert 

Both services transcode videos 

Elastic Transcoder - Old way - Transcode videos to streaming formats

AWS Elemental MediaConvert - New way - Transcode videos to streaming formats - Overlays Images - inserts video clips - Extracts captions data - Robust UI 


# SNS vs SQS

Both connect apps via messages 

Simple Notifications Service
    
    Sends notification to subscribe of topics via multiple protocols - Http, Email, SQS, SMS
    SNS is generally used for sending plain text emails which is triggered via other AWS Services. The best example of this is billing alarms 
    Can retry sending in case of failiure for HTTPS
    Really good for webhooks, simple internal emails, triggering lambda functions
    
Simple Queue Service
    
    Places messaged into a queue. Applications pull queue using AWS SDK 
    Can retain a message for up to 14 days can send them in sequential  order or in parallel
    Can ensure only one message is sent 
    Can ensure messages are delivered at least once 
    
    Really good for delayed tasks, queueing up emails 


# AWS inspector vs AWS Trusted Advisor

Both are security tools and they both perform audits 

Amazon Inspector
    
    Audits a single EC2 instance that you've selected
    Generates a report from a long list of security checks

trusted Advisor 
    
    Trusted Advisor doesnt generate out a PDF report 
    Gives you a holistic view of recommendations across multiple services and best practices 
    e.g.
    You have open ports on these security groups 
    You should enable MFA on your root account when using trusted advisor 



# ALB vs NLB vs CLB

Application Load Balancer 
    
    Layer 7 Requests
    HTTP and HTTPS traffic
    Routing Rules, more usability from one load balancer 
    Can attach a WAF (Web Application Firewall)
    Can attached Amazon Certificate Manager SSL Certificate
    
Network Load Balancer 
    
    Layer 4 IP protocol data
    TCP and TLS traffic where extreme performance is required
    Capable of handling millions of requests per second while maintaining ultra-low latencies
    Optimized for sudden and volatile traffic patterns while using a single static IP address per Availability Zone 
    Can attached Amazon Certificate Manager SSL Certificate

Classic Load Balancer 
    
    Layer 4 and layer 7
    Intended for applications that were built within the EC2-Classic network 
    Can attached Amazon Certificate Manager SSL Certificate

# SNS vs SES 

They both send email

Simple Notifications Service - Practical and Internal 
    
    Sends notification to subscribe of topics via multiple protocols - Http, Email, SQS, SMS
    SNS is generally used for sending plain text emails which is triggered via other AWS Services. The best example of this is billing alarms 
    Alot of services can trigger SNS for notifications
    Topics and Subsriptions regardeding SNS 
    
Simple Email Service - Professional, Marketing, Email
    A cloud based email service - SendGrid
    SES sends HTML Emails, SNS cannot
    SES can receive inbound emails
    SES can create Email Templates
    Custom domain name email 
    Monitor your email reputation 
    
    
# Artifact vs Inspector 

Both Artifact and Inspector compile out PDFs

Artifact
    
    Generates a security report that's based on global compliance frameworks such as:
    Service Organization Control 
    Payment Card Industry 
    
    
Inspector 
    
    Runs a script that analyzes your EC2 instance, then generates a PDF report telling you which security checks passed
    Is a Audit tool for security of EC2 instances     





























