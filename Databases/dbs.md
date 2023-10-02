# Different database options on AWS include Amazon Aurora, Amazon RDS, Amazon DynamoDB, Amazon ElastiCache, Amazon Redshift, Amazon Neptune, and Amazon DocumentDB.
# AWS RDS Overview 
    - OLTP (Online Transaction Processing) suitable 
    - AWS stands for Amazon Relational Database Service
    - AWS RDS is a managed service that allows you to run relational databases in the cloud
# AWS Aurora 
    - AWS Aurora is a MySQL and PostgreSQL compatible relational database built for the cloud
    - Aurora is a proprietary technology from AWS
    - Faster than standard MySQL and PostgreSQL databases
# RDS read replica 
    - RDS read replicas are used for scaling read operations
    - You can have up to 15 read replicas
    - Data is only written to the primary database
# Multi AZ
    - Multi AZ is used for disaster recovery
    - Failover incase of loss of availability zone (high availability)
    - Data is only read/write to the primary database
    - Can only have one other AZ for failover
# Multi Region 
    - Multi region is used for disaster recovery
    - Local perfomarance for global reads 
    - Replication costs
# ElastiCache Overview 
    - The same way RDS is to get manages relational databases in the cloud, ElastiCache is to get managed Redis or Memcached in the cloud
    - Caches are in-memory databases with really high performance, low latency
    - Helps reduce load off databases for read intensive workloads
# Dynamo DB 
    - DynamoDB is a NoSQL database (Non-relational)
    - Fully manages highly available with replication across 3 AZ
    - Scales to massive workloads with very low latency
    - Millions of requests per seconds, trillions of rows, 100s of TB of storage
    - Serverless
    - Integrated with IAM for security
    - low cost and auto scaling capabilities
## Types of data use cases 
    -key-value pair 
    -document
    -graph
    -in-memory
## DAX 
    - DAX is a DynamoDB accelerator
    - Fully managed, highly available, in-memory cache for DynamoDB
    - Writes go through DAX to DynamoDB
    - Microsecond latency for cached reads and queries
    - Solves the Hot Key problem (too many reads)
    - No need to manage your own caching logic
    - DAX is multi AZ
    - DAX is not a write-through cache (eventual consistency)
# Dynamo DB - Global tables 
    - Make a DynamoDB table available w/ low latency in multiple regions
    - Active-Active replication (read/write to any AWS region)
# Redshift 
    - Based on PostgreSQL but its not used for OLTP (Online Transaction Processing)
    - Used for OLAP (Online Analytics Processing)
    - Columnar storage (instead of row based)
    - Massively Parallel query execution
    - Pay as you go (only for what you use)
    - Has a SQL interface for performing queries
    - BI tools such as AWS Quicksight, Tableau etc 
# EMR Elastic MapReduce
    - EMR helps crewate Hadoop clusters (Big Data) to analyze and process vast amounts of data
    - Clusters can be made of hundreds of EC2 instances
    - Also supports Apache Spark, HBase, Presto, Flink, and more
    - EMR Rakes care of all provisioning and configuration
    - Auto Scaling and integrated with Spot instances
    - Use cases: data processing, machine learning, web indexing, big data analysis, etc
    - Hadoop cluster = EMR 
# Athena
    - Serveless query service to perfomr analytics directly on S3 files
    - Uses SQL language to query the files
    - supports CSV, JSON, ORC, Avro, and Parquet files
    - Pricicng around $5 per TB of data scanned
    - Use Cases: Business intelligence/analytics/reporting, analyze AWS CloudTrail data, analyze VPC Flow Logs, etc
# Amazon quicksight 
    - Allows you to create dashboards on your dbs to show you the data in a visual way
    - Fast, automatically scales, serverless
    - Use cases include: business intelligence, visualize AWS billing, ad-hoc visualization, etc
    - integreated with AWS services (RDS, DynamoDB, S3, Athena, etc)
# Document DB (MongoDB)
    - Aurora is a relational database that is compatible with MySQL and PostgreSQL
    - DocumentDB is a NoSQL database that is compatible with MongoDB
    - Similar deployment concepts to aurora 
    - fully managed, highly available, with replication across 3 AZ and auto scaling
    - DDB storage automatically grows up to 64 TB
    - Automatically scales to workloads with millions of requests per second
# Neptune 
    - Neptune is a fully managed graph database
    - A graph database is a database that uses graph structures for semantic queries with nodes, edges, and properties to represent and store data example of a graph database is a social network
    - Highly available across 3 AZ up to 15 read replicas
    - Build and run applications working with highly connected datasets optimized for complex hard queuries
    - Use cases: social networking, recommendation engines, fraud detection, knowledge graphs, life sciences, network security, etc
# Amazon QLDB
    - Stands for Amazon Quantum Ledger Database
    - A ledger is a record of transactions or events over time
    - QLDB is a fully managed ledger database
    - It is immutable, transparent, and cryptographically verifiable
    - It uses an append-only journal, which means that you cannot delete or update records
    - Use cases: finance, retail, manufacturing, HR, etc not blockchain
# Amazon manages blockchain 
    - Blockchain is a decentralized distributed ledger that keeps a record of all transactions that take place across a peer-to-peer network
    - Amazon managed blockchain is a managed service to 
        - join public blockchain networks 
        - or create your own scalable private network 
    - compatible with Hyperledger Fabric and Ethereum
# AWS glue 
    - Managed extract transform and load (ETL) service
    - Useful to prepare and transofrm data for analytics
    - ETL moves and transforms data from one place to another to make it more digestible and accessible for downstream applications
    - AWS Glue is serverless 
# DMS (Database migration service)
    - DMS helps you migrate databases to AWS quickly and securely
    - The source database remains fully operational during the migration, minimizing downtime to applications that rely on the database
    - Supprts homogenous migrations (e.g. Oracle to Oracle) and heterogeneous migrations (e.g. Microsoft SQL Server to Amazon Aurora) ei when the source and target databases are not the same or the same 
# Summary 
    - relational dbs - OLTP - RDS, Aurora, Redshift, DMS
    - differences between multi AZ,replia, and multi region
    - in memeory dbs - ElastiCache
    - NoSQL dbs - DynamoDB, DocumentDB, Neptune, QLDB
    - EMR - Hadoop
    - warehouse - Redshift (OLAP)
    - Athena - query S3
    - Quicksight - visualize data
    - document DB - aurora for MongoDB
    - amazon qldp - ledger database
    - amazon managed blockchain - blockchain
    - AWS glue - ETL
    - DMS - migrate dbs to AWS
    - neptune - graph db
