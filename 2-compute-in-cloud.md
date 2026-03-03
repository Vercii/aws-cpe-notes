## Amazon EC2 
Amazon EC2 (Elastic Compute Cloud) provides resizable virtual machines in the cloud.<br><br>
<b> Key Features: </b>
- Full control over operating system
- Customizable CPU, memory, storage, and networking
- Can be launched in different regions and AZs

## EC2 Instance Types
- General Purpose: Balanced CPU, memory, and networking.
- Compute Optimized: High CPU performance, ideal for gaming.
- Memory Optimized: Large memory capacity used for large datasets.
- Storage Optimized: High performance for locally stored data.
- Accelerated Computing: High GPU performance.

## EC2 Pricing Options
- On-Demand Instances: Pay only for what you use, no upfront payment or long-term commitments required.
- Reserved Instances: Get savings of up to 75% by committing to a 1 or 3-year term for predictable workloads using specific instance families and AWS Regions.
- Spot Instances: 90% off the On-Demand price, at the cost of interruptions when AWS reclaims the instance.
- Savings Plans: Save up to 72% across a variety of instance types by committing to a consistent usage level for 1 or 3 years.
- Dedicated Hosts: Reserve an entire physical server for exclusive use. Offers full control for your workloads with strict security and licensing needs.
- Dedicated Instances: Pay for instances running on hardware dedicated solely to your account. This option provides isolation from other AWS customers.

<b> The difference between DH and DI is that DI provides isolation without giving you the freedom to choose which physical server will be ran. DH gives you an entire physical server, and provides you with full control over resource allocation. </b>

## Scalability
- Refers the ability of a system to handle an increased load by adding resources.
  - Scaling horizontally (or scaling out) means adding more macihnes, scaling vertically (or scaling up) means adding more power to an existing machine.
 
## Elasticity
- Refers to the ability to automatically scale resources up or down in response to the demand. Providing cost efficiency and optimal resource usage at any given moment.

## Amazon EC2 Auto Scaling
- Maintain the desired amount of compute capacity for your application by dynamically adjusting the number of EC2 instances based on demand.
- Configured by the following:
  - Minimum Capacity: Defines the least number of EC2 instances required to keep the application running.
  - Desired Capacity: Provides the ideal number of instances needed to handle the current workload.
  - Maximum Capacity: Sets the upper limit on the amount of instances that can be launched, preventing over-scaling and controlling costs. For example, you might configure the Auto Scaling group to scale out in response to increased demand.

<b> You only pay for the instance that you use because Amazon EC2 Auto Scaling uses EC2 instances.</b>

## Elastic Load Balancing (ELB)
- Automatically distributes incoming traffic across multiple resources, such as EC2 instanfces, to optimize performance and reliability. A load balancer becomes the single contact point for all incoming web traffic. As the number of EC2 instances fluctuates, the load balancer is where the incoming requests are directed. The traffic is then distributed evenly to available instances.
- It scales with traffic and automatically adjusts to changes in demand. It also handles maintenance, updates, and failover to ease operational overhead.

## Routing Methods
ELB has routing methods to optimize traffic distribution.
- Round Robin: Distributes the traffic in a cyclic manner.
- Least Connections: Picks the least active server in order to balance out the workload.
- IP Hash: Uses the client's IP address to consistently route traffic to the same server.
- Least Response Time: Directs traffic to the server with the fastest response time.
  
<b> ELB works with Auto Scaling in order to optimize workload, and increase efficiency. Auto Scaling changes the amount of instances based on demand, while ELB distributes the incoming requests evenly. </b>

## EventBridge
- Serverless service that helps connect different parts of an application using events, helping to build scalable, event-driven systems.
- It can route events, like order placed or payment completed, to the relevant services (payment, restaurant, inventory, and delivery). It is capable of handling high volumes of events during peak times, making sure each service works independently. If one service fails, EventBridge will store the event and process it as soon as the service is available again.

## Amazon SQS
- A message queuing service that facilitates reliable communication between software components. It can send, store, and receive messages at any scale, making sure messages are not lost and that other services don't need to be available for processing.
- Uses a queue system, where messages are sent. The receiver would retrieve this data, removing it from the queue.

## Amazon SNS
- A publish-subscribe service that publishers use to send messages to subscribers through SNS topics. Customers can subscribe to the topics they're interested in, then the company can send personalied notifications based on the customer's specific interests.
