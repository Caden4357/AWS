# Cloud Formation 
    - a declarative way of outlining your AWS infrastructure, for any resources (most of them are supported)
## Benefits 
    - Infrastructure as code meaning you can version control your infrastructure
    - Cost 
        - each resources within the stack is stagged with an identifier so you can easily see how much a stack costs you
        - you can estimate the costs of your resources using the CloudFormation template
        - savings strategy: In dev you could automation deletion of templates at 5pm and recreate them at 8am (or whatever times you want) to save money
    - Productivity
        - Ability to destroy and re-create an infrastructure on the cloud on the fly
        - Automated generation of Diagram for your templates
        - Declarative programming (no need to figure out ordering and orchestration)
        - Widely adopted (lots of documentation online + lots of help)
        - Transcend the use of AWS console
        - Supports pretty much every AWS service
# We can see all the recourses and the relations between components 

# CDK (Cloud development kit) gotta check this out
    - open source framework to define your cloud application resources using familiar programming languages
    - provision anything in AWS using Typescript, Javascript, Python, Java, C#, etc then its compiled to CloudFormation template 

# Elastic Beanstalk 
    - Elastic Beanstalk is a developer centric view of deploying an application on AWS
    - It uses all the component we have seen before: EC2, ASG, ELB, RDS, etc
    - But its all in one view 
    - We still have full control over the configuration
    - Beanstalk = Platform as a service (PaaS)
    - Beanstalk is free but you pay for the underlying instances
    - Managed service
    - Instance configuration is handled by Beanstalk
    - Deployment strategies and health monitoring all handled by Beanstalk
    - Only responsiblity for developer is application code
# Health monitoring 
    - Beanstalk can use SNS, CloudWatch, and other services to monitor the health of your application
    - You get an email if something goes wrong

# CodeCommit 
    - Version control service hosted by AWS
    - Fully managed
    - Private Git repositories
    - No size limit on repositories
    - CodeCommit eliminates the need to operate your own source control system or worry about scaling its infrastructure