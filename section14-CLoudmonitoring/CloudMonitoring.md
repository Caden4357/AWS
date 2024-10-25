# Cloudwatch
- CloudWatch provides metrics for every service in AWS,
- CloudWatch can monitor:
    - Compute: EC2 instances, Autoscaling groups, Elastic Load Balancers, Route53 health checks
    - Storage & Content Delivery: EBS Volumes, Storage Gateways, CloudFront
    - Database & Analytics: DynamoDB, RDS, ElasticCache, Redshift
    - Other: SNS, SQS, Lambda, API Gateway, CloudWatch Logs
- CloudWatch Alarms can be created to notify you when a metric goes beyond a threshold
- Can create custom metrics in CloudWatch
- alrms can trigger notifications to:
    - Auto Scaling
    - EC2 Actions
    - SNS Notifications
alarm states:
- OK
- INSUFFICIENT_DATA
- ALARM
# Cloud Watch Logs:
    - Monitor, store, and access log files from EC2 instances, CloudTrail, and other sources
    - real time monitoring
    - archive logs
    - by default logs will not be created run a cloud watch agent to create logs use IAM roles
    - can work on premise as well
# EventBridge: 
    - schedule cron jobs
    - event driven programming
    - can be used to trigger lambda functions 
    - can be used to trigger SNS notifications 
    - And more 
    - EventBridge is the new version of CloudWatch Events
    - can use 3rd party events and custom events
# Cloudtrail:
    - provides governance compliance and audit for your AWS account 
    - CloudTrail is enabled by default
    -get a history of events/API calls made within your AWS account by:
        - Console
        - SDK
        - CLI
        - AWS Services
    - can put logs from cloudtrail into cloudwatch logs
    - can put logs from cloudtrail into S3
    - can be applied to all regions or just one
# X Ray: 
    - helps developers debug production, distributed applications, such as those built using a microservices architecture
    - visual analysis of your applications
    - uses: 
        - troubleshooting performance
        - understand dependencies
        - pinpoint service issues
    - can trace requests from beginning to end
    - can be used for performance optimization
    more..
# Code guru:
    - automated code reviews AI
    - automated code reviews and application performance recommendations
    - supports java and python currently 
## code guru profiler:
    - helps you find the most expensive lines of code in your application
    - helps you reduce CPU utilization and improve performance
# AWS Health dashboard service history 
    - shows all regions all services health 
    - shows historical info for each day 
    - has a rss feed (rss -> RSS is a web feed that allows users and applications to access updates to websites in a standardized, computer-readable format)
# AWS Health dashboard 
    - provides alerts and remediation guidance when AWS is experiencing events that may impact you
    - can aggregate data for your entire app 
    - global service 
