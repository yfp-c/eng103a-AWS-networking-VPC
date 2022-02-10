# eng103a-AWS-networking-VPC

## What is a VPC?
A Virtual Private Cloud (VPC) is a virtual network that you use to connect your virtual servers and virtual machines such as EC2 instances. 

AWS VPC is a service that provides the base to build cloud infrastructure, with control over security, of the traffic between services and overall more control over the network.

## What is a CIDR block?
CIDR stands for Classless Inter-Domain Routing. The CIDR value denotes the max number of IP addresses that can be used in the VPC.

CIDR blocks split IP addresses depending on the block number. If the block size is 4, and the starting IP address is 12.0.0.0, the 4 addresses will be 12.0.0.0, 12.0.0.1, 12.0.0.2, 12.0.0.3.

## What is internet gateway
An Internet Gateway allows instances and resources within your VPC to access the internet, and vice versa. For this to happen, there needs to be a routing table entry allowing a subnet to access the internet gateway.

## What is a route table
a routing table tells the network to route traffic to if the destination isn't within the same subnet. Traffic can be routed to an interface or gateway.

## What is a subnet
A subnet is a subdivision of an IP network, which is a segment of the CIDR block. Specific EC2 instances can be launched into the subnet.

## What is NACL
A network access control list (NACL) operates on a subnet level, it allows/denies inbound and outbound IPv4 traffic acting as a firewall. NACL on a subnet level, protects your instances (e.g. could be 1 or 10), whereas security groups act on an instance level.

![aws vpcdiagram](https://user-images.githubusercontent.com/98178943/153408226-c9fa438d-9725-45e1-8fa0-c9fdd9e7a679.png)

## Creating a VPC
- Select the region - in this case Ireland
- Create a VPC
- Select a valid CDIR block for our VPC to split into blocks. e.g. 10.0.0.0/16
- Step 2: Create an Internet Gateway(IGW)
- step 2.1: Attach the IGW to our VPC
- step 3: create a public subnet
- step 3.1: associate subnet to VPC
- Step 4: route table for publc subnet
- step 4.1: edit routes to allow IG
- step 4.2: associate to our public subnet
- step 5: create a security group in our public subnet to allow required ports/traffic:
- - allow port 80 port 3000, http -ssl
- Create a subnet CIDR block for public - 10.0.1.0/24 - 10.0.2.0/24 - 10.0.3.0/24