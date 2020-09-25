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
Get notified by providing an email or Chatbot and threshhold how close to the current or forecasted budget

# TCO Calculator 

The total Cost of Ownership allows you to estimate how much you would save when moving to AWS from on-premise
Provides you a detailed set of reports that can be used in executive presenations 
The tool is built on underlying calculation models that generate fair assessment of value that you can achieve given the data provided
This TCO helps by reducing the need to invest in large capital expenditures
The tool is for approximation only 

# AWS Landing Zone

Helps Enterprises quicly set-up a secure, AWS multi-account
Provides you with a baseline environment to get 
















































