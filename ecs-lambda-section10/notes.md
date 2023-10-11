# Docker what is it?
    - Docker is a tool that allows developers, sys-admins etc to easily deploy their applications in a sandbox (called containers) to run on the host operating system i.e. Linux.
# ECS 
    - Elastic container service
    - Launch docker containers on AWS
    - Anytime on exam you hear about docker or docker containers think ECS 
# Fargate 
    - Serverless compute engine for containers
    - No need to provision or manage servers (no EC2 instances)
    - Just package your application into a container image, upload it to ECS, and ECS will run and scale your container for you
    - You only pay for the resources required to run your containers, so there is no over-provisioning and paying for additional servers
    - Fargate is a launch type for ECS
# ECR 
    - Elastic Container Registry
    - Private dokcer registry on AWS
    - This is where you store your docker images so they can be run on ECS or Fargate
# What is serverless 
    - Serverless is a new paradigm in which the developers don't have to manage servers anymore
    - They just deploy code and the cloud provider runs and scales their code for them
    - serverless does not mean there are no servers, it just means you don't manage them
    - examples: S3 (serverless storage), DynamoDB (serverless database), fargate (docker containers), Lambda (serverless functions)
# Lambda
    - virtual functions - no servers to manage
    - limited by time - short executions 
    - run on demand - event driven
    - scales automatically
    - pay per execution and compute time
    - free tier of 1 million requests per month 400,000 GB-seconds of compute time per month (after that its $0.20 per 1 million requests and $0.00001667 for every GB-second used) remember pricing is determined per call 
    - integrated with the whole aws suite of services
    - integrated with many programming languages
    - easy monitoring 
    - easy to get more resources per function (up to 10GB of RAM)
    - You can also run very specific docker images on lambda functions (lambda container image) ECS and Fargate are preferred for docker containers 
    - lambda functions are not exposed to the internet by default, you need to put them behind an API gateway or a load balancer
## example of a lambda function would be serverless thumbnail creation which really just means you upload an image to S3 and then lambda will create a thumbnail of that image and put it in another S3 bucket and possibly also save that in a database (if you want)
## serverless CRON job - you can use lambda to run a cron job which is a job that runs at a specific time or interval

# API gateway 
    - Create serverless REST APIs that trigger lambda functions
    - Scales automatically
    - supports resful apis and websockets
    - support for security (authentication and authorization) api throttling, caching, logging, monitoring, etc
    - on exam if you see a question about creating a serverless api think api gateway and lambda
# AWS batch 
    - fully managed batch processing service at any scale
    - a batch job is a job with a start and an end (opposed to continuous)
    - batch will dynamically launch EC2 instances and scale out to process your batch jobs
    - batch will also scale in and shut down EC2 instances when your jobs are complete
    - defined as a docker image and run on ECS 
    - use cases: long running batch jobs, batch jobs with dependencies, batch jobs with scaling needs, etc
# Batch vs Lambda 
    - Lambda is for short jobs (less than 15 minutes)
    - limited runtimes 
    - limited temporary disk space
    - serverless
    - batch has no time limit
    - any runtime as long as its in a docker image
    - rely on ebs / instance store for disk space
    - not serverless relies on EC2 (can be managed by AWS)
# Amazon lightsale 
    - virtual servers, storage, dbs, and networking 
    - simpler alternative to things like EC2, RDS, etc
    - low and predictable pricing
    - great for beginners or small projects and people with little cloud experience that dont care to learn 
    - use cases: Simple web apps, websites, dev/test environments, etc
    - high availability but no auto scaling
    - on exam if you see a question about someone w/ no cloud experience and needs to get started quickly 