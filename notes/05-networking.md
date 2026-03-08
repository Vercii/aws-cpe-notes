
## What is a VPC?

A VPC (Virtual Private Cloud) is your private network in AWS.

- You define your own private IP address range.
- You launch resources (EC2, Load Balancers, etc.) inside it.
- Nothing enters or leaves without explicit permission.
- Acts as a logically isolated section of the AWS Cloud.

# Subnets

Subnets are smaller IP ranges inside a VPC.

- Used to group resources.
- Control public or private accessibility.
- Distributed across Availability Zones for high availability.

## Types of Subnets

### Public Subnet
- Has access to the internet.
- Requires:
  - Internet Gateway
  - Route to 0.0.0.0/0
  - Public IP assignment enabled

Used for:
- Web servers
- Load balancers
- Bastion hosts

### Private Subnet
- No direct internet access.
- Used for internal services.

Used for:
- Databases
- Internal applications
- Backend services

# Internet Gateway (IGW)

An Internet Gateway allows traffic between a VPC and the public internet.

- Must be attached to a VPC.
- Enables inbound and outbound internet traffic.
- Required for public subnets.

Without an Internet Gateway, resources cannot be reached from the internet.

# Virtual Private Gateway (VGW)

A Virtual Private Gateway enables VPN connections between:

- On-premises data centers
- Corporate networks
- AWS VPC

Used for encrypted private connections over the public internet.

# AWS Direct Connect

AWS Direct Connect provides a dedicated physical fiber connection between:

- Your data center
- Your Amazon VPC

Benefits:

- Higher bandwidth
- Lower latency
- More consistent performance
- Helps meet compliance requirements
- Bypasses public internet congestion

Use when:
- Large data transfers
- Strict regulatory requirements
- Stable, high-throughput connectivity is needed

# Ways to Connect to AWS

## AWS Client VPN

Fully managed VPN for remote users.

- OpenVPN-based
- Scales automatically
- No hardware required

Use case:
- Remote workforce access

Benefits:
- Elastic
- Secure
- Easy to scale

## AWS Site-to-Site VPN

Creates a secure encrypted tunnel between:

- On-premises network
- AWS VPC

Use case:
- Branch office to AWS connection
- Application migration

Benefits:
- Secure
- Private
- Highly available

## AWS PrivateLink

Privately connects your VPC to:

- AWS services
- Other VPCs
- Third-party services

Without:
- Internet Gateway
- NAT
- Public IP
- VPN
- Direct Connect

Benefits:
- Private connectivity
- Simplified network management
- Secure API-level access

## AWS Direct Connect

Dedicated private connection to AWS.

Benefits:
- Increased bandwidth
- Reduced network cost
- Predictable performance

Often paired with:
- VPN as failover

# Network Security Inside a VPC

Security operates at two levels:

- Subnet level → Network ACL
- Instance level → Security Group

# Network Access Control List (NACL)

Subnet-level firewall.

- Stateless
- Evaluates every packet
- Separate inbound and outbound rules
- Must allow return traffic explicitly

Characteristics:

- Applies to entire subnet
- Checked when traffic crosses subnet boundary
- Default NACL allows all traffic (customizable)

# Security Groups

Instance-level firewall.

- Stateful
- Remembers connections
- Allows return traffic automatically
- Default denies all inbound traffic
- Default allows all outbound traffic

Characteristics:

- Applied to EC2 instances
- Controls allowed ports and IP ranges
- More commonly used than NACLs

# Stateful vs Stateless

## Security Groups (Stateful)

- If inbound traffic is allowed,
  return traffic is automatically allowed.
- Keeps memory of connections.

## Network ACLs (Stateless)

- No memory.
- Every inbound and outbound packet is evaluated independently.
- Must explicitly allow both directions.

# Example: Packet Flow Between Two Instances

Instance A → Instance B (Different Subnets)

Outbound path:

1. Security Group of Instance A (allows outbound by default)
2. NACL of Subnet A (outbound rule check)
3. NACL of Subnet B (inbound rule check)
4. Security Group of Instance B (inbound rule check)

Return path:

1. Security Group of Instance B (automatically allows return traffic)
2. NACL of Subnet B (outbound rule check)
3. NACL of Subnet A (inbound rule check)
4. Security Group of Instance A (automatically allows return traffic)

# Route Tables

Route tables determine where traffic is directed.

Each subnet must be associated with a route table.

Example:

Destination: 0.0.0.0/0  
Target: Internet Gateway  

This makes a subnet public.

# CIDR Blocks

CIDR defines IP ranges.

Example:

VPC: 10.0.0.0/16  
Subnet 1: 10.0.1.0/24  
Subnet 2: 10.0.2.0/24  

Smaller subnet = fewer IP addresses.

# DNS & Content Delivery

## Amazon Route 53

Domain Name System (DNS) service.

- Translates domain names to IP addresses.
- Supports routing policies:
  - Latency-based routing
  - Geolocation routing
  - Geoproximity routing
  - Weighted routing
- Can register domains.

## Amazon CloudFront

Content Delivery Network (CDN).

- Uses global Edge Locations.
- Delivers content closer to users.
- Reduces latency.
- Caches static assets.

Used for:
- Images
- Videos
- Static sites
- APIs

# Global Architecture Pattern

For global applications:

1. User enters domain.
2. Route 53 routes to closest Region.
3. CloudFront serves from nearest Edge Location.
4. Content retrieved from origin in chosen Region.
5. Multi-Region + Multi-VPC architecture possible.

# VPN vs Direct Connect

## Use VPN When:

- Secure remote access is needed
- Smaller data transfers
- Flexible setup required
- Budget-sensitive

## Use Direct Connect When:

- High bandwidth required
- Large data transfers
- Dedicated private connection needed
- Compliance requirements exist

## Use Both When:

- Direct Connect is primary
- VPN acts as failover

# Networking Design Principles

- Isolate resources using subnets
- Use private subnets for sensitive workloads
- Attach Internet Gateway only when needed
- Use Security Groups for instance-level control
- Use NACLs for subnet-level filtering
- Design for redundancy
- Plan for failover
