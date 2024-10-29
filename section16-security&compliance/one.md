# Shared responsibility model: reminders/examples
    - aws is responsible for security of the cloud
    - also any services that are managed by AWS (S3, DynamoDB, RDS, etc)
    - customer is responsible for security in the cloud
    - also any services that are managed by the customer (EC2, Lambda, etc)
    - example: EC2 instance is managed by the customer
    - example: S3 is managed by AWS
    - example: RDS is managed by AWS your responsibility is the data, the database, the encryption at rest, IAM, etc
# DDos protection:
    - distrubuted denial of service attack which is an attempt to make a website or application unavailable by overwhelming it with traffic from multiple sources
    - AWS Shield - managed DDos protection service that safeguards applications running on AWS for all customers at no additional cost
    - AWS Shield Advanced - provides enhanced DDoS protection for more demanding applications
# AWS WAF:
    - Web Application Firewall - helps protect your web applications from common web exploits that could affect application availability, compromise security, or consume excessive resources
    - layer 7 http 
    - deploy on application load balancer, cloudfront, api gateway
    - rules can be created to block or allow traffic based on IP addresses, http headers, http body, or URI strings
    - can be used to block SQL injection, cross site scripting, etc
    - rate based rules for ddos protection
# Cloudfront and route53
    - availability protection using global edge network
    - combined with aws shield provides attack mitigation at edge locations
# AWS network firewall
    - protect your entire vpc from layer 3 to 7 
    - any direction
    - rules can be created to block or allow traffic based on IP addresses, protocols, ports, etc
    - better than network cdl 
# AWS firewall manager
    - manage all security rules across all your accounts and applications
# For exam
    - If you see a question around managing your VPC Security Groups across multiple accounts in an organization, think no more than the AWS Firewall Manager.
    - can also manage WAF aws sheilds advance and network firewall
    - rulles are applied to all current and future resources
# Penetration testing
    - Penetration testing is when you're trying to attack your own infrastructure to test your security. A customer of AWS is welcome to carry out these security assessments and penetration testing against your own infrastructure without prior approval for eight services.
    - prohibited services: Route 53, CloudFront, WAF, Shield, and any other managed service
    - you cannot do DoS or DDoS attacks or simulate them. port flooding, protocol flooding, request flooding 
    - for any othher simulated events you must contact AWS
# Encryption 
    - 2 types of encryption: in transit and at rest
    - in transit: data is encrypted as it moves between your computer and the server
    - at rest: data is encrypted when it is stored on disk
    - we want to encrypt data at rest and in transit we do this with KMS for encryption at rest and SSL/TLS for encryption in transit
    - AWS KMS: key management service - fully managed service that makes it easy for you to create and control the encryption keys used to encrypt your data
    - AWS CloudHSM: hardware security module - dedicated hardware for encryption key storage aws provisions the hardware and you manage the keys its tamper resistant
    - types of kms keys: customer managed keys, aws managed keys, aws owned keys
    - customer managed keys: you create and manage the keys 
    - aws managed keys: created and managed by AWS whenever you see aws/ its an aws managed key
    - aws owned keys: used by AWS services to encrypt data on your behalf you cant view the keys
# AWS certificate manager (ACM)
    - lets your easily provision manage and deploy public and private SSL/TLS certificates for use with AWS services and your internal connected resources
    - use to provide in flight encryption for websites (HTTPS)
    - free service
# AWS Secrets manager 
    - newer service meant for storing Secrets like database credentials, passwords, third party API keys, etc
    - can rotate secrets automatically
    - can be used to store secrets for RDS, Redshift, DocumentDB, etc 
## For Exam anything related to secrets and RDS think AWS Secrets Manager
# Artifact (not really a service)
    - portal that provides on demand access to AWS security and compliance reports and select online agreements
    - can be used to download SOC reports, PCI reports, etc
    - can be used to accept agreements like the DPA (Data Processing Agreement)
# Guard duty 
    - Intelligent threat discovery to protect your account using ML algorithms and 3rd party data
    - analyzes VPC flow logs, CloudTrail logs, and DNS logs
## Note for exam: can protect against crypto mining, credential leaks, etc 
# Inspector
    - automated security assessment service to help improve the security and compliance of applications deployed on AWS
    - can be used to test the network accessibility of your EC2 instances
    - can be used to test the security of your applications
    - can be used to test the security of your instance configuration
    - for container images like docker you can use ECR image scanning
    - for serverless you can use lambda security automator
# Config
    - view compiance or configuration of a resource over time also view cloudtrail api calls if enabled
    - not free  
    - helps with auditing and recording compliance of your AWS resources
    - helps record configurations of your AWS resources over time
    - stored in s3 to be analyzed or retrieved later
    - The question that can be solved by using Config,
    - can be is there unrestricted SSH access
    - to my security groups?
    - Or do buckets have any public access?
    - Or has my ALB configuration changed over time?
# Macie
    - fully managed data security and data privacy service that uses machine learning and pattern matching to discover and protect your sensitive data in AWS
    - alert you to any unusual activity (pii personal identifiable information)
    - can be used to monitor S3 buckets
# Security hub
    - central security management and compliance service that aggregates, organizes, and prioritizes your security alerts or findings from multiple AWS services 
    - a dashboard that gives you a view of your security state within AWS combines findings from GuardDuty, Inspector, Macie, etc
    - can be used to monitor your security compliance
# Detective
    - service that automatically collects log data from your AWS resources and uses machine learning, statistical analysis, and graph theory to build a linked set of data that enables you to easily conduct faster and more efficient security investigations
# AWS abuse 
    - report any abuse to AWS
    - phishing, spam, scanning, dos ddos attacks, etc
# Root user privileges
    - root user has full access to all resources in your AWS account
    - should not be used for everyday tasks
    - really only use for the following:
    - account settings view certain tax invoices, close account, restore iam user permissions, change or cancel plan, register as a seller, etc.
# IAM Access analyzer
    - IAM Access Analyzer helps you identify the resources in your organization and accounts, such as Amazon S3 buckets or IAM roles, that are shared with an external entity. 
    - You can do this by creating an analyzer in the AWS Management Console, and then running an analysis on your resources. 
    - IAM Access Analyzer generates findings for resources that are shared with external entities and provides you with the information you need to take action on those resources.
# Summary 
    - 
