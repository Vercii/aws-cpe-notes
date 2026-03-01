
## AWS Cloud Benefits 
- Elastic scalability, resources can scale up or down based on demand. <br>
- Pay-as-you-go pricing model. <br>
- Eliminates the need for physical data center investments. <br>
- Global infrastructure enables low-latency access worldwide. <br>

## AWS Regions and AZ
- AWS is spread out through different regions. <br>
- Each AWS Region contains multiple Availability Zones (AZs), typically 3 or more. <br>
- Availability Zones (AZs) are physically separate data centers within a region. If one AZ fails, traffic can automatically be routed to another AZ. Deploying applications across multiple AZs increases high availability and fault tolerance.<br>

## Shared Responsibility Model 
AWS: Security **OF** the Cloud<br>
- Global infrastructure<br>
- Physical security<br>
- Networking hardware<br>
- Managed services infrastructure<br>

Customer: Security **IN** the Cloud<br>
- Customer data<br>
- Identity and access management<br>
- OS patches (for EC2)<br>
- Application configuration<br>
- Firewall settings<br>

Responsibility varies depending on service type (IaaS, PaaS, SaaS).
