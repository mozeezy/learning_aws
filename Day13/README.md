### Day13 - VPC and Networking

##### IP Addresses
- IPv4 is the fourth version of the Internet Protocol (IP). It is an address that can be used on the internet to access a website.
- Public IPv4 is available for everyone on the internet. This changes when we start and stop our EC2 instance.
- Private IPv4 can only be used on local access networks (LAN). This is fixed even if we start and stop our EC2 instance.
- Elastic IP allows us to attach a fixed public IPv4 to our EC2 instance.
  -  We only pay for ongoing cost when it's not attached to EC2 instance or if the EC2 instance is stopped.
- IPv6 is version 6 and there's are no private IP addresses.

##### VPC And Subnets
- VPC (virtual private network) is a private network to deploy our resources. It is a regional resource.
- A subnet is a partition of our network within the VPC. It is an AZ resource.
  - We can have public and private subnets, which can be accessible or not from the internet.
  - To define access to the internet and subnets, we need Route Tables.

##### Internet Gateway and NAT Gateways
- Internet Gateways help our VPC instances connect with the internet.
- NAT Gateways allow private subnets in our VPC instances to access the internet.

##### Network ACL & Security Groups
- Network ACL (NACL) is a firewall that controls traffic to and from our subnet. These are attached at the subnet level.
  - They can have ALLOW or DENY rules and the rules include only IP addresses.
- Security Group is a firewall that controls traffic to and from our EC2 instances. They only have ALLOW rules.
  - Rules can include IP addresses or other security groups.

##### VPC Flow Logs
- These are logs that capture IP traffic going into our interfaces.
- Helps to monitor and troubleshoot connectivity issues.

##### VPC Peering
- They connect two VPC privately on the AWS' network.
- Must not have overlapping CIDR

##### VPC Endpoints
- These are endpoints that allow you to connect to AWS services using a private network
- This has an added benefit of security and lower latency.

##### AWS PrivateLink
- This is the most secure and scalable way to expose a service to 1000s of VPCs.
- Does not require VPC peering, internet gateway, NAT, etc...

##### Site to Site VPN and Direct Connect
- Site to site VPN
  - Connect an on-prem VPC to an AWS VPN.
  - The connection is encrypted and goes over public internet.
  - On the on-prem side: we need a Customer Gateway
  - On the AWS: we need a virual private gateway
- Direct Connect (DX)
  - Establish a physical connection between on-prem and AWS.
  - More private, secure, and fast.
  - But, takes about a month to establish.

##### AWS ClientVPN
- Connect from your computer using OpenVPN to your private network in AWS and on-prem
- Allows to connect to our EC2 instances over a private IP

##### Transite Gateway
- allowing transitive peering between thousands of VPC, on-prem, and star connection.

##### Summary
- VPC: virtual private cloud. exists at the regional level.
- Subnets are network partitions of the VPC and they exist at the AZ level.
- Internet Gateway: allows internet access at the VPC level.
- NAT Gateway: allows internet access to private subnets.
- NACL: stateless, subnet rules for inbound and outbound.
- Security groups: stateful, operate at the EC2 instance level.
- VPC Peering: connect two VPC with non overlapping IP ranges.
- Elastic IP: fixed public IPv4. Have an on-going if not used.
- VPC endpoints: they provide private access to AWS services within the VPC.
- PrivateLink: Privately connect to a service in a 3rd party VPC.
- VPC flow logs: network traffic logs.
- Site to Site VPN: vpn connection between on-prem and AWS over public internet
- ClientVPN: vpn connection between your computer into your VPC.
- Direct Connect: direct private connection to AWS from on-prem.
- Transit Gateway: connect thousands of VPC and on-prem networks.