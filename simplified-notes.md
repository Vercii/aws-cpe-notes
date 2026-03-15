# All in One 
## How the Internet Works
- Every device needs an IP Address.
    - IPv4
    - IPv6 : Created because we ran out of IPv4 addresses.
      
IP Addresses are hard to remember since they are a string of numbers and letters. People use domain names instead.

## DNS Domain Name System
- AWS uses <i>Route53</i>. It converts domain names into IP addresses that computers understand.

When using the internet, such as loading a website or sending an email; everything starts with packets.

## Packets
- Data does NOT move as one big chunks, it gets broken down into small pieces called packets.
- Each packet carries the actual data, and information like:
  - Destination IP: Where it's going
  - Source IP: Where it came from

This is all handled by TCP/IP.
  - TCP: Breaks down data and make sure it <b>arrives</b> correctly.
  - IP: Makes sure the data gets to the right <b>destination</b>.

IP makes sure that it gets there while TCP makes sure that it gets there <b>complete</b>.

## AWS Networking
AWS has public and private spaces. Creating a network in AWS (aka VPC), things are divided into subnets.

You can configure these subnets to determine what can to talk to what, and what can access the internet.
- Web Server need to accept traffic from users on the internet, thus they go to the PUBLIC subnet. Users can access your website, but you also need to have extra security.
    - Public subnets have a connection to the internet through <i>Internet Gateway</i>.
- Databases should not be exposed, making PRIVATE subnets the perfect fit for them.
    - Private subnets have NO direct path to the internet. In case of updates, these subnets can be accessed through a <i>Nat Gateway</i>.
 
In order to control traffic within networks, AWS offers two tools: <b>Security Groups</b>, and <b>Network ACLs</b>.

## Security Groups
Controls traffic for individual resources, like EC2 servers.
When setting up, you need to SPECIFY EXACTLY what kind of traffic can reach that server. <br><br><b>Typical</b> configurations are:
- Web Server
  - HTTP traffic on port 80 so people can access website.
  - HTTPS on port 443 for secure connections.
  - SSH on port 22 to manage the server.
 
You may change this as you like and/or to suit what is needed for your own web server.

## Network ACLs
- Controls traffic for ENTIRE sections of your network (subnets).

Together they help build multiple layers of security.

## Example Scenario
1. Someone types the web address.
   - Route 53 converts the domain name into an IP address that computers can understand.
   - AWS S3 stores static content like images, JS and CSS files.
   - CloudFront keeps copies of your content in data centers around the world.
   - ELB distributes all incoming traffic across multiple servers.
     - <b> This is crucial because if one server gets overloaded, ELB can send the traffic to other healthy servers. </b>
     - Auto Scaling ELB can create new servers automatically when you need more capacity, and remove them when you don't. <br><br>
     
To sum it up:
- Route 53 helps people find a web server.
- AWs S3 handles file storage. 
- CloudFront delivers content quickly. 
- AWS VPC provides network isolation.
- ELB distributes traffic.

# How a website actually works
## 1. Hosting and Delivery
S3 is where ALL your website files live. Images, HTML files, JS, CSS Styles are all organized inside buckets. Buckets act like root folder of your website.

S3 is powerful for web hosting because of its <b> Versioning Feature </b>.
- Versioning makes S3 keep track of all of the previous versions. Making it easy to revert versions when an accident occurs.
- CloudFront helps users access these files quickly. Instead of serving all of the content from one location, CF copies all of the files from data centers around the world.

### Real Life Application 
When someone is watching a show in Netflix (that uses AWS), they're not watching it from one central data center. CloudFront's content delivery network means if someone is watching in Tokyo, they are streaming from a Tokyo data center.

CloudFront can also be a security tool. Through Signed URLs and Cookies, you can control who gets access to your content. CloudFront also works with AWS WAF to protect your website from attacks. WAF watches the traffic and looks out for any suspicious, blocking them.

## 2. Running the Backend
Ways to handle backend operations:
1. Serverless with API Gateway & Lambda
   - When an action occurs, the API Gateway receives the request and directs it to the right Lambda function.
   - The Lambda function is what automates the logic in milliseconds. It is made to automatically scale to handle any number of requests.
   - Less responsibilities to handle, but the environment could be a little restricted.
2. EC2 & Virtualization
   - When launching an EC2 instance, you're getting a Virtual Server in AWS's data centers. You can scale up or down whenever you need, unlike traditional servers.
   - You get to choose the OS, install any software, configure security settings, and manage it just like you would with a physical server.
   - Ideal for custom applications that have specific dependencies.
   - You are in charge of managing your servers, you have more control but it also comes with more responsibilities.
3. Containers with ECS (Elastic Container Service)
   - It sits BETWEEN serverless and traditional servers. It solves the challenge of running applications consistently in different environments.
   - Specific versions of PLs, libraries, configuration files, and dependencies are packaged together in a standardized way.
   - Your application will run exactly the same way in development, testing, and production.
  
### When to use each service
- <b>Lambda</b> - Unpredictable traffic, pay per request, and scenarios where you don't want server management.
- <b>EC2</b> - Full OS control, pay for uptime, persistent workloads, or have apps with specific dependencies. 
- <b>ECS</b> - Perfect for applications with multiple services that need to run consistently across environments, allowing updates to only the parts that change.

## 3. Database Solutions
- S3 - An infinite scalable object storage used for storing files. Each file is stored as an "object". Ideal for storing things that don't need to be modified frequently. You either get the whole file or nothing.
Databases - Designed for data that needs to be queried, updated, and has relationships between different pieces of information. DBs let you work with individual pieces of a larger structure. AWS offers two different types of databases:
    - Amazon RDS - Data is organized in tables similar to an Excel spreadsheet where tables can be connected. You can write specific commands to find and update the exact data that you need.
      - Perfect for information that fits neatly into tables with clear relationships between them.
        - An e-commerce website needs to categorize which user is connected to a product, and which product is connected to a seller.
    - DynamoDB - AWS's NoSQL Database, it is built for speed and scale. It can handle massive amounts of data while still responding in milliseconds.
      - Perfect for applications that require massive scale, low latency, or flexible data structures.
        - Good for tracking delivery positions. Their locations are updated every few seconds requiring a system that can handle frequent changes while providing INSTANT access to the latest state.

Both RDS and DynamoDB can integrate with other AWS Services, and modern applications are likely to use both types of databases together.

You might keep core data in RDS where you need strong relationships and complex queries. While using DynamoDB for things like fast user sessions and/or real-time features.

<b>Summary:</b>
- RDS = relational, structured, complex queries
- DynamoDB = high-scale, low latency, flexible schema
- S3 = file/object storage (images, videos, backups)

## 4. AI and Machine Learning
- AWS offers Amazon Bedrock, and Sagemaker.
- Amazon Bedrock gives you access to foundation AI models created by companies like Anthropic, Meta, and others in a single interface.
  - Instead of building from scratch, you can get ready-to-go models, customize them, and plug them into your application.
  - Supports RAG (Retrieval-Augmented-Generation), which lets the model give up-to-date answers pulled from your database.
- SageMaker lets you have full control in letting you train, build, and deploy your own machine learning model.
  - Perfect for predicting user behavior, detecting fraud, or recommending products since it can utilize pattern recognition.
 
<b>Summary:</b>
- Bedrock = Use AI models
- Sagemaker = Build AI models 

Both can integrate seamlessly with your existing architecture.

## 5. Security
AWS offers two services that serve as the backbone for security; VPC and IAM.

- VPC (Virtual Private Cloud) - Your own private section in AWS's cloud where you control how your app's networking works. You control how resources communicate, which ones can access the internet, and which remain private.

- IAM - Controls who can access what within your AWS environment. Give every user or service only the permissions they need, and <b>nothing more</b>.
  - You can create an IAM role that allows a specific Lambda function that needs to use a Bedrock AI model to analyze data.
  - You can create an IAM role that permits to read data but not to modify it.
 
### Full Picture
- VPC isolates your entire network.
- Public and private subnets separate your internet-facing resources from your internal ones.
- NAT Gateways allow resources in private subnets to access the internet without being directly exposed to it.
- Network ACLs protect traffic at subnet level.
- Security groups protect traffic at instance level.
- IAM ensures that every component only has the permissions it needs.

Security isn't optional, it's something you add from the beginning.
