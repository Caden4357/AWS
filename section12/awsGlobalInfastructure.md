# Why Global Applications 
- deployed in mutliple geographies. On aws this could be regions or edge locations 
- this will cause decreased latency for users 
- deploy code near where your users are located 
- disaster recovery: if an aws region goes down you can fail-over to another region this is important for increase availability in your apps 
- attack protection: global inf. is harder to attack 

# Route 53 overview:
    - A managed DNS 
    - A DNS is just like a phone book. A collection of rules and records which helps clients understand how to reach a server through URL's
    - For exam Route 53 is a managed DNS 
## Routing policies for exam
    - Simple routing policy has no health checks
    - Weighted routing policy distributes traffic to different server like a load balancer 
    - Latency routing policy: in a more global app it directs the user to a server that is closest to them 
    - Failover routing policy: if a server fails it will direct the user to a working one (disaster recovery)
# CLoudfront 
    - CDN (content delivery network)
    - Content is cached so it improves read performance 
    - DDos Protection 
    - Easy way to make objects in an s3 public without having to do it on the s3 bucket itself 
# s3 transfer acceleration 
    - Increase transfer speed by transferring file to an aws edge location which will forward the data to the s3 bucket in the target region 
    - Used when you want to download or upload a file from an s3 bucket that is far away from the client 
    - there is a website to test out all of this lecture 143 is where this is shown
# Global accelerator 
    - Improve global application avail. & performance using the AWS global network 
    - for example if you have a ALB in india and users connecting from all around the world the users would connect to an edge location that is public and then that would privately connect to the alb which would make it faster for the user 
    - Only 2 ips (anycast ips)
# AWS outposts
    - for hybrid cloud 
    - 2 ways of dealing with IT systems 
    - this makes it easier to deal with them 
# Wavelength 
    - tip: whenever you see 5g in exam think wavelength 
    - Brings AWS services to edgs of 5g networks 
    - ultra low latency to application through 5g networks 
# Local zones 
    - Places AWS compute, storage, database and other selected AWS services closer to the end users to run latency-sensitive applications 
    