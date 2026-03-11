# aws-vpc-secure-infrastructure

This project demonstrates the design and deployment of a segmented AWS cloud network architecture using a VPC, public and private subnets, NAT Gateway, Internet Gateway, route tables, and Network ACL security controls.

The goal was to simulate a secure cloud environment where public-facing services are separated from internal resources while maintaining outbound connectivity.

---

## Architecture Diagram
![AWS Architecture](architecture/aws-vpc-diagram.png)

## Infrastructure Components

VPC
CIDR: 10.0.0.0/16

Public Subnet
10.0.1.0/24
Hosts public resources and NAT Gateway

Private Subnet
10.0.2.0/24
Hosts internal EC2 instances with no direct internet access

Internet Gateway
Provides inbound and outbound internet connectivity for the public subnet

NAT Gateway
Allows private subnet instances to access the internet securely

Route Tables
Public subnet routes internet traffic to the Internet Gateway
Private subnet routes internet traffic through the NAT Gateway

Network ACL
Restricts inbound traffic to HTTP and ephemeral return traffic
