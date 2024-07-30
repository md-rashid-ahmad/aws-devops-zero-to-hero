# VPC

Imagine you want to set up a private, secure, and isolated area in the cloud where you can run your applications and store your data. This is where a VPC comes into play.

A VPC is a virtual network that you create in the cloud. It allows you to have your own private section of the internet, just like having your own network within a larger network. Within this VPC, you can create and manage various resources, such as servers, databases, and storage.

It’s like setting up your own mini internet inside AWS cloud. You have full control over your virtual networking environment, including selecting your own IP address range, creating subnets, configuring route tables and network gateways. You can define access rules, set up firewalls, and configure security groups to regulate who can access your resources and how they can communicate.

To connect your VPC to the internet or other networks, you can set up gateways or routers. These act as entry and exit points for traffic going in and out of your VPC. You can control the flow of traffic and set up security measures to protect your resources from unauthorized access.

By default, when you create an AWS account, AWS will create a default VPC for you but this default VPC is just to get started with AWS. You should create VPCs for applications or projects. 

## VPC components 

The following features help you configure a VPC to provide the connectivity that your applications need:

Virtual private clouds (VPC)
------------------------------

A VPC is a virtual network that closely resembles a traditional network that you'd operate in your own data center. After you create a VPC, you can add subnets.

Subnets
---------------
A subnet is a range of IP addresses in your VPC. A subnet must reside in a single Availability Zone. After you add subnets, you can deploy AWS resources in your VPC.

IP addressing
---------------
You can assign IP addresses, both IPv4 and IPv6, to your VPCs and subnets. You can also bring your public IPv4 and IPv6 GUA addresses to AWS and allocate them to resources in your VPC, such as EC2 instances, NAT gateways, and Network Load Balancers.

Network Access Control List (NACL)
-------------------------------------
NACL Provides an additional layer of security at the subnet level. Network ACLs are stateless, meaning both inbound and outbound rules must be configured. It operates at the IP address level and can allow or deny traffic based on rules that you define.
   
Security Group
------------------
Act as virtual firewalls for your instances to control inbound and outbound traffic at the instance level. Security Groups are stateful, meaning if you allow inbound traffic from an IP address, the response traffic to that IP address is automatically allowed. 

Rout Table
--------------
These are like maps that dictate where traffic goes within your VPC. Each subnet is associated with a route table that directs the traffic.

Internet Gateways
------------------------
This acts as a bridge between your VPC and the internet, allowing your resources in public subnets to communicate with the outside world.

VPC Peering
--------------------------
A networking connection between two VPCs that enables routing traffic between them privately. This is useful for creating multi-region architectures or connecting different AWS accounts.

VPC Endpoints
---------------
VPC Endpoints: Allow you to privately connect your VPC to supported AWS services without requiring an Internet Gateway, NAT device, VPN connection, or AWS Direct Connect connection. There are two types:

Interface Endpoints: Use AWS Private Link and provide private connectivity to services like Amazon S3, DynamoDB, and other AWS services.

Gateway Endpoints: Only for Amazon S3 and DynamoDB, routing traffic through a specified gateway.

Traffic Mirroring
--------------------------
Copy network traffic from network interfaces and send it to security and monitoring appliances for deep packet inspection.

Transit gateways
--------------------
Use a transit gateway, which acts as a central hub, to route traffic between your VPCs, VPN connections, and AWS Direct Connect connections.

VPC Flow Logs
--------------------
Flow Logs: Capture information about the IP traffic going to and from network interfaces in your VPC. This data is used for monitoring, troubleshooting, and security analysis.

NAT Gateway/Bastion Host
-----------------------------
NAT Gateway/Bastion Host: While public subnets can directly access the internet via the Internet Gateway, private subnets need a NAT Gateway or a Bastion Host to securely interact with the internet without exposing instances directly.

VPN connections
------------------------
Connect your VPCs to your on-premises networks using AWS Virtual Private Network (AWS VPN).


## Resources 

VPC with servers in private subnets and NAT

https://docs.aws.amazon.com/vpc/latest/userguide/vpc-example-private-subnets-nat.html

![image](https://github.com/iam-veeramalla/aws-devops-zero-to-hero/assets/43399466/89d8316e-7b70-4821-a6bf-67d1dcc4d2fb)



