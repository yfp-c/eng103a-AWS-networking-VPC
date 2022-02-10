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
A network access control list (NACL) operates on a subnet level, it allows/denies inbound and outbound IPv4 traffic acting as a firewall.

![aws vpcdiagram](https://user-images.githubusercontent.com/98178943/153402309-469354cf-49a3-48cc-902c-ca7964c8fb31.png)