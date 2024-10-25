# IP Addresses
    - IPv4 - internet protocol version 4 4.3bil addresses
    - pulbic IPv4 - can be reached over the internet
    - EC2 instances gets a new public IP each time they are stopped and started
    - private IPv4 - can be used on private networks 
    - private IPv4 is fixed for EC2 insatnces and will not change
    - Elastic IP - allows you to attach a fixed IP to an instance
    - all public ipv4 on aws will be charged .005 per hour 
    - free tier is 750 hours per month 
    - IPv6 - internet protocol version 6 340 undecillion addresses
    - IPv6 is the new version of the IP protocol
    - free 
# VPC, Subnet internet gateway and NAT gateway
    - VPC - Virtual Private Cloud: private network to deploy your resources (regional resource)
    - A subnet allows you to partition your network inside your VPC (AZ resource)
    - a public subnet is accessible from the internet
    - a private subnet is not accessible from the internet
    - an internet gateway allows your VPC to connect to the internet
    - a NAT gateway allows your instances in a private subnet to access the internet while remaining private
# Security Groups and NACLs
    - NACL (Network Access Control List) - a firewall which controls traffic from and to subnet
    - can allow and deny rules 
    - attached to subnets
    - rules only include IP addresses
## Security groups
    - a firewall that controlls traffic to and from an EC2 instance
    - can only allow rules
    - rules include ip adresses and other security groups
# VPC Flow logs & VPC Peering
    - capture information about IP traffic going to and from network interfaces in your VPC
    - VPC flow logs 
    - Subnets flow logs 
    - elastic network interfaces flow logs
# VPC Peering 
    - connect 2 vpc privatley using AWS network
    - make them behave as if they were in the same network
    - must not have overlapping CIDR (IP address range)
    - vpc peering is not transitive
# VPC Endpoints
    - allow you to connect to AWS services using a private network instead of the public www
    - S3 and DynamoDB endpoints
    - gateway endpoints for S3 and DynamoDB
    - interface endpoints for other AWS services
# AWS Private Link:
    - Most secure and scalable way to share resources between VPCs
    - share services with other accounts
# Direct connect  and on site VPN
    - site to site VPN connect an on premise data center to AWS
    - connection is automatically encrypted
    - goes over public internet
    - Direct connect is a physical connection between your data center and AWS
    - goes over a private network
# Note for exam 
    - on premise must use a customer gateway (CGW)
    - AWS side must use a virtual private gateway (VGW)
# AWS client VPN:
    - connect your computer using openVPN to your private network in AWS or on premise 
    - secure connection over the internet
    - can be used to connect to AWS resources
# Transit gateway:
    - connect multiple VPCs and on premise networks together
    - acts as a hub that can be used to route traffic between all connected networks
# VPC Summary:
    - VPC - Virtual Private Cloud
    - Subnet - partition your network inside your VPC tied to a specific AZ
    - Internet Gateway - allows your VPC to connect to the internet
    - NAT Gateway - allows your instances in a private subnet to access the internet while remaining private
    - NACL - Network Access Control List - a firewall which controls traffic from and to subnet stateless
    - Security Group - a firewall that controlls traffic to and from an EC2 instance stateful
    - VPC peering - connect 2 VPCs privately using AWS network
    - Elastic IP - allows you to attach a fixed IP to an instance
    - VPC Endpoints - allow you to connect to AWS services using a private network instead of the public www
    - Private Link - most secure and scalable way to share resources between VPCs
    - VPC Flow logs - capture information about IP traffic going to and from network interfaces in your VPC
    - Site to site VPN - connect an on premise data center to AWS
    - client VPN - connect your computer using openVPN to your private network in AWS or on premise
    - Direct connect - a physical connection between your data center and AWS
    - Transit gateway - connect multiple VPCs and on premise networks together
