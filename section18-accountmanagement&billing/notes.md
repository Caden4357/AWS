# Organizations 
    - Organizations are a way to group accounts together. manage them as a single entity. 
    - consilation billing, control access, and share resources across accounts, discount pricing, pooled resources
    - API driven
    - 2 types of accounts: master and member
    - send cloudwatch logs to a central account
    - common exam questions:
        - consolidated billing
        - pricing benefit from aggregated usage
        - pooling of reserved instances for savings 
        - api available to automate aws account creation
        - restrict account privileges using service control policies (SCP)
# consolidated billing  
    - one bill for all accounts
    - volume pricing discount
    - reserved instance pooling
    - easy to track charges
# control tower 
    - set up and govern a new, secure, multi-account AWS environment based on best practices established through AWS' experience working with thousands of enterprises as they move to the cloud
    - automate the set-up of a new baseline multi-account AWS environment that is secure, well-architected, and ready to use
    - runs on top of organizations
    - 3 main components:
        - **Organizational Units (OUs)**: a collection of AWS accounts within an organization. OUs help you manage your AWS accounts by grouping them based on your organizational model. 
        - **Service Control Policies (SCPs)**: a type of policy that you can use to manage permissions in your organization. SCPs offer central control over the maximum available permissions for all accounts in your organization. 
        - **Guardrails**: a set of rules that enforce policies or best practices in your organization. Guardrails help to ensure that your accounts stay within your organization’s guidelines.
# Resource Access Manager (RAM)
    - share aws resources that you own with other aws accounts
    - avoid resource duplication
# Service catalog 
    - create and manage catalogs of IT services that are approved for use on AWS
    - create portfolios of products, manage access to products, and view usage information
# Pricing models (Go back through this section)
    - 4 different pricing models: 
        - Pay as you go: pay for what you use, remain agile responsive meet scale demands 
        - save when you reserve: commit to a specific instance configuration with a 1 or 3 year term
        - pay less by using more: volume based discounts
        - pay less as aws grows: long term contracts
    - free services:
        - IAM 
        - VPC 
        - Consolidated billing 
    - free tier 
        - 12 months free
        - 750 hours of EC2
        - 5GB of S3
        - 25GB of DynamoDB
        - 1 million requests of Lambda
        - 15GB of Cloudwatch
    - ec2 pricing: 
        - on demand: pay by the hour or second
        - reserved: 1 or 3 year term
        - spot: bid on unused capacity
        - dedicated hosts: physical server dedicated to your use
    Lambda pricing: 
        - pay per request and compute time
        - free tier: 1 million requests per month
    ecs pricing: 
        - pay for EC2 instances
        - free tier: 750 hours per month
    - fargate pricing: 
        - pay for vCPU and memory
        - free tier: 750 hours per month
    s3 pricing:
        - storage class: standard, intelligent tiering, infrequent access, glacier 
        - free tier: 5GB
    ebs pricing:
        - pay for provisioned storage
        - free tier: 30GB
    rds pricing:
        - per hour pricing
# Savings plan 
    - commitment to a consistent amount of usage for a 1 or 3 year term
    - 2 types of savings plans: 
        - Compute savings plan: save up to 66% on EC2 and Fargate and lambda. most flexible 
        - EC2 instance savings plan: save up to 72% on EC2 usage
        - machine learning savings plan: sage maker 
# Compute optimizer 
    - reduce cost and imrpove performance by recommending optimal AWS resources for your workloads
    - ec2 auto scaling groups, ec2 instances, lambda functions, and ebs volumes
# Billing and costing tools 
    - estimate costs in the cloud: 
        - pricing calculator 
    - tracking costs in the could: 
        - billing dashboard 
        - colst allocation tags
        - cost and usage reports 
        - cost explorer
    - montioring against cost plans"
        - budgets
        - billing alarms 
# pricing calculator
    - estimate costs for aws services
    - you can create groups of services and resources to estimate costs for your use case
# Tracking costs in the cloud 
    - billing dashboard 
        - view your current bill
        - see how much you are forecasted to spend
        - see how much you have spent in the past
        - break down costs by service, region etc.
    - free tier 
        - see what services your free tier usage is being spent on
    - cost allocation tags
        - tags are key value pairs that you can assign to aws resources
        - tags are used to track costs on a granular level
        - tags can be used to track costs in cost explorer
        - resource groups can be created based on tags
    - cost and usage reports
        - detailed billing reports
        - the most comprehensive report
        - integrated with athena redshift and quicksight
    - cost explorer
        - visualize, understand, and manage your aws costs and usage over time
        - forecast costs
        - identify trends
        - identify cost drivers
        - create custom reports
# monitoring costs
    - billing alarms in cloudwatch 
        - set up billing alarms to be notified when you exceed your budget
        - set up billing alarms to be notified when you exceed a certain threshold
    - budgets
        - create a budget and send alarms when costw exceed the budget
        4 types of budgets: 
            - cost budget
            - usage budget
            - reservation budget
            - savings plan budget
# AWS cost anomaly detection / compute optimizer
    - detect unusual spending patterns
    - uses machine learning to analyze your usage and cost data
    - sends an alert if an anomaly is detected
    - can be used to detect unusual spending patterns
# AWS service quotas 
    - notify you when you are approaching a service limit
    - create cloudwatch alarms on service quotas console 
# trusted advisor 
    - analyze your aws environment and provides recs. on cost optimization, security, fault tolerance, performance, and service limits, operational excellence
# support plan pricing 
    - basic: free customer service, documentation, whitepapers, and support forums
        - trusted advispor: 7 checks
        - personal health dashboard
    - developer: $29 per month - basic plan + email support unlimited cases 
    - business: $100 per month - developer plan + 24/7 phone, chat, and email support, unlimited cases, and infrastructure event management full trusted advisor 
    - enterprise: $15,000 per month - business plan + a technical account manager, infrastructure event management, and training
